# RR0
The RR0 librairies have been built to:
1. implement the [RR0 website](https://rr0.org)
2. allow others to implement their own database/website.

```mermaid
classDiagram
    class RR0["RR0 website"]
    namespace rr0 {
        class common
        class lang
        class time
        class data
        class place
        class org
        class cms
    }
    data --> common
    data --> lang
    data --> time
    data --> fileutil
    RR0 --> cms
    cms --> ssg-api
    class ssg-api
    namespace javarome {
        class fileutil
    }
    ssg-api --> fileutil
```
