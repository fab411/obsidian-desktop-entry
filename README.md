README: Creating a .desktop File for Application Shortcuts

# 📌 Creating a `.desktop` File for Application Shortcuts  

## 🚀 Introduction  
This guide walks you through creating a `.desktop` file to add an application shortcut to your system's application menu. This is useful for launching programs that do not automatically create a menu entry.  

Once added, the shortcut will be searchable using the **Super key**, and you can pin it to favorites for easy access.  

---

## 📂 What is a `.desktop` File?  
A `.desktop` file is a configuration file used in Linux desktop environments (**GNOME, KDE, XFCE, etc.**) to create application shortcuts.  

## 🛠 How to Create a `.desktop` File  

### 1️⃣ Step 1: Create the `.desktop` File  
Create a `.desktop` file in one of the following locations:  
- **User-specific:** `~/.local/share/applications/`  
- **System-wide:** `/usr/share/applications/`

Run the following command to create the file:  
```bash
sudo nano ~/.local/share/obsidian/Obsidian.desktop
```


### 2️⃣ Step 2: Add the Following Content
Copy, paste and save the following content into the .desktop file:
```bash
[Desktop Entry]
Version=1.0  # Version of the desktop entry specification
Name=Obsidian  # Name of the application
Comment=Open a Vault  # Tooltip description
Path=/home/fab/Applications/Obsidian/  # Path to the application folder
Exec=/home/fab/Applications/Obsidian/Obsidian-1.8.7.AppImage  # Executable file
Icon=/home/fab/Applications/Obsidian/Icon/obsidian1.svg  # Icon file path
Terminal=false  # Does not require a terminal
Categories=Utility;  # Application category
Type=Application  # Specifies the file type
X-Desktop-File-Install-Version=0.26
```


### 3️⃣ Step 3: Validate and Make It Executable
Run the following command to validate the .desktop file:
```bash
desktop-file-validate ~/.local/share/obsidian/Obsidian.desktop
```
Make it executable:
```bash
chmod +x ~/.local/share/obsidian/Obsidian.desktop
```


### 4️⃣ Step 4: Install the .desktop File
To install the file, run:
```bash 
desktop-file-install --dir=$HOME/.local/share/applications $HOME/.local/share/obsidian/Obsidian.desktop
```


### 5️⃣ Step 5: Update the Application Database
Update the application database so the new shortcut is recognized:
```bash 
update-desktop-database ~/.local/share/applications
```
The .desktop file should be stored in:
```bash
ls ~/.local/share/applications/ #Obsidian.desktop
```


### 6️⃣ Step 6: Launch the Application
Now, you should be able to find Obsidian in your application menu. You can also search for it using the Super key or add it to favorites.


---



## 🔗 Useful Links
Read more at: [https://www.commandlinux.com/man-page/man1/](https://specifications.freedesktop.org/desktop-entry-spec/latest/index.html#introduction) 

more information: https://www.baeldung.com/linux/desktop-entry-files
desktop-file-install: https://www.commandlinux.com/man-page/man1/desktop-file-install.1.html
create own icon: https://obsidian.md/blog/new-obsidian-icon/


Let me know if you need help with anything else!

