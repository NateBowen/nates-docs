# Learn SE Class Project

## 01 Project System

Remote Patient Monitoring System

*Quick Notes*:

Reference: FDA Video "Home Use Medical Devices: New Risks" (2011)

What happens when:

The power goes out?
Other environmental factors are present?
* Pets
* Children
* Patients are left alone?
* Loud noises (TV?)

## 02 Physical Hierarchy

```{admonition} Problem
Using your chosen system, create a physical hierarchy of its critical elements.
```

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

object "Power SS" as PowerSS
object "Batteries" as Batteries
object "Charging Devices" as Chargers

object "Security SS" as SecuritySS

RPM *-- ComputingSS
RPM *-- SensingSS
RPM *-- CommunicationSS
RPM *-- CloudSS
RPM *-- UserInterfaceSS
RPM *-- SecuritySS
RPM *-- Enclosure
RPM *-- PowerSS

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

PowerSS *-- Batteries
PowerSS *-- Chargers
```

## 03 Mission Description

```{admonition} Problem
Using your chosen system, draft a story/walkthrough of the primary mission for your system.
For added value, draft stories/walkthroughs of secondary, tertiary and even adversarial missions for your system.
Typically, the more, the better.
```

### System Onboarding

The Remote Patient Monitoring System (RPM) is installed in a patient's home.

The RPM is turned on and a mobile device application connects to the RPM to begin system onboarding.
The networking information is entered into the mobile device application and the data link to the cloud services are confirmed.

The RPM sensors are placed on the patient by a health care provider.
The RPM sensors gather initial data and are tested for expected functionality.
Upon successful calibration, the data is stored securely on the RPM and the mobile device application signals that onboarding is complete.

### System Charge

The mobile device application detects that the RPM needs to be charged and issues a notification on device and in the cloud.
The RPM sensors are removed from the patient and the RPM is placed into its charging apparatus.
When the RPM is sufficiently charged, the mobile device issues a notification on device and in the cloud.
The RPM sensors are placed on the patient and calibration is checked.

### Data Analytics

Patient data is analyzed to provide...

### System Offboarding

The RPM is removed from a patient's home.

## 04 Users and Stakeholders

```{admonition} Problem
 Think about and list as many users and stakeholders for your system.
```

Primary:

* Patient
* In-home care provider
* System technician
* Remote health care provider

Secondary:

* Development engineers
* Maintenance and support engineers
* Owner (may not be the patient)
* Manufacturers
* Third-party data services
* Adversaries (hackers)

## 05 Context Diagram

```{admonition} Problem
Using the mission description(s) and stakeholder list from the previous exercises,
create a system level context diagram.
```

```{uml}

```
