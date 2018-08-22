<!SLIDE>

# Cluster

    @@@ render-diagram
    graph LR
      raspi1
      raspi2
      raspi3
      raspi4
      raspi5
      switch
      AP
      router
      internet

      internet =.= router
      subgraph NAT
        router === switch
        router === AP
        switch === raspi1
        switch === raspi2
        switch === raspi3
        switch === raspi4
        switch === raspi5
      end
