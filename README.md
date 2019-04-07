# DCPMData
Pickle files for DDoS attacks in SIP networks

This archieve contains the DDoS attack pickle files (zipped) used in the paper below. Please refer to the paper below if you use this data in your work.

@article{SEMERCI2018137,
title = "An intelligent cyber security system against DDoS attacks in SIP networks",
journal = "Computer Networks",
volume = "136",
pages = "137 - 154",
year = "2018",
issn = "1389-1286",
doi = "https://doi.org/10.1016/j.comnet.2018.02.025",
url = "http://www.sciencedirect.com/science/article/pii/S1389128618300987",
author = "Murat Semerci and Ali Taylan Cemgil and Bülent Sankur"
}


NOTE: All the data used in the paper is stored as pickle files. To process them, you could either implement your own pickle reader, or you could install and use BOUN-SIM, which can be downloaded from https://github.com/cagatayyildiz/boun-sim 

NOTES: 
- Params folder contains the parameters used in creating the attacks. The lines at the end of the files provides information about the attack:
--Ddos-20-50-REGISTER-50-0-True-UDP-subnet-pool-False-False-10094 10096 10014 10021 10023 10073 10010 10068 10043 10085 -> At 20th second, a DDoS attack with a duration of 50 seconds starts. It is a "register" attack. Its magnitude is 50 (the attackers send 50 messages per second in average). The attacker ID numbers are: 10094	10096 10014 10021 10023 10073 10010 10068 10043 10085.

- The folder names in the data folder represents the traffic windows used in the experiements in the paper: sec1 -> the size of 1 second is used.
- There are 5 levels of normal traffic intensity for each traffic window: Lowest (level1), low, middle, high, highest (level5).
- Note that the attack times by the attack module in the params files do not mean that the exact attack time in the monitored traffic will exactly match. E.g.: In the example above the register attack started at 20th second of the attack module, might be observed around 80th second of the monitored traffic (pickle) file. The order, the type, the duration and the magnitude of the attacks and the attackers are the same as in the params file, but the timing might not exactly match with the monitored traffic in the pickle files.
- The change point times (the time the attacks are observed in the monitored SIP traffic) in the pickle files for sec1, sec2 and sec 3 are also provided explicitly. The "cps" the start and the end time of the attacks are given in order. 