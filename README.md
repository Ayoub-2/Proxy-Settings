# Linux Settings for proxy 
I always suffer from switching to my academy network or any network using local proxy while using any linux based systems, i have to configure my package manager , my programms like git , curl , wget ...
it's really a Headache, so i thougth i could juste create a script that easily switch between network with or without proxies.
## Installation 
```bash 
git clone https://github.com/Ayoub-2/proxy_settings
cd proxy_settings/
```
## Configuration 
I recommand putting this **proxy** file in your /usr/bin/local/
and you need to make it executable (alert : this a bash script so it might not work in your zsh|sh ... )
```bash 
cp ./proxy /usr/bin/local/proxy
chmod +x /usr/bin/local/proxy
```
## Manual 
```bash 
$proxy --help
Usage: proxy -i ip -p port -t http -e 
Options:
  -i, --ip 10.23.201.11        the proxy IP
  -p, --port 3128              the proxy port
  -t, --type http|https|socks5 the type of proxy
  -e, --env                    set the environment flag to True (this will make all the terminals use the same proxy)
  --default                    use default options
  --clean                      clean all settings
  -h, --help                   help maual
  -v, --version                Get version
Example: 
	proxy -i 10.23.201.11 -p 3128 -t http 
```
