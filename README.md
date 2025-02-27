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
*** The Markdown Links & Immages reference links are at the end of the readme 
-->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![Unlicense License][license-shield]][license-url]
<!--[![LinkedIn][linkedin-shield]][linkedin-url] -->

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/fab411/Obsidian.desktop/blob/main/images/obsidian_core.svg">
    <img src="images/obsidian_core.svg" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">Creating a .desktop File for Application Shortcuts</h3>
  <p align="center">
    An awesome README to run Obsidian via the graphical interface and make the work process smoother
    <br />
    <a href="https://github.com/fab411/Obsidian.desktop"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/fab411/Obsidian.desktop">View Demo</a>
    &middot;
    <a href="https://github.com/fab411/Obsidian.desktop/issues/new?labels=bug&template=bug-report---.md">Report Bug</a>
    &middot;
    <a href="https://github.com/fab411/Obsidian.desktop/issues/new?labels=enhancement&template=feature-request---.md">Request Feature</a>
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <!--<ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>-->
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <!--<ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>-->
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#links">Useful Links</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>


# Creating a Obsidian.desktop File for Application Shortcuts

## About The Project

This guide helps you create a `.desktop` file to add an application shortcut to your Linux desktop environment (GNOME, KDE, XFCE, etc.). Once added, the shortcut will be searchable using the **Super key**, and you can pin it to favorites.

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!--
### Built With

This section should list any major frameworks/libraries used to bootstrap your project. Leave any add-ons/plugins for the acknowledgements section. Here are a few examples.

