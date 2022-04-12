# Learn SE Class Project

## Project System

Remote Patient Monitoring System

## Physical Hierarchy

```{uml}
skinparam linetype ortho

object "Remote Patient Monitoring System" as RPM

object "Enclosure" as Enclosure

object "Sensing SS" as SensingSS
object "Heart Rate Monitor" as HeartRateSensor
object "Blood Oxygen" as PulseOxSensor
object "Blood Pressure" as BloodPressureSensor

object "Computing SS" as ComputingSS
object "Processor" as Processor
object "Firmware" as Firmware
object "I/O" as IO

object "Communication SS" as CommunicationSS
object "Radio Module" as Radio
object "Antenna" as Antenna

object "User Interface SS" as UserInterfaceSS
object "Mobile Device" as MobileUI
object "Mobile Software" as MobileSoftware

object "Cloud SS" as CloudSS

object "Security SS" as SecuritySS

RPM *-- ComputingSS
RPM *-- SensingSS
RPM *-- CommunicationSS
RPM *-- CloudSS
RPM *-- UserInterfaceSS
RPM *-- SecuritySS
RPM *-- Enclosure

ComputingSS *-- Processor
ComputingSS *-- Firmware
ComputingSS *-- IO

SensingSS *-- HeartRateSensor
SensingSS *-- PulseOxSensor
SensingSS *-- BloodPressureSensor

CommunicationSS *-- Radio
CommunicationSS *-- Antenna

UserInterfaceSS *-- MobileUI
UserInterfaceSS *-- MobileSoftware
```
