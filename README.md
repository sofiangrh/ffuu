# Description:
THIS IS A HARD TO USE THEME FOR BEGINNERS. TO USE THIS THEME PROPERLY, FOLLOW ALL STEPS BELOW ON HOW TO EMBED A CUSTOM PANEL ON YOUR WALLPAPER.
My purpose behind this theme is just to find ways around the limitations and to be a bit more creative.

GTK engines required:
- The Murrine engine. (0.90.3+git20100323.)
- The latest Equinox engine - http://gnome-look.org/content/show.php/Equinox+Gtk+Engine?content=121881
- The Pixbuf/pixmap engine.

This theme contains 3 emerald themes.
ffuu (Preview 1)
ffuu 2 (Preview 2)
SquareGlass - http://lassekongo83.deviantart.com/art/July-scrot-2010-170167283

The gtk theme is a mod of Zuki with all colors set to #EEEEEE to match the emerald borders. New scrollbar and other minor changes has also been added.

HOW TO INSTALL THE GTK AND EMERALD THEMES
GTK
1. Install the package p7zip.
2. Double-click on the ffuu.7z file to open it in file-roller.
3. Extract the ffuu-folder to /home/your username/.themes
4. Go to System->Preferences->Appearance and click on the Customize button to select your preferred controls, window border, icon and cursor theme. (In this case it\'s ffuu.)

EMERALD
1. Install emerald.
2. Press ALT+F2 and type emerald --replace
3. Go to System->Preferences->Emerald theme manager.
4. Click on the import button to import the .emerald files.
5. Select a theme from the list.

Note: If you like emerald and want to use it as your main window manager you can add the command to your compiz settings or startup applications. If you want to switch back to the standard window manager press ALT+F2 and type gtk-window-decorator --replace (or metacity --replace if it can\'t find gtk-window-decorator.)

---------------

HOW TO USE A CUSTOM PANEL

As you can see in my preview image I\'ve added a custom panel. Gnome-panel unfortunately can\'t handle real transparency without making it all look like a frellwit. We can work around this by embedding some graphics on our wallpaper, making it look like real transparency.

For this to work you need to have GIMP installed.
Ubuntu users - Open a terminal and type: sudo apt-get install gimp You also need a GIMP plugin call Liquid Rescale: sudo apt-get install gimp-plugin-registry
Other users - http://liquidrescale.wikidot.com/en:download-page-linux

### THE IMAGE ###

1. Locate the panel.png file in the archive.

2. Open the PNG-file in GIMP.

3. Go to Layer > Liquid Rescale.

4. Enter your screen width in the Width area and then resize the image. 
(The \"chain\" icon next to the values needs to be \"open\". If it\'s locked, just click on it. It should be open by default though.)

5. Press CTRL+A (or Select > All.) Copy the image and paste it on your wallpaper of choice. 
Important: Your wallpaper must have the same width and height as your desktop resolution.

6. Move the pasted layer to the top and then save your new wallpaper as whatever.png.

Optional advanced step: If you want the background behind your panel blurred or a bit darkened you can use the \"magic wand\" tool. Select the panel layer, then use the magic wand to select the empty area below the panel. Invert your selection and copy a panel look-a-like part from your wallpaper, then paste it as a new layer. Now you can experiment with layer styles and blur.

### THE PANEL ###

(Make sure your panel is set to 24px in height.)

1. Go to the directory where you installed the theme. Open the panel.rc file.

2. Put a # in front of bg_pixmap[NORMAL] so it will look like this:
#bg_pixmap[NORMAL] = \"/Panel/panel-bg.png\" # Disable for normal panel backgrounds.
Then save the document.

3. Right-click on your panel and select properties. Go to the Background tab and select Solid color. Move the Style slider all the way to the left.

4. And you\'re done! Enjoy your fake transparent panel. :p
