# Multipath Routing SDN Controller

As seen on articles:

* [Theory](https://wildanmsyah.wordpress.com/2018/01/13/multipath-routing-with-load-balancing-using-ryu-openflow-controller)
* [Testing](https://wildanmsyah.wordpress.com/2018/01/21/testing-ryu-multipath-routing-with-load-balancing-on-mininet)

Multipath routing is a routing method which finds multiple routes to a destination in a network topology. Here is an Implementation of a Multipath Routing SDN Controller in Ryu (OpenFlow1.3).

## quickStart

1. Run mininet topo

```bash
sudo python multipath.py 
```

2. Open another terminal

* ryu multipath Demo

   
    ryu-manager --observe-links ryu_multipath.py
    
*  ryu multipath with Yen's Algorithm (calculate on delay) Demo
    
    
    ryu-manager --observe-links ryu_multipath_yens.py

    
3. Run ping test

```bash
# in Mininet Bash
xterm h1

# in xterm
ping 10.0.0.2
```

