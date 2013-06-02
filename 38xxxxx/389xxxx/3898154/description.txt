DC++ Readme

--------------------------------------------------
DC++
Copyright (C) 2001-2003 Jacek Sieka, jacek@creatio.se

License

This program is free software; you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation; either version 2 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program; if not, write to the Free Software
Foundation, Inc., 59 Temple Place - Suite 330, Boston, MA 02111-1307, USA.
--------------------------------------------------

This Readme will give you a quick startup guide and explain some features
that are NOT obvious :)
So this is especially for NMDC upgraders.
Newbies should (also) check out the web site, http://dcplusplus.sourceforge.net
There you can also find a FAQ (Frequenty Asked Questions) and a forum
(http://dcplusplus.sf.net/forum).

Contents
----------
 1 Installation
 2 Upgrade
 3 Uninstall
 4 Available commands (type in main chat or pm)
 5 What do those Icons mean ??
 6 Not-so-obvious options
 7 Other things you might want to know about
 8 Shortcuts
 9 Automatic search for alternative download locations
10 Further information
11 Have fun


 1 Installation
-----------------

  Just run the installer and fire it up, then enter the settings to set it up according to your
  preferences (most important is nick, download location and shared folders).

  version without installer available at http://sourceforge.net/projects/dcplusplus

 2 Upgrade
------------
  If u used NMDC: You can import your queue file now !
  If u used older DC++ version:
   Just install in the folder your old version was in.
   Your old settings will still be there as is your queue.

  BEWARE: Old (ver <= 0.163) Notepad notes will get lost, format change in 0.17
  BEWARE: If you upgrade to 0.22, all old queue items that are missing a directory in the
  target file-name will be removed. Don't upgrade if your queue is precious to you, and you didn't have
  anything in the default download directory box in the settings (finish it with version 0.181
  or edit your queue.xml file and add a directory to all targets without...).

 3 Uninstall
--------------
  There is an uninstaller as well ...
  If you didn't use the installer: Just delete the folder, there are no .dll's or registry settings :)

 4 Available commands (type in main chat or pm)
-------------------------------------------------
  /grant            grants a slot to the user of the pm window you type in
  /close            close current window
  /help             short help message
  /refresh          Refreshes list of shared files :)
  /away <message>   Specifies a message to auto-respond in PM's while you're AFK
                     (there's a default message so you don't need to specify one)
  /back             Turn away message off
  /slots <#>        Changes number of slots to <#>
  /clear            Clears the main chat windows
  /ts               Switches timestamps in chat windows on and off
  /showjoins        Toggles joins/parts messages for the current hub
  /search <string>  Searches for <string>
  /join <hub>       Joins <hub>
  /dc++             Gives a comment about DC++ and shows the URL where
                     you can get it
  /fav /favorite    Adds hub to favourites (also works in pm's from that user)

 5 What do those Icons mean ??
--------------------------------
 green       = normal Icon
 blue        = DC++ user (identified on 1st direct connection to this user)
 with bricks = User is in passive mode
 with key    = User is an Operator

 6 Not-so-obvious options
---------------------------
  Settings:
   General:
    Active:              The usual connection mode, you can specify your IP
                          if detection fails and a port of your choice if you need to.
                          This mode will use a random port between 1025 and 32000
                          chosen anew on restart if nothing is set in settings.
    Passive:             Compatibility connection mode for users behind
                          Firewalls they can't change to let DC++
                          connections trough.
                         Only use this if Active is not working.
                         Note: Passive <-> Passive connections aren't possible.
   Downloads:
    Unfinished files temporary directory:    You can specify a Directory for your
                         partial files here, suggestion si to have it on another
                         partition than the "Default download directory" to have
                         the files defragmented through moving there :)
    Download slots:      Maximum number of Downloads runing at once, suggestion
                         is to set it to the same number as your upload slots
   Sharing:
    Upload slots:        The number of maximum simultaneous uploads, set to a reasonable
                          value; you should have at least 4-5 KB/s uplaod speed per slot.
   Appearance:
    Use system icons:    Displays the icons set in Windows for filetypes
    Language File:       A XML-file containing most of the text used in DC++.
                          You can specify a file to have DC++ in your favourite language.
                          There's an example.xml if you want to make your own.
                          Language files available at http://DCPlusPlus.sourceforge.net
   Logs and Sound:
    Log Downloads:       You can use this feature to see what downloads
                          completed while you were AFK :)
    Parameters for the logging (the things in %[xxx]):
     target         target filename (for downloads)
     source         source filename (for uploads)
     user           nick
     hub            hub name
     hubip          hub ip
     size           size of the file
     sizeshort      size in b/kB/MB/GB (short version)
     chunksize      size downloaded this session (if resuming, otherwise the same as size)
     chunksizeshort ...
     speed          speed of download
     time           time to download (hh:mm:ss format)
     sfv            1 if the file was sfv/crc32 checked, 0 otherwise
   
    You can also use all date and time parameters (%Y, %m, ...) of strftime (google for it).


   Advanced:
    Rollback:            Size of bytes to rollback when resuming a file to
                          ensure it contains no errors.
                         If there is an error DC++ deletes <rollback>
                          bytes and checks again.
    Write buffer size:   Anti-fragmentation feature, DC++ saves every
                          <write buffer size> bytes to keep fragmentation low.
    Client version:      Since most hubs specify a min client version that
                          is much higher than DC++'s real version number you
                          can set something here, i suggest adding 1 to version
                          number e.g. 1.181
                         to be able to enter the hub.
    Automatically search for alternate download locations:  Allows DC++ to try
                          to find other locations to download your files.
                          Useful if you're AFK a lot.
    Install URL handler on startup:     Set if you want URLS of type dchub://
                         to open in DC++
    Use small send buffer:    If uploads slow down your downloads A LOT you may
                         try this option, but beware it increases HD usage and
                         slows down upload, so it's not suggested.
    Enable SFV checking: Many downloads on DC contain an sfv file to check the integrity of
                         a download. DC++ can on-the-fly calculate CRC-32 values for
                         a file and compare it agains the sfv file. If the check fails,
                         the file is automatically downloaded once more from the same user
                         and if that fails, the user is removed as a source. For this to work,
                         the .sfv file must be in the same target directory as the download goes.

 7 Other things you might want to know about
