Keychain Plugin for Apache Cordova
=====================================
created by Shazron Abdullah

Updated by Max Lynch <max@ionic.io>

Modified by Human Practice to disable iCloud sync.

### Installation

```shell
cordova plugin add https://github.com/humanpractice/cordova-plugin-key-storage
```

### iCloud keychain *disabled*

This fork disables iCloud keychain syncing.

### Usage

See the **example** folder for example usage.

```js
/*
 Retrieves a value for a key

 @param successCallback returns the value as the argument to the callback when successful
 @param failureCallback returns the error string as the argument to the callback, for a failure
 @param key the key to retrieve
 @param TouchIDMessage the message to show underneath the TouchID prompt (if any)
 */
Keychain.get(successCallback, failureCallback, 'key', 'TouchID Message');

/*
 Sets a value for a key

 @param successCallback returns when successful
 @param failureCallback returns the error string as the argument to the callback, for a failure
 @param key the key to set
 @param value the value to set
 @param useTouchID whether to store the value with security such that TouchID will be needed to grab it
 */
Keychain.set(successCallback, failureCallback, 'key', 'value', useTouchID);

/*
 Removes a value for a key

 @param successCallback returns when successful
 @param failureCallback returns the error string as the argument to the callback
 @param key the key to remove
 */
Keychain.remove(successCallback, failureCallback, 'key');

/*
 Sets a JSON value for a key

 @param successCallback returns when successful
 @param failureCallback returns the error string as the argument to the callback, for a failure
 @param key the key to set
 @param value the value to set
 @param useTouchID whether to store the value with security such that TouchID will be needed to grab it
 */
Keychain.setJson(successCallback, failureCallback, 'key', 'value', useTouchID);

/*
 Gets a JSON value for a key

 @param successCallback returns when successful
 @param failureCallback returns the error string as the argument to the callback, for a failure
 @param key the key to set
 @param value the value to set
 @param useTouchID whether to store the value with security such that TouchID will be needed to grab it
 */
Keychain.getJson(successCallback, failureCallback, 'key', useTouchID);
```

### License

[Apache 2.0 License](http://www.apache.org/licenses/LICENSE-2.0.html) except for the Auth0 SimpelKeychain code that is under MIT
