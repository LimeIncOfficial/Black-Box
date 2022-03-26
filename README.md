<h1 align="center">
  <br>
  <a href="https://github.com/LimeIncOfficial/Black-Box"><img src="https://github.com/LimeIncOfficial/Black-Box/blob/main/5d1f6c762bce1031a206b7eb453d22ab.jpg" width="150px" alt="Logo"></a>
  <br>
  Black-Box
  <br>
</h1>

# Whats is It?

Black-Box is essentially a modified fork of parrot, you can use kali too since the setup will work accross all debian OS's (we just prefer those two in particular since they're more security oriented). 

![[]](https://raw.githubusercontent.com/LimeIncOfficial/Black-Box/main/Screen_Shot_2022-03-17_at_8.00.58_PM.png)

# Manager setup
## I3 
`sudo apt-install i3`
`sudo shutdown -r now`

You now should see a new windows manager appear when logging on.
![[]](https://user-images.githubusercontent.com/81391176/160227588-3b45b4b8-5c76-46ec-9253-ff213a5b290d.png)

According to the i3 wiki: "After the first login, each user will be prompted to have a configuration file generated for them such as **~ /.i3/config** or **~ /.config/i3/config** if this file still not exist. On fresh install it shouldn't, so pick **~ /.config/i3/config**.The prompt allows the user to select Alt or the Windows key (AKA Meta key, Start key) as the $Mod key for i3." Pick your preffered $MOD key.

##  Dotfiles Download
`git clone https://github.com/LimeIncOfficial/Black-Box.git`


Copy the config i3 config in `/Black-Box/.config/i3/config`, and then reload configs with `$mod+Shift+c`

## Package install 
Full package list can be found in `/Black-Box/packages/`
and python packages in `/Black-Box/pip3Packages/`

`sudo apt install bash-completion bash bc chromium amd64 compton colord ranger neofetch cmake cmake-data libcairo2-dev libxcb1-dev libxcb-ewmh-dev libxcb-icccm4-dev libxcb-image0-dev libxcb-randr0-dev libxcb-util0-dev libxcb-xkb-dev pkg-config python3-xcbgen xcb-proto libxcb-xrm-dev i3-wm libasound2-dev libmpdclient-dev libiw-dev libcurl4-openssl-dev libpulse-dev libxcb-composite0-dev libjsoncpp-dev feh && sudo ln -s /usr/include/jsoncpp/json/ /usr/include/json `

## Polybar Setup

`git clone https://github.com/jaagr/polybar.git`

`cd polybar && ./build.sh`

`git clone --depth=1 https://github.com/adi1090x/polybar-themes.git`

`cd polybar-themes
`chmod +x setup.sh`

`./setup.sh` 

`bash ~/.config/polybar/launch.sh --hack` > Add this to your startup script of choice, I have yet to do that.

## Other Setup/Debug

Set the wallpaper using feh or your preffer program. I included one that works with the theme in `/Black-Box/Wallpaper.jpg/`

If your i3 config is acting strange on boot, `$MOD+enter` and type `pkill compton` and run it again. I've had problems in the past and forgot what I did to fix the startup error.

All other config files are found in`/Black-Box/.config/` or in `/Black-Box/~` you can copy thier respective configs one by one or use something like https://github.com/Bhupesh-V/dotman











