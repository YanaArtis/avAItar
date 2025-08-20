# avAItar
AI-Powered computer that can act in physical world in wearable and autonomos/robotic modes.
List of **avAItar** project (formerly known as **AR-Go**) units in the version of 2025:
 - **Head-Mounted Display with DIY Wireless Module** (Eyetop Centra, Xreal, Epson Moverio or another suitable eyewear) for connection to custom CPU unit, smartphone or your personal cloud;
 - **CPU Unit** (smartphone, or Raspberry Pi, or another suitable device)
 - **Head-Mounted Camera**
 - **Remote Control Unit** (smartphone, bluetooth keyboard, etc.)
 - **Robotic Unit** (i.e. iRobot Create) permitting the system to act as autonome agent

## Inception
From 2007 to 2012, I worked on a pet project AR-Go - developing a wearable computer. At first, it seemed like nothing complicated: a laptop in a backpack, a display-glasses on your nose - and here you have a wearable computer, allowing you to have fun with augmented reality and other interesting features. The main thing is to choose the right hardware - and off you go! But it turned out to be not so simple.

After a lot of trials and fails, I settled on the discontinued (but still available on eBay) Eyetop Centra monocular as my head-mounted display.

![Eyetop Centra - wearable DVD player.](https://habrastorage.org/r/w1560/storage2/d0a/deb/cd8/d0adebcd8950901e3a2b3da9c22537b2.png)\
_Eyetop Centra - wearable DVD player._

![Eyetop Centra monocular - closer view.](https://habrastorage.org/r/w1560/storage2/168/db7/efa/168db7efaa3fd6b726518a1c46394e9c.png)\
_Eyetop Centra monocular - closer view._

In 2008 this head-mounted display turned out to be the most suitable option. To be honest, the resolution was small - 320 * 240, but enough for walking on the street or riding the bike wearing this eyewear.

I chose Nokia N900 as the "brains" for my smart glasses. This smartphone with Linux on the board turned out to be almost as versatile and flexible as a "big" computer. I managed to install the necessary development tools on it - and all software for my wearable computer was written (C++/Qt) and compiled directly on the smartphone - mainly on the road between my home and office.

![Nokia N900, Linux-based smartphone.](https://habrastorage.org/r/w1560/storage2/536/719/81d/53671981d9ff087e2df6fa6a27ce4232.png)\
_Nokia N900, Linux-based smartphone._

However, it was not possible to immediately turn the N900 into a wearable computer. It would seem that it would be enough to hang the N900 by the strap on the wrist, pack the Eyetop Centra video block into some kind of small case with  with neck lanyard, plug the glasses video cable into the N900 - and that's it, but it was not there... Once I spent half an hour in such a configuration. It was wildly inconvenient - and you were constantly afraid that the rigid video cable would break off the smartphone's socket. I had to puzzle over creating a case. I took a ready-made plastic box for radio components. I had to make holes for the camera and glasses wires, break out the internal plastic partitions, insert new ones made of rigid foam rubber so that the smartphone with the video block would not dangle, but sit like a glove. At the same time, I ordered a couple of cables - a very short video cable instead of the native one and a wire to replace the standard USB adapter, which did not fit into the new case.

![AR-Go, the wearable computer.](https://habrastorage.org/r/w1560/storage2/43d/d87/728/43dd87728df13ed3f7279a6b45310554.png)\
_AR-Go, the wearable computer: Eyetop Centra HMD, Nokia N900 (computational block), headband with USB webcam, yet another Nokia N900 as remote control._

In the winter of 2010-2011 we went on "field tests" with professional biathletes to test whether the prototype I created would be convenient as a ski simulator. It turned out to be quite convenient and useful!

![Biathlete on the training session with AR-Go.](https://habrastorage.org/r/w1560/storage2/990/6a4/72c/9906a472cc4b6f60085345f5cf16f79c.jpg)
![Biathlete on the training session with AR-Go.](https://habrastorage.org/r/w1560/storage2/504/08b/c3e/50408bc3e43120a53119498bac44d24b.jpg)\
_Biathlete on the training session with AR-Go._

In the spring 2011, with the end of the ski season, I continued testing the AR-Go on a bicycle. What does a cyclist lack during a ride? Information in front of her eyes - time, speed, heart rate. And if you add a map - it's a fairy tale. Of course, you can use a bike computer mounted on the handlebars. But glancing at it distracts you from the road. You can still glance, but peering and reading the map is already risky. To begin with, I tested the capabilities I needed using ready-made programs. I recorded a video from a head-mounted camera looking forward (a kind of DVR) and looking back (a rearview mirror). I tested GPS navigation using the eCoach sports application. It turned out that using all this is quite convenient. Personally, riding in Eyetop Centra glasses is comfortable for me. The wide side temples of the glasses block the side view - but in 2025 you can print your own temples on a 3D printer or choose more suitable eyewear.

Having made sure that AR-Go can be used as a sports computer, I started writing a program that would turn my system into a wearable GPS navigator. The development was done in C++/Qt using QtMobility. However, I was unable to make Bluetooth work via QtMobility. But we have Linux on the board, right? So the bluetooth part was implemented in BlueZ.

In the end, I managed to make a fully functional navigator. The program can display maps (taken from Google Maps or OpenStreetMap, cached to minimize traffic), positions them by the current position, displays the time, current speed, draws a compass. The navigator can also record the current route, save it to a file, display the current route and the target route leading to the desired destination.

![AR-Go'naut in full gear (head-mounted camera, HMD eyewear, wearable computer in bag, remote control in hands. 2012)](https://habrastorage.org/r/w1560/storage2/61a/771/5b1/61a7715b17eb90abeaaed67248742751.jpg)\
_AR-Go'naut in full gear (head-mounted camera, HMD eyewear, wearable computer in bag, remote control in hands. 2012_

In April 2012, the AR-Go project received a prize from Lenovo at the Lenovo DoNetwork competition. And the prize was not presented to us by the actors-hosts of the evening, but by a representative of Intel R&D Department who specially came up on stage. And he didn’t just present the prize, he took a blitz interview right on stage. Damn, I’m proud of it!

![Lenovo DoNetwork Award Ceremony.](https://habrastorage.org/r/w1560/storage2/517/913/de1/517913de19611284e8958da58c32fdb6.jpg)\
_Lenovo DoNetwork Award Ceremony._

That was the beginning of this project. Let's continue! :)
