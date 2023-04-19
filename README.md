-------
Floppy999 archived the original repo. 
The original script unfortunately polls the Realtime Values every 10 sec, which leads to a DoS Attack of the Tibber server.

So this fork was necessary to fix the code in order to prevent the plugin from exessive polling, but its only a mitigation -
The complete Realtime liveMeasurement Polling has to be redesigned.

Realtime liveMeasurement is disabled by default.

If you want to enable it, you have to set. 
PUlse = 1 
in plugin.py

WARNING: Tibber probably will lock your API Key if you enable  RealtimeMessurement.

-----  The Usage of this Version is completely without any guarantee or support.

------ YOU USE IT ON YOUR OWN RISK. 

------- I am not responsible for any damage the plugin causes  ---------- 

-------- If you use the plugin, you accept this conditions. --------------

-------- If you do not accept this, you are entitled to  use the plugin ------------------

Cheers Shakelton52

-------------------------


Important, you must Allow new devices, in Domoticz, Setup-Settings-System-Hardware/Devices.

Create a folder with a name that you like in "domoticz/plugins"  
Put plugin.py, tibber.zip, requirements.txt in that folder  

or

In domoticz/plugins run command "sudo git clone  https://github.com/Shakelton52/Tibber-Domoticz-slow.git"

-------------------

Run "sudo pip3 install -r requirements.txt" to install all packages that this plugin needs  
Restart Domoticz  
Add Tibber from Hardware  
Input your Token and HomeID, get it by log in to this page https://developer.tibber.com/explorer  
Load personal token and paste below code click PLAY
```
{
  viewer {
    homes {
      id
    }
  }
}
```

![](./tibber.png "Photo")


Support me with a coffee https://www.buymeacoffee.com/flopp999
