# shell-folder-shortcuts
Shell: folder shortcuts

Thanks to https://ss64.com/nt/shell.html

Unless indicated otherwise, all the shortcuts above work in all versions of Windows from Vista upwards.

Shell folder shortcuts can be used directly in the Windows Explorer Address bar:  shell:Desktop

Or in the Start Menu Start | Run | shell:Desktop

Command Line
From the command line shell: shortcuts can be passed to Explorer.exe:
C:\> explorer.exe shell:desktop

You can also pass a variable or string:

C:\> explorer.exe %ProgramFiles%

The START command also accepts shell: shortcuts with spaces but they have to be quoted like so:

C:\> start "" "shell:my music"

C:\> start "" %UserProfile%\Music\

In PowerShell:
[Environment]::GetFolderPath('MyVideos')
Where 'MyVideos' may be any of the constants defined under: [Enum]::GetNames([System.Environment+SpecialFolder])

Shortcuts
To create a shortcut to any of the shell folders above: Right click the Desktop > New Shortcut and set the location/target to explorer.exe followed by the shell:option
For example:

  explorer.exe shell:PrintersFolder

Alternatively you can use a variable/string:

  explorer.exe "%ProgramData%\Microsoft\Windows\Start Menu\"

Non admin users will find it difficult to create a Shell: shortcut directly on the Task bar, it can be done but requires creating the shortcut in: %USERPROFILE%\AppData\Roaming\Microsoft\Internet Explorer\Quick Launch\User Pinned\TaskBar
It can then be dragged into the taskbar.

Create a 'God mode' shortcut (a full set of Control Panel options) by setting the shortcut target to:

%WinDir%\explorer.exe shell:::{ED7BA470-8E54-465E-825C-99712043E01C}
