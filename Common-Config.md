### name

string - A string to identify your config.

### context

string - A path relative to the workspace root folder. Using this when you want to map a subfolder to the remotePath.

#### Default

workspace root

### protocol

string - sftp or ftp.

#### Default

sftp

### host

string - Hostname or IP address of the server.

### port

integer - Port number of the server.

#### Default

22

### username

string - Username for authentication.

### password

string - Password for password-based user authentication.

### remotePath

string - The absolute path on remote

#### Default

/

### uploadOnSave

boolean - Upload on every save operation of VS code

#### Default

false

### downloadOnOpen

boolean - Download the file from the remote server whenever it is opened

#### Default

false

### syncOption

object - Config the behavior of `Sync` command.

#### Default

`{}`

### syncOption.delete

boolean - Delete extraneous files from dest dirs.

### syncOption.skipCreate

boolean - Skip creating new files on dest.

### syncOption.ignoreExisting

boolean - Skip updating files that exist on dest.

### syncOption.update

boolean - Update the dest only if a newer version is on the src filesystem.

### ignore

string[] - Same behavior as gitignore, all path reltative to context of the current config

#### Default

[]

### ignoreFile

string - Absolute path to the ignore file or Relative path relative to the workspace root folder.

### watcher

object.

### watcher.files

string - glob patterns that are watched and when edited outside of the VS cdoe editor are processed. Set `uploadOnSave` to false when you watch everything.

### watcher.autoUpload

boolean - upload when file changed

### watcher.autoDelete

boolean - delete when file removed

### remoteTimeOffsetInHours
number - The number of hours difference between the local machine and remote/server. (remote minus local)

#### Default

0

### remoteExplorer

object.

### remoteExplorer.filesExclude

string[] - Configure patterns for excluding files and folders. The Remote Explorer decides which files and folders to show or hide based on this setting.

### concurrency
number - Lower concurrency could get more stability because some client/server have some sort of configured/hard coded limit.

#### Default

4

### connectTimeout
number - the maximum connection time

#### Default
10000

### limitOpenFilesOnRemote
mixed - Limit open file descriptors to the specific number in a remote server. Set to true for using default limit(222). Do not set this unless you have to.
 
#### Default

false