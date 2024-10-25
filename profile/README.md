The RR0 librairies have been built to:
1. implement the [RR0 website](https://rr0.org)
2. allow others to implement their own database/website.

```mermaid
classDiagram
    namespace rr0 {
        class RR0["rr0.org"] {
            files.html
            build()
        }
        class common
        class lang
        class time {
            Level2Date
            Level2Duration
            Level2Interval
            TimeContext
        }
        class data {
            RR0Data
            RR0Event
        }
        class place {
            Place
            PlaceLocation
        }
        class org {
            Organization
            Country
            Region
            City
            Company
            University
            Foundation
        }
        class cms {
            build()
        }
    }
    data --> common
    data --> lang
    data --> time
    data --> fileutil
    RR0 --> cms
    cms --> common
    cms --> lang
    cms --> time
    cms --> place
    cms --> org
    cms --> ssg-api
    place --> common
    place --> lang
    place --> data
    class ssg-api
    namespace javarome {
        class fileutil {
            FileContents
        }
    }
    ssg-api --> fileutil
```
