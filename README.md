Plugin module for VLC player
============================

This plugin allows you to automatically save and restore the position
of the last played files in the VLC player.

Installation
============
  * MS Windows:
    Copy file libsrpos*_plugin.dll to {VLC installation folder}\plugins;

  * Unix/Linux and similar systems:
    Build and install plugin module:
      ./configure
      make
      make install
    Use configure options to specify VLC include/library/output paths
    (--with-vlc-*-path options).


VLC player setup
================
  1. Start VLC player;
  2. Open preferences window (menu Tools->Preferences);
  3. Select 'All' in 'Show settings';
  4. Open Control interfaces panel (Interface->Control interfaces);
  5. Check 'Save/restore position of the last played files' checkbox;
  6. Click 'Save' button;
  7. Restart VLC player.

Warning:
  This plugin is provided "as is". The author is not responsible for the
  consequences of use of this software.

Best regards,
Artem Senichev (artemsen@gmail.com)
               http://vlcsrposplugin.sourceforge.net
