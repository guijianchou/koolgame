This project based on koolgame(abandoned by koolshare team), as traffic transfer get cheaper about 25RMB/1TB/3month, self-hosted ss with udp proxy more effinciently

##1.Downloads game-server to your VPS
##2.Add permission to game-server:
chmod 777 game-server
##3.Edit config file:
###config.json:
```Json
{
    "server":"0.0.0.0",
    "local_port":1080,
    "timeout": 600,
    "method":"chacha20",
    "port_password":
    {
        "port": "password"
    },
    "_comment":
    {
        "端口1": "HK"
    }
}
```
##4.Mv config.json to game-server same folder
##5.Execute: ./game-server -c config.json -d
##6.find an traffic transfer provider like "NNR" "Gorelay"
