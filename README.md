# Order of installations

1. Install FISH
   - Linux:
      - add repositories by following this link: https://launchpad.net/~fish-shell/+archive/ubuntu/release-3
      - set as default shell by:
        ```
        chsh -s /usr/bin/fish
      - log out/log back in of Operating System
      - run fish_config for changing themes/prompt options
   - Mac OS:
      - Check the fish path with which fish. In the examples below it was located at: /opt/homebrew/bin/fish. On older Macs the path might differ.
      - Add fish to the know shells run the command: sudo sh -c 'echo /opt/homebrew/bin/fish >> /etc/shells'
      - Restart your terminal
      - Set fish as the default shell run the command: chsh -s /opt/homebrew/bin/fish
      - Restart your terminal and check if it launched with fish or not
      - Add brew binaries in fish path run the command: fish_add_path /opt/homebrew/bin 
2. Install fisher:
    - https://github.com/jorgebucaran/fisher
3. Install bass with fisher ( https://github.com/edc/bass ):
   ```
      fisher install edc/bass
   ```
4. Install nvm: https://github.com/nvm-sh/nvm#installation-and-update
5. Create a function file to hold the source command for nvm:
   ```
      touch ~/.config/fish/functions/nvm.fish
   ```
6. add the following function in that newly created file:
     ```
        function nvm
           bass source ~/.nvm/nvm.sh --no-use ';' nvm $argv
        end
     ```
7. Install node.js and npm via nvm:
    ```
      nvm install --lts
    ```
   ```
      nvm alias default node
   ```
8. Verify that the step above worked by:
   ```
      node --version
   ```
   ```
      npm -- version
   ```
9. Install live-server:
    ```
    npm install -g live-server
    ```
10. Install tmux:
    ```
    sudo apt-get install tmux
    ```
11. Install Rust & Cargo
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
12. Install EZA (don't use cargo, follow the respective Distribution directions)
    - Go to: https://eza.rocks/
13. Install Hack Nerd Fonts (https://www.nerdfonts.com/font-downloads)
    - On windows unzip the file and highlight all fonts and right click -> install
    - On linux unzip -> double click -> and you should see an option to install. You might have to google it if this is not the case
    - In your terminal, go to settings and change the default font to Hack Nerd
