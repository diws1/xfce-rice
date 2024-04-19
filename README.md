# xfce-rice

## Introduction
This repository is dominated by how to customize the xfce desktop, especially the panels which can be much more flexible, but are not included in the default panel settings.

## How to customize xfce panel ?
By default, to customize the xfce panel you only need to right click on the panel, then select Panel Preferences.\
However, if you want to customize the xfce panel freely, you can create a [<b>gtk.css</b>](https://github.com/diws1/xfce-rice/blob/main/.config/gtk-3.0/gtk.css) file in the <i>~/.config/gtk-3.0/</i> folder.
```
sudo nano ~/.config/gtk-3.0/gtk.css
```
And copy this [<b>gtk.css</b>](https://github.com/diws1/xfce-rice/blob/main/.config/gtk-3.0/gtk.css) file on your own.


Or you can clone this repository, with : 
```
cd ~/
git clone https://github.com/diws1/xfce-rice
```
Then go to xfce-rice directory, and copy the <i>gtk.css</i> file on your <i>~/.config/gtk-3.0/</i> folder.
```
cd xfce-rice/
cd .config/gtk-3.0/
sudo cp -r gtk.css ~/.config/gtk-3.0/
```

To see your modifications applied, you can reset the xfce4-panel process by typing the following command into a terminal :
```
xfce4-panel -r
```

>[!NOTE]
> To see your modifications applied, you can reset the xfce4-panel process by typing the following command into a terminal :
```
xfce4-panel -r
```

## Preview
<i>Nelo</i>
![My Image](https://github.com/diws1/xfce/blob/main/screenshot/xfce%20nelo.png)

<i>Aestethic</i>
![My Image](https://github.com/diws1/xfce/blob/main/screenshot/xfce%20aestethic.png)

<i>Blumon</i>
![My Image](https://github.com/diws1/xfce/blob/main/screenshot/xfce%20blumon.png)


