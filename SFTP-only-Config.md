### agent

string - Path to ssh-agent's UNIX socket for ssh-agent-based user authentication. Windows users: set to 'pageant' for authenticating with Pageant or (actual) path to a cygwin "UNIX socket".ld get more stability because some client/server have some sort of configured/hard coded limit.

### privateKeyPath

string - Absolute path to user private key.

### passphrase

mixed - For an encrypted private key, this is the passphrase string used to decrypt it. Set to true for enable passphrase dialog. This will prevent from using cleartext passphrase in this config.

### interactiveAuth

boolean - Set to true for enable verifyCode dialog. Keyboard interaction authentication mechanism. For example using Google Authentication (Multi factor)

Note: _(requires the server to have keyboard-interactive authentication enabled)_

#### Default

false

### algorithms

Explicit overrides for the default transport layer algorithms used for the connection.

#### Default

```js
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
},
```

### sshConfigPath

Absolute path to your SSH config file.

#### Default

~/.ssh/config
