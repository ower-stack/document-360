<!--Used to be: http://spryker.github.io/tutorials/zed/database-transaction-handling/-->

@(Warning)()(To reduce boilerplate code and properly handle database transactions you can use `Spryker\Zed\PropelOrm\Business\Transaction\DatabaseTransactionHandlerTrait`.)

## Usage

To use database transactions in the `DatabaseTransactionHandlingExample` class:

<details open>
<summary>Code sample:</summary>
    
```php
<?php

use Spryker\Zed\PropelOrm\Business\Transaction\DatabaseTransactionHandlerTrait;

class DatabaseTransactionHandlingExample
{

    use DatabaseTransactionHandlerTrait;
    
    /**
     * @param string $fooName
     * @param \Bar[] $barCollection
     *
     * @return \Foo
     */
    public function createFoo($fooName, array $barCollection)
    {
        return $this->handleDatabaseTransaction(function () use ($fooName, $barCollection) {
            return $this->executeCreateFooTransaction($fooName, $barCollection);
        });
    }
    
    /**
     * @param string $fooName
     * @param \Bar[] $barCollection
     *
     * @return \Foo
     */
    protected function executeCreateFooTransaction($fooName, array $barCollection)
    {
        $fooEntity = new Foo();
        $fooEntity->setFooName($fooName);
        $fooEntity->save();
        
        foreach ($barCollection as $bar) {
            $bar->setFkFoo($fooEntity->getIdFoo());
            $bar->save();
        }

        return $fooEntity;
    }

}
```

</br>
</details>

## Under the Hood

In case of any error, the transaction will be rolled back and an exception will be rethrown. The code only has one method. The `$connection` parameter is optional and if not specified `Propel::getConnection()` will be used.

<details open>
<summary>Code sample:</summary>

```php
<?php

    /**
     * @param \Closure $callback
     * @param \Propel\Runtime\Connection\ConnectionInterface|null $connection
     *
     * @throws \Exception
     * @throws \Throwable
     *
     * @return mixed
     */
    protected function handleDatabaseTransaction(Closure $callback, ConnectionInterface $connection = null)
    {
        if (!$connection) {
            $connection = Propel::getConnection();
        }

        $connection->beginTransaction();

        try {
            $result = $callback();

            $connection->commit();

            return $result;
        } catch (\Exception $exception) {
            $connection->rollBack();
            throw $exception;
        } catch (\Throwable $exception) {
            $connection->rollBack();
            throw $exception;
        }
    }
```

</br>
</details>

