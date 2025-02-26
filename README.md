README: Creating a .desktop File for Application Shortcuts

📌 Introduction
This guide helps you create a .desktop file to add an application shortcut to your system's application menu. This is useful for launching programs that do not automatically create a menu entry.
After that, there is a desktop entry and is be searchable using the Super key or to add to favourites.

📂 What is a .desktop File?
A .desktop file is a configuration file used in Linux desktop environments (GNOME, KDE, XFCE, etc.) to create application shortcuts.

🛠 How to Create a .desktop File
1️⃣ Step 1: Create the .desktop File
Create a .desktop file in ~/.local/share/applications/ (for a user) or /usr/share/applications/ (for system-wide use).

Run:
sudo nano ~/.local/share/obsidian/Obsidian.desktop

2️⃣ Step 2: Add the Following Content
[Desktop Entry]
# The version of the desktop entry specification to which this file complies
Version=1.0
# The name of the application
Name=Obsidian
# A comment which can/will be used as a tooltip
Comment=Open a Vault
# The path to the folder in which the executable is run
Path=/home/fab/Applications/Obsidian/
# The executable of the application, possibly with arguments.
Exec=/home/fab/Applications/Obsidian/Obsidian-1.8.7.AppImage
# The name of the icon that will be used to display this entry
Icon=/home/fab/Applications/Obsidian/Icon/obsidian1.svg
# Describes whether this application needs to be run in a terminal or not
Terminal=false
# Describes the categories in which this entry should be shown
Categories=Utility;
# The type as listed above
Type=Application
X-Desktop-File-Install-Version=0.26


3️⃣ Step 3: Validate and Make It Executable
desktop-file-validate ~/.local/share/obsidian/Obsidian.desktop
chmod +x ~/.local/share/obsidian/Obsidian.desktop

4️⃣ Step 4 install .desktop file. All .desktop files are saved in $HOME/.local/share/applications
desktop-file-install --dir=$HOME/.local/share/applications $HOME/.local/share/obsidian/Obsidian.desktop

4️⃣ Step 4: Update the Application Database
update-desktop-database ~/.local/share/obsidian

5️⃣ Step 5: Launch the Application


🔗 Useful Links
Read more at: [https://www.commandlinux.com/man-page/man1/](https://specifications.freedesktop.org/desktop-entry-spec/latest/index.html#introduction)
more information: https://www.baeldung.com/linux/desktop-entry-files
desktop-file-install: https://www.commandlinux.com/man-page/man1/desktop-file-install.1.html
create own icon: https://obsidian.md/blog/new-obsidian-icon/


Feel free to improve this README by adding new helpful links and tips! 🚀

