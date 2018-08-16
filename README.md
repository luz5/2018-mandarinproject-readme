# 2018 Summer Mandarin Project

Mandarin Project is ..... (#todo)







## Table of Contents 

1. [User Guide](#user-guide)
   * [Installation](#installation)
   * [Demo Playthrough](#demo-playthrough)
2. [Spetial Context System](#spetial-context-system)
   * [API Guide](#api-guide)
   * [Kinects Controller](#kinects-controller)
3. [Troubleshooting](#troubleshooting)







## User Guide

#### Installation

(#todo)

#### Demo Playthrough

1. ##### Start TTS 

   (Mac mini)

   you can also do it in Linux server or Display PC just make sure Mac mini is not in sleep mode.

   Should be always running in the backend

   For more information [readme.txt]() (#todo)

   > 1. Open http://128.113.21.81:7777/ (Username: `admin` Password: `password`)
   > 2. Check if `multichannel-transcript-worker` is running

2. ##### Run Watson send_intents

   (Display PC)

   > If using terminal:
   >
   > - go to `~/Mandarin-project/Node.js\ Backend/Watson/`
   >
   > - run `$node Watson_Send_Intents.js`
   >
   > For quick start: 
   >
   > - run `Watson_Send_Intents.bat`
   >
   > If you want to reset the backend in unity:
   >
   > - Hit `Rset Cntxt` button at the debug menu 
   >
   > For more information check `node.js backend` [readme.txt](https://github.com/luz5/2018-mandarinproject-readme/blob/master/README.txt.txt) file
   >
   > If you want to reset the backend in unity

3. ##### Run Unity Build

   (Display PC)

   > If using Studio 2 display pc (#todo)
   >
   > 

4. ##### Run SCW backend

   (Linux server) 

   For **pointing system** and **gesture system** to work Mou's SCW scripts need to be running in the backend. 

   > In terminal:
   >
   > - Go to `~/CISL/Spatial_Context/Implementation/core`
   > - Run `$ python3 start_spatial_context_server.py`

   Right now we do not have auto switch for pointing system and gesture system. So when you need pointing system only:

   > Go to `~/CISL/Spatial_Context/Implementation/core`
   >
   > Open `cog.json`
   >
   > Change `pointing_enabled` to 'true', set `gesture_enabled` and `mp_backend_service` to 'false'
   >
   > *** In the [kinects controller](#kinects-controller) , open number 3 kinect by enter `2` first and enter `13`. You can enter `5` to check if `kinect_3` is the only one open when you try to point.***

   If you need gesture system only:

   > Go to `~/CISL/Spatial_Context/Implementation/core`
   >
   > Open `cog.json`
   >
   > Change `pointing_enabled` to 'false', set `gesture_enabled` and `mp_backend_service` to 'true'
   >
   > *** In the [kinects controller](#kinects-controller) , open number 4 kinect by enter `2` first and enter `14`. You can enter `5` to check if `kinect_4` is the only one open when you try to use gesture (like Taiji) .***

   You can turn on both system at the same time by setting all the variables to 'true' but the accuracy level for both system will decrease.

   Make sure kinects are on for motion capture. You can use [kinects controller](#kinects-controller).

   Re-run the `start_spatial_context_server.py` if anything happens (etc. connection error)

5. ##### Demo Dialogue Detail

   - [Main Street](#===main-street===)
   - [Garden](#===garden===)
   - [Restaurant](#===restaurant===)

   ##### ===Main Street===

   丽莎好的 

   老板我要买蛋糕 

   老板我要买两个

   老板不用了

   小姐我要买明信片

   小姐我要买两个

   小姐不用了

   （hit space bar on the keyboard to go another waypoint）

   阿姨我要买项链

   阿姨我要买两个

   阿姨不用了

   先生我要买水

   先生我要买两个

   先生我要买茶

   先生我要买两个

   先生不用了

   （hit space bar again to go back）

   丽莎不玩了

   丽莎好的

   丽莎好的

   (press G and click "finish" button)

   丽莎不完了

   （press G to go to garden）

   ##### ===Garden===

   同学你好

   师傅我想打太极

   师傅没有

   （begin to do 4 separate movements）

   师傅不要

   师傅好的

   （begin to do all 4 movements together）

   师傅不要

   （press G to go to restaurant）

   ##### ===Restaurant===

   大姐你好

   大姐我要咖啡

   大姐我要饺子

   大姐再见

For more information check [summer challenge dialogues](https://docs.google.com/document/d/1KCpw9ZSXUizJuU2y8bDQvNJw6xpRIclGGiuFVKeB3A0/edit#heading=h.h0vqzkscp9u3) 





## Spetial Context System

#### API Guide

#todo

#### Kinects Controller

It can control all 4 kinects in studio 2 (for more information ask Mou ? #todo)

> In terminal:
>
> - Go to `~/CISL/Spatial_Context/Implementation/core`
> - Run `$ python3 controller.py`

Enter `1`: Start all active kinects

Enter `1[kinects number]`: Start specified kinect

> For example: Enter `12` will start number 2 kinect 

Enter `2`: Stop all active kinects

Enter `2[kinects number]` : Stop specified kinect

> For example: Enter `22` will stop number 2 kinect

Enter `5`: Check the status of all active kinects and show if people is detected by kinects







## Troubleshooting

Here are some fixes to some common problems.

1. If no voice input

   Check if **mac mini** is in sleep. 

   If it is, wake it up and check if [TTS](#start-tts) is running

2. Check if the node.js backend is running. 

   If it is running you should see `waiting for input` at the terminal

   If it is not running, [restart](#run-watson-send_intents) it 

3. If system can not recognize gestures, see if SCW server is disconnected.

   If it is, [restart](#run-scw-backend) it 

4. If Lisa is talking like crazy, check if you have two `node.js backend` programs running at the same time.

