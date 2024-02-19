# Example Configurations

In this folder you will find example configuration files. 
Try the exercises first and then compare your work with these example.

The files are always called the following names, but the contents vary `CHUBB-TVBS-CAMERA-MIB.events.xml` `eventconf.xml`

## Events generated directly from the CHUBB-TVBS-CAMERA.mib

[events-generated-from-mib](../example-configurations/events-generated-from-mib/) These files are the result of following the steps to simply parse the CHUBB-TVBS-CAMERA.mib

To load into the running container do the following 

```
cd minimal-minion-activemq
docker compose cp ./example-configurations/events-generated-from-mib/eventconf.xml horizon:/usr/share/opennms/etc/
docker compose cp ./example-configurations/events-generated-from-mib/CHUBB-TVBS-CAMERA-MIB.events.xml horizon:/usr/share/opennms/etc/events/

# send an event to reload the daemon
docker compose exec horizon /usr/share/opennms/bin/send-event.pl uei.opennms.org/internal/reloadDaemonConfig -p 'daemonName Eventd' 
```

## Simple set of alarms created from the CHUBB-TVBS-CAMERA.mib

[simple-alarms-from-mib](../example-configurations/simple-alarms-from-mib/) These files contain a first cut at alarm definitions 

To load into the running container do the following 

```
cd minimal-minion-activemq
docker compose cp ./example-configurations/simple-alarms-from-mib/eventconf.xml horizon:/usr/share/opennms/etc/
docker compose cp ./example-configurations/simple-alarms-from-mib/CHUBB-TVBS-CAMERA-MIB.events.xml horizon:/usr/share/opennms/etc/events/

# send an event to reload the daemon
docker compose exec horizon /usr/share/opennms/bin/send-event.pl uei.opennms.org/internal/reloadDaemonConfig -p 'daemonName Eventd' 
```
