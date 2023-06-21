# Welcome to Utility Version Manager (uvm)

## Description
This is a simple project to help developers manage versioning for as many Utilities as they need:
- Add/Remove Utilities (Languages, Frameworks, ...)
- Manage multiple versions for each utility  

Currently, project is for **Windows** users only.

## Downloads

| Version      | Download                                                                |
|:-------------|:------------------------------------------------------------------------|
| all versions | [all releases (zip)](https://github.com/Panaith/uvm.github.io/releases) |

## Commands
Once the uvm project is installed, open terminal (cmd, powershell) and execute any of the following commands:

| Command     | Documentation                              | What it does                                                                            |
|:------------|:-------------------------------------------|:----------------------------------------------------------------------------------------|
| uvm install | [Installation](#installation-uvm-install)  | install uvm project                                                                     |
| uvm config  | [Configuration](#configuration-uvm-config) | add / remove utilities to uvm                                                           |
| uvm use     | [Usage](#usage-uvm-use)                    | select version for your utilities                                                       |
| uvm fix     | [Fix](#fix-uvm-fix)                        | if something is not working properly, <br />this command will refresh the whole project |
| uvm version | [Version](#version-uvm-version)            | retrieve current uvm version                                                            |


## Installation (uvm install)
This process creates installation folder for uvm project.
1. Download latest [release](https://github.com/Panaith/uvm.github.io/releases/latest).
2. Extract .zip file.
3. Open extracted folder find "uvm_install.bat" file and execute it.
4. Click "Yes" in Powershell prompt:  
   ![powershell admin mode](./readmePics/powershell_admin_mode.png)
5. Follow instructions...

### What happens
1. Creates the installation directory "C:\uvm".
2. Adds uvm project at directory "C:\uvm".
3. Updates Windows environment variables according to added utilities.
4. Continues to Configuration process...

## Configuration (uvm config)
This process allows user to configure uvm project according to his needs.
1. Click "Yes" in Powershell prompt.
2. Follow instructions...
3. Add as many utilities (Git, Java, Gradle, Maven, Node, Flutter, ...) as you need.
4. Remove any utilities that you don't need anymore.

### What happens
1. For example if you add "Java" utility:
    1. Adds "Java" utility directory "C:\uvm\utilities\java".
    2. Updates Windows environment variables according to added utilities.
2. For example if you remove "Java" utility:
    1. Deletes "Java" utility directory "C:\uvm\utilities\java".
    2. Updates Windows environment variables according to removed utilities.

## Add multiple versions for each registered utility (manually)
In this process the user manually adds the versions he wants for each of the utilities added in previous step.
For example if you added "Java" utility
1. Go to directory "C:\uvm\utilities". Here you will find a subfolder for your utility (i.e. if your utility is JAVA: you will find a subfolder named "java").
2. Download as many versions of your utility as you want (i.e. if your utility is JAVA: jdk_1.8, jdk_18, ...):
    1. Work with **binary** versions:
        1. Download **binary** version.
        2. Make sure that the downloaded folder is renamed according to its version.
        3. Move renamed folder to the corresponding utility subfolder under "C:\uvm\utilities" directory.
    2. Work with executable versions:
        1. Download **executable** version.
        2. Go to "C:\uvm\utilities" directory and open the subfolder that corresponds to your utility.
        3. Create a subfolder named according to the version you downloaded.
        4. Execute the executable and select as installation path the subfolder you created in previous step.
3. Do this whenever you want to support a **new** utility version.
4. Keep a structure as:  
   ![utilities - Version - Directory](./readmePics/utilities_versions_directory.png)

### What happens
Now for each utility, you have multiple versions.

## Usage (uvm use)
This process allows user to select which utility and which version he wants to use.
1. Follow instructions...

### What happens
1. Automatically Update Windows environment variables according to selected versions.
2. Now you can use the version you selected through terminal (cmd, powershell).

## Fix (uvm fix)
This process will refresh the whole uvm project installation, so you can use it in case something is not working properly.
It will automatically guide you to [Usage](#usage-uvm-use) process.

## Version (uvm version)
This process will return the current installed uvm project version.

## Future Work
- Support for other platforms (Linux, iOS, ...)
- Add uninstall feature.
- Support basic Utilities: Support for some basic utilities (Git, Java, Gradle, Maven, Flutter, ...) so that user does not need to give details for these utilities when adding one of them.
- Automate "Add multiple versions for each registered utility": Show all available/official versions for all supported utilities and ability to download selected versions from within uvm project.

## Most Important
This project was created for my convenience at my free time.  
Testing was time limited, but I don't think you will have any issues hopefully :).  
If you find a bug execute command ["uvm fix"](#fix-uvm-fix) and please [contact me](mailto:psarrid@gmail.com).  
If you want to participate in the project, you are most welcome, [contact me](mailto:psarrid@gmail.com).  
