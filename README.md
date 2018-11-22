# Electronics, microcomputing + IoT resources

>Tutorials, events, software, hardware and reading material for getting started in electronics + IoT

## About

I put this list together after getting into a lengthy conversation with a colleague about electronics, microcomputing and the internet of things (IoT). After the conversation, by which time our hot drinks had gone cold, we realised we'd forgotten most of the things we talked about! This GitHub repository is an attempt to gather together some of the most useful links, in order to share them with my colleague, and the community.

If you'd like to contribute, I'll happily accept pull requests that add useful links in a similar vein to the rest in this repository. I won't accept pull requests that contain advertisements for your own products, unless you're contributing a useful tutorial, or video guide!

## Hardware

### Raspberry Pi

Link: https://www.raspberrypi.org/

The Raspberry Pi is a wonderful suite of devices for building connected projects. It can run Linux (the excellent [Raspbian](https://www.raspberrypi.org/downloads/raspbian/) distribution works well if you want a full desktop experience), and has a full 40-pin input / output (IO) header, for connecting to various sensors and devices.

The Raspberry Pi Zero W, which has onboard Wi-Fi and Bluetooth, is a great way into the ecosystem without spending lots of money.

### ESP8266 / ESP32

Link: https://en.wikipedia.org/wiki/ESP8266

The ESP8266 (and successor ESP32) is a super small, low powered device with onboard Wi-Fi. It can be used to build small standalone internet connected sensors (think thermometer, soil moisture sensor etc.), and loads more.

Thanks to their 'deep sleep mode', they can draw very little power, so you can even run them on small batteries for years at a time. See [this link](https://openhomeautomation.net/esp8266-battery/) for more details on that.

## Software

### Johnny-Five [JavaScript]

Link: http://johnny-five.io/

If you're familiar with JavaScript, and want to dive into robotics, electronics or IoT, then you should definitely check out Johnny-Five. It is a fully feature JavaScript library for interfacing with all kinds of microcomputers, including Raspberry Pi, Particle Photon, Tessel, Arduino, and loads more!

The electronics equivalent of "Hello, world!" is to flash an LED, which can be as simple as this using Johnny-Five:

```js
var five = require("johnny-five");
var board = new five.Board();

board.on("ready", function() {
  var led = new five.Led(13);
  led.blink(500);
});
```

Find out more, and read the docs on their website, linked above.

### Mozilla's Project Things

Link: https://iot.mozilla.org/

Mozilla has been developing their "Things" platform since early 2017, and is applying their principles of openness, decentralisation, and standardisation to IoT. Project Things consists of a few core elements, a communication gateway (Things Gateway), a set of cloud services (Things Cloud), and a framework of software components (Things Framework).

You can find out lots more about the platform at the above link.

### MQTT

Link: http://mqtt.org/

If you're writing software to run on connected devices, you may wish to send data between them, or back to a central store or database. MQTT is one messaging protocol that makes sending these messages very easy.

### Homebridge

Link: https://github.com/nfarina/homebridge

Homebridge is a simple service (written in Node.JS) for connecting your smart devices to an Apple HomeKit network. This allows you to control non-HomeKit devices from the iOS Home app, and from Siri!

It's simple to run on a low power Linux device like a Raspberry Pi, and has a range of pre-built plugins for existing devices, and you can write your own if you'd like to hook up something you've made to your HomeKit network.

### Fritzing

Link: http://fritzing.org/home/

If you're looking to design a circuit board, or even just record what you hacked together on your breadboard, Fritzing is an excellent open source tool for designing and creating electronics layouts.

It is completely free (donations recommended), and works on all major desktop platforms (Windows, macOS and Linux).

### Alexa Skills Kit

Link: https://developer.amazon.com/alexa-skills-kit

While not _formally_ electronics, you might want to integrate your latest project into the Amazon Echo ecosystem. To do that, you'll need to build a Skill. If you're familiar with JavaScript or Python, building an Alexa Skill is a great challenge, and is really rewarding.

If your IoT device can connect to the internet, then your Alexa Skill can connect to it, and could enable a whole range of interesting voice-controlled opportunities!

I've previously put together a quick-start template for building Alexa skills using the [Serverless](https://serverless.com/) framework and Node.js. You can find more about that here: https://github.com/chrishutchinson/alexa-serverless-template.

### IFTTT Maker Hooks / Webhooks

Link: https://ifttt.com/maker_webhooks

If you're interested in getting multiple internet-connected devices talking to each other, the IFTTT platform is a _really_ easy way to get started.

With just a few lines of code you can be sending notifications to your phone, and getting your smart light bulbs flashing, and sending off API requests.

If you don't want the headache of maintaining code for all the different internet platforms, IFTTT is an excellent choice.

## Components

> TODO: Lots more to come here!

### Sensors

#### Soil moisture sensor

Link: https://shop.pimoroni.com/products/sparkfun-soil-moisture-sensor-with-screw-terminals

This is a super simple sensor to get started with. If you have a plant (ideally indoors!), wire this up, and stick it in the soil. You'll be able to read out a value of the moisture content in the soil (really, it is a measure of how much electricity the soil can conduct).

Initially, this might not seem like much, but after wiring that up to a notification service (see IFTTT), or a motor, you could be well on your way to building an automated plant watering system!

## Projects + events

### Raspberry Pi NAS

Link: https://blog.alexellis.io/hardened-raspberry-pi-nas/

### Pi Wars

Link: https://piwars.org/

For fans of Robot Wars, this is for you. From the Pi Wars website:

>Pi Wars is an international, challenge-based robotics competition in which teams build Raspberry Pi-controlled robots and then compete in various non-destructive challenges to earn points.

If you're looking for a project that is fun and has some level of purpose, building a Raspberry Pi (or other microcomputer) robot might be just what you're looking for.

### Multi-druino

Link: https://www.youtube.com/watch?v=vuz9x18RQl0

A cool project using an Arduino to build a device that can be used for a multide of different things, including a multimeter, a calculator, and a component tester.

### Furlexa

Link: https://howchoo.com/g/otewzwmwnzb/amazon-echo-furby-using-raspberry-pi-furlexa

If you really hate yourself, why not try incorporating Alexa into a Furby, the '90s classic toy! Is this possibly the creepiest use of a Furby ever? I'll let you decide.

## Reading material

### HackSpace

Link: https://hackspace.raspberrypi.org/

While not officially an electronics / software magazine, if you're interested in the maker space, the HackSpace magazine is an excellent read. Published monthly, the PDFs for all past and future editions are available on their website for free, but I highly recommended subscribing. Not only do you support the excellent work done by the HackSpace editorial team, it looks wonderful in printed form!
