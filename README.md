<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a id="readme-top"></a>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![Unlicense License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/fab411/Obsidian/blob/main/Icons/obsidian1.svg">
    <img src="Icons/obsidian1.svg" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">Creating a .desktop File for Application Shortcuts</h3>
  <!--
  <p align="center">
    An awesome README template to jumpstart your projects!
    <br />
    <a href="https://github.com/othneildrew/Best-README-Template"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/othneildrew/Best-README-Template">View Demo</a>
    &middot;
    <a href="https://github.com/othneildrew/Best-README-Template/issues/new?labels=bug&template=bug-report---.md">Report Bug</a>
    &middot;
    <a href="https://github.com/othneildrew/Best-README-Template/issues/new?labels=enhancement&template=feature-request---.md">Request Feature</a>
  </p>
  -->
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>


# README: Creating a .desktop File for Application Shortcuts

## About The Project

This guide helps you create a `.desktop` file to add an application shortcut to your Linux desktop environment (GNOME, KDE, XFCE, etc.). Once added, the shortcut will be searchable using the **Super key**, and you can pin it to favorites.

<p align="right">(<a href="#readme-top">back to top</a>)</p>
---

## Getting Started
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

---
## Usage
After completing the above steps, you can:
- [x] Launch Obsidian from your application menu.
- [x] Pin it to your favorites for quick access.


## 🔗 Useful Links
<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
* [Read more at ](https://specifications.freedesktop.org/desktop-entry-spec/latest/)
* [more information](https://www.baeldung.com/linux/desktop-entry-files)
* [desktop-file-install](https://www.commandlinux.com/man-page/man1/desktop-file-install.1.html)
* [create own icon](https://obsidian.md/blog/new-obsidian-icon/)


Let me know if you need help with anything else!

<!-- LICENSE -->
<!-- ## License

Distributed under the Unlicense License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p> -->

