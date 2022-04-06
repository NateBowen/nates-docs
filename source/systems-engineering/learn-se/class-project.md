# Learn SE Class Project

## Project System

Remote Health Monitoring System

## Physical Hierarchy

```{uml}
skinparam linetype ortho

object "Automated Teller" as ATM
object "Frame/Chassis" as Frame
object "Computing SS" as ComputingSS
object "Cash Management SS" as CashSS
object "Communication SS" as CommunicationSS
object "User Interface SS" as UserInterfaceSS
object "Security SS" as SecuritySS

ATM *-- Frame
ATM *-- ComputingSS
ATM *-- CashSS
ATM *-- CommunicationSS
ATM *-- UserInterfaceSS
ATM *-- SecuritySS
```
