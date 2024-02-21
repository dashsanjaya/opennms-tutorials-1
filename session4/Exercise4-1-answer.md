# Exercise 4-1 Answer

[Main Menu](../README.md) | [Session 4](../session4/README.md) | [Exercise-4-1 Answer](../session4/Exercise4-1-answer.md)

This is the answer to [Exercise-4-1](../session4/Exercise-4-1.md)

```
      <!-- Translations FOR CAMERA CONTROLLER EVENTS -->
      <event-translation-spec uei="uei.opennms.org/traps/CHUBB-TVBS-CAMERA-MIB/healthChange/panMotor">
         <mappings>
            <mapping preserve-snmp-data="false">

               <assignment name="nodeid" type="field">
                  <value type="sql" result="SELECT n.nodeid FROM node n  WHERE n.nodelabel = ? ">
                     <value type="parameter" name=".1.3.6.1.4.1.52330.6.2.7.0" matches=".*" result="${0}" />
                  </value>
               </assignment>
            </mapping>
         </mappings>
      </event-translation-spec>
      
```