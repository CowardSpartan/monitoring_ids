# BME Network and Security Specialsation thematic laboratory

### 2020/02

## Network monitoring

## Intrusion detection

|                               | Snort                                                                                        | Suricata                                                                                    | Bro/Zeek                                             |
| ----------------------------- | -------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ---------------------------------------------------- |
| price/licensing               | GNU GPL free                                                                                 | GNU GPL free                                                                                | BSD free                                             |
| target os                     | windows, linux                                                                               | windows, linux, bsd, osx                                                                    | linux, bsd, osx                                      |
| ease of use                   | good resources, large community, cisco provides full documentation (sometimes a bit cryptic) | straightforward installation guide, requires a few more steps                               | steep learning curve due to scripting                |
| web ui                        | sguil, snorby, BASE                                                                          | snort compatible + ELK stack                                                                | less options, ELK stack or paid Corelight            |
| distinctive features          | OpenAppId (layer 7 application detection), community + Cisco support                         | file extraction, multi-threading, performance, lua scripting, layer 7 application detection | custom workflows with policy scripts, not rule based |
| shortcomings                  | single threaded (Snort 3 will support multithreading)                                        | not exactly Snort compatbile, some newer Snort VRT rules are problematic                    | complicated configuration and learning curve, age    |
| category                      | open source rule based NIDS                                                                  | open source rule based NIDS                                                                 | open source anomaly based NIDS                       |
| first release/current support | 1999/yes                                                                                     | 2009/yes                                                                                    | 1994/yes                                             |

ELK stack: elastic + logstash + kibana

Common trend: some rules have to be paid for, but then released for free after 30 or 60 days

## Test environment

### Network: OpenVpn network

- all traffic goes through the OpenVpn server

- clients are addressed by static IP addresses for convenience

- clients are students' home computers or VMs running in BME Cloud

- clients will run different operating systems



### Server, where IDS and monitoring software will be installed

- running Ubuntu 18.04

- OpenVpn set up with all traffic going through tun0 adapter

- VPS: 4 vCPUs, 8GB RAM, 200GB SSD
