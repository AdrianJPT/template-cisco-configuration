****************************************
    CISCO TEMPLATE CONFIGURATION
****************************************

##### RIP ##########

router rip
network 192.168.1.0   #Network you want to share
network x.x.x.x
network x.x.x.x
no auto-summary


##### OSPF ######

router ospf 1
network x.x.x.x wildcard area x
network 10.20.20.0 0.0.0.3 area 0
router-id 1.1.1.1                   #UNIQUE IDENTIFIER FOR THE ROUTER
**#no auto-summary by default (OSPF doesn't support auto-summary)**

##### EIGRP #####

router eigrp 1    # N° de proceso
network x.x.x.x x.x.x.x area 0
network 10.20.20.12 0.0.0.3 area 0
no auto-summary

***************************************************************************************************
      Redistribution of routes between differents Routing Protocols in ONE ROUTER
***************************************************************************************************


router eigrp 2020  #speficy the process ID 
redistribute ospf 1 metric 1500 10 255 1 1500    #speficy the process ID 

router ospf 1      #speficy the process ID 
redistribute eigrp 2022 subnets     #speficy the process ID 



