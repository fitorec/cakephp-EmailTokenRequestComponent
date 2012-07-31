A Email Token Request Component.
==========================================================================================

Required
------------------------------------------------------------------------------------------
 -  **cakephp** 2.X

1 - Installation
------------------------------------------------------------------------------------------

Once the Component has been added to your application, add it to your Controllers $components property:

```php
<?php
	class UsersController extends AppController {
	/*
	 * Components
	 */
	var $components = array('EmailTokenRequest');
```

2 - Configuration
------------------------------------------------------------------------------------------

```php
<?php
public function beforeFilter() {
	$this->AutoLogin->settings = array(
		// Model settings
		'modelName' => 'User',
		'email' => 'mail',
		'email_token' => 'mail_hash',
		'email_token_expires' => 'mail_hash_expires',	
	);
}
```

3.- Debugging
------------------------------------------------------------------------------------------

Functionality not implemented yet but is expected to send emails to help debug:

```php
<?php
Configure::write('EmailTokenRequest', array(
	'email_debug' => 'chanerec@gmail.com'
));

```
