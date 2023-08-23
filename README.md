
Fork declaration
=========

Because [erlyvideo/publisher](https://github.com/erlyvideo/publisher) has not been maintained for too long, so Fork it.

由于 [erlyvideo/publisher](https://github.com/erlyvideo/publisher) 太久没有维护，所以 Fork 了一个。


For [erlyvideo/publisher] (https://github.com/erlyvideo/publisher) code, i am not familiar; I looked at the code and learned it, hoping to put it into production and have like-minded people working together to improve it.

我对[erlyvideo/publisher](https://github.com/erlyvideo/publisher)的代码不熟悉；我一边看代码、一边学习，期望能够投把它入生产，也期望有志同道合的人一起完善它。

debug
```
erl -pa _build/default/lib//*/ebin -pz +K true +A 4 +a 4096 -sasl errlog_type error -s publisher run
```

Publisher
=========

This software allows you to:
1) capture video from USB/RTSP camera + audio from USB camera/external microphone
2) encode it to H.264/AAC
3) publish it to streaming server erlyvideo  http://erlyvideo.org/


Clone it, make, edit self-descriptive publisher.conf and use runit folder to start it via "runit" software.


Debian installation
-------------------

```
apt-get install build-essential erlang-nox git libasound2-dev libfaac-dev libx264-dev libswscale-dev
git clone git://github.com/erlyvideo/publisher.git
cd publisher
make linux
./run
```


Vagrant launch
==============

Install http://vagrantup.com/  then 

```
vagrant up
vagrant ssh
cd publisher
./run
```
