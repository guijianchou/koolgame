This project based on koolgame(abandoned by koolshare team), as traffic transfer get cheaper about 25RMB/1TB/3month, self-hosted ss with udp proxy more effinciently  
  
1.Downloads [game-server](https://https://dl.falsemeet.pro/Share/game-server)  and check sha1sum to your VPS  
```shasum
game-server sha1sum:d7cc165b336ca955d97d32c20d2f357405a9340d
```
2.Add permission to game-server:  
```bash
chmod 777 game-server
```
3.Edit config file:   
```Json
config.json:
{
    "server":"0.0.0.0",
    "local_port":1080,
    "timeout": 600,
    "method":"chacha20", #cfb,chacha,md5 chose what you like
    "port_password":
    {
        "port": "password" #port do not include 53,22,80,443
    },
    "_comment":
    {
        "Prot 1": "HK"
    }
}
```
  
4.Mv config.json to game-server same folder  
5.Execute in background:
```
./game-server -c config.json -d
``` 
6.find an traffic transfer provider like "NNR" "Gorelay"  
7.Downloads and install [shadowsocks.tar.gz](https://dl.falsemeet.pro/Share/shadowsocks.tar.gz) on your koolshare merlin firmware:  
'''
shadowsocks.tar.gz sh1sum:4182a7a72e31c324f63959a81bd983ce80b3d2dd
'''
This ss ver3.6 work perfect with koolgame v2 and along with uu booster, very tiny.
''' remove ss install restricted
sed -i 's/\tdetect_package/\t# detect_package/g' /koolshare/scripts/ks_tar_install.sh 
'''

8.fill in config and enjoy u game  
