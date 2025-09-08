# dotfiles-win

These are my user-specific configuration files that I use to personalize my Windows experience.

> :warning: Be aware, products can change over time. I do my best to keep up with the latest changes and releases, but please understand that this won’t always be the case.

## Usage

1. Clone this repository
2. Make sure to move, rename or delete the original config files
3. Create symlinks to the configuration files provided by this repository using the mklink console command (cmd.exe with admin rights).:
    - Starship:
        ```console
           mklink "C:\Users\<user>\.starship\starship.toml" "<path-to-git-repo>\starship.toml"
        ```
    - PowerShell:
        ```console
           mklink "C:\Users\<user>\Documents\WindowsPowerShell\Microsoft.PowerShell_profile.ps1" "<path-to-git-repo>\Microsoft.PowerShell_profile.ps1"
        ```
    - Windows Terminal (the additional deletion of the original file is needed because it gets recreated within seconds):
        ```console
           del "<settings-path>" && mklink "<settings-path>" "C:\Dev\git\dotfiles-win\windows-terminal-settings.json
        ```
        Depending on the Windows Terminal installation type, use one of the following for `<settings-path>`:
        - stable / general release: `%LOCALAPPDATA%\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState\settings.json`
        - preview release: `%LOCALAPPDATA%\Packages\Microsoft.WindowsTerminalPreview_8wekyb3d8bbwe\LocalState\settings.json`
        - unpackaged (Scoop, Chocolatey, etc): `%LOCALAPPDATA%\Microsoft\Windows Terminal\settings.json`

## Terminal and Application Icons with Nerd-Fonts

To display icons in terminal or applications Fonts, I'm using [Nerd-Fonts](https://www.nerdfonts.com). I'm currently using the **Hack Nerd Font Mono** in terminal applications.

## Contribution

If you’d like to contribute to this project, feel free to create a pull request for the necessary changes.