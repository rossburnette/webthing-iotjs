# WEBTHING-IOTJS #

[![GitHub forks](
https://img.shields.io/github/forks/rzr/webthing-iotjs.svg?style=social&label=Fork&maxAge=2592000
)](
https://GitHub.com/rzr/webthing-iotjs/network/
)
[![license](
https://img.shields.io/badge/license-MPL--2.0-blue.svg
)](LICENSE)
[![Build Status](
https://travis-ci.org/rzr/webthing-iotjs.svg?branch=master
)](
https://travis-ci.org/rzr/webthing-iotjs
)
[![NPM](
https://img.shields.io/npm/v/webthing-iotjs.svg
)](
https://www.npmjs.com/package/webthing-iotjs
)
[![pulls](
https://img.shields.io/docker/pulls/rzrfreefr/webthing-iotjs.svg
)](
https://cloud.docker.com/repository/docker/rzrfreefr/webthing-iotjs
)
[![Automated Builds](
https://img.shields.io/docker/cloud/automated/rzrfreefr/webthing-iotjs.svg
)](
https://cloud.docker.com/repository/docker/rzrfreefr/webthing-iotjs/timeline
)
[![Build Status](
https://img.shields.io/docker/cloud/build/rzrfreefr/webthing-iotjs.svg
)](
https://cloud.docker.com/repository/docker/rzrfreefr/webthing-iotjs/builds
)
[![Codacy Badge](
https://api.codacy.com/project/badge/Grade/dd6c1c71603e49cdb1be332681491900
)](
https://app.codacy.com/app/rzr/webthing-iotjs?utm_source=github.com&utm_medium=referral&utm_content=rzr/webthing-iotjs&utm_campaign=Badge_Grade_Dashboard
)
[![FOSSA Status](
https://app.fossa.io/api/projects/git%2Bgithub.com%2Frzr%2Fwebthing-iotjs.svg?type=shield
)](
https://app.fossa.io/projects/git%2Bgithub.com%2Frzr%2Fwebthing-iotjs?ref=badge_shield
)
[![IRC Channel](
https://img.shields.io/badge/chat-on%20freenode-brightgreen.svg
)](
https://kiwiirc.com/client/irc.freenode.net/#tizen
)

[![NPM](
https://nodei.co/npm/webthing-iotjs.png
)](
https://npmjs.org/package/webthing-iotjs
)


[![Presentation](https://image.slidesharecdn.com/webthing-iotjs-20181022rzr-181027220201/95/webthingiotjs20181022rzr-1-638.jpg)](https://www.slideshare.net/slideshow/embed_code/key/BGdKOn9HHRF4Oa#webthing-iotjs# "WebThingIotJs")


## DISCLAIMER: ##

Webthing-iotjs is derived of webthing-node project (supporting Node.js)
but adapted for IoT.js runtime (based on JerryScript engine for constrained devices).

This downstream project plans to keep aligned to upstream and only focus on IoT.js port.

New contributions should be submitted to webthing-node first
and then should land here (once rebased on webthing-node's master branch).


## BASIC USAGE: ##

After installing IoT.js program on your system,
you can get started by running example program


```
iotjs -h

iotjs example/multiple-things.js 
# setting new humidity level: 18.207531485648474

curl T -H 'Content-Type: application/json'  http://localhost:8888/
# [{"name":"My Lamp","href":"/0", (...)  "href":"/1/properties/level"} .. (...) }]

curl T -H 'Content-Type: application/json'  http://$HOSTNAME:8888/1/properties/level
# {"level":42.666}
```
Then thing can be monitored once connected to Mozilla IoT gateway using the Thing Web URL adapter.

Also you can control a "Simplest Thing"
which is just simulating an actuator (LED, switch, relay...).

```
iotjs example/simplest-thing.js 
# Usage:
# 
# iotjs example/simplest-thing.js [port]

curl -X PUT -H 'Content-Type: application/json' --data '{"on": true }' http://localhost:8888/properties/on
# {"on":true}
```

Then this thing can be connected to gateway, and rules configured to use the actuator.


## GUIDE: ##

For more insights and details please follow guide about setting up gateway, iotjs and demos howtos:

* https://github.com/rzr/webthing-iotjs/wiki

[![Demo](https://media.giphy.com/media/1xo9BDFa4B40JPEzZN/giphy.gif)](https://www.slideshare.net/rzrfreefr/webthingiotjs20181022rzr-120959360/19 "webthing-iotjs-20181027rzr")


## REFERENCES: ##

* <https://github.com/mozilla-iot/webthing-node>
* <https://github.com/rzr/webthing-iotjs/wiki>
* <https://github.com/rzr/webthing-iotjs/wiki/GnuLinux>
* <https://cloud.docker.com/repository/docker/rzrfreefr/webthing-iotjs>
* <https://libraries.io/npm/webthing-iotjs/>
* <https://github.com/jerryscript-project/iotjs-modules/pull/3>


## LICENSE: ##

[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Frzr%2Fwebthing-iotjs.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2Frzr%2Fwebthing-iotjs?ref=badge_large)
