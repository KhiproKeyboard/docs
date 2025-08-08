# Khipro Keyboard Documentation

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

Khipro is an innovative Bengali typing system designed for a fast, efficient, and intelligent typing experience. It eliminates the need for frequent use of the Shift key, offering a more streamlined and comfortable typing experience.

## Features

-   **Shift-Free Typing:** No need to use the Shift key for most characters.
-   **Intelligent Suggestions:** Smart auto-completion with typing booster.
-   **Cross-Platform:** Supports Linux, Windows, and Android (coming soon).
-   **Case-Insensitive:** Inspired by the Chinese Pinyin method.

## Installation

### Linux

1.  **Install Prerequisites:**
    *   Install `m17n` and either `Fcitx-m17n` or `ibus-m17n` depending on your input method.
    *   For intelligent suggestions, install `ibus-typing-booster` (recommended with `ibus-m17n`).

    ```bash
    # Debian/Ubuntu
    sudo apt install ibus-m17n ibus-typing-booster

    # Fedora
    sudo dnf install ibus-m17n ibus-typing-booster
    ```

2.  **Install Khipro:**

    ```bash
    # IBus users
    sudo rm /usr/share/m17n/bn-khipro*.mim; cd ~/; rm -rf khipro-m17n; git clone https://github.com/rank-coder/khipro-m17n.git; cd ~/khipro-m17n; sudo cp bn-khipro*.mim /usr/share/m17n/

    # Fcitx5 users
    sudo rm /usr/share/m17n/bn-khipro*.mim && cd ~/ && sudo rm -rf ~/khipro-m17n && git clone https://github.com/rank-coder/khipro-m17n.git && cd ~/khipro-m17n && sudo cp bn-khipro*.mim /usr/share/m17n/ && fcitx5 restart
    ```

3.  **Configure:**
    *   Restart your computer or log out and log back in.
    *   Add "Bengali (khipro-m17n)" in your system's input method settings.
    *   Configure `ibus-typing-booster` for the best experience.

### Windows

-   **Borno Keyboard:** Khipro layout is built-in in the latest version of Borno Native.
    1.  Download the latest version from [Codepotro's Telegram Support Group](https://t.me/codepotro).
    2.  Install the application.
    3.  Select the Khipro layout from keyboard settings.
-   **Nms Kontho:** Use the custom layout for Nms Kontho application.
    1.  Install [NMS Kontho](https://nabil-bot.github.io/Kontho/).
    2.  Download [Khipro NMS Layout](https://github.com/NabilSnigdho/khipro-nms/raw/refs/heads/main/Khipro.nmsLayout).
    3.  Import the downloaded layout.
    4.  Restart NMS Kontho.
    5.  Select the Khipro layout.

### Android

-   Coming soon in [Borno Android Keyboard](https://play.google.com/store/apps/details?id=com.codepotro.borno.keyboard).

## Usage

Khipro offers a unique typing experience by mapping Bengali characters to the English keyboard in a case-insensitive manner. This eliminates the need for the Shift key, resulting in faster and more comfortable typing.


### Mapping and Syntax

Refer to the [Mapping and Syntax Guide](docs/mapping-syntax) for a complete mapping table and usage instructions.

## Configuration

For the best experience, configure `ibus-typing-booster` with Khipro. See the [Configuration Guide](docs/configuration) for detailed instructions.

## Updating and Uninstalling

Refer to the [Update and Uninstall Guide](docs/update-uninstall) for instructions on how to update or uninstall Khipro.

## Using Without Typing Booster

Khipro can also be used without typing booster. See the [Using Without Typing Booster Guide](docs/without-typing-booster) for more information.

## Contributing

Khipro is a community project. You are welcome to contribute!

-   [Telegram Group](https://t.me/+oXLVpYDtyDNmYzll): For direct support and discussions.
-   [GitHub Organization](https://github.com/KhiproKeyboard): View code and contribute.

## License

Khipro is a free software project. All code is open source and community-driven.

[MIT](LICENSE)
