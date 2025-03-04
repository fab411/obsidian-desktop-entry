# Manual Installation Guide

If you prefer to set up Obsidian manually without cloning this repository, follow these steps.

<!-- GETTING STARTED -->
## Getting Started
### Step 1: Create the `.desktop` File  
&nbsp; Create a `.desktop` file in one of the following locations:  
- **User-specific:** `~/.local/share/applications/`  

- **System-wide:** `/usr/share/applications/`


&nbsp; Run the following command to create the file:  
```bash
mkdir -p ~/.local/share/obsidian/
nano ~/.local/share/obsidian/Obsidian.desktop
```


### Step 2: Add the Following Content
&nbsp; Copy, paste and save the following content into the `Obsidian.desktop` file:
```bash
[Desktop Entry]
# Version of the desktop entry specification
Version=1.0 
# Name of the application
Name=Obsidian 
# Tooltip description
Comment=Open a Vault
# The path to the folder in which the executable is run
Path=HOME_DIR/.local/share/obsidian/
# The executable of the application, possibly with arguments.
Exec=HOME_DIR/.local/share/obsidian/Obsidian-1.8.7.AppImage
# The name of the icon that will be used to display this entry
Icon=HOME_DIR/.local/share/obsidian/images/obsidian_core.svg
# Describes whether this application needs to be run in a terminal or not
Terminal=false
# Describes the categories in which this entry should be shown
Categories=Utility;
# The type as listed above
Type=Application
X-Desktop-File-Install-Version=0.26
```

### Step 4: Rename the `HOME_DIR` 
Since `.desktop` files do not support `$HOME` or `~`, replace the placeholder `HOME_DIR` in `Obsidian.desktop` with your actual home directory:
```bash
cd ~/.local/share/obsidian
sed -i "s|HOME_DIR|$HOME|g" ~/.local/share/obsidian/Obsidian.desktop
```

### Step 5: Validate and Make It Executable
&nbsp; Run the following command to validate the `.desktop` file:
```bash
sudo desktop-file-validate ~/.local/share/obsidian/Obsidian.desktop
```
&nbsp; Make it executable:
```bash
chmod +x ~/.local/share/obsidian/Obsidian.desktop
```


### Step 6: Install the .desktop File
&nbsp; To install the file, run:
```bash 
sudo desktop-file-install --dir=$HOME/.local/share/applications $HOME/.local/share/obsidian/Obsidian.desktop
```


### Step 7: Update the Application Database
&nbsp; Update the application database so the new shortcut is recognized:
```bash 
sudo update-desktop-database ~/.local/share/applications/
```
&nbsp; The `Obsidian.desktop` file should be stored in:
```bash
ls ~/.local/share/applications/
```

<p align="right">(<a href="#readme-top">back to top</a>)</p>


## Usage
After completing the above steps, you can:
 - [x] Launch Obsidian from your application menu.
 - [x] Pin it to your favorites for quick access.

Let me know if you need help with anything else!

<p align="right">(<a href="#readme-top">back to top</a>)</p>
