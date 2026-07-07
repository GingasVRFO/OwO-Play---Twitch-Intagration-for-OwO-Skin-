
OwOPlay - Twitch Haptics for the OwO Suit!
---------------
Let your Twitch chat control your OWO suit! OwoPlay plays OWO
sensation (.owo) files and triggers them from channel point
redeems, subs, bits, raids and chat commands.

- Windows 10/11, 64-bit. No install: unzip anywhere and run.
- No Twitch login, password or token - it reads chat anonymously.
- Free & open source (GPL-3.0)

GETTING STARTED
---------------
1. Open the myOWO app (phone or PC), suit paired and calibrated.
2. Run "OwoPlay App.exe".
   IP box:  127.0.0.1  if the myOWO app runs on this same PC
            leave empty to auto-scan the network
            or type your phone's WiFi IP
3. Click Connect. When it says Connected, double-click a
   sensation in the list - you should feel it.

First run: allow OwoPlay in the Windows Firewall popup for BOTH
private and public networks (it talks to the myOWO app over UDP).


YOUR OWN SENSATIONS
-------------------
Sensations are .owo files (make them with OWO's free Sensation
Creator, or download shared ones). Click "Open folder", drop
files in, "Refresh list", then reconnect. A sensation's name is
its file name. Samples included, you can create your own with the Sensation creator from OwO


TWITCH SETUP
------------
Type your channel name, click "Start Twitch" - done.

What viewers can do:
* Chat command:  !owo Punch   plays owo\Punch.owo
  - Limit who can use it with "Who" (all/subs/vips/mods)
  - Rename it with "Chat cmd"
* Short commands: edit owo\aliases.txt, e.g.  !zap=Punch
* Channel points: make the reward REQUIRE VIEWER TEXT; when the
  viewer types a sensation name (e.g. "Heart Beat") it plays.
  To lock a reward to one sensation regardless of what the
  viewer types, add a line to owo\redeems.txt - redeem it once
  and the log shows the exact line to copy.
  (Rewards without viewer text never appear in chat, so OwoPlay
  can't see them - a Twitch limitation of login-free chat.)
* Subs, bits, raids: pick sensations in the dropdowns.

"Cooldown" stops chat spam (mods and redeems bypass it).

Going live: tick "Connect on launch" + "Start Twitch on launch"
and put a shortcut to OwoPlay App.exe in your stream startup.
Settings are saved in owoplay.ini next to the exe.


STREAM DECKS / LIORANBOARD / SAMMI (optional)
---------------------------------------------
OwoPlay.exe is a command-line version for "run program" actions:

    OwoPlay.exe "Heart Beat" --quiet

If OwoPlay App is open, triggers play instantly through it.
Run OwoPlay.exe --help for all options (scan, server, --ip...).


GOOD TO KNOW
------------
* The myOWO app accepts ONE connection at a time (an OWO
  limitation). Games without OWO support: no conflict, leave
  OwoPlay connected all stream. Games with their own OWO
  integration: the game owns the suit while you play it -
  reconnect OwoPlay afterwards.
* OwoPlay can never exceed your calibrated intensity - the myOWO
  app and the suit enforce your calibration, like with any game.


TROUBLESHOOTING
---------------
Nothing happens?
1. myOWO app open? Suit paired/calibrated? Same network?
2. Run "OwoPlay.exe scan" in cmd - if it can't find the app,
   it's the firewall (allow BOTH network types) or the network.
3. OwoPlay.exe "Heart Beat" --ip <ip> --verbose  shows every
   handshake step - where it stops is what's broken.
Twitch not firing? The log window shows every match, permission
block, cooldown skip and unmapped reward as it happens.
