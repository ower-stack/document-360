Event module implements an Observer pattern where you can add hooks (events) to your code and allow other bundles to listen and react to those events. Event enables to create synchronous and asynchronous events: traditional synchronous where listeners are handled at the same time as they are dispatched, and asynchronous (queueable) where events are put into a queue and handled later by some queue service.

Latest version: **2.4.0**
Last update: **18 Jan 2019**
Type: **Core Splitted**
Group: **Functional**
[View on GitHub](https://github.com/spryker/event/releases/tag/2.4.0)

## API (Facades)

|        Facade Method        |                         Description                          |
| :-------------------------: | :----------------------------------------------------------: |
|         **trigger**         | * Handles all events by registered by give $eventName<br> * Passes transfer object to each listener <br> * If listener is queueable then it will put into queue system. |
|       **triggerBulk**       | * Handles all events by registered by give $eventName<br> * Passes array of transfer object to each listener <br> * If listener is queueable then it will put into queue system. |
|  **triggerByListenerName**  | * Triggers event processing by listener name with an optional parameter event name.<br> * Listener name is a listener class name in short, qualified or a fully qualified form.<br> * Throws an exception if event listener is not found or ambiguous. |
| **processEnqueuedMessages** | * Processes all listeners enqueued in event queue (queue consumer) |
|     **forwardMessages**     |           * Forward consumed messages to event queue           |

## Plugins

|                            Plugin                            |         Method          |                         Description                          |
| :----------------------------------------------------------: | :---------------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventSubscriberInterface.php** | **getSubscribedEvents** |                                                              |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventHandlerInterface.php** |       **handle**        | * Listeners needs to implement this interface to execute the codes for each event. |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventBulkHandlerInterface.php** |     **handleBulk**      | * Listeners needs to implement this interface to execute the codes for morethan one event at same time (Bulk Operation) |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventBaseHandlerInterface.php** |                         |                                                              |

## Dependencies:

* **PHP** >=7.1
* **ErrorHandler** ^2.0.0
* **Kernel** ^3.0.0
* **Log** ^3.0.0
* **Monolog** ^2.0.0
* **Queue** ^1.1.0
* **UtilEncoding** ^2.1.0


<details open>
<summary>Previous Versions </summary>

<details open>
<summary>2.3.2</summary>



## API (Facades) 

|        Facade Method        |                         Description                          |
| :-------------------------: | :----------------------------------------------------------: |
|         **trigger**         | Handles all events by registered by give $eventNamePasses transfer object to each listenerIf listener is queueable then it will put into queue system. |
|       **triggerBulk**       | Handles all events by registered by give $eventNamePasses array of transfer object to each listenerIf listener is queueable then it will put into queue system. |
| **processEnqueuedMessages** | Processes all listeners enqueued in event queue (queue consumer) |
|     **forwardMessages**     |           Forward consumed messages to event queue           |

## Plugins 

|                            Plugin                            |         Method          |                         Description                          |
| :----------------------------------------------------------: | :---------------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventSubscriberInterface.php** | **getSubscribedEvents** |                                                              |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventHandlerInterface.php** |       **handle**        | Listeners needs to implement this interface to execute the codes for eachevent. |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventBulkHandlerInterface.php** |     **handleBulk**      | Listeners needs to implement this interface to execute the codes for morethan one event at same time (Bulk Operation) |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventBaseHandlerInterface.php** |                         |                                                              |

## Dependencies: 

* **PHP** >=7.1
* **ErrorHandler** ^2.0.0
* **Kernel** ^3.0.0
* **Log** ^3.0.0
* **Monolog** ^2.0.0
* **Queue** ^1.1.0
* **UtilEncoding** ^2.0.0

<br>
</details>

<details open>
<summary>2.3.1</summary>



## API (Facades) 

|        Facade Method        |                         Description                          |
| :-------------------------: | :----------------------------------------------------------: |
|         **trigger**         | Handles all events by registered by give $eventNamePasses transfer object to each listenerIf listener is queueable then it will put into queue system. |
|       **triggerBulk**       | Handles all events by registered by give $eventNamePasses array of transfer object to each listenerIf listener is queueable then it will put into queue system. |
| **processEnqueuedMessages** | Processes all listeners enqueued in event queue (queue consumer) |
|     **forwardMessages**     |           Forward consumed messages to event queue           |

## Plugins 

|                            Plugin                            |         Method          |                         Description                          |
| :----------------------------------------------------------: | :---------------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventSubscriberInterface.php** | **getSubscribedEvents** |                                                              |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventHandlerInterface.php** |       **handle**        | Listeners needs to implement this interface to execute the codes for eachevent. |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventBulkHandlerInterface.php** |     **handleBulk**      | Listeners needs to implement this interface to execute the codes for morethan one event at same time (Bulk Operation) |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventBaseHandlerInterface.php** |                         |                                                              |

## Dependencies: 

* **PHP** >=7.1
* **ErrorHandler** ^2.0.0
* **Kernel** ^3.0.0
* **Log** ^3.0.0
* **Monolog** ^2.0.0
* **Queue** ^1.1.0
* **UtilEncoding** ^2.0.0

<br>
</details>

<details open>
<summary>2.3.0</summary>



## API (Facades) 

|        Facade Method        |                         Description                          |
| :-------------------------: | :----------------------------------------------------------: |
|         **trigger**         | Handles all events by registered by give $eventNamePasses transfer object to each listenerIf listener is queueable then it will put into queue system. |
|       **triggerBulk**       | Handles all events by registered by give $eventNamePasses array of transfer object to each listenerIf listener is queueable then it will put into queue system. |
| **processEnqueuedMessages** | Processes all listeners enqueued in event queue (queue consumer) |
|     **forwardMessages**     |           Forward consumed messages to event queue           |

## Plugins 

|                            Plugin                            |         Method          |                         Description                          |
| :----------------------------------------------------------: | :---------------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventSubscriberInterface.php** | **getSubscribedEvents** |                                                              |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventHandlerInterface.php** |       **handle**        | Listeners needs to implement this interface to execute the codes for eachevent. |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventBulkHandlerInterface.php** |     **handleBulk**      | Listeners needs to implement this interface to execute the codes for morethan one event at same time (Bulk Operation) |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventBaseHandlerInterface.php** |                         |                                                              |

## Dependencies: 

* **PHP** >=7.1
* **ErrorHandler** ^2.0.0
* **Kernel** ^3.0.0
* **Log** ^3.0.0
* **Monolog** ^2.0.0
* **Queue** ^1.1.0
* **UtilEncoding** ^2.0.0

<br>
</details>

<details open>
<summary>2.2.0</summary>



## API (Facades) 

|        Facade Method        |                         Description                          |
| :-------------------------: | :----------------------------------------------------------: |
|         **trigger**         | Handles all events by registered by give $eventNamePasses eventTransfer to each listenerIf listener is queueable then it will put into queue system. |
| **processEnqueuedMessages** | Processes all listeners enqueued in event queue (queue consumer) |

## Plugins 

|                            Plugin                            |         Method          |                         Description                          |
| :----------------------------------------------------------: | :---------------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventBulkHandlerInterface.php** |     **handleBulk**      | Listeners needs to implement this interface to execute the codes for morethan one event at same time (Bulk Operation) |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventSubscriberInterface.php** | **getSubscribedEvents** |                                                              |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventHandlerInterface.php** |       **handle**        | Listeners needs to implement this interface to execute the codes for eachevent. |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventBaseHandlerInterface.php** |                         |                                                              |

## Dependencies: 

* **PHP** >=7.1
* **ErrorHandler** ^2.0.0
* **Kernel** ^3.0.0
* **Log** ^3.0.0
* **Monolog** ^2.0.0
* **Queue** ^1.1.0
* **UtilEncoding** ^2.0.0

<br>
</details>

<details open>
<summary>2.1.1</summary>



## API (Facades) 

|        Facade Method        |                         Description                          |
| :-------------------------: | :----------------------------------------------------------: |
|         **trigger**         | Handles all events by registered by give $eventNamePasses eventTransfer to each listenerIf listener is queueable then it will put into queue system. |
| **processEnqueuedMessages** | Processes all listeners enqueued in event queue (queue consumer) |

## Plugins 

|                            Plugin                            |         Method          |                         Description                          |
| :----------------------------------------------------------: | :---------------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventSubscriberInterface.php** | **getSubscribedEvents** |                                                              |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventBaseHandlerInterface.php** |                         |                                                              |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventHandlerInterface.php** |       **handle**        | Listeners needs to implement this interface to execute the codes for eachevent. |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventBulkHandlerInterface.php** |     **handleBulk**      | Listeners needs to implement this interface to execute the codes for morethan one event at same time (Bulk Operation) |

## Dependencies: 

* **PHP** >=7.1
* **Kernel** ^3.0.0
* **Log** ^3.0.0
* **Monolog** ^2.0.0
* **Queue** ^1.0.0
* **UtilEncoding** ^2.0.0

<br>
</details>

<details open>
<summary>2.1.0</summary>



## API (Facades) 

|        Facade Method        |                         Description                          |
| :-------------------------: | :----------------------------------------------------------: |
|         **trigger**         | Handles all events by registered by give $eventNamePasses eventTransfer to each listenerIf listener is queueable then it will put into queue system. |
| **processEnqueuedMessages** | Processes all listeners enqueued in event queue (queue consumer) |

## Plugins 

|                            Plugin                            |         Method          |                         Description                          |
| :----------------------------------------------------------: | :---------------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventSubscriberInterface.php** | **getSubscribedEvents** |                                                              |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventBaseHandlerInterface.php** |                         |                                                              |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventHandlerInterface.php** |       **handle**        | Listeners needs to implement this interface to execute the codes for eachevent. |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventBulkHandlerInterface.php** |     **handleBulk**      | Listeners needs to implement this interface to execute the codes for morethan one event at same time (Bulk Operation) |

## Dependencies: 

* **PHP** >=7.1
* **Kernel** ^3.0.0
* **Log** ^3.0.0
* **Monolog** ^2.0.0
* **Queue** ^1.0.0
* **UtilEncoding** ^2.0.0

<br>
</details>

<details open>
<summary>2.0.0</summary>



## API (Facades) 

|        Facade Method        |                         Description                          |
| :-------------------------: | :----------------------------------------------------------: |
|         **trigger**         | Handles all events by registered by give $eventNamePasses eventTransfer to each listenerIf listener is queueable then it will put into queue system. |
| **processEnqueuedMessages** | Processes all listeners enqueued in event queue (queue consumer) |

## Plugins 

|                            Plugin                            |         Method          |                         Description                          |
| :----------------------------------------------------------: | :---------------------: | :----------------------------------------------------------: |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventBaseHandlerInterface.php** |                         |                                                              |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventSubscriberInterface.php** | **getSubscribedEvents** |                                                              |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventHandlerInterface.php** |       **handle**        | Listeners needs to implement this interface to execute the codes for eachevent. |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventBulkHandlerInterface.php** |     **handleBulk**      | Listeners needs to implement this interface to execute the codes for morethan one event at same time (Bulk Operation) |

## Dependencies: 

* **Kernel** ^3.0.0
* **Log** ^3.0.0
* **Monolog** ^2.0.0
* **Queue** ^1.0.0
* **UtilEncoding** ^2.0.0

<br>
</details>

<details open>
<summary>1.0.1</summary>



## API (Facades) 

|        Facade Method        |                         Description                          |
| :-------------------------: | :----------------------------------------------------------: |
|         **trigger**         | Handles all events by registered by give $eventNamePasses eventTransfer to each listenerIf listener is queueable then it will put into queue system. |
| **processEnqueuedMessages** | Processes all listeners enqueued in event queue (queue consumer) |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventListenerInterface.php** |       **handle**        |             |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventSubscriberInterface.php** | **getSubscribedEvents** |             |

## Dependencies: 

* **Kernel** ^3.0.0
* **Log** ^3.0.0
* **Monolog** ^2.0.0
* **Queue** ^0.3.0
* **UtilEncoding** ^2.0.0

<br>
</details>

<details open>
<summary>1.0.0</summary>



## API (Facades) 

|        Facade Method        |                         Description                          |
| :-------------------------: | :----------------------------------------------------------: |
|         **trigger**         | Handles all events by registered by give $eventNamePasses eventTransfer to each listenerIf listener is queueable then it will put into queue system. |
| **processEnqueuedMessages** | Processes all listeners enqueued in event queue (queue consumer) |

## Plugins 

|                            Plugin                            |         Method          | Description |
| :----------------------------------------------------------: | :---------------------: | :---------: |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventListenerInterface.php** |       **handle**        |             |
| **/src/Spryker/Zed/Event/Dependency/Plugin/EventSubscriberInterface.php** | **getSubscribedEvents** |             |

## Dependencies: 

* **Kernel** ^3.0.0
* **Log** ^3.0.0
* **Monolog** ^2.0.0
* **Queue** ^1.0.0
* **UtilEncoding** ^2.0.0

<br>
</details>


<br>
</details>
