## badips   
  https://www.badips.com/get/list/any/3?age=2d

### Overview
badips.com is an IP based abuse tracker. Anyone can report "bad" IPs as well as anyone can consume compiled blocklists for free to do whatever they like to do with it.
We refer to a 'badip' or 'badips' as an IP that was seen in context with malicious activities on hosts which are connected with the internet. 


#### badips IP feed
This feed includes, but are not limited to
- brute force login attempts
- SPAM delivery attempts
- Form SPAM attempts 
- (D)DOS attacks and so on and so forth.


### Using the badips feed API
 The badips feed API is found on github at

https://github.com/dnif/enrich-badips

#### Getting started with badips feed API

1. #####    Login to your AD, A10 containers  
   ACCESS DNIF CONTAINER VIA SSH : [Click To Know How](https://dnif.it/docs/guides/tutorials/access-dnif-container-via-ssh.html)
2. #####    Move to the ‘/dnif/<Deployment-key/enrichment_plugin’ folder path.
```
$cd /dnif/CnxxxxxxxxxxxxV8/enrichment_plugin/
```
3. #####   Clone using the following command  
```  
git clone https://github.com/dnif/enrich-badip.git badips
```
### API feed output structure
  | Fields        | Description  |
| ------------- |:-------------:|
| EvtType      | An IP |
| EvtName      | The IOC      |
| IntelRef | Feed Name      |
| IntelRefURL | Feed URL      |
| ThreatType | DNIF Feed Identification Name |      

An example of API feed output
```
{'EvtType': 'IPv4',
'EvtName': '212.129.46.64',
'AddFields': {
'IntelRef': ['BADIPS'],
'IntelRefURL': ['https://www.badips.com/get/list/any/3?age=2d'],
'ThreatType': ['blacklist'] }}
```
