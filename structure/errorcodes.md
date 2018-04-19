# Error Codes
Below there is a list of all error codes and what each one does mean for Zmbackup. Please keep in mind that the program still inform you about what's wrong during the execution, so this doc is more for development than usage.

## Code **1**
Can't backup any account because some of the services Zmbackup need to access is offline. Please check if the script has access to the server and if they are enable, because Zmbackup only does Hot Backup at the moment.

## Code **2**
This error code means that you are trying to execute Zmbackup not using Zimbra's default user (normally the user is zimbra). If you are really trying to use the correctly user, probably the error is inside the config file /etc/zmbackup/zmbackup.conf. Change the option BACKUPUSER and probably the error will be fixed.

## Code **3**
This error means that your config file wasn't found inside the server or some of the options aren't informed inside the file. The script will inform each field that need to be informed before finish the execution.

## Code **4**
The PID file still exist inside your server, probably meaning that a Zmbackup process is in execution and you should wait a little more before execute the process. If a failure occured and no process is in execution, remove the PID file and try again.

## Code **5**
You used an invalid parameter while trying to use Zmbackup. Check the parameters and see if all of them are in the correct order and if all of them are valid. SEE zmbackup -h
