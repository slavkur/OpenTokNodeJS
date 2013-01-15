# Getting started:  NodeJS + OpenTok
This repo is designed for beginners. It's the bare minimum to build a fully functioning video chat room

## How it works
After you run the nodejs server, simply go to your browser and type `localhost:9393/roomid` Everyone in the same room will be able to video chat with each other.

For a live demo, this is hosted at [http://nodeopentok.aws.af.cm/]().  This application is hosted with [appfog](https://www.appfog.com/)

## Requirements
This app features the latest in Web Media Streaming technology using WebRTC. Currently, only **Chrome** supports it. To run on other browsers using flash, simply change the javascript library to use flash in `view.ejs`
> `<script src="http://static.opentok.com/v0.91/js/TB.min.js"></script>`

## File Descriptions
#### README.md
> This is this readme file, written in Markdown

#### package.json 
> Json object of your app description and all the modules that your nodejs app needs to run

#### node_modules
> All the modules that you defined in package.json will be downloaded into this folder after you type `npm install`

#### app.js
> Server side code! Code Summary:
> > Whenever we get a request, check the url to see if an OpenTok sessionID exist for that particular URL. If not, create a new OpenTok sessionID. Pass the OpenTok sessionID and corresponding Token into the view

#### view.ejs
> Client Side Code! Code Summary:
>> With the OpenTok sessionID and token generated by `app.js`, Connect to the OpenTok session. When we are connected, create a publisher and start publishing video into the session. Subscribe to all video streams from other publishers. 

## To Run
First install all necessary dependencies from package.json `npm install`

Run NodeJS app `node app.js`

## Go Code!

Thanks for reading. My name is Song Zheng and I am a Developer Evangelist at [TokBox](http://tokbox.com) - [@songz](http://twitter.com/songz) 
