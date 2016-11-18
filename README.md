# Overview

RocketChat charm

# Installation

You'll need a working juju installation.

To deploy the charm you need:
```
juju deploy mongodb
juju deploy rocketchat
```

If deploying from the git repo run: `juju deploy ./ --series trusty`

Next you need to add a relationship between rocketchat and the mongo instance

`juju add-relation mongodb rocketchat`

And finally you need to expose RocketChat

`juju expose rocketchat`

