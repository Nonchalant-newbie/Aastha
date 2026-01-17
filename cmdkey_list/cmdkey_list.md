It contains **Windows Stored Credentials information** retrieved from the local system credential store.

The following data is present for each stored credential:

* **Target Identifier**

  * Specifies the application or service associated with the credential (e.g., MicrosoftAccount, WindowsLive, LegacyGeneric)
  * Helps identify which services rely on saved authentication data

* **Credential Type**

  * Indicates the credential classification (e.g., Generic, LegacyGeneric)
  * Determines how Windows handles storage and access control

* **User Identifier**

  * Shows the username, account reference, or token associated with the credential
  * May represent a real user account or an internal system identifier

* **Persistence Scope**

  * Indicates whether the credential is saved temporarily (current logon only) or persistently on the local machine
  * Helps assess long-term exposure risk

---

## Observed Stored Credentials

* **MicrosoftAccount: SSO_POP_Device**

  * Type: Generic
  * User: 02njbdqyatmqxuik
  * Persistence: Saved for current logon session only

* **Olk/PushNotificationsBackupKey**

  * Type: LegacyGeneric
  * User: Olk/PushNotificationsBackupKey
  * Persistence: Local machine persistence

* **MicrosoftAccount (User-linked)**

  * Type: LegacyGeneric
  * User: [bharatk.kanan@gmail.com](mailto:bharatk.kanan@gmail.com)
  * Persistence: Local machine persistence

* **WindowsLive: virtualapp/didlogical**

  * Type: Generic
  * User: 02njbdqyatmqxuik
  * Persistence: Local machine persistence

* **Olk/PushNotificationsKey**

  * Type: LegacyGeneric
  * User: Olk/PushNotificationsKey
  * Persistence: Local machine persistence

---

## Cybersecurity Significance

* Identifies **accounts and services with cached credentials**, which may be reused without reauthentication.
* Highlights **persistent credentials** that remain stored across reboots, increasing risk if the system is compromised.
* Reveals linkage to **Microsoft and Windows Live accounts**, which may grant access to email, cloud storage, and synced services.
* Indicates presence of **background service keys** (e.g., Outlook push notification keys), which could be abused for lateral access if extracted.
* Shows use of **session-only credentials**, which reduce long-term risk compared to persistent storage.
* Assists in evaluating **credential hygiene**, forensic investigations, and post-compromise impact assessment.

