# Hanifin Smart Home

| My Repository | Home Assistant Community |
| :---| :--- |
| [![Github Action Status][github-build-status-shield]][github-build-status] [![Github Linter Status][github-linter-status-shield]][github-linter-status] | [![Community Forum][discourse-shield]][discourse]
| [![GitHub Activity][commits-shield]][commits] [![Last Commit][github-last-commit]][github-master] | [![Discord][discord-shield]][discord] |
| [![Home Assistant Version][ha-version-shield]][ha-version] |

## Smart Home Articles

I write instructional articles on [brianhanifin.com](https://brianhanifin.com/). Topics primarily revolve around Home Assistant and ESPHome code and devices, but I also I have written about my HomeLab server setup.

---

## An occasionally updated summary of our smart home
I started using Home Assistant in the spring of 2018 when we outgrew the limited automations on Apple's HomeKit platform. Our Home Assistant initially included many HomeKit smart plugs our collection of smart lights, switches, plugs, cameras, and sensors. Since we have added many devices that use protocols like Zigbee and Z-Wave and even several custom built electronic modules.

Home Assistant now manages our smart home devices with lots of intelligence handled by automations. It is important that our devices can be controlled by standard wall switches, but we also use Google Nest speakers to control our devices with our voice. Not only can we talk to Google, but she can let us know when a laundry cycle, 3D Print, or laser cutting job is complete.

## User Interface

### Physical Buttons
We use a variety of physical switches from hard-wired to battery powered.

#### In-wall Dimmers and Switches
These can be used to control dumb lights. However, some devices allow you pass constant power so you can control smart bulbs with Home Assistant. For example a switch in my Dining Room leaves power to my Hue bulbs so I can turn the lights on with my voice or the physical wall switch.

<span style="float:left">![bedroom_switches]</span>
#### Bedside Toggle Switches
A battery powered double switch to my wife's bedside table. Single clicks toggle the lights on either side of our bed. While a double click toggles the bedroom fan, or the sound machine.

### Google Nest Speakers and Displays
We can also interact with our devices with Google Nest speakers in all of the major rooms of the house.

Our Google Nest also make announcements when something needs our immediate attention. For example: when it is time to leave for school, or its time to start cooking dinner because mom's on her way home from work.

### Tablet Reference User Interface
We have a 7-inch Amazon tablet in the Kitchen which displays useful information such as our family calendar and which child's turn is it do the dishes this week.

### Mobile User Interface (Lovelace)
I exclusively Interact with Home Assistant with my phone (or computer when coding). If noone else needs to bother with it, I have done a good job!  :smirk:

---

## Smart Home Devices

> Disclosure: This article may contain affiliate links. If you decide to make a purchase, I'll make a small commission at no extra cost to you.

### Lutron Caseta
Device recommendations: [Dimmer](https://amzn.to/3pHXJth), [Pico Remote](https://amzn.to/2OYVHZ4), [Dimmer and Pico Remote](https://amzn.to/3unpD0Y), [Lutron Caseta Pro Bridge](https://amzn.to/3aH1pqO)

In-wall dimmer switches and in-wall (or handheld) wireless remotes. Get the [Lutron Caseta Pro Bridge](https://amzn.to/3aH1pqO) so you can us your Pico Remotes with Home Assistant to control any device in your house! The standard bridge is less expensive but you cannot watch for Pico Remote button press events.

#### Project Ideas
1. Add a battery powered Pico Remote next to a room which doesn't have a wall switch! Control a smart bulb by any manufacturer! My Living Room was lacking a switch, but I cut a little hole in drywall and now it does! :beers:
2. Replace a dumb wired light switch or dimmer with a Caseta Dimmer so Home Assistant can automatically turn the lights on at night when a motion sensor detects you have entered the room!
3. Use Home Assistant to brighten the lights gradually to help you wake up in the morning.

### Inovelli Red Series Switches and Dimmers
Device recommendations: [Red Series Dimmer](https://amzn.to/2ZY73i3), [Red Series Switch](https://amzn.to/3r2WtT5), [Red Series Fan & Light Switch](https://amzn.to/3q0yB12)

Inovelli Z-Wave devices are high quality and they really care about our niche community. The Red Series switches handle double, triple, quadruple, and event quintuple click events. These even have a led light strip on the right side which we use different color and animations to indicate the state of things around the house.

#### Project Ideas
1. **Multi-click actions!** 2x click to turn on/off the bright floor lamp, 3x click to turn on/off the floor fan, 4x click to activate your "Goodnight" scene, 5x click to activate guest mode on your way to answer the door!<br>
*See my automation: [automations/buttons/zwjs_button_click.yaml](https://github.com/brianhanifin/Home-Assistant-Config/blob/master/automations/buttons/zwjs_button_click.yaml)*
2. **House Status Indicator** Use the Led Strip to indicate when the garage is open, or the alarm is disarmed.<br>
*See my article: "[Inovelli Red Series Status LED Update](https://brianhanifin.com/posts/inovelli-red-series-status-led-update/)"*

### Philips Hue Bulbs
Device recommendations: [Starter Kit](https://amzn.to/37AqeTq) (3 color bulbs, battery dimmer, & hub)

The Hue ecosystem is easy to get setup with Home Assistant. We primarily use their tunable white bulbs for plug in floor and table lamps, but we do have 9 colored bulbs in our dining room chandelier for holiday fun.

#### Project Ideas
1. Use these bulbs to make your plug in lamps controllable by Home Assistant.
2. Create a realistic sunrise to wakeup in the morning using the tunable white light.

### Smoke + Carbon Monoxide Detectors

Device recommendation: [First Alert Z-Wave 2-in-1 Smoke Detector & Carbon Monoxide Alarm](https://amzn.to/3r0RjGV)

Thanks to Carlo's article "[PSA: CHECK OUT YOUR SMOKE DETECTORS (ONCE EVERY 10 YEARS)][carlo-blog-smoke]" I realized that I had lived in my house for almost 11 years, and we were due for new smoke detectors. So I replaced them with new First Alert ZCombo Z-Wave smoke detectors.

#### Project ideas:
1. **Safety Alert!** Have Home Assistant alert you which detector sensed the Smoke so you can decide whether to try to put it out, or get to safety!

### Xiaomi Aqara Zigbee Smart Home Devices
Device recommendations: [Wireless Buttons](https://amzn.to/3q4jd3w), [Motion & Luminance Sensors](https://amzn.to/3q0OOTK), [Temperature & Humidity Sensors](https://amzn.to/2ZYWV8I), [Door & Window Sensors](https://amzn.to/2ZWptjl), [Leak Sensors](https://amzn.to/3r1bYef), [Vibration Sensors](https://amzn.to/2ZUvrBl)
Hub recomendations: [Phoscon Conbee II USB Gateway](https://amzn.to/2Mz3jk8), [Aqara Homekit Hub](https://amzn.to/37TN6xv), [Aqara Starter Kit: Hub, Plug, Button, Motion, Door/Window](https://amzn.to/2O6STIO)

This Chinese company makes a lot of very useful and inexpensive wireless smart home products. At first I used their Zigbee smart hub to get these devices to talk to Home Assistant. However I now use a USB Stick connected to my server to communicate with all of my Zigbee devices.

#### Project ideas
1. **Door and window sensors**: Stick door and window sensors on doors and windows around your house and have Home Assistant remind you to close the doors and windows when it starts to get warm outside.
2. **Motion lights**: stick a motion sensor in your<br>
   2a. Kitchen to turn on an LED strip under your cabinets to give yourself a nightlight when getting water in the middle of the night.<br>
   2b. Bedroom to light a dim path to the bathroom.
3. **Flood damage alert!** Place leak sensors under your all sinks, dishwasher, clothes washer, refrigerator, and water heater. Setup an alert to notify you where the leak is. This will give you valuable time to stop major flood damage!
4. **Medicine logger**: stick a wireless button inside the medicine cabinet to log when you gave seizure medicine to your dog.
5. **Automatic bathroom exhaust**: use a Temperature & Humidity Sensor to automatically turn on your exhaust fan and turn it back off when the humidity drops again.

## DIY Smart Home Devices

I have flashed the below devices with ESPHome firmware which I have full control 
over! You can see my code at my [esphome-config GitHub repository][esphome-config].

### Shelly 1 Boards
Device recommendations: Shelly 1 ([1 pack](https://amzn.to/3qKTyhI), [2 pack](https://amzn.to/3bw9bmN)), [Shelly 2](https://amzn.to/37Aq7qY)

These devices are great for shoving in a box behind a light switch to add smarts.

#### Project ideas
1. **Hue Bulb functional light switch**: my dining room has a 9 bulb chandelier, this provides constant power, while allowing the switch to remain functional.
2. **Smart Bathroom Exhaust Fan**<br>
*2a.* turns the fan off after 10 minutes when manually turned on (*note: a battery powered motion sensor resets the countdown*).<br>
*2b.* turns the fan on then back off when the humidity is up due to a shower (*note: a battery powered humidity sensor in the bathroom is compared to one in a neighboring room*).
3. **Garage Door Controller**: I plan to replace the cloud based Chamberlain MyQ controller soon using [The Hook Up's video for reference ](https://www.youtube.com/watch?v=WEZUxXNiERQ).

### SonOff S31 Plugs
Device recommendations: [S31](https://amzn.to/2OOEilB), [S31 Lite](https://amzn.to/2NMhi6i)

The SonOff S31 is a reliable Wi-Fi controlled smart switch which can be flashed with Tasmota or ESPHome if you wish. The original S31 has Power Monitoring built in, while the new S31 Lite omits that for a discount.

#### S31 Power Monitoring Project Ideas
*Note: the relay can be left always on to put these in a monitor only mode.*
1. Monitor your washing machine so Home Assistant can notify you when your wash is ready to be hung up or moved to the dryer! No more stinky clothes!
2. Monitor your dishwasher or clothes dryer.
3. Monitor your 3D Printer or Laser Cutter to let you know when it is time to check out that thing you just created!

#### S31 Lite Project Ideas
1. Plug one of these into every floor and table fan you own and just ask your Google or Alexa to *"turn on the bedroom fan!"*.
2. Plug one into a sound machine to help you sleep at night. Have Home Assistant automatically start this when your phone starts charging for the night.

### Presence detection

#### Life360 Integration
I use [Life360](https://www.life360.com/) for presence tracking on my son's, wife's, and my phone. This has made me comfortable enough to do things like having Home Assistant close the garage door if one of us leaves the home zone. This covers us for those few times we may forget to close the door before driving away! :)

#### Ubiquiti UniFi Integration
For extended family visitors I use the [Home Assistant Ubiquiti UniFi Integration](https://www.home-assistant.io/integrations/unifi/#presence-detection) to track when their phones are connected to my Wireless Access points.

#### Guest Mode Helper
Finally, I have a "Guest Mode" input_boolean setup as both a trigger and a condition on many of my lighting and front door locking automations.

## Wireless Communications

### Wi-FI: Ubiquiti Unifi
Device recommendations: [Unifi 6 Lite Access Point](https://amzn.to/3q1OUut) (Wi-Fi 6), [Unifi AC-PRO Access Point](https://amzn.to/2NMc1vW) (802.11ac, I have 3 of these), [Unifi Security Gateway](https://amzn.to/2NEbooj)

Eventually you outgrow even the fanciest home WiFi setup. There were just too many devices for my Netgear Orbi mesh networking system to handle, so I had to upgrade to a business grade solution.

Pros:
* Rock solid WiFi all throughout the downstairs.
* Household members don't complain about the WiFi anymore!
* Long Ethernet cable runs make all access points equally fast!

Cons:
* Requires a long Ethernet cable run to each Access Point. (But also a "Pro"... see the last point above.)

### Zigbee
Recommendation: [Phoscon Conbee II USB Gateway](https://amzn.to/2Mz3jk8)

Home Assistant's ZHA Integration directly runs all of my Zigbee devices. This includes all of my Philips Hue bulbs and all of my Xiaomi Aqara sensors!

### Z-Wave
Recommendation: [Aeotec Z-Stick Gen5 Plus](https://amzn.to/3kw7YzO)

As of February 2021 Home Assistant's Z-Wave JS Integration directly runs all of my Z-Wave devices. To be precise I am running [Zwavejs2Mqtt](https://zwave-js.github.io/zwavejs2mqtt/#/)) with MQTT disabled so I can make use of the Z-Wave Device Management UI built in. This includes several in-wall switches and dimmers, smoke detectors, and a bulb.
## Technical Details

Our Home Assistant install has approximately **1200 total entities**, 
including **564 sensors**.

<details><summary>22 Custom Integrations</summary>
  

#### [Adaptive Lighting](https://github.com/basnijholt/adaptive-lighting)
    Adaptive Lighting custom component for Home Assistant
    Authors:@basnijholt.
  
  

#### [Anniversaries v4.3.0](https://github.com/pinkywafer/Anniversaries)
    Anniversary Countdown Sensor for Home Assistant
    Authors:@pinkywafer.
  
  

#### [Average Sensor v1.7.3](https://github.com/Limych/ha-average)
    Average Sensor for Home Assistant
    Authors:@Limych.
  
  

#### [Browser Mod v1.3.0](https://github.com/thomasloven/hass-browser_mod)
    🔹 A Home Assistant integration to turn your browser into a controllable entity - and also an audio player
    
  

#### [Config Check](https://github.com/custom-components/config_check)
    Run the CLI config_check from a service call.
    Authors:@ludeeus.
  
  

#### [Event Sensor v2.4.1](https://github.com/azogue/eventsensor)
    HomeAssistant custom sensor to track specific events
    Authors:@azogue.
  
  

#### [Frigate v1.0.4](https://github.com/blakeblackshear/frigate-hass-integration)
    Frigate integration for homeassistant
    Authors:@blakeblackshear.
  
  

#### [Google Home v1.4.3](https://github.com/leikoilja/ha-google-home)
    Home Assistant Google Home custom component
    Authors:@leikoilja, @DurgNomis-drol, @ArnyminerZ, @KapJI.
  
  

#### [Ha Sun2 v2.0.0](https://github.com/pnbruckner/ha-sun2)
    Home Assistant Sun2 Sensor
    Authors:@pnbruckner.
  
  

#### [Home Assistant Community Store (HACS) v1.12.3](https://github.com/hacs/integration)
    HACS gives you a powerful UI to handle downloads of all your custom needs.
    Authors:@ludeeus.

#### [Rainforest Energy Monitoring Component](https://github.com/damienheiser/home-assistant)
    Use your Rainforest Automation EMU-2™ Energy Monitoring Unit in Home Assistant.
    Authors:@jrhorrisberger.
  
  

#### [Iphone Device Tracker v1.4.0](https://github.com/mudape/iphonedetect)
    A custom component for Home Assistant to detect iPhones connected to local LAN, even if the phone is in deep sleep.
    Authors:@mudape.
  

#### [Readme](https://github.com/custom-components/readme)
    Use Jinja and data from Home Assistant to generate your README.md file
    Authors:@ludeeus.
  
  

#### [Samsungtv Smart v0.3.34](https://github.com/ollo69/ha-samsungtv-smart)
    📺 Home Assistant SamsungTV Smart Component with simplified SmartThings API Support configurable from User Interface.
    Authors:@ollo69.
  
  

#### [Scheduler Component v3.1.0](https://github.com/nielsfaber/scheduler-component)
    Custom component for HA that enables the creation of scheduler entities
    Authors:@nielsfaber.
  
  

#### [Sensor.Unifigateway v0.3.3](https://github.com/custom-components/sensor.unifigateway)
    High level health status of UniFi Security Gateway devices via UniFi Controller
    Authors:@jchasey.
  
  

#### [Smartthinq Lge Sensors v0.6.8](https://github.com/ollo69/ha-smartthinq-sensors)
    Home Assistant custom integration for SmartThinQ LG devices configurable with Lovelace User Interface.
    Authors:@ollo69.
  
  

#### [Spacex Next Launch And Starman v028](https://github.com/djtimca/HASpaceX)
    Home Assistant integration for SpaceX Next Launch and Starman data.
    Authors:@djtimca.
  
  

#### [Ui Template Sensor Configuration v0.1.2](https://github.com/custom-components/templatesensor)
    Add template sensors from the UI.
    Authors:@ludeeus.
  
  

#### [Weatheralerts v0.1.4](https://github.com/custom-components/weatheralerts)
    A sensor that gives you weather alerts from alerts.weather.gov.
    Authors:@ludeeus, @jlverhagen.
  
  

#### [Wyze Bulb, Switch And Sensor Integration v2021.5.5-deices-update-beta.3](https://github.com/JoshuaMulliken/ha-wyzeapi)
    Home Assistant Integration for Wyze devices.
    Authors:@JoshuaMulliken.
  
  

#### [Youtube v0.7.0](https://github.com/custom-components/youtube)
    A platform which give you info about the newest video on a channel
    Authors:@ludeeus, @pinkywafer.
</details>

<details><summary>30 Lovelace Plugins</summary>

#### [Atomic Calendar Revive v3.4.1](https://github.com/marksie1988/atomic-calendar-revive)
    Custom calendar card for Home Assistant with Lovelace


#### [Auto Entities v1.8.5](https://github.com/thomasloven/lovelace-auto-entities)
    🔹Automatically populate the entities-list of lovelace cards

  

#### [Badge Card](https://github.com/thomasloven/lovelace-badge-card)
    🔹 Place badges anywhere in the lovelace layout


#### [Button Card v3.4.2](https://github.com/custom-cards/button-card)
    ❇️ Lovelace button-card for home assistant


#### [Card Mod v3.0.12](https://github.com/thomasloven/lovelace-card-mod)
    🔹 Add CSS styles to (almost) any lovelace card


#### [Card Tools v11](https://github.com/thomasloven/lovelace-card-tools)
    🔹A collection of tools for other lovelace plugins to use


#### [Decluttering Card v0.6.3](https://github.com/custom-cards/decluttering-card)
    🧹 Declutter your lovelace configuration with the help of this card


#### [Favicon Counter v1.0.0](https://github.com/custom-cards/favicon-counter)
    Show a notification count badge.


#### [Fold Entity Row v20.0.4](https://github.com/thomasloven/lovelace-fold-entity-row)
    🔹 A foldable row for entities card, containing other rows

  

#### [Gap Card](https://github.com/thomasloven/lovelace-gap-card)
    🔹 A lovelace card that does nothing and looks like nothing. Incredibly useful! No, really.


#### [Ha (Lovelace) Card Weather Conditions v1.9.12](https://github.com/r-renato/ha-card-weather-conditions)
    Weather condition card (Lovelace) for Home Assistant.


#### [Kiosk Mode v1.6.5](https://github.com/maykar/kiosk-mode)
    🙈 Hides the Home Assistant header and/or sidebar


#### [Layout Card v2.2.3](https://github.com/thomasloven/lovelace-layout-card)
    🔹 Get more control over the placement of lovelace cards.


#### [Lovelace Home Feed Card v0.5.0](https://github.com/gadgetchnnel/lovelace-home-feed-card)
    A custom Lovelace card for displaying a combination of persistent notifications, calendar events, and entities in the style of a feed.


#### [Lovelace Text Input Row v0.0.8](https://github.com/gadgetchnnel/lovelace-text-input-row)
    A custom Lovelace text input row for use in entities cards


#### [Mini Graph Card v0.10.0](https://github.com/kalkih/mini-graph-card)
    Minimalistic graph card for Home Assistant Lovelace UI


#### [Mini Media Player v1.12.1](https://github.com/kalkih/mini-media-player)
    Minimalistic media card for Home Assistant Lovelace UI


#### [Multiple Entity Row v4.2.0](https://github.com/benct/lovelace-multiple-entity-row)
    Show multiple entity states and attributes on entity rows in Home Assistant's Lovelace UI


#### [Power Wheel Card v0.1.5](https://github.com/gurbyz/power-wheel-card)
    An intuitive way to represent the power and energy that your home is consuming or producing. (A custom card for the Lovelace UI of Home Assistant.)


#### [Restriction Card v1.2.6](https://github.com/iantrich/restriction-card)
    🔒 Apply restrictions to Lovelace cards


#### [Scheduler Card v2.1.1](https://github.com/nielsfaber/scheduler-card)
    HA Lovelace card for control of scheduler entities


#### [Sidebar Card v0.1.7.9](https://github.com/DBuit/sidebar-card)
    


#### [Simple Thermostat v2.4.0](https://github.com/nervetattoo/simple-thermostat)
    A different take on the thermostat card for Home Assistant ♨️


#### [Slider Entity Row v17.0.1](https://github.com/thomasloven/lovelace-slider-entity-row)
    🔹 Add sliders to entity cards


#### [Stack In Card v0.2.0](https://github.com/custom-cards/stack-in-card)
    🛠 group multiple cards into one card without the borders


#### [State Switch v8](https://github.com/thomasloven/lovelace-state-switch)
    🔹Dynamically replace lovelace cards depending on occasion


#### [Template Entity Row v1.1.1](https://github.com/thomasloven/lovelace-template-entity-row)
    🔹 Display whatever you want in an entities card row.


#### [Tesla Style Solar Power Card v1.2.2](https://github.com/reptilex/tesla-style-solar-power-card)
    Home assistant power card mimicking the one tesla provides for the powerwall app.


#### [Time Picker Card v1.2.1](https://github.com/GeorgeSG/lovelace-time-picker-card)
    🕰️ Time Picker Card for Home Assistant's Lovelace UI


#### [Weather Card v1.5.0](https://github.com/bramkragten/weather-card)
    Weather Card with animated icons for Home Assistant Lovelace

</details>

<details><summary>3 Addons</summary>

#### ESPHome v1.17.1
    ESPHome Hass.io add-on for intelligently managing all your ESP8266/ESP32 devices.


#### Home Assistant Google Drive Backup v0.104.3
    Automatically back up Home Assistant snapshots to Google Drive


#### Samba share v9.3.1
    Expose Home Assistant folders with SMB/CIFS

</details>

---

## Inspiration
The following are just some of the people that have inspired my smart home.

### Carlo
I aspire to Carlo's level of home connectedness. I have taken baby steps to giving my home a voice, but my speech routines are not being utilized quite as elegantly as at Carlo's house!
* Github: [Bear Stone Smart Home Configuration][carlo-github]
* Blog: [vCloudInfo][carlo-blog]
* YouTube: [vCloudInfo Channel][carlo-youtube]

### DrZzs
I wish I could be more like this guy. He is just so darn positive and happy all of the time. He taught me how to "Tasmota". I like to have one of his videos or streams playing in the background while I am coding.
* Github:  [SniperCanie's Repositories][drzzs-github]
* YouTube: [DrZzs Channel][drzzs-youtube]

### Frenck
I just learned of Frenck recently, but he is a long time member of the community. I just refactored my code to be similar to his config ([as discussed in this video][frenck-youtube-config]).
* Github: [Frenck's Home Assistant Configuration][frenck-github]
* YouTube: [Frenck's Channel][frenck-youtube]

---

All of my configuration files are tested against the most stable version of home-assistant using [Github Actions](https://github.com/brianhanifin/Home-Assistant-Config/actions).


[bedroom_switches]: ./README-images/xiaomi_double_switch.jpeg

[esphome-config]: https://github.com/brianhanifin/esphome-config

[ha-version]: https://www.home-assistant.io/blog/categories/release-notes/
[ha-version-shield]: https://img.shields.io/badge/Home_Assistant-2021.5.0-41BDF5?logo=home%20assistant

[github-build-status-shield]: https://github.com/brianhanifin/Home-Assistant-Config/actions/workflows/build.yml/badge.svg
[github-build-status]: https://github.com/brianhanifin/Home-Assistant-Config/actions/workflows/build.yml
[github-linter-status-shield]: https://github.com/brianhanifin/Home-Assistant-Config/actions/workflows/linters.yml/badge.svg
[github-linter-status]: https://github.com/brianhanifin/Home-Assistant-Config/actions/workflows/linters.yml

[commits-shield]: https://img.shields.io/github/commit-activity/m/brianhanifin/Home-Assistant-Config.svg?logo=github&logoColor=838B95
[commits]: https://github.com/brianhanifin/Home-Assistant-Config/pulse

[maintained]: https://img.shields.io/maintenance/yes/2021.svg

[github-last-commit]: https://img.shields.io/github/last-commit/BrianHanifin/Home-Assistant-Config.svg?logo=github&logoColor=838B95
[github-master]: https://github.com/BrianHanifin/Home-Assistant-Config/commits/master

[discord-shield]: https://img.shields.io/discord/330944238910963714.svg?logo=discord&color=7289da
[discord]: https://discord.gg/c5DvZ4e

[discourse-shield]: https://img.shields.io/discourse/topics?color=46B4ED&label=community&logo=discourse&logoColor=46B4ED&server=https%3A%2F%2Fcommunity.home-assistant.io
[discourse]: https://community.home-assistant.io/u/brianhanifin/summary

[esphome-ble-hub]:https://esphome.io/components/esp32_ble_tracker.html
[esphome-sonoff-basic]:https://esphome.io/devices/sonoff_basic.html

[hue-strip-guide]:https://char.gd/blog/2018/building-better-cheaper-philips-hue-led-strips

[carlo-blog]: https://www.vcloudinfo.com
[carlo-github]: https://github.com/CCOSTAN/Home-AssistantConfig
[carlo-youtube]: https://YouTube.com/vCloudInfo
[carlo-blog-smoke]: https://www.vcloudinfo.com/2017/06/psa-check-out-your-smoke-detectors-once.html

[drzzs-github]: https://github.com/Snipercaine
[drzzs-youtube]: https://www.youtube.com/channel/UC7G4tLa4Kt6A9e3hJ-HO8ng

[frenck-github]: https://github.com/frenck/home-assistant-config/
[frenck-youtube]: https://www.youtube.com/user/Frenck
[frenck-youtube-config]: https://youtu.be/lndeybw21PY