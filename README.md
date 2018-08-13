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

1. ##### Start TTS (Should be always running in the backend)

   > 1. Open http://128.113.21.81:7777/ (Username: `admin` Password: `password`)
   > 2. Check if `multichannel-transcript-worker` is running

2. ##### Run Watson send_intents.js

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
   > For more information check `node.js backend` readme.txt(#todo) file

3. ##### Run Unity Build

   > If using Studio 2 display pc (#todo)
   >
   > 

4. ##### Run SCW backend

   For **pointing system** and **gesture system** to work Mou's SCW scripts need to be running in the backend. 

   > In terminal:
   >
   > - Go to `~/CISL/Spatial_Context/Implementation/core`
   > - Run `$ python3 start_spatial_context_server.py`

   Make sure kinects are on for motion capture. You can use [kinects controller](#kinects-controller)

5. ##### Demo Dialogue Detail

   - [Main Street](#main-street)
   - [Garden](#garden)
   - [Restaurant](#restaurant)

## Spetial Context System

#### Kinects Controller

It can control all 4 kinects in studio 2 (for more information ask Mou ? #todo)

> In terminal:
>
> - Go to `~/CISL/Spatial_Context/Implementation/core`
> - Run `$ python3 controller.py`

Enter `1`: Start all kinects

Enter `1[kinects number]`: Start specified kinect

> For example: Enter `12` will start number 2 kinect 

Enter 2: Stop all kinects

 