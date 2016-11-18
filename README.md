# Overview

RocketChat charm

# Installation

You'll need a working juju installation.

To deploy the charm you need:

juju deploy mongodb
juju deploy rocketchat

Next you need to add a relationship between rocketchat and the mongo instance

juju add-relation mongo rocketchat

And finally you need to expose RocketChat

juju expose rocketchat

