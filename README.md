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
3. Install fisher:
    - https://github.com/jorgebucaran/fisher
4. Install bass with fisher ( https://github.com/edc/bass ):
   ```
      fisher install edc/bass
   ```
5. Install nvm: https://github.com/nvm-sh/nvm#installation-and-update
6. Create a function file to hold the source command for nvm:
   ```
      touch ~/.config/fish/functions/nvm.fish
   ```
7. add the following function in that newly created file:
     ```
        function nvm
           bass source ~/.nvm/nvm.sh --no-use ';' nvm $argv
        end
     ```
8. Install node.js and npm via nvm:
    ```
      nvm install --lts
    ```
   ```
      nvm alias default node
   ```
9. Verify that the step above worked by:
   ```
      node --version
   ```
   ```
      npm -- version
   ```
10. Install Helix editor
      - Go to: https://docs.helix-editor.com/install.html
      - Remember: to use hx instead of vim when editing a file in the terminal!
      - Install HTML language-server:npm i -g vscode-langservers-extracted (https://github.com/hrsh7th/vscode-langservers-extracted)
      - Install javascript language-server: npm install -g typescript-language-server typescript (https://github.com/typescript-language-server/typescript-language-server)  
11. Install EXA:
      - Linux: 
        ```
           sudo apt install exa
        ```  
      - Mac OS:
        ```
           brew install exa
        ```
12. Install python pip
       - Linux:
          ```
             sudo apt install python3-pip
          ```
       - Mac OS:
           ```
               brew install python3
           ```
13. Install Dotbot
    ```
       pip3 install dotbot
    ```
      - add dotobot to path ( only for Linux ):
        ```
           set -U fish_user_paths $HOME/.local/bin $fish_user_paths
        ```
      - Go to your github page and copy the SSH link to the dotfiles repository
      - In your terminal, make sure you are in the home directory
      - Enter the following command in the terminal:
        ```
           git clone git@github.com:valtix/.dotfiles.git
        ```
      - cd into your new dotfiles folder
      - run the terminal command:
        ```
           dotbot -c install.conf.yaml
        ```
14. Install live-server:
    - npm install -g live-server
15. Install tmux:
    - sudo apt-get install tmux
16. Install Rust & Cargo
    - Go to: https://doc.rust-lang.org/cargo/getting-started/installation.html
    - Exit shell and log back in
    - Add to FISH path: set -U fish_user_paths $HOME/.cargo/env $fish_user_paths
    - Exit shell and log back in
17. Install Hack Nerd Fonts (https://www.nerdfonts.com/font-downloads)
    - On windows unzip the file and highlight all fonts and right click -> install
    - On linux unzip -> double click -> and you should see an option to install. You might have to google it if this is not the case
