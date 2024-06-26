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