* [![Next][Next.js]][Next-url]
* [![React][React.js]][React-url]
* [![Vue][Vue.js]][Vue-url]
* [![Angular][Angular.io]][Angular-url]
* [![Svelte][Svelte.dev]][Svelte-url]
* [![Laravel][Laravel.com]][Laravel-url]
* [![Bootstrap][Bootstrap.com]][Bootstrap-url]
* [![JQuery][JQuery.com]][JQuery-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>
-->
## Obsidian-*.AppImage Placeholder  

This repository does **not** include the Obsidian `.AppImage` file to keep the project lightweight.  

### Download Obsidian  
To get the latest version, download `Obsidian-*.AppImage` from the official website: [Obsidian Download Page](https://obsidian.md)  

After downloading, place the file in:  
```bash
~/.local/share/obsidian/
```
<!-- GETTING STARTED -->
## Getting Started
### Step 1: Create the `.desktop` File  
&nbsp; Create a `.desktop` file in one of the following locations:  
- **User-specific:** `~/.local/share/applications/`  
- **System-wide:** `/usr/share/applications/`

&nbsp; Run the following command to create the file:  
```bash
sudo nano ~/.local/share/obsidian/Obsidian.desktop
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
Path=/home/fab/.local/share/obsidian/
# The executable of the application, possibly with arguments.
Exec=/home/fab/.local/share/obsidian/Obsidian-1.8.7.AppImage
# The name of the icon that will be used to display this entry
Icon=/home/fab/.local/share/obsidian/images/obsidian_core.svg
# Describes whether this application needs to be run in a terminal or not
Terminal=false
# Describes the categories in which this entry should be shown
Categories=Utility;
# The type as listed above
Type=Application
X-Desktop-File-Install-Version=0.26
```


### Step 3: Validate and Make It Executable
&nbsp; Run the following command to validate the `.desktop` file:
```bash
sudo desktop-file-validate ~/.local/share/obsidian/Obsidian.desktop
```
&nbsp; Make it executable:
```bash
chmod +x ~/.local/share/obsidian/Obsidian.desktop
```


### Step 4: Install the .desktop File
&nbsp; To install the file, run:
```bash 
sudo desktop-file-install --dir=$HOME/.local/share/applications $HOME/.local/share/obsidian/Obsidian.desktop
```


### Step 5: Update the Application Database
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

<!-- LINKS -->
## Links
<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
* [Here you can find all Desktop Entry Specifications](https://specifications.freedesktop.org/desktop-entry-spec/latest/)
* [plus further explanations](https://www.baeldung.com/linux/desktop-entry-files)
* [and the arguments of the `desktop-file-install` terminal command](https://www.commandlinux.com/man-page/man1/desktop-file-install.1.html)
* [an Icon randomizer also exists](https://obsidian.md/blog/new-obsidian-icon/)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!--ROADMAP--> 
## Roadmap

- [x] Add Changelog
- [x] Add AppImage Stuff
- [ ] Add Acknowledgments
    - [ ] Move Link Section to acknowledgement
    - [ ] Obsidian Forum link
- [ ] Repository Structure & Organization
    - [ ] Just download "obsidian" repo an copy into  ~/.local/share/
    - [ ] Just download "obsidian.desktop" repo, with an obsidian folder into it.
    - [ ] Modify paths after decision
- [ ] Modify file paths to be more generic and avoid hardcoded /home/fab/ paths
    - [ ] .desktop files and compatibility
- [ ] Update Table of Contents
- [ ] Add "components" document to easily copy & paste sections of the readme
- [ ] Multi-language Support
    - [ ] German
    - [ ] Arabic

See the [open issues](https://github.com/othneildrew/Best-README-Template/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Top :

<a href="https://github.com/fab411/Obsidian.desktop/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=fab411/Obsidian.desktop" alt="contrib.rocks image" />
</a>

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- LICENSE -->
## License

Distributed under the Unlicense License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- CONTACT -->
## Contact

Fabian Lang - FabianLang@posteo.net <!--[@your_twitter](https://twitter.com/your_username)-->

Project Link: [https://github.com/fab411/Obsidian.desktop](https://github.com/fab411/Obsidian.desktop)


<!--https://github.com/fab411/Obsidian.desktop/blob/main/README.md-->

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

Use this space to list resources you find helpful and would like to give credit to. I've included a few of my favorites to kick things off!

* [Choose an Open Source License](https://choosealicense.com)
* [GitHub Pages](https://pages.github.com)
* [Img Shields](https://shields.io)
* [GitHub Emoji Cheat Sheet](https://www.webpagefx.com/tools/emoji-cheat-sheet)
* [React Icons](https://react-icons.github.io/react-icons/search)

<!--* * [Font Awesome](https://fontawesome.com)
  * * [Malven's Flexbox Cheatsheet](https://flexbox.malven.co/)
* [Malven's Grid Cheatsheet](https://grid.malven.co/-->

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
[repo]: https://github.com/fab411/Obsidian.desktop
[link]: fab411/Obsidian.desktop
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=for-the-badge
[contributors-url]: https://github.com/fab411/Obsidian.desktop/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/fab411/Obsidian.desktop.svg?style=for-the-badge
[forks-url]: https://github.com/fab411/Obsidian.desktop/network/members
[stars-shield]: https://img.shields.io/github/stars/fab411/Obsidian.desktop.svg?style=for-the-badge
[stars-url]: https://github.com/fab411/Obsidian.desktop/stargazers
[issues-shield]: https://img.shields.io/github/issues/fab411/Obsidian.desktop.svg?style=for-the-badge
[issues-url]: https://github.com/fab411/Obsidian.desktop/issues
[license-shield]: https://img.shields.io/github/license/fab411/Obsidian.desktop.svg?style=for-the-badge
[license-url]: https://github.com/fab411/Obsidian.desktop/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/othneildrew

<!--
[Next.js]: https://img.shields.io/badge/next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white
[Next-url]: https://nextjs.org/
[React.js]: https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB
[React-url]: https://reactjs.org/
[Vue.js]: https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D
[Vue-url]: https://vuejs.org/
[Angular.io]: https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white
[Angular-url]: https://angular.io/
[Svelte.dev]: https://img.shields.io/badge/Svelte-4A4A55?style=for-the-badge&logo=svelte&logoColor=FF3E00
[Svelte-url]: https://svelte.dev/
[Laravel.com]: https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white
[Laravel-url]: https://laravel.com
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[JQuery.com]: https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white
[JQuery-url]: https://jquery.com 
[forks-url]: https://github.com/othneildrew/Best-README-Template/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=for-the-badge
[stars-url]: https://github.com/othneildrew/Best-README-Template/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=for-the-badge
[issues-url]: https://github.com/othneildrew/Best-README-Template/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/othneildrew/Best-README-Template/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/othneildrew
[product-screenshot]: images/screenshot.png
[Next.js]: https://img.shields.io/badge/next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white
[Next-url]: https://nextjs.org/
[React.js]: https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB
[React-url]: https://reactjs.org/
[Vue.js]: https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D
[Vue-url]: https://vuejs.org/
[Angular.io]: https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white
[Angular-url]: https://angular.io/
[Svelte.dev]: https://img.shields.io/badge/Svelte-4A4A55?style=for-the-badge&logo=svelte&logoColor=FF3E00
[Svelte-url]: https://svelte.dev/
[Laravel.com]: https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white
[Laravel-url]: https://laravel.com
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[JQuery.com]: https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white
[JQuery-url]: https://jquery.com 
-->
