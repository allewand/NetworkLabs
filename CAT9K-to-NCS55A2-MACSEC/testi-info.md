**Purpose:**
    Test MACSec functionality between a cat9500 and NCS 5500 series router. Specifically testing if key-server priority configuration has impact on function on the c9500.

**Devices:**
    1. c9500-48Y4C with software 17.6.1
    2. ncs55a2-mod-s with software 25.1.2

**Setup:**
    c9500 tw1/0/45 (port-channel22) <----10G TwinAx---> ncs55a2 te0/0/0/36 (bundle member of be17)
 
 **Results:**
    Successful in that c9500 works with any tested key-server priority.  Tested priorities were *1, 14, 15, 16, 255*
    
    Note: In order for the LACP neighborship to establish across the interface ***ssci-based-on-sci*** was required to be configured in the mka policy of the c9500. This is consistent with previous testing of similar setups.

    