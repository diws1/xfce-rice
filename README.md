# XFCE Customization Guide 

<img align="right" height="192" width="341" src="https://github.com/diws1/xfce/blob/main/screenshot/xfce%20blumon.png" alt="image" />
This repository is dominated by how to customize the xfce desktop, <s>especially the panels which can be much more flexible, but are not included in the default panel settings</s> various things that can be hacked in xfce desktop environtment will be explained here. There are many ways to customize the xfce desktop, and this repository is one of them while still prioritizing simplicity and efficiency of <b><i>ram</i></b> and <b><i>cpu</i></b> usage.
  
# Table of Contents
- [XFCE PANEL](https://github.com/diws1/xfce-rice?tab=readme-ov-file#panel)
  - [Restart panel](https://github.com/diws1/xfce-rice?tab=readme-ov-file#restart-panel)
  - [Styling](https://github.com/diws1/xfce-rice?tab=readme-ov-file#styling)
  - [Transform](https://github.com/diws1/xfce-rice?tab=readme-ov-file#transform)
  - [Using various icons](https://github.com/diws1/xfce-rice?tab=readme-ov-file#using-various-icons)
  - [Fake effect in xfce panel](https://github.com/diws1/xfce-rice?tab=readme-ov-file#fake-effect-in-xfce-panel)
  - [Launcher ID](https://github.com/diws1/xfce-rice?tab=readme-ov-file#launcher-id)
  - [Global settings](https://github.com/diws1/xfce-rice?tab=readme-ov-file#global-settings)
  - [Whisker menu](https://github.com/diws1/xfce-rice?tab=readme-ov-file#whisker-menu)
  - [Workspace styling](https://github.com/diws1/xfce-rice?tab=readme-ov-file#workspace-styling)
  - [Window button](https://github.com/diws1/xfce-rice?tab=readme-ov-file#window-button)
  - [Notification Plugin](https://github.com/diws1/xfce-rice?tab=readme-ov-file#notification-plugin)
  - [Pulse Audio Plugin](https://github.com/diws1/xfce-rice?tab=readme-ov-file#pulse-audion-plugin)
  - [Battery Plugin](https://github.com/diws1/xfce-rice?tab=readme-ov-file#battery-plugin)
  - [Date/Clock](https://github.com/diws1/xfce-rice?tab=readme-ov-file#date/clock)
  - [Another Launcher](https://github.com/diws1/xfce-rice?tab=readme-ov-file#another-launcher)
  - [Replace to another panel](https://github.com/diws1/xfce-rice?tab=readme-ov-file#replace-to-another-panel)

- [WINDOW MANAGER](https://github.com/diws1/xfce-rice?tab=readme-ov-file#window-manager)
  - [XFWM standalone](https://github.com/diws1/xfce-rice?tab=readme-ov-file#xfwm-standalone)
  - [Shortcut](https://github.com/diws1/xfce-rice?tab=readme-ov-file#shortcut)
  - [Compositor](https://github.com/diws1/xfce-rice?tab=readme-ov-file#compositor)
  - [Replace to another window manager](https://github.com/diws1/xfce-rice?tab=readme-ov-file#replace-to-another-window-manager)
  - [Tittle/button](https://github.com/diws1/xfce-rice?tab=readme-ov-file#title/button)

- [XFCE TERMINAL](https://github.com/diws1/xfce-rice?tab=readme-ov-file#xfce-terminal)
  - [Adding new theme](https://github.com/diws1/xfce-rice?tab=readme-ov-file#adding-new-theme)

- [SCREENSHOTS](https://github.com/diws1/xfce-rice?tab=readme-ov-file#screenshots)
- [REFERENCES](https://github.com/diws1/xfce-rice?tab=readme-ov-file#references)

## XFCE PANEL
By default, to customize the xfce panel you only need to right click on the panel, then select Panel Preferences.\
However, if you want to customize the xfce panel freely, you can create a [<b>gtk.css</b>](https://github.com/diws1/xfce-rice/blob/main/.config/gtk-3.0/gtk.css) file in the <i>~/.config/gtk-3.0/</i> folder.
>[!NOTE]
><i>gtk.css</i> file are like exterior paint. You need to arrange the items on your panels with the default panel settings, then <i>gtk.css</i> will color it.

### Restart panel
The xfce panel can be restarted by running the following command in terminal, this will restart xfce panel with the changes made.
```
xfce4-panel -r
```

### Styling
```
... {
	background: #c5c8c6; opacity: 0.9;
	color: #282828;
	border-color: #c5c8c6;
        border-bottom-left-radius: 4px;
        border-bottom-right-radius: 4px;
        border-top-left-radius: 4px;
        border-top-right-radius: 4px;
        margin: 4px;
}
```
### Transform
```
#xfce4-power-manager-plugin image {
        -gtk-icon-transform: scale(0.4) rotate(90deg); margin:-10px;
}
```
### Using various icons
```
#xfce4-power-manager-plugin image {
	-gtk-icon-theme: 'Tela-circle';
}
```
```
#xfce4-notification-plugin image {
	-gtk-icon-theme: 'Tela-circle';

```
### Fake effect in xfce panel
```
/*Window Buttons*/
.xfce4-panel .tasklist .toggle {
	...
        margin: 5px;
        padding: 5px;
}
.xfce4-panel .tasklist .toggle:checked {
	...
	margin: 2px;
	padding: 0px;
}
.xfce4-panel .tasklist .toggle:hover {
	...
        margin: 4px;
        padding: 0px;
}
```
```
.tasklist .toggle image {
        -gtk-icon-transform: scale(0.5);
}
.tasklist .toggle:checked image {
        -gtk-icon-transform: scale(0.9);
}
.tasklist .toggle:hover image {
        -gtk-icon-transform: scale(0.8);
}
```

### Launcher ID

### Global settings
```
.xfce4-panel {
	background: #010101;
	border-bottom-left-radius: 4px;
	border-bottom-right-radius: 4px;
        border-top-left-radius: 4px;
        border-top-right-radius: 4px;
        font-family: 'Roboto Regular';
        font-size: 12px;
	opacity: 1;
} 
```
```
.xfce4-panel {
        font-family: 'Roboto Regular';
        font-size: 10px;
} 
```

### Whisker menu
```
/*Whisker Menu*/
#whiskermenu-button {
        margin: 4px;
}
#whiskermenu-button:hover {
	background: #c5c8c6; opacity: 0.9;
	color: #282828;
	border-color: #c5c8c6;
        border-bottom-left-radius: 4px;
        border-bottom-right-radius: 4px;
        border-top-left-radius: 4px;
        border-top-right-radius: 4px;
        margin: 4px;
}
#whiskermenu-button image {
	-gtk-icon-theme: 'Tela-circle';
        -gtk-icon-transform: scale(0.8); margin: -10px;
}
```

### Workspace styling
```
/*Workspace*/
#pager-32 #xfce-panel-toggle-button {
	color: #f9f9f9;
	margin: 4px;
	padding: 2px;
}
#pager-32 #xfce-panel-toggle-button:checked {
        background: #c5c8c6; opacity: 0.5;
	color: #282828;
	border-color: #c5c8c6;
	border-bottom-left-radius: 4px;
        border-bottom-right-radius: 4px;
        border-top-left-radius: 4px;
        border-top-right-radius: 4px;
	margin-top: 8px;
	margin-bottom: 8px;
	padding: 2px;
}
#pager-32 #xfce-panel-toggle-button:hover {
        background: #c5c8c6; opacity: 0.9;
	color: #282828;
	border-color: #c5c8c6;
	border-bottom-left-radius: 4px;
        border-bottom-right-radius: 4px;
        border-top-left-radius: 4px;
        border-top-right-radius: 4px;
	margin-top: 5px;	
	margin-bottom: 10px;
	padding: 2px;
}
```

### Window button
```
/*Window Buttons*/
.xfce4-panel .tasklist .toggle {
        background: #c5c8c6; opacity: 0.9;
	border-color: #c5c8c6;
        border-bottom-left-radius: 4px;
        border-bottom-right-radius: 4px;
        border-top-left-radius: 4px;
        border-top-right-radius: 4px;
        margin: 5px;
        padding: 5px;
}
.xfce4-panel .tasklist .toggle:checked {
        background: #c5c8c6; opacity: 0.9;
	border-color: #c5c8c6;
        border-bottom-left-radius: 4px;
        border-bottom-right-radius: 4px;
        border-top-left-radius: 4px;
        border-top-right-radius: 4px;
	margin: 2px;
	padding: 0px;
}
.xfce4-panel .tasklist .toggle:hover {
        background: #c5c8c6; opacity: 0.9;
	border-color: #c5c8c6;
        border-bottom-left-radius: 4px;
        border-bottom-right-radius: 4px;
        border-top-left-radius: 4px;
        border-top-right-radius: 4px;
        margin: 4px;
        padding: 0px;
}
.tasklist .toggle image {
        -gtk-icon-transform: scale(0.5);
}
.tasklist .toggle:checked image {
        -gtk-icon-transform: scale(0.9);
}
.tasklist .toggle:hover image {
        -gtk-icon-transform: scale(0.8);
}
```

### Notification Plugin
```
/*Notification*/
#xfce4-notification-plugin {
	color: #f9f9f9;
        margin: 4px;
	padding: 5px;
}
#xfce4-notification-plugin:hover {
        background: #c5c8c6; opacity: 0.9;
	color: #282828;
	border-color: #c5c8c6;
        border-bottom-left-radius: 4px;
        border-bottom-right-radius: 4px;
        border-top-left-radius: 4px;
        border-top-right-radius: 4px;
        margin: 4px;
        padding: 5px;
}
#xfce4-notification-plugin image {
	-gtk-icon-theme: 'Tela-circle';
        -gtk-icon-transform: scale(0.4); margin: -10px;
}
```

### Pulse Audio Plugin
```
/*Sound*/
#pulseaudio-button {
	color: #f9f9f9;
        margin: 4px;
        padding: 5px;
}
#pulseaudio-button:hover {
        background: #c5c8c6; opacity: 0.9;
	color: #282828;
	border-color: #c5c8c6;
        border-bottom-left-radius: 4px;
        border-bottom-right-radius: 4px;
        border-top-left-radius: 4px;
        border-top-right-radius: 4px;
        margin: 4px;
        padding: 5px;
}
#pulseaudio-button image {
	-gtk-icon-theme: 'Tela-circle';
        -gtk-icon-transform: scale(0.4); margin: -10px;
}
```

### Battery Plugin
```
/*Battery*/
#xfce4-power-manager-plugin {
	color: #f9f9f9;
        margin: 4px;
        padding: 5px;
}
#xfce4-power-manager-plugin:hover {
        background: #c5c8c6; opacity: 0.9;
        color: #282828;
	border-color: #c5c8c6;
        border-bottom-left-radius: 4px;
        border-bottom-right-radius: 4px;
        border-top-left-radius: 4px;
        border-top-right-radius: 4px;
        margin: 4px;
        padding: 5px;
}
#xfce4-power-manager-plugin image {
	-gtk-icon-theme: 'Tela-circle';
        -gtk-icon-transform: scale(0.4) rotate(90deg); margin:-10px;
}
```

### Date/Clock
```
/*Clock*/
#clock-button {
	color: #f9f9f9;
        margin: 4px;
        padding: 5px;
}

#clock-button:hover {
        background: #c5c8c6; opacity: 0.9;
	color: #282828 ;
	border-color: #c5c8c6;
        border-bottom-left-radius: 4px;
        border-bottom-right-radius: 4px;
        border-top-left-radius: 4px;
        border-top-right-radius: 4px;
        margin: 4px;
        padding: 5px;
}
```

### Another Launcher
```
#launcher-10 #launcher-arrow:hover {
        background: #c5c8c6; opacity: 0.9;
	border-color: #c5c8c6;
        border-bottom-left-radius: 4px;
        border-bottom-right-radius: 4px;
        border-top-left-radius: 4px;
        border-top-right-radius: 4px;
        margin: 2px; 
}
#launcher-10 image {
	-gtk-icon-theme: 'Tela-circle'; 
}
#launcher-10 #launcher-arrow:hover image {
        -gtk-icon-transform: scale(0.7); 
}


#launcher-15 #launcher-arrow:hover {
        background: #c5c8c6; opacity: 0.9; 
	border-color: #c5c8c6;
        border-bottom-left-radius: 4px;
        border-bottom-right-radius: 4px;
        border-top-left-radius: 4px;
        border-top-right-radius: 4px;
        margin: 2px; 
}
#launcher-15 image {
	-gtk-icon-theme: 'Tela-circle'; 
}
#launcher-15 #launcher-arrow:hover image {
        -gtk-icon-transform: scale(0.7); 
}
```

## WINDOW MANAGER
### XFWM standalone
### Shortcut
### Compositor
### Replace to another window manager
### Tittle/button

## XFCE TERMINAL
### Adding new theme 

## SCREENSHOTS
<p align="center">
<img height="192" width="341" src="https://github.com/diws1/xfce/blob/main/screenshot/xfce%20nelo.png" hspace="10"/>
<img height="192" width="341" src="https://github.com/diws1/xfce/blob/main/screenshot/xfce%20aestethic.png" hspace="10"/>
<img height="192" width="341" src="https://github.com/diws1/xfce/blob/main/screenshot/xfce%20blumon.png" hspace="10"/>

</p>

## REFERENCES

<!--
### Replace panel
User can be replace default xfce panel with another panel or bar, for example polybar. To do this, we have two options:
-->







<!--
# xfce-rice

## Introduction
This repository is dominated by how to customize the xfce desktop, especially the panels which can be much more flexible, but are not included in the default panel settings.

## How to customize xfce panel ?
By default, to customize the xfce panel you only need to right click on the panel, then select Panel Preferences.\
However, if you want to customize the xfce panel freely, you can create a [<b>gtk.css</b>](https://github.com/diws1/xfce-rice/blob/main/.config/gtk-3.0/gtk.css) file in the <i>~/.config/gtk-3.0/</i> folder.
>[!NOTE]
><i>gtk.css</i> file are like exterior paint. You need to arrange the items on your panels with the default panel settings, then <i>gtk.css</i> will color it.


```
sudo nano ~/.config/gtk-3.0/gtk.css
```
And copy this [<b>gtk.css</b>](https://github.com/diws1/xfce-rice/blob/main/.config/gtk-3.0/gtk.css) file on your own.


Or you can clone this repository, with : 
```
cd ~/
git clone https://github.com/diws1/xfce-rice
```
Then go to <i>xfce-rice</i> directory, and copy the <i>gtk.css</i> file on your <i>~/.config/gtk-3.0/</i> folder.
```
cd xfce-rice/
cd .config/gtk-3.0/
sudo cp -r gtk.css ~/.config/gtk-3.0/
```

To see your modifications applied, you can reset the xfce4-panel process by typing the following command into a terminal :
```
xfce4-panel -r
```

>[!IMPORTANT]
> Some items on the panel may not change immediately. You need to read the instructions I wrote on each gtk.css theme in this repository, for example :
```
/*
Panel Settings
	Top:
	Row size: 22px
	Length: 1014px
	Icons: 13px
	Background style: solid color
		   color: #1b1b1b opacity: 0

	Clock Font: Terminus (TTF) Medium 9
	      Format: " %I:%M %p "

	Side:
	Row size: 27px
	Length: automatic
	Icons: 20px
	Background style: solid color
		   color: #1b1b1b opacity: 0
Appereance
	GTK-Theme: Adwaita-Dark
	Window-manager-Theme: Ant Bloody
	Icons: Papirus-Dark, Gruvbox Plus Dark (manual change)
*/
```
and
```
/*Note: The launcher ID is obtained by hovering the mouse over the plugin in the panel properties*/
```


## Preview
<i>Nelo</i>
![My Image](https://github.com/diws1/xfce/blob/main/screenshot/xfce%20nelo.png)

<i>Aestethic</i>
![My Image](https://github.com/diws1/xfce/blob/main/screenshot/xfce%20aestethic.png)

<i>Blumon</i>
![My Image](https://github.com/diws1/xfce/blob/main/screenshot/xfce%20blumon.png)



## Tips & Tricks
soon :)

-->
