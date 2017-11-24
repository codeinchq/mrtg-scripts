# MRTG scripts

This repository is dedicated to store [Code Inc.](https://www.codeinc.fr/)'s various [MRTG](https://www.mrtg.com/) scripts. 

## Scripts list

### Ping script

Here is an example of a ping to `ping.ovh.net`: 
```
#---------Ping OVH--------------------
Target[ping_ovh]: `/etc/mrtg/ping ping.ovh.net`
Options[ping_ovh]: nopercent,growright,gauge,noinfo, nobanner
MaxBytes[ping_ovh]: 10000
AbsMax[ping_ovh]: 10000
YLegend[ping_ovh]: Latency
ShortLegend[ping_ovh]: ms
Legend1[ping_ovh]: Max latency (ms)
Legend2[ping_ovh]: Min latency (ms)
LegendI[ping_ovh]: Max latency:
LegendO[ping_ovh]: Min latency:
Title[ping_ovh]: Pinging ping.ovh.net
PageTop[ping_ovh]: <h1>Pinging OVH</h1>
WithPeak[ping_ovh]:wmy
Legend4[ping_ovh]: Min latency maximum
Legend3[ping_ovh]: Max latency maximum
#--------end ping-----------------------------
```

The script can be used many time with different hosts, here is an example with `www.google.com`:
```
#---------Ping Google--------------------
Target[ping_google]: `/etc/mrtg/ping www.google.com`
Options[ping_google]: nopercent,growright,gauge,noinfo, nobanner
MaxBytes[ping_google]: 10000
AbsMax[ping_google]: 10000
YLegend[ping_google]: Latency
ShortLegend[ping_google]: ms
Legend1[ping_google]: Max latency (ms)
Legend2[ping_google]: Min latency (ms)
LegendI[ping_google]: Max latency:
LegendO[ping_google]: Min latency:
Title[ping_google]: Pinging www.google.com
PageTop[ping_google]: <h1>Pinging Google</h1>
WithPeak[ping_google]:wmy
Legend4[ping_google]: Min latency maximum
Legend3[ping_google]: Max latency maximum
#--------end ping-----------------------------
```

### Memory

```
#---------Memory--------------------
Target[mem]: `/etc/mrtg/mem`
Options[mem]: nopercent,growright,gauge,noinfo, nobanner
Unscaled[mem]:dwmy
MaxBytes[mem]: 261025792
Kilo[mem]:1024
YLegend[mem]: RAM
ShortLegend[mem]: o
Legend1[mem]: Free memory
Legend2[mem]: Used memory
LegendI[mem]: Free memory:
LegendO[mem]: Used memory:
Title[mem]: Memory
PageTop[mem]: <h1>Memory</h1>
WithPeak[mem]:wmy
Legend3[mem]: Mémoire libre max
Legend4[mem]: Mémoire utilisée max
#--------end Memory-----------------------------
```
