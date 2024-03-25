# My TMUX Setup

## Steps

1. Install the latest version of **TMUX** by following instructions from [here](https://github.com/tmux/tmux/wiki/Installing).

   - For Fedora use : `dnf install tmux`

2. Copy the configuration file from this repository as `~/.tmux.conf` or `XDG_CONFIG_HOME/tmux/tmux.conf`

   ```bash
   # For symlink
   mkdir ~/.config/tmux
   git clone https://github.com/Aadmi1234/my-tmux-config.git
   ln -s my-tmux-config/tmux.conf ~/.config/tmux/tmux.conf
   ```

   <p style="text-align: center;">OR</p>

   ```bash
   cd ~
   curl -L https://raw.githubusercontent.com/Aadmi1234/my-tmux-config/master/tmux.conf | > .tmux.conf
   ```

   <p style="text-align: center;">OR</p>

   ```bash
   mkdir ~/.config/tmux
   cd ~/.config/tmux
   curl -L https://raw.githubusercontent.com/Aadmi1234/my-tmux-config/master/tmux.conf | > tmux.conf
   ```

4. Download [**TPM**](https://github.com/tmux-plugins/tpm) to install and load **TMUX** plugins.

   Clone TPM :

   ```bash
   git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
   ```

5. Reload TMUX environment so TPM is sourced, type this in terminal if tmux is already running :

   ```bash
   tmux source-file ~/.tmux.conf
   ```

   <p style="text-align: center;">OR</p>

   ```bash
   tmux source-file ~/.config/tmux/tmux.conf
   ```

6. To install the existing plugins :

   - Press `prefix` + <kbd>I</kbd> , to fetch the plugin.
   - The plugin was cloned to `~/.tmux/plugins` dir and sourced.

7. To install new plugins :

   - See the instruction [here](https://github.com/tmux-plugins/tpm#installation).
   - See the list of plugins [here](https://github.com/tmux-plugins/list).
