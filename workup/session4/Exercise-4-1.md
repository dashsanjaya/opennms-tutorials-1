# Exercise 4-1 

[Main Menu](../README.md) | [Session 4](../session3/README.md) | [Exercise-4-1](../session4/Exercise-4-1.md)

In this exercise we will translate received traps into a set of modified traps using the [event translator](https://docs.opennms.com/horizon/33/operation/deep-dive/events/event-translator.html).

Imagine that multiple cameras from the examples in [Session 3](../session3/README.md) are controlled from a single `camera-controller`. 
The cameras themselves are not directly manageable from OpenNMS but the `camera-controller` monitors the cameras and will send traps to OpenNMS if it detects any problems with any of the cameras.

The operator wishes to show the status of all the cameras on a map, so they need to be represented as OpenNMS nodes which may or may not have alarms associated with them.
The camera nodes are themselves not monitored by OpenNMS, so they are in effect `dummy nodes` which can have alarms associated with them. 

Each camera has a unique `cameraIdentifier` to identify it in the `camera-controller` and on OpenNMS.

The traps sent from the `camera-controller` follow exactly the same pattern as the traps in the previous exercise but they all have an extra string varbind which contains the cameraIdentifier.

You need to design an event translator configuration which will translate the new traps into the old events with the correct nodeid corresponding to the 
`cameraIdentifier` in the traps.
