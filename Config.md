### Full Config
```js
{
  // string - A string to identify your config.
  name: '',

  // string - A path relative to the vsode workspace root folder.
  context: '.',
 
  // string - sftp or ftp
  protocol: "sftp", 
 
  // string - Hostname or IP address of the server.
  host: "host",

  // integer - Port number of the server.
  port: 22,

  // string - Username for authentication.
  username: "username",

   // string - Password for password-based user authentication.
  password: null,

  // string - The absolute path on remote
  remotePath: "/", 

  // integer - How long (in milliseconds) to wait for the connect to complete. 
  connectTimeout: 10000,

  // boolean - Upload on every save operation of VS code 
  uploadOnSave: false,
  
  // boolean - Download the file from the remote server whenever it is opened 
  downloadOnOpen: false,
 
  // string - Set to 'update' so 'sync command' will only affect those files exist in both local and server. Set to 'full', 'sync' will be same as 'download/upload' besides deleting file not exist in origin from target.
  syncMode: 'update',

  // string[] - Same behavior as gitignore, all path reltative to context of the current config
  ignore: [],

  // object - Default: null. 
  watcher: {
    //  string - glob patterns that are watched and when edited outside of the VS cdoe editor are processed. Set `uploadOnSave` to false when you watch everything.
    files: "", 
  
    // boolean - upload when file changed
    autoUpload: true,

    // boolean - delete when file removed
    autoDelete: true
  }，
 
  // number - Lower concurrency could get more stability because some client/server have some sort of configured/hard coded limit. 
  concurrency: 4
}
```
### SFTP only Config
```js
{
  // string - Path to ssh-agent's UNIX socket for ssh-agent-based user authentication.  Windows users: set to 'pageant' for authenticating with Pageant or (actual) path to a cygwin "UNIX socket".
  agent: null, 

  // string - Absolute path to user private key.
  privateKeyPath: null, 

  // mixed - For an encrypted private key, this is the passphrase string used to decrypt it. Set to true for enable passphrase dialog. This will prevent from using cleartext passphrase in this config.
  passphrase: null,

  // boolean - Set to true for enable verifyCode dialog. Keyboard interaction authentication mechanism. For example using Google Authentication (Multi factor)
  // (requires the server to have keyboard-interactive authentication enabled)
  interactiveAuth: false, 

  // Explicit overrides for the default transport layer algorithms used for the connection.
  algorithms: {
    "kex": [
      "ecdh-sha2-nistp256",
      "ecdh-sha2-nistp384",
      "ecdh-sha2-nistp521",
      "diffie-hellman-group-exchange-sha256",
      "diffie-hellman-group14-sha1"
    ],
    "cipher": [
      "aes128-ctr",
      "aes192-ctr",
      "aes256-ctr",
      "aes128-gcm",
      "aes128-gcm@openssh.com",
      "aes256-gcm",
      "aes256-gcm@openssh.com"
    ],
    "serverHostKey": [
      "ssh-rsa",
      "ecdsa-sha2-nistp256",
      "ecdsa-sha2-nistp384",
      "ecdsa-sha2-nistp521"
    ],
    "hmac": [
      "hmac-sha2-256",
      "hmac-sha2-512",
      "hmac-sha1"
    ]
  }
}
```

### FTP only Config
```js
{
  // mixed - Set to true for both control and data connection encryption, 'control' for control connection encryption only, or 'implicit' for implicitly encrypted control connection (this mode is deprecated in modern times, but usually uses port 990)
  secure: false,
  
  // object - Additional options to be passed to tls.connect(). Default: (null) see https://nodejs.org/api/tls.html#tls_tls_connect_options_callback
  secureOptions: null, 
}
```
