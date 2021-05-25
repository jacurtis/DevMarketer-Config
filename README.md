# My Computer Configuration
One of the most common questions I get within my videos is "what [theme/setting/configuration] do you use for [application]". You can literally open any of my videos at random and scroll down to find at least a few comments that are asking this question.

I enjoy customizing my system to meet my exact preferences, and I love sharing those with other people. However, many of these settings can get a little complicated for a YouTube comment. So, for that reason, I am going to share it all here.

This repo will serve as my up-to-date place to save all my configuration settings that I want to publically share.

### Table of Contents

* [Applications](#applications)
  * [iTerm2](#iterm2)
  * [Terminal](#terminal)
  * [Vim](#vim)
  * [Visual Studio Code](#visual-studio-code)

* [System](#system)
  * [Fonts](#fonts)
  * [Oh My Zsh](#oh-my-zsh)
  * [Shell](#shell)

## Applications

### iTerm2

I use iTerm2 in most of my videos after 2018 or so. Many videos before that where using standard Terminal.app. Since then, I have left the base terminal in the dust and exclusively use iTerm2.

// TODO: Add Features about iTerm here

I recommend installing the Shell Integration. This can be setup by going to **iTerm2 > Install Shell Integration** in the menu.

![image]

If you are new, I also recommend turning on the "Tip of the Day" for iTerm. You will be surprised at how much cool new stuff there is to learn. I do admit that this gets annoying after a while. But I continually learn new things when I turn it on. So give it a try. This is found in the menu **iTerm2 > Show Tip of the Day**.

#### iTerm Settings

Here are a list of settings that I **HIGHLY RECOMMEND** when configuring iTerm for the first time. All of these are accessed in the preferences pane (iTerm2 > Preferences or clicking `⌘ + ,`).

1. **General > Closing > Confirm closing multiple session**: Please check this box. You don't want to accidently close an SSH session accidently because you were looking at a local file in the front tab and just meant to close that. This makes sure you really want to kill everything.

1. **General > Closing > Confirm "Quit iTerm2 (⌘Q)"**: Make sure this is checked. I have accidently closed a terminal session, because my terminal was highlighted on another monitor but I meant to close a notes app or calendar app that I was looking at. This makes sure you don't accidently close an SSH session or something you were working on in Vim. However, the next checkbox says "Even if there are no windows". I leave that UNCHECKED. Because if there are no active windows of iTerm, then I don't care if I accidently quit it.

1. **General > Magic > Save copy/paste and command history to disk**: Turn this OFF. You should be using an app like [Paste](https://pasteapp.io/) anyway. Don't let two apps conflict with eachother doing the same thing.

1. **General > Magic > GPU Rendering**: Turn it on. It makes your terminal experience feel luxurious.

1. **General > Services > Check for updates automatically**: Yes, turn this ON. iTerm updates every day or two. The updates are really easy to do. So keep auto-update on.

1. **General > Selection > Copy to pasteboard on selection**: Yes, I like this turned this ON. It can be annoying for some people. But it means that whenever you highlight text in terminal, it automatically copies it to your clipboard. I find that I really like this feature and rely on it.

1. **General > Services > Copied text includes trailing newline**: You will want this OFF. You just want the text you highlighted, you don't want a newline character at the end, it is just annoying.

1. **General > Services > Applications in terminal may access clipboard**: Turn this OFF. This is super sketchy. Don't have it turned on. Again, use a clipboard manager and let the universal clipboard manager manage your clipboard instead of a random terminal app.

1. **Appearance > General > Theme**: Set to "Minimal". The minimal window look is incredible! You will see it change as soon as you change the setting. It's awesome.

1. **Pointer > General > ⌘-Click opens URL**: Set to ON. This is a cool feature that I like about iTerm. When you get a URL (or relative link to a file) in your terminal, you can command-click the link to open it in your default browser. I use this daily. A lot of comments in videos ask how I do this. This is how.

1. **Pointer > General > ⌥ - Click moves cursor**: Set to ON. This is another frequent request I get. How do I use the mouse cursor to interact with the terminal? This option allows you to hold down the Option/Opt/⌥ key on your mac keyboard and click with the mouse to move the cursor like a GUI application. I really love this about iTerm. Most of the time the terminal acts like a terminal. But holding Option, lets you treat it like a GUI app. This is the best of both worlds.

__NOTE: There are a lot of other settings in iTerm. Literally thousands when you click the advanced tab and scroll through those. I only went over the ones I find are the most important and that I get the most questions about. Other settings are personal preference, so I recommend spending an hour to go through the preferences pane and reading each option to customize the setup for yourself.__

#### iTerm2 Theme (Profiles)



#### Learn More About iTerm2

I plan to add a full video guide or tip series on using iTerm2. I will update this section with a link once the guide is ready to view.

### Terminal

**See Also:** [iTerm2](#iterm2) and [Oh My Zsh](#oh-my-zsh)

I rarely use the normal terminal, except in some of my oldest videos. Now I regularly get questions about my terminal and why it looks so different. This is because I am using iTerm2 instead of Terminal.app on Mac OS. See [iTerm2](#iterm2) for details about my terminal setup.

I also use Zsh + OhMyZsh for my shell, with many OhMyZsh plugins and a highly customized Powerlevel9k theme. You can read more about that in the [Zsh](#shell) and [Oh My Zsh](#oh-my-zsh) sections.

### Vim

Vim is the preferred text editor that I use within the terminal. It is fast and powerful. However, I don't use it in very many of my videos because I don't want new programmers to get "stuck" in vim and frustrated or confused. So I tend to use `nano` in my videos just for simplicity sake. But `vim` is what I use for all my remote file editing (usually via SSH) and for editing files quick within the terminal, like config files.

Vim has a very steep learning curve. But the steep learning curve is rewarded with effeciency and speed after you master the program. I recommend you learn Vim slowly. Start by pushing yourself to use it and memorize basic commands like inserting, appending, deleting, etc. Then add more commands and use it frequently to instill those commands to muscle memory. In no time you will be a Vim whiz, without even thinking about it.

#### Vim Installation

Vim is pre-installed on Macs. But it can also be easily installed with any package manager. More install options can be [found here](https://www.vim.org/download.php).

#### Vim Configuration

I have customized my Vim setup a decent amount, but not anything too crazy. For the most part I use a standard install, with a custom theme.

Here are the few features I have customized:

1. `syntax on` is an obvious one. This actually turns on syntax highlighting (which is off by default for some reason...)

1. `tabstop=4` which sets 4 space tabs (as opposed to the ridiculous 8 spaces that are default). I will sometimes change this to 2 space tabs in the editor if I am using a highly indented file. But I usually only change it for the single session and maintain 4 as my default.

1. `set number` gives you line numbers on the left of the screen. These are off by default

1. `set laststatus=2` and `set noshowmode` changes the config of the status and show bars at the bottom. I have a plugin called airbar, which overrides these settings to some degree. This combination is my preferred setup with airbar. Not going to get into details here though.

1. `set whichwrap+=<,>,h,l,[,]` allows you to press the forward and back arrows, and up and down arrows to navigate to the next/previous line at the end or start of a new line. This makes Vim work a lot more like a modern text editor handles arrow navigation when starting and ending lines.

1. Everying after line 6 in the `.vimrc` is configuration for my theme.

#### Vim Theme

I use the [OneDark.vim theme](https://github.com/joshdick/onedark.vim/) for Vim.

This matches the theme I use in VSCode and other text editors and is the theme I get a lot of compliments about in my videos. You can clone the github repo into your `~/.vim/colors/` directory. I don't think this theme works very good in the standard Terminal.app that is on Mac OS. But with iTerm2, this thing is a beauty!

To use my configuration, you can reference [my Vim configuration file in this repo](Vim/.vimrc). You can simply copy this configuration into your `~/.vim/` directory. It is possible that you don't have a `.vimrc` file yet if you haven't customized Vim yet, so in that case you can just copy this file and restart Vim. The changes will immediately take effect. You can also just rip parts that you like from my config and combine them with your own setup.

You will also want to install [Polygot](https://github.com/sheerun/vim-polyglot) for better syntax highlighting in Vim.

I also installed [airline](https://github.com/vim-airline/vim-airline) for a better _"lean and mean status/tabline that is light as air"_ (those aren't my words, that is how the creator describes his tool).

When using airline, I have found that setting showmode off with `set noshowmode` and turning on the status line with `set laststatus=2` was the best combination to get Vim to work with Airline how I liked. It will work with other configurations, but this is what I found most desirable.

Also, if you have squared off edges on your Airline and want the angled edges, then make sure to set `let g:airline_powerline_fonts=1` in your `/.vimrc` file. You will also want to make sure that you are using a powerline-compatible font (I use Nerdfonts) in your terminal.

#### Learn More About Vim

I plan to make a video series on how to use Vim in the future, so that this SUPER POWERFUL tool can be more accessible to more people.

### Visual Studio Code (VSCode)

**My Theme**: One Dark Pro -> https://marketplace.visualstudio.com/items?itemName=zhuangtongfa.Material-theme

This is the main text editor/ IDE that I use in all of my videos. It is also the result of the most questions about my setup. Most people want to know what theme I am using. I actually tend to use several different themes at times, but for my videos I usually use [One Dark Pro](https://marketplace.visualstudio.com/items?itemName=zhuangtongfa.Material-theme). This was the old default theme in Atom (another text editor) that I fell in love with and wanted to keep when I moved to VSCode. It seems to be a favorite by a lot of different people.

If you are looking for other great themes, I have to recommend Monokai. This is a classic theme that has been around forever. It was my old go-to theme, and it still gives me nostalgia when I look back on it. In VSCode there is a version called [Monokai Dark Soda](https://marketplace.visualstudio.com/items?itemName=AdamCaviness.theme-monokai-dark-soda) which holds very close to the original, but with slightly modified colors to give even greater contrast and brighter colors. I really like the work done with that theme and would recommend it. If you can't decide between Dark One and Monokai, then you can always try [Monokai One Dark Vivid](https://marketplace.visualstudio.com/items?itemName=ashpowell.monokai-one-dark-vivid), which tends to "split the difference", by combining the best of both these two excellent theme trends into one theme.

## System

### Fonts

This is mostly pretaining to fonts I use in my code editors and terminal. There are a few things to know when I am considering the correct font selection. First I am looking for a monospaced font so that text columns like up correctly. We also want a font that has clear distinctions between characters. There should be no confusing the letter "ohh" (`o`) with a capital "ohh" (`O`) or the number zero (`0`). Likewise characters like lowercase "el" (`l`) should be distinct from a capital "eye" (`I`). Other ideals are "aggressive parenthesis". We want square brackets (`[ ]`), curly brackets (`{ }`), and parenthesis (`( )`) to all look distinct from a glance. It is also important that tilde character, also known as "squiggly", doesn't resemble a hyphen, also known as a "dash". We also want slashes to have substantial leaning to them.

Furthermore it is preferable if a zero has either a slash or dot in the middle. I prefer dotted zeros, but these are overall less popular than slashed zeros, so many fonts have converted to the slashed zero.

Another personal preferance is squared characters. I personally love the look of squared characters, but it has become stylish to use "legible monos" which are monospaced fonts designed to resemble traditional dynamic fonts like Helvetica.

I also personally look for fonts that support programming ligatures. Not all fonts do this, but more and more font options are becoming available that support it. I often turn ligatures off in my videos because it causes significant confusion among new programmers. For example I get asked how you type a triple line equals sign. Sometimes a double equals gets confused for a single equals. Not equals also throws a lot of people off. So I tend to film beginner videos with ligatures turned off. I also turn ligatures off in my terminal. But I find that ligatures really make code easier to read and understand, so I use them in all my own projects or more advanced videos.

![Programming Ligatures](https://hanselmanblogcontent.azureedge.net/FiraCodeFont.gif)

Here are some of the fonts I find to be the best.

1. [FiraCode](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/FiraCode)
    - **PRO:** Supports Retina screens
    - **PRO:** HUGE Variety of weights available
    - **PRO:** Tall descenders (high m-height)
    - **PRO:** Large line height
    - **PRO:** Lots of ligatures
    - **PRO:** Space shifting ligatures
    - **PRO:** FiraMono is an identical font set without ligatures (if you are into that)
    - **CON:** Why does the `r` have a serif? What a strange design choice. 
    - Maintained by Mozilla

2. [JetBrains Mono](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/JetBrainsMono)
    - **PRO:** Enlarged operators. They are perfect.
    - **PRO:** Lots of ligatures
    - **PRO:** Space shifting ligatures
    - **PRO:** Tall descenders (high m-height)
    - **PRO:** Large line height
    - **PRO:** I really like the `g` character on this font. Much cleaner than other stylized g's that other mono's use
    - **PRO:** The `s and S` characters are incredible. Very distinct from the number `5`. The curls at the ends curl in on themselves more than  most S characters.
    - **PRO:** Includes both dotted zero and slashed zero. Dotted being default and slashed available via OpenType. This is something you can set   in your IDE. I like that they include both.
    - **PRO:** Best semicolon I have ever seen. Especially if you write code in a semi-colon ended language, this thing is really a stamp of power  at the end of a line. You can tell it is terminating a statement. I love it.
    - **PRO:** Brackets and Parentheses are very distinct and clear
    - **PRO:** Free and open source
    - **PRO:** 7 weights with matching italics
    - **CON:** The `@` is really weigh. It circles the left half of the a, but not the right half? Out of context you can actually be unsure what   character it is trying to be.
    - **CON:** The number `4` is really "aggressive" and starts to actually resemble what looks like a "git branch" character if you look at it too   long. It is distinct, but overall I don't like it.
    - **CON:** The `t` character could use shorter arms. It is close to resembling the `+` excempt for the tail on it's leg.
    - **CON:** The `g` character is WAY too busy, ruining legibility

3. [Meslo](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/Meslo)
    - **PRO:** EXTRA LARGE line height
    - **PRO:** Clean overall look. Soft edges, clear characters.
    - **PRO:** The `l` character is really nice without trying too hard
    - **PRO:** Some of the best tilde and hyphen distinctions. The tilde in general is really well designed.
    - **PRO:** Slashed zero, which I prefer.
    - **PRO:** All the numbers are crystal clear. The 4 is very clear, the 8 has more curve than other fonts, making it distinct from the zero. The   nine is also solidly designed.
    - **CON:** EXTRA LARGE line height - I know i listed this as a "pro" as well. That is the thing about Meslo that I hate. The extra large line   height is cool in some contexts and aweful in others. For example when running terminal commands and navigating directories in the terminal it  is great. When you open Vim with this font, it almost breaks Vim. It's greatest strength is also its greatest weakness. There is a philosophy  lesson in there somewhere.
    - **CON:** Without the slash, the `O` and `0` characters look identical
    - **CON:** Parenthesis are weak, but legible
    - **CON:** No ligatures

4. [Space Mono](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/SpaceMono)
    - **PRO:** Clean, easy to read
    - **PRO:** Aggressive parentheses characters
    - **PRO:** Very squared characters. If you are into that style.
    - **PRO:** Clear distinction between double quote and single quote characters
    - **CON:** Square brackets and Curley Braces are very hard to tell apart.
    - **CON:** Undersized operators
    - **CON:** Excessively elongated characters
    - **CON:** Short line-height'
    - **CON:** No ligatures

5. [Hack](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/Hack)
    - **PRO:** Active development
    - **PRO:** Open source & Free
    - **PRO:** Easily [install with all major package managers](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/  Hack#package-managers)
    - **PRO:** Webfont compatible. Hosted version available via jsdelivr and cdnjs
    - **PRO:** Customizable with the [alt-hack library](https://github.com/source-foundry/alt-hack) which allows you to recompile your font with  rounder parenthesis, slash-zero instead of dot-zero, flat-top numbers, slab characters, and more.
    - **PRO:** Customizable [line-height](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/Hack#line-spacing-adjustments)
    - **PRO:** Clean and clear reading in source code
    - **PRO:** Designed for high-contrast themes like Monokai
    - **PRO:** Offset parenthesis create natural space on wrapped characters that I really love!
    - **PRO:** Great design of semi-colon, with distinct comma section. Great ending to a line.
    - **PRO:** Powerline support included by default (additional glyphs via Nerdfonts)
    - **PRO:** Oversized operators
    - **PRO:** Great Tilde character. Distinct from hyphen.
    - **PRO:** All numerals are excellently designed. I particularly like the zero, which is a cross between dotted and slashed with a line down the center. Each character is unique and distinct from letters.
    - **CON:** The baseline of symbols is very off. Ampersands and percentages sit very high, compared to dollar signs and at signs.
    - **CON:** The backtick needs to be more distinct
    - **CON:** Decimal/period is a little small
    - **CON:** No ligatures

THese 5 fonts are my favorite to mess around with. I find that I am turning to Hack and FiraCode the most often. Although I have started converting to JetBrains Mono now in my primary text editor. It just looks really good and has the best ligatures. I really like the design of the characters for the Hack font, and its' native powerline support. But because it doesn't support ligatures, I have to reach for a different font when I am in a text editor, playing with my code.

**My Font in iTerm2:** [Hack w/ Nerdfonts Complete](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/Hack)
**My Font in VSCode:** [JetBrains Mono](https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/JetBrainsMono)

### Oh My Zsh

The default shell that I use on my system is Zsh. However, there is also an extension to Zsh called "Oh My Zsh", which adds a lot of additional features to the shell, most of which offer increased customizability for the user. This includes theming and plugins. I use these plugins in order to improve things like autocompletion and syntax highlighting within the terminal. In addition, I have an array of aliases that I use for quick commands.

Install Oh My Zsh by [following the installation instructions](https://ohmyz.sh/#install) on their website. A simple one-line installation script in your terminal will get the job done.

Once you have _Oh My Zsh_ installed, then you can start customizing your installation. All of the customization happens in a file called `.zshrc`, which by default is at the root of your user directory. Which is generally located at `~/.zshrc`, since `~/` denotes your user directory by default on mac and most linux distros.

Edit the `~/.zshrc` file with any text editor. You can open it in a GUI editor if you like (such as Sublime Text or VS Code), or in the terminal via Nano (easiest), or Vim (which I will be showing for the screenshots).

#### OhMyZsh Plugins

1. **[aws](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/aws):** This is installed by default and gives access to a few useful tools for AWS (Amazon Web Services). This plugin used to offer autocomplete for AWS CLI commands, which was a game-changing feature. But that has been removed now that AWS has implimented autocomplete directly into their new CLI tool. Now this plugin adds a few useful commands such as `asp <profile>` and `acp <profile>` which allows you to set a AWS profiles or change to a specific AWS profile. This is really nice when you are using multiple AWS profiles (such as dev and prod or work and home). You can also use the `agp` command to get the current `$AWS_PROFILE`. I also like the `aws_profiles` to see all the available profiles that you have on your computer without having to manually open up the `~/.aws/credentials` file. All of these are tools that AWS really should have in their CLI already, but since they don't, this little script gives them to you.

1. **[battery](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/battery):** I don't actually use this one on my mac, but I figured I would mention it because I do have it on my linux laptop (although I rarely/never use it that computer in videos). This allows you to add current battery information into terminal prompts. Just keep in mind that this will work out of the box on Mac, but on Linux you need to install `acpi` in addition to enabling this plugin.

1. **[bgnotify](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/bgnotify):** Lots of people have seen my computer pop up notifications when certain commands complete in my terminal and they wonder why their terminal doesn't do the same thing. Bgnotify is the plugin that enables this. You will also need to [install `terminal-notifier`](https://github.com/julienXX/terminal-notifier) if you are on Mac. [You will need `notifu`](https://www.paralint.com/projects/notifu/) if you are on Windows. Linux users don't need to do anything except enable the plugin.

1. **[colored-man-pages](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/colored-man-pages):** This plugin automatically adds color to man pages. If you read man pages often, this is really nice to have. It really gives you a modern terminal experience.

1. **[dash](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/dash):** This allows you to open offline api documentation using [the Dash app](https://kapeli.com/dash). a simple command like `dash laravel` will open up the Dash app to the Laravel documentation. `dash laravel:collections` will open it directly to the collections part of the documentation. It can be nice to have. It only works on Mac, sorry.

1. **[docker-compose](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/docker-compose):** I don't use this anymore, but it enables a series of aliases for quick `docker-compose` commands. For example `dco` would run the main `docker-compose` command, `dcb` runs `docker-compose build`, `dcps` runs `docker-compose ps`, `dce` runs `docker-compose exec`. You get the idea. Basically it was trying to shorten all the long commands you commonly run and help you avoid typing `docker-compose` so many times. Honestly though, I could never remember the commands. So I ended up getting rid of this. Alternatively, I made my own alias that is just `dco`, which is simply an alias for `docker-compose`. It saves you from typing that phrase, then you can combine it with anything else you want. So for example `dco ps` would run the `docker-compose ps` command, or `dco build` runs `docker-compose build`. I decided I liked this and it made it easier to remember and read. You might wonder why I aliased `dco` instead of just `dc`. This is because `dc` is a built-in calculator for the terminal (that supports unlimited percision arithmitic). So I used `dco` to avoid `docker-compose`. Everything else is the same for docker.  
**Additional Installs:** You would need `docker` / `docker-compose` in order to use this. 

1. **[gh](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/gh):** This plugin adds autocompletion to the Github CLI (gh). I really like this CLI tool, so the autocomplete is a nice touch to have.  
**Additional Installs:** This does require you to have the `gh` [GitHub CLI](https://cli.github.com/) installed in order to use. See the CLI's website for full install instructions. It's as easy as `brew install gh` for Mac.

1. **[git](https://github.com/davidde/git) \(Not the default one):** I do not use the default OhMyZsh git plugin, because it is very inconsistent, and even random. For example, the default `git` plugin uses `glg` for half of the `git log` commands and `gl` for the other half. But `gl` by itself is actually `git pull`. That plugin just doesn't seem very well thought out. But this plugin is much better, and provides the functionality you would expect.  
**Installation:** This is a custom plugin, so you must download it to your `/.oh-my-zsh/custom/plugins/` directory. It is easy. Full [installation instructions are on github](https://github.com/davidde/git#installation). But essentially you just need to run `git clone https://github.com/davidde/git.git ~/.oh-my-zsh/custom/plugins/git` and it will put the file where it needs to be and this will override the built-in git plugin.

1. **[git-auto-fetch](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/git-auto-fetch):** This plugin creates a background process in git repos that checks the fetch status of your repo so that your git prompts are always up to date.

1. **[thefuck](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/thefuck):** You didn't even know you needed this tool. [Thefuck](https://github.com/nvbn/thefuck) is a tool that tries to correct common mistakes in terminal commands. For example if you type `aptget install moo`, it would correct it to `apt-get install moo`, or it might notice you mispelled `python` and other commands like that. With the OhMyZsh plugin, it binds double `ESC` to the `fuck` command, so you don't actually have to type `fuck` into your console. Simply press `ESC` + `ESC` to fix the previous command. It is really cool!  
**Additional Installs:** TheFuck requires you to install the base `thefuck` library. This can be done on make with `brew install thefuck` or with any other OS with `pip install thefuck`

1. **[urltools](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/urltools):** This plugin adds two easy commands, `urlencode` and `urldecode`. Pass it a url and it will encode or decode your url strings respectively. Simple and beautiful tool to have.

1. **[zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions):** This tool provides automatic suggestions for typeahead functionality on common tasks, especially those you repeat often. It is one of those tools that you don't think would be very useful, but you end up using every single time you are in the terminal. It is really nice to have. You might want to spend some time customizing how it makes suggestions, but the defaults are a great place to start if you are new.  
**Installation:** Most of the plugins so far came pre-installed with OhMyZsh. But this plugin requires additional installation. Essentially you just need to clone the folder into your `~/.oh-my-zsh/custom/` directory. But here are the full [install instructions](https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md#oh-my-zsh). 

1. **[zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting):** This is another great tool that brings live syntax highlighting into your terminal. It is really great because it shows that the terminal recognizes certain commands before you even execute them. This is one of those tools that everyone always asks me about.  
**Installation:** This tool does NOT come pre-installed with OhMyZsh. You need to add it to your custom plugins folder. The full [install instructions](https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md#oh-my-zsh) are available on GitHub.

#### OhMyZsh Theme

The style of the terminal window is another thing I get lots of compliments and questions on. One of the benefits of OhMyZsh is that it allows much easier theme customization compared to Vanilla Zsh and Bash. You really can customize your terminal prompts to look exactly how you want them.

The theme that I use is a variant of Powerlevel9k.

#### OhMyZsh Colors

Lots of people ask about the colors that they see in the terminal of my videos. I spent a long time fine-tuning these colors so that they work in all types of light and conditions. They are definetely favored and work best on a dark background terminal. But they will work on light colored terminals as well. This is important if you pull up a terminal in another tool like [Pathfinder](https://cocoatech.com/#/), [VSCode](https://code.visualstudio.com/), [Nova](https://www.nova.app/), [Forklift](https://binarynights.com/), [Commander One](https://ftp-mac.com/https://ftp-mac.com/), or [Transmit](https://www.panic.com/transmit/).

The colors that your terminal uses are dictated by a few different things. First the Shell actually outputs a color code like `\e[0;30m` which maps to `RED` for the terminal. But the exact color that is displayed to the user is determined by the Terminal. This means that if a console command wants to display an error message to the user, it would send a command with the text based on this `RED` color code. But the terminal user might have customized the `RED` color in their terminal to be a purple color. So the text will actually be purple when the user sees it.

In the case of theming, we can determine what color codes are sent for our OhMyZsh themes within our theme templates that we create. But most of the color customization needs to happen within the terminal that you are using.

This is why color codes are very complicated to work with when sharing colors across the internet. In general we only have 8 colors to work with:

- Black
- Red
- Green
- Yellow
- Blue
- Purple
- Cyan
- White

But there are also variants of all of those colors that some commands might utilize:

- Regular
- Bold
- Underline
- Foreground
- Background
- High Intensity
- High Intensity Bold
- High Intensity Background

Then there are a few more modern variants that have been added:

- Dim Text (`\e[2;Nm`)
- Blinking Text (`\e[5;Nm`)
- Reversed Text (`\e[7;Nm`)

To further complicate this, not all terminals support all of these variants, but they should support all 8 of the main colors. So when using embedded terminals in other applications (like an FTP console or another text editor) it is possible that you are stuck with the main colors and/or might not be able to customize them at the terminal level.

This is one of the main benefits for using [iTerm](https://iterm2.com/) on Mac. It is a full-featured editor. As far as I know, I think it is the most fully-featured editor on the market.

**Try this Tool:**

### Shell

Right now I am using the Zsh shell, as opposed to Bash. Mostly everything is interchangable with Bash, but Zsh adds many additional features to Bash. By default most Macs now run Zsh by default, but also have Bash installed as well.

You can find these installed at `/bin/bash` and `/bin/zsh` and both can be switched between by using the `bash` and `zsh` commands (by themselves) in the terminal. But by default you will already be in the Zsh shell when booting up the terminal for the first time.

As mentioned above, I also install [OhMyZsh](#oh-my-zsh), which adds many quality-of-life improvements to the Zsh Shell experience.

You can read more about my setup of OhMyZsh in the section above, [click here](#oh-my-zsh).