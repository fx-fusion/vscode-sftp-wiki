## SFTP: Config
Create a new config file for a selected project.

## Set Profile
Set an active profile
           
### KeyBindings Args
func(profileName: string)

## SFTP: Upload Active File
Upload active file to remote, overwriting the remote one.

## SFTP: Download Active File
Same as `Upload Active File`, but in the opposite direction.

## SFTP: Sync To Remote
Sync local directory to remote, only available for a directory. Copy common files (that exist on both sides) from local dir to remote, overwriting destination. (If syncMode is set to `full`, files that exist only on the local side will be created remotely, and files that exist only on the remote side will be deleted. The remote will be exactly the same as the local after `sync`.)

## SFTP: Sync To Local
Same as `Sync To Remote`, but in the opposite direction.

## sftp.upload
### KeyBindings Args
func(fspaths: string[])
