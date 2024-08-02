# Order of installations

1. Install FISH
   - Linux:
      - add repositories by following this link: https://launchpad.net/~fish-shell/+archive/ubuntu/release-3
      - set as default shell by:
        ```
        chsh -s /usr/bin/fish
      - log out/log back in of Operating System
      - run fish_config for changing themes/prompt options
3. Install NEOVIM
   - Go to: https://github.com/neovim/neovim/releases/tag/v0.10.0
   - Under Assets (at the bottom of screen) donwload: nvim.appimage
   - Run ```chmod u+x nvim.appimage && ./nvim.appimage```
   - Move the Neovim app image to /usr/local/bin folder ```sudo mv nvim.appimage /usr/local/bin/nvim```
   - Try openning from any location in terminal by running: ```nvim```
4. Install fisher:
    - https://github.com/jorgebucaran/fisher
5. Install bass with fisher ( https://github.com/edc/bass ):
   ```
      fisher install edc/bass
   ```
6. Install nvm: https://github.com/nvm-sh/nvm#installation-and-update
7. Create a function file to hold the source command for nvm:
   ```
      touch ~/.config/fish/functions/nvm.fish
   ```
8. add the following function in that newly created file:
     ```
        function nvm
           bass source ~/.nvm/nvm.sh --no-use ';' nvm $argv
        end
     ```
9. Install node.js and npm via nvm:
    ```
      nvm install --lts
    ```
   ```
      nvm alias default node
10. Verify that the step above worked by:
   ```
      node --version
   ```
   ```
      npm -- version
   ```
11. Install live-server:
    ```
    npm install -g live-server
    ```
12. Install tmux:
    ```
    sudo apt-get install tmux
    ```
13. Install Rust & Cargo
    - Go to: https://doc.rust-lang.org/book/ch01-01-installation.html
    - Add to FISH path:
      ```
      fish_add_path ~/.cargo/bin/
      ```
    - Log out/log in of OS
    - Confirm rust is in path by the following:
      ```
      rustc --version
      ```
14. Install EZA (don't use cargo, follow the respective Distribution directions)
    - Go to: https://eza.rocks/
15. Install Hack Nerd Fonts (https://www.nerdfonts.com/font-downloads)
    - On windows unzip the file and highlight all fonts and right click -> install
    - On linux unzip -> double click -> and you should see an option to install. You might have to google it if this is not the case
    - In your terminal, go to settings and change the default font to Hack Nerd
