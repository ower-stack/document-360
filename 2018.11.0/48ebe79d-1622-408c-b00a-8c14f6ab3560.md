AuthMailConnector provides a plugin for extending the Auth to use it in Mail. This extension supports functionality like passwords reset mail.

Latest version: **3.1.0**
Last update: **21 Feb 2019**
Type: **Core Splitted**
Group: **Supportive**
[View on GitHub](https://github.com/spryker/auth-mail-connector/releases/tag/3.1.0)

## API (Facades)

|       Facade Method       |                         Description                          |
| :-----------------------: | :----------------------------------------------------------: |
| **sendResetPasswordMail** | Generates MailTransfer for reset password functionality.Uses MailFacade::handleMail() to handle generated MailTransfer. |

## Dependencies:

* **PHP** >=7.1
* **Kernel** ^3.0.0
* **Mail** ^4.0.0

## Suggested Installations:

* **Auth** If you want to use Auth plugins.

<details open>
<summary>Previous Versions</summary>

<details open>
<summary>3.0.0</summary>

## Dependencies:

* **Kernel** ^3.0.0
* **Mail** ^4.0.0

## Suggested Installations:

* **Auth** If you want to use Auth plugins you need to install spryker/auth.
<br>
</details>

<details open>
<summary>2.0.1</summary>

## Dependencies:

* **Kernel** ^2.0.0
* **Mail** ^2.0.0 || ^3.0.0
<br>
</details>

<details open>
<summary>2.0.0 </summary>

## Dependencies:

* **Kernel** ^2.0.0
* **Mail** ^2.0.0
<br>
</details>


<br>
</details>

_13 Apr 2019_