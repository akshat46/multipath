# Multipath Routing SDN Controller

As seen on articles:

* [Theory](https://wildanmsyah.wordpress.com/2018/01/13/multipath-routing-with-load-balancing-using-ryu-openflow-controller)
* [Testing](https://wildanmsyah.wordpress.com/2018/01/21/testing-ryu-multipath-routing-with-load-balancing-on-mininet)

Multipath routing is a routing method which finds multiple routes to a destination in a network topology. Here is an Implementation of a Multipath Routing SDN Controller in Ryu (OpenFlow1.3).

## v3

Contains python3 version of the project. Do the following to convert anymore files: 

```bash
# install 2to3 package
pip install 2to3

# cd to project root
cd multipath

# convert and save to directory v3/
2to3 -n -W --add-suffix=3 --output-dir=v3 *.py
```

## quickStart

1. Run mininet topo

```bash
sudo python multipath.py <(option. default: localhost)remote IP address>
```

2. Open another terminal

```bash   
# ryu multipath Demo
ryu-manager --observe-links ryu_multipath.py

# ryu multipath with Yen's Algorithm (calculate on delay) Demo
ryu-manager --observe-links ryu_multipath_yens.py
```
    
3. Run ping test

```bash
# in Mininet Bash
xterm h1

# in xterm
ping 10.0.0.2
```
