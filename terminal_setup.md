Software Engineers Terminal Settings

Note: This setup is opinionated and reflects personal preferences. Feel free to tweak as needed.

Following assumptions are made for the environment
* Mac
* Iterm


### 1. Terminal Apperance


1.1 Theme Setup – Dracula

```
curl -O https://raw.githubusercontent.com/mbadolato/iTerm2-Color-Schemes/master/schemes/Dracula.itermcolors
```

Open iTerm2 → Preferences → Profiles → Colors → Color Presets

Import the downloaded file and select Dracula

1.2 Font Setup – JetBrains Mono

Download Fonts
```
curl -LO https://download.jetbrains.com/fonts/JetBrainsMono-2.304.zip && \
unzip JetBrainsMono-2.304.zip -d JetBrainsMono-2.304 && \
rm JetBrainsMono-2.304.zip
```

Copy the font to the Font Book
```
find JetBrainsMono-2.304 -name "*.ttf" -exec cp {} ~/Library/Fonts/ \;
```

3. UI Tweaks

Preferences → Appearance

Select Minimal for tab style


---


### 2. Shell setup

2.1 Install oh-my-zsh

Oh My Zsh is a Zsh configuration framework that:

* Organizes your .zshrc
* Provides many ready-to-use plugins (like git, z)
* Offers themes for customizing the prompt
* Simplifies setup and management of Zsh features

```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

2.1 Recommended Zsh Plugins 

**zsh-autosuggestions**
```
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```
Note: This plugin is installed in the same directory as existing plugins provided by oh-my-zsh for convienience.


**zsh-syntax-highlighting**

```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

After downloading the required plugins, enable them by editing your ~/.zshrc file. The plugin section should look like 

plugins=(git zsh-autosuggestions zsh-syntax-highlighting)

