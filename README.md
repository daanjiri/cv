# cv instructions

## install latex in your machine:

To install LaTeX on different operating systems, you'll typically use a distribution of LaTeX. TeX Live is a popular one for Unix/Linux, macOS, and Windows, while MiKTeX is often preferred for Windows. MacTeX is a variant of TeX Live tailored for macOS. Here are general instructions for installing LaTeX on these different OS systems:

### Windows

#### Using MiKTeX
1. **Download MiKTeX**: Go to the MiKTeX website (https://miktex.org/) and download the installer for Windows.
2. **Install MiKTeX**: Run the downloaded installer and follow the on-screen instructions to complete the installation. During the installation, you can choose whether to install missing packages on-the-fly.
3. **Update MiKTeX**: After installation, open the MiKTeX Console and check for updates. Apply any available updates to ensure you have the latest packages.

#### Using TeX Live
1. **Download TeX Live**: Visit the TeX Live website (http://tug.org/texlive/) and download the installer for Windows.
2. **Install TeX Live**: Run the installer and follow the instructions. This can take some time, as TeX Live is comprehensive.
3. **Update TeX Live**: Use the TeX Live Manager to update your installation with the latest packages.

### macOS

#### Using MacTeX
1. **Download MacTeX**: Go to the MacTeX website (http://tug.org/mactex/) and download the MacTeX.pkg file.
2. **Install MacTeX**: Open the downloaded package and follow the installation instructions. MacTeX includes the TeX Live distribution and additional Mac-specific utilities.
3. **Update MacTeX**: After installation, you can use the TeX Live Utility to update your packages.

### Unix/Linux

#### Using TeX Live
1. **Install TeX Live via Terminal**: Most Unix/Linux distributions include TeX Live in their package repositories. You can install it using your package manager.
   - For Debian/Ubuntu and derivatives: `sudo apt-get install texlive-full`
   - For Fedora/Red Hat: `sudo dnf install texlive-scheme-full` or `sudo yum install texlive-scheme-full`
   - For Arch Linux: `sudo pacman -S texlive-most`
2. **Update TeX Live**: Use `tlmgr`, the TeX Live Manager, to update your packages. Run `sudo tlmgr update --self && sudo tlmgr update --all` in the terminal.

## install LaTeX Workshop vs code extension
    - https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop
    - this is a tutorial how to use it and compile your document into pdf! https://www.youtube.com/watch?v=CmagZthwhaY

## install dependencies packages:

    To manage LaTeX package dependencies like `geometry`, `hyperref`, `enumitem`, and `titlesec`, the process is quite straightforward and generally OS-independent because it relies on the LaTeX distribution's package manager. Both TeX Live and MiKTeX, the most popular LaTeX distributions, include package managers that automate the installation of packages. Here's how to handle it in each:

### Using TeX Live (Linux, macOS, and Windows)

TeX Live uses `tlmgr` (TeX Live Manager) for package management. To install packages, you would use the terminal (Command Prompt in Windows, Terminal in macOS and Linux). The basic command format is:

```sh
tlmgr install packagename
```

To install your dependencies, you would execute:

```sh
tlmgr install geometry hyperref enumitem titlesec
```

You might need to prefix the command with `sudo` on macOS and Linux if you're installing packages system-wide:

```sh
sudo tlmgr install geometry hyperref enumitem titlesec
```

This requires an internet connection, and `tlmgr` will automatically download and install the packages for you.

### Using MiKTeX (Primarily Windows, also available on macOS and Linux)

MiKTeX uses the MiKTeX Console to manage packages. You can install packages using both the console's GUI and the command line. Here’s how:

#### Using MiKTeX Console GUI
1. Open the MiKTeX Console.
2. Go to the "Packages" section.
3. Search for the package you wish to install (`geometry`, `hyperref`, `enumitem`, `titlesec`).
4. Right-click on the package name and choose "Install".

#### Using the Command Line in MiKTeX
MiKTeX also allows you to install packages via command line with `mpm` (MiKTeX Package Manager). The command format is:

```sh
mpm --install=packagename
```

However, for most users, MiKTeX's auto-install feature simplifies the process. If you compile a document that requires a package not currently installed, MiKTeX prompts you to install the missing package on-the-fly (if this feature is enabled in the MiKTeX Console settings).

# RUN
compile your cv.tex and see the pdf 