----------------------------------------------
  * you can doubleclick on a user name in chat to select him in the user list
  * you can doubleclick on stuff starting with www. http:// of ftp:// to open :)
  * DC++ supports uploading filelists and files <16 kB to other DC++ users
    WITHOUT REQUIRING A SLOT. There's a max of 3 connections in addition to
    normal slots.
  * Files <16 kB and filelists are downloaded first.
  * There is information added to the description field:
    <++ V:x,M:x,H:x/y/z,S:x[,O:x]> where
     V = client version,
     M = mode (a=active, p=passive),
     H: x = number of hubs connected to where you're not a registered user
        y = number of hubs you're registered in
        z = number of hubs you're registered as op
     S = number of slots you have open.
     O = if total upload is below this value DC++ will open another slot
         this part of the tag is only shown when the option for it is enabled
     This is updated every 1-2 minutes if there are changes.
  * There is a limit so that only 15 users and 1 op can be kicked at a time
    from the hub user list
  * Passive user detection, those that are behind a set of bricks are passive.
    (detected when the user searches or tries to connect to you)
  * DC++ user detection, those appear blue.
  * Dupe file removal, files with same name and size are automatically removed
    from your share
  * Search flood detection (If more than 5 searches are received from the same
    user within 7 seconds, DC++ will send out a warning)
  * if a user leaves the hub DC++ will close his slots, if the user is back within 10 minutes
    DC++ will grant him a slot.
    THIS CAN CAUSE YOUR UPLOAD GOING OVER MAXIMUM SET IN SETTINGS
  * filelist will be recreated if missing on request
  * optional SFV will remove and requeue file if check failed
  * If DC++ receives "banned" during the login phase, it'll stop automatically reconnecting
  * Files containing "$" aren't added to share 'cause they won't be downloadable alter on.
    This is a protocol limitation ....


 8 Shortcuts
--------------
  ALT-s   send chat message


 9 Automatic search for alternative download locations
--------------------------------------------------------
An automatic search (the advanced option "Automatically search for 
alternative download locations") will use the search string defined in the 
download queue and it can be changed by the user. Previously (before 
v0.301) the search used the target filename. A good search string is the 
key to find many sources. If the search string is empty there will be no 
search. The search string is also used when manually searching for alternates.

You can change the search string for many files at once, which is good for 
rar sets. However, a client will return at most 10 results on a search, 5 
if you are passive, and trying to alter the search string for more than 
those numbers will give you a warning.

The option in advanced settings below auto-search "Automatically add search 
string for alternative download locations" will automatically set the 
target file name as search string when adding files to the download queue.

Since v0.301 the auto search will also search for items in the download 
queue which have online users. Previously only items with offline users 
were searched and lead people to believe auto search was not working at 
all. This feature comes at a cost though. The delay between searches for 
items with online users is 5 minutes whereas searches for items with no 
online users is done every other minute. No search will be made for an item 
which has a source from whom you are already downloading a different file 
from. A file will be searched for no more than once per hour, so if you 
only have one item in the download queue it will take one hour between 
searches.

What does "Automatically search for alternative download locations" do when 
no search strings are set? It will automatically match any search results 
coming from manual searches against files in the download queue. So 
basically it saves you the trouble of right-clicking every file you want to 
add as an alternate source.

Example search string for rar sets:
Files abc-cd1.r01 to abc-cd1.r09 can have the same search string set to 
"abc-cd1.r0" (passive users will only get 5 files returned so one search 
string per file, like "abc-cd1.r01"). But don't set it to "abc .r0" or 
something similar, this will give you rar files for CD2 as well. If you 
don't have sfv checking enabled (the advanced option "Enable automatic SFV 
checking") you can end up with the right files in the wrong place. This 
search for rar sets is so good that it's even better (at least less time 
consuming) than doing it yourself with manual searches and getting 
filelists and use match queue. It gives you 10 files at once, even if there 
are online users.

That pretty much covers it.

Thanks Lundis for the first draft of this feature description and 
suggesting and testing of the enhanced auto search in the first place.


10 Further information
------------------------
  * Homepage                  @ http://dcplusplus.sourceforge.net
  * Forum                     @ http://dcplusplus.sourceforge.net/forum
  * Report bugs               @ http://sourceforge.net/tracker/?atid=427632&group_id=40287&func=browse
  * Request features          @ http://sourceforge.net/tracker/?atid=427635&group_id=40287&func=browse
  * Download language files   @ http://dcplusplus.sourceforge.net/index.php?page=download
  * Get newest version        @ http://dcplusplus.sourceforge.net/index.php?page=download
  * Typos and errors in readme go to Fireball@enLightning.de

11 Have fun
-------------
  Go out, share some files, be a happy DC++ user and have fun.