Oh My Zsh is an open source, community-driven framework for managing your zsh configuration. Sounds boring. Lets try again. Oh My Zsh will not make you a 10x developer...but you might feel like one. Once installed, your terminal shell will become the talk of the town or your money back! With each keystroke in your command prompt, youll take advantage of the hundreds of powerful plugins and beautiful themes. Strangers will come up to you in cafés and ask you, "that is amazing! are you some sort of genius?" Finally, youll begin to get the sort of attention that you have always felt you deserved. ...or maybe youll use the time that youre saving to start flossing more often. 😬 To learn more, visit ohmyz.sh and follow @ohmyzsh on Twitter. Getting Started Prerequisites Disclaimer: Oh My Zsh works best on macOS and Linux. Unix-like operating system (macOS or Linux) Zsh should be installed (v4.3.9 or more recent). If not pre-installed (zsh --version to confirm), check the following instruction here: Installing ZSH curl or wget should be installed git should be installed Basic Installation Oh My Zsh is installed by running one of the following commands in your terminal. You can install this via the command-line with either curl or wget. via curl shell sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)" via wget shell sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)" Using Oh My Zsh Plugins Oh My Zsh comes with a shitload of plugins to take advantage of. You can take a look in the plugins directory and/or the wiki to see whats currently available. Enabling Plugins Once you spot a plugin (or several) that youd like to use with Oh My Zsh, youll need to enable them in the .zshrc file. Youll find the zshrc file in your $HOME directory. Open it with your favorite text editor and youll see a spot to list all the plugins you want to load. shell vi ~/.zshrc For example, this might begin to look like this: shell plugins=( git bundler dotenv osx rake rbenv ruby ) Using Plugins Most plugins (should! were working on this) include a README, which documents how to use them. Themes Well admit it. Early in the Oh My Zsh world, we may have gotten a bit too theme happy. We have over one hundred themes now bundled. Most of them have screenshots on the wiki. Check them out! Selecting a Theme Robbys theme is the default one. Its not the fanciest one. Its not the simplest one. Its just the right one (for him). Once you find a theme that youd like to use, you will need to edit the ~/.zshrc file. Youll see an environment variable (all caps) in there that looks like: shell ZSH_THEME="robbyrussell" To use a different theme, simply change the value to match the name of your desired theme. For example: ```shell ZSH_THEME="agnoster" # (this is one of the fancy ones) see https://github.com/robbyrussell/oh-my-zsh/wiki/Themes#agnoster ``` Note: many themes require installing the Powerline Fonts in order to render properly. Open up a new terminal window and your prompt should look something like this: In case you did not find a suitable theme for your needs, please have a look at the wiki for more of them. If youre feeling feisty, you can let the computer select one randomly for you each time you open a new terminal window. shell ZSH_THEME="random" # (...please let it be pie... please be some pie..) And if you want to pick random theme from a list of your favorite themes: shell ZSH_THEME_RANDOM_CANDIDATES=( "robbyrussell" "agnoster" ) Advanced Topics If youre the type that likes to get their hands dirty, these sections might resonate. Advanced Installation Some users may want to change the default path, or manually install Oh My Zsh. Custom Directory The default location is ~/.oh-my-zsh (hidden in your home directory) If youd like to change the install directory with the ZSH environment variable, either by running export ZSH=/your/path before installing, or by setting it before the end of the install pipeline like this: shell export ZSH="$HOME/.dotfiles/oh-my-zsh"; sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)" Manual Installation 1. Clone the repository: shell git clone https://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh 2. Optionally, backup your existing ~/.zshrc file: shell cp ~/.zshrc ~/.zshrc.orig 3. Create a new zsh configuration file You can create a new zsh config file by copying the template that we have included for you. shell cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc 4. Change your default shell shell chsh -s /bin/zsh 5. Initialize your new zsh configuration Once you open up a new terminal window, it should load zsh with Oh My Zshs configuration. Installation Problems If you have any hiccups installing, here are a few common fixes. You might need to modify your PATH in ~/.zshrc if youre not able to find some commands after switching to oh-my-zsh. If you installed manually or changed the install location, check the ZSH environment variable in ~/.zshrc. Custom Plugins and Themes If you want to override any of the default behaviors, just add a new file (ending in .zsh) in the custom/ directory. If you have many functions that go well together, you can put them as a XYZ.plugin.zsh file in the custom/plugins/ directory and then enable this plugin. If you would like to override the functionality of a plugin distributed with Oh My Zsh, create a plugin of the same name in the custom/plugins/ directory and it will be loaded instead of the one in plugins/. Getting Updates By default, you will be prompted to check for upgrades every few weeks. If you would like oh-my-zsh to automatically upgrade itself without prompting you, set the following in your ~/.zshrc: shell DISABLE_UPDATE_PROMPT=true To disable automatic upgrades, set the following in your ~/.zshrc: shell DISABLE_AUTO_UPDATE=true Manual Updates If youd like to upgrade at any point in time (maybe someone just released a new plugin and you dont want to wait a week?) you just need to run: shell upgrade_oh_my_zsh Magic! 🎉 Uninstalling Oh My Zsh Oh My Zsh isnt for everyone. Well miss you, but we want to make this an easy breakup. If you want to uninstall oh-my-zsh, just run uninstall_oh_my_zsh from the command-line. It will remove itself and revert your previous bash or zsh configuration. Contributing Im far from being a Zsh expert and suspect there are many ways to improve – if you have ideas on how to make the configuration easier to maintain (and faster), dont hesitate to fork and send pull requests! We also need people to test out pull-requests. So take a look through the open issues and help where you can. Do NOT send us themes We have (more than) enough themes for the time being. Please add your theme to the external themes wiki page. Contributors Oh My Zsh has a vibrant community of happy users and delightful contributors. Without all the time and help from our contributors, it wouldnt be so awesome. Thank you so much! Follow Us Were on the social media. @ohmyzsh on Twitter. You should follow it. Oh My Zsh on Facebook. Merchandise We have stickers and shirts for you to show off your love of Oh My Zsh. Again, this will help you become the talk of the town! License Oh My Zsh is released under the MIT license. About Planet Argon Oh My Zsh was started by the team at Planet Argon, a Ruby on Rails development agency. Check out our other open source projects.