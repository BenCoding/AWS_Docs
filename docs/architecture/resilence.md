---
hide:
  - tags
---

# Solution Resilency

## Business Continuity (Why?)

## Principles (What?)

1. In this ever changing world resilency is a factor of building solutions

## Options

| $     | Element          | Pros                                                                                                    | Cons                                                                                                     |
| ----- | ---------------- | ------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| $     | Backup & Restore | with relatively small data size and generous RTO, simple backup and restore would work well             | Takes a while to come back online                                                                        |
| $$    | Pilot Light      | very minimal AWS footprint; standby                                                                     | manual intervention for failover, spinning up cloud environment will take min-hours                      |
| $$$   | Warm Standby     | All service are up and ready to accept a failover faster Shadow Environment for Test/Staging            | Resources would need to be scaled to accept load, still requires some envrionment adjustments            |
| $$$$  | Multi-Site(AZ)   | Ready all the time to take full production load, Failover in seconds or less, no or little intervention | Most Expensive, Can be perceived as wasteful; resources just standing around waiting for primary to fail |
| $$$$$ | Multi-Region     | Most reliable as multiple areas of the world will support the solution                                  | Most Expensive, Network infrastructure & pipelines need to be configured for multi-region                |

??? info  "Multi-AZ"
    Multi Site = Multi=AZ = ==Multiple Datacenters==<br />

??? info  "Multi-Region"
    Region 1 (US-EAST = Virgina Area Data centers)<br />
    Region 2 (US-West = Oregon Area Data centers)<br />

---

## Applications (How?)

text

## Reference

### Key Terms
| Acronym           | Term                     | Description                                                                                     |
| ----------------- | ------------------------ | ----------------------------------------------------------------------------------------------- |
| RTO               | Recovery Time Objective  | ==Time== that it takes after a disruption to restore business processed to their service levels |
| RPO               | Recovery Point Objective | Acceptable amount of data loss measure in time                                                  |
| High Availability | Redundancies             |                                                                                                 |
| Fault Tolerance   | Absorb Problems          |                                                                                                 |
| DR                | Disaster Recovery        | ==Act of responding== to an event that threatens continunity                                    |
| BC                | Business Continunity     | Seeks to ==minimize== business activity ==discruption==                                         |

!!! info "Recall"
    RTO ~ T is for Time <br/>
    RPO ~ P is for data that goes "poof"


## Disaster Recovery

## Uptime & Availability Requirements
