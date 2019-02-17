# Change-server-port-on-Blynk
how to change server port on blynk 

tow steps to solve : "connecting to blynk-cloud.com:80 login timeout"

First step:

open file "BlynkProtocol.h"
on DIR: ....\Documents\Arduino\libraries\Blynk\src\Blynk

comment line 338 & 339 :

//   if (++it < param.end())

       //   redir_port = it.asLong();

Second step:

open file "BlynkConfig.h" at the same folder and change the define BLYNK_DEFAULT_PORT as you want like:

#define BLYNK_DEFAULT_PORT       8080

and be happy the blynk will connected succssfully without set server or port set like :

Blynk.begin(auth, ssid, pass);
