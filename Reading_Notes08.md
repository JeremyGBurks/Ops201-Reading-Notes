## Windows Registry Demystified: What You Can Do With It

### Summary 
Windows Registry is a database where many programs store their config settings.  
There are system wide settings and user-specific settings.  
Can edit it to enable hidden features "registry hacks".  
Settings are e stored under C:\Windows\System32\Config\  
Each user account has its own NTUSER.Dat file containing keys which you can edit directly.  
Contains folder-like "keys" and "values" inside those key that can contain numbers, text, or other data.  
Groups are called "hives".  
Registry brings together settings that would otherwise be scattered in many different locations.  
Can edit it with the "Registry Editor".  
Can find registry hacks online.  
Editing isn't dangerous if you know what you are doing. Follow instructions and only change settings you are instructed to change
If you screw things up and delete or change things haphazardly you could mess up your system's configuration. Potentially render Windows unbootable.   
Backup Registry before changing things.  
You can also edit the registry by downloading .reg files. You can also make your own reg hack files.  


### New Vocab

**_Keys and Values:_** Registry keys are container objects similar to folders. Registry values are non-container objects similar to files. Keys may contain values and subkeys. Keys are referenced with a syntax similar to Windows' path names, using backslashes to indicate levels of hierarchy.

_**Hive:**_ A hive is a logical group of keys, subkeys, and values in the registry that has a set of supporting files loaded into memory when the operating system is started or a user logs in. 

### Why this reading matters in relation to topics covered this week
This reading directly ties into the new subject that was introduced this week. It is important to get comfortable with this tool as it applies to the lab: 08 and is an important Windows feature to understand/utilize.

### Sources Cited
[Windows Registry Demystified](https://www.howtogeek.com/370022/windows-registry-demystified-what-you-can-do-with-it/)

[Keys and Values Definition](https://en.wikipedia.org/wiki/Windows_Registry#:~:text=Registry%20keys%20are%20container%20objects,to%20indicate%20levels%20of%20hierarchy.)

[Windows Registry Hive Definition](https://docs.microsoft.com/en-us/windows/win32/sysinfo/registry-hives#:~:text=A%20hive%20is%20a%20logical,or%20a%20user%20logs%20in.)
