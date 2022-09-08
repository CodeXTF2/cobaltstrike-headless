# Headless Strike
Aggressorscript that turns the headless aggressor client into a (mostly) functional cobalt strike client.

## Usage
- connect to your teamserver via the builtin headless aggressor utility (./agscript)
```
./agscript host port user password
```
- load the .cna file 
```
aggressor> 
load headless-strike.cna
[+] Load headless-strike.cna

█▀▀ █▀█ █▄▄ ▄▀█ █░░ ▀█▀ █▀ ▀█▀ █▀█ █ █▄▀ █▀▀
█▄▄ █▄█ █▄█ █▀█ █▄▄ ░█░ ▄█ ░█░ █▀▄ █ █░█ ██▄  (headless)
https://github.com/CodeXTF2/cobaltstrike-headless

aggressor> 
```
- profit!

## Commands
Currently, the following beacon commands are implemented:
```
beacons
blockdlls
cd
clear
dcsync
dir
download
downloads
drives
execute
execute-assembly
exit
getsystem
getuid
hashdump
help
help
history
info
inject
ipconfig
jobkill
jobs
jump
keylogger
keystrokes
kill
link
logonpasswords
make_token
mimikatz
mkdir
mv
net
note
powerpick
powerpick_inject
powershell
powershell_import
powershell_import_clear
ppid
ps
pwd
reload
remove
rev2self
rm
run
runu
screenshot
screenwatch
shell
shinject
shspawn
sleep
socks
socks_stop
spawn
spawnto
steal_token
sync_download
unlink
upload
use
```
The syntax is the same as in the GUI client. The only ones you should take note of are:
- ls is replaced with dir due to ./agscript already using ls for listing loaded scripts
- use [beacon id] - start interacting with a beacon
- beacons - list beacons
- info - info about current beacon
- sync_download - sync the teamserver downloads to local storage


## Example
```
aggressor> 
reload headless-strike.cna
[+] Reload headless-strike.cna

█▀▀ █▀█ █▄▄ ▄▀█ █░░ ▀█▀ █▀ ▀█▀ █▀█ █ █▄▀ █▀▀
█▄▄ █▄█ █▄█ █▀█ █▄▄ ░█░ ▄█ ░█░ █▀▄ █ █░█ ██▄  (headless)
https://github.com/CodeXTF2/cobaltstrike-headless

beacons
[+] Listing beacons
______________________
|    beacon id       |
1615823462 ( x64 ) ⛓ | IEUser @ MSEDGEWIN10 ( runonce.exe - 3228 ) | last: 49s | listener https  (via 1100299032)
1100299032 ( x64 )  | IEUser @ MSEDGEWIN10 ( beacon.exe - 7048 ) | last: 49s | listener https


use 1615823462
[+] Interacting with beacon 1615823462
```

## Why did I make this?
I had some fun recently with nethunter (mobile kali) and thought it would be a fun thing to be able to task beacons while not at a computer, such as if a slack/discord beacon notification came in while the operator was outside. This was my (hacky) solution :D Feel free to submit issues or PRs etc.

Have fun!

