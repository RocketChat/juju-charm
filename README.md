# Overview

RocketChat charm

# Installation

You'll need a working juju installation.

You'll need a MongoDB juju charm.

The existing juju charm available in the Charm Store contains a MongoDB version that is too old (2.4) and cannot be used with the latest versions of Rocket.Chat.

Instead, clone, build and deploy this work in progress MongoDB juju charm instead (for 2.6.10 version of Mongo)

https://github.com/marcoceppi/layer-mongodb

To deploy the Rocket.Chat charm you need to first have deployed the mongodb charm above.

Then:

```
juju deploy rocketchat
```

If deploying from the git repo run: `juju deploy ./ --series trusty`

Next you need to add a relationship between rocketchat and the mongo instance

`juju add-relation mongodb rocketchat`

And finally you need to expose RocketChat

`juju expose rocketchat`

