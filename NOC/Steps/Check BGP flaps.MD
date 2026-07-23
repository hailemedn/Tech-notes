2026-07-23
Tags: #cmg 

## Check BGP flaps

Look for flap timing and note down there svc

```sh
show router bgp summary all
```

Filter that specific router

```sh
show router 1001 bgp summary
```

find the neighbor by pressing tab after the following cmd

```sh
show router 1001 bgp neighbor
```


Check whether it's active and established for all neighbors

```sh
show router 1001 bgp neighbor 4200010002 | match State 
```

