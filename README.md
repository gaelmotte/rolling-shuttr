# rolling-shuttr
Idee for future project, mobile app that captures video and applies a slow running shutter effect on it

## What is it ?
We sometimes see some videos that illustrate rolling shutter effect. How about a service that could apply this to your video, with a much more accentuated effect ?

<img src="http://payload325.cargocollective.com/1/0/21154/8811319/twisted.gif" width="200">
source : http://markusmagnusson.tv/

The idea comes from this gif and my little experience with my scanner based camera.

## What could i do with it ? 
Here are some exemple of what i would do with it, feel free to add ideas :)
###Twisted couple
Just like in the gif above, why not record a couple set on a rotating platform. With a top down rolling shuter, they would twist arround each other
###Ultra fast bike rider
Have some rider enter frame from the left side, mark a break, then accelerate to leave frame on the other side. A top to down rolling shutter whould deform him just as if he were extremely fast, animation style.

## How would it work ?
User grabs his smartphone and opens the app. The app captures a short video and uploads it to a service.
The service extracts frames from the video, and assembles a gif applying really slow running shutter effect.
User gets the gif back from the service.

## Ideas of implementation
### Mobile App
* HTML5 web app. No native. 
* Could be installed on FxOS and Android via Chrome maybe ?
* Would rely on WebRTC http://www.html5rocks.com/en/tutorials/getusermedia/intro/
* Consider placing frames extraction on client for bandwith and service computational requieremetns savings

### Server Components
 * NodeJS app
 * will have to read uploaded frames of video, extract line by line and assemble everything as a gif. https://github.com/pkrumins/node-gif/blob/master/tests/animated-gif/animated-gif.js
 * Possible auth, and keeping user uploads for sharing on social media.
 
