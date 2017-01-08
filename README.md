# keyb_change

For a lot of years there was no app in AmigaOS 4 to switch language on keyboard. So I created a couple of scripts to do that. The following guide will help you use these scripts. As an example the alternative language is Greek, but you can use your own.

Now you can use the KeymapSwitcher docky (http://os4depot.net/index.php?function=showfile&file=utility/docky/keymapswitcher_docky.lha) to do the same thing.

## How to use

### English guide ###
1. Open Locale prefs and at the "Prefered Languages" select first the Greek (greek_ISO-8859-7) and second the English
2. Open the Input prefs and at the "Keyboard" list select the "English & Greek". By the menu at the select "Save as" and save the prefs as "SYS:Prefs/Presets/usa_input.prefs"
3. Now, change at the keyboard list the selection to "Greek & English" and save as "SYS:Prefs/Presets/gr_input.prefs"
4. Copy the files from the floder keyb_change/S/Shell/#? to the folder SYS:S/Shell/. Be sure that the file is configured as "Executable" and "Script".
5. Copy the files from the floder keyb_change/S/ARexx/#? to the folder SYS:S/ARexx/.
6. Insert in FKey  tooltypes the following line

!"LALT `!" RUN S:Shell/ChangeKeymap 

The above line runs the script that switches the keymap by using the keys "Left Alt + `". FKey should run at the background, so you better add it at your WBStartup. Of 'course you can use the keys that are best for you.
7. If you try to write in Greek, but the font doesn't support it, use the TypeManager utility, which you can find at "Sys:System", and add the ISO8859-7 encoding for the Greek language, to the font that you want to use.
8.  If you do not use the Greek language as alternative, then you might need to edit the file "S/Shell/ChangeKeymap" and add there your keymap names.

If everything goes fine, then the language switch should work.

A Greek guide you can find at http://amitrace.gr/articles_show.php?arid=9