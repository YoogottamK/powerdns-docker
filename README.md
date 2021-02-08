# powerdns-docker
[PowerDNS](https://www.powerdns.com/) on docker with admin web interface.

## Instructions
1. Clone this repository
2. Start the database and wait for about 30s.  
[Database setup takes a little time.  Only necessary if the related volume doesn't exist]
```sh
docker-compose up -d mysql
```
3. Start everything else
```sh
docker-compose up -d
```
4. Open [admin web interface](http://localhost:9191)
5. Create an account and login
6. Set `PDNS API URL` to `http://pdns:8081` and `PDNS API KEY` to the key you set in `.env`


## Setup
 - A single authoritative nameserver listening on `:53` (udp and tcp)
 - admin web interface on `:9191`

## Configuration
 - Some options are configurable via the `.env` file.  
### PowerDNS
To configure powerdns, check out:
 - [pschiffe/docker-pdns](https://github.com/pschiffe/docker-pdns)
 - [Authoritative Server Settings](https://doc.powerdns.com/authoritative/settings.html) page on PowerDNS docs.

## Credits
I haven't written anything other than the files present in this repo.
 - awesome admin web interface: [ngoduykhanh/PowerDNS-Admin](https://github.com/ngoduykhanh/PowerDNS-Admin)
 - easily configurable dockerized powerdns: [pschiffe/docker-pdns](https://github.com/pschiffe/docker-pdns)
 - [mariadb](https://github.com/docker-library/mariadb)
