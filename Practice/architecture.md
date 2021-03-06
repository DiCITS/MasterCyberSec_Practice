**Course 2017-2018**

[Master CyberSecurity -- University of Granada](http://ucys.ugr.es/master-propio-en-ciberseguridad/)

![LogoHeadMasterCES](https://sites.google.com/site/manuparra/home/logo_master_ciber.png)


[UGR](http://www.ugr.es) | [DICITS](http://dicits.ugr.es) | [SCI2S](http://sci2s.ugr.es) | [DECSAI](http://decsai.ugr.es)

Manuel J. Parra Royón (manuelparra@decsai.ugr.es) & José. M. Benítez Sánchez (j.m.benitez@decsai.ugr.es)


This is the repository for:

## Module: Network and Systems Protection and the course Security in Operating Systems

In this section you can consult the cluster structure to be used in the subject.

### Access to the servers

Two servers will be accessed:

- ```bahia.ugr.es```
- ```docker.ugr.es```

To access the clusters it is necessary to use SSH, if you use Windows, you will need the SSH Putty application or if you use Linux, the ssh command is already integrated.

The connection data to the clusters are:

- Server: ```bahia.ugr.es```   or    ```docker.ugr.es```
- Port: ```22```
- Username: ```<your assigned username>```
- Password: ```<your assigned password>```


To connect by ssh to the servers is used:

```ssh <your assigned username>@bahia.ugr.es```

or 

```ssh <your assigned username>@docker.ugr.es```

Use your assigned password when asked.


### Port diagram enabled for each user:

Each user has a range of 10 TCP ports and 10 open UDP ports on X and Y. These ports will be used to make available services that are enabled from containers or virtual machines.

So ports that are used locally on bahia.ugr.es and ```docker.ugr.es``` for services must always go in the range that has been set for each user.

This is the schema of the port range:

![Schema](https://github.com/DiCITS/MasterCiberSeguridad/blob/master/extras/images/schema2.png?raw=true)

Each user has 10 ports within the range ```14XXX```. The rank assigned to each user will be provided during the practice class, always being a contiguous range of ports.

To access the services, depending on the service we will use the corresponding application. For example, if it is a web service that has been installed/published in port 14067, to see the service, we can see it in the browser: ```http://bahia.ugr.es:14067/``` and this will redirect traffic to the service that is running in that port within ```bahia.ugr.es```.

Table with port assignment:

| 	User      |  bahia.ugr.es   |   docker.ugr.es | docker.ugr.es | docker.ugr.es  | docker.ugr.es  |
|-------------|-----------------|-----------------|---------------|----------------|----------------|
| 	Name      |  external MULTI |   external LDAP | external WEB  | internal WEB IP| internal WEB IP|
| cs_75XXXXX2 |  14000 al 14009	| 	30200,30201   | 30800         | 192.168.10.161 | 192.168.10.141 |
| cs_76XXXXX5 |  14010 al 14019	| 	30202,30203   | 30801         | 192.168.10.162 | 192.168.10.142 |
| cs_76XXXXX2 |  14020 al 14029	| 	30204,30205   | 30802         | 192.168.10.163 | 192.168.10.143 |
| cs_44XXXXX9 |  14030 al 14039	| 	30206,30207   | 30803         | 192.168.10.165 | 192.168.10.144 |
| cs_31XXXXX3 |  14040 al 14049	| 	30208,30209   | 30804         | 192.168.10.166 | 192.168.10.145 |
| cs_14XXXXX8 |  14050 al 14059	| 	30210,30211   | 30805         | 192.168.10.167 | 192.168.10.146 |
| cs_76XXXXX7 |  14060 al 14069	| 	30212,30213   | 30806         | 192.168.10.168 | 192.168.10.147 |
| cs_75XXXXX4 |  14070 al 14079	| 	30214,30215   | 30807         | 192.168.10.169 | 192.168.10.148 |
| cs_75XXXXX6 |  14080 al 14089	| 	30216,30217   | 30808         | 192.168.10.170 | 192.168.10.149 |
| cs_15XXXXX7 |  14090 al 14099	| 	30218,30219   | 30809         | 192.168.10.171 | 192.168.10.150 |
| cs_23XXXXX6 |  14100 al 14109	| 	30220,30221   | 30810         | 192.168.10.172 | 192.168.10.151 |
| cs_14XXXXX5 |  14110 al 14119	| 	30222,30223   | 30811         | 192.168.10.173 | 192.168.10.152 |
| cs_76XXXXX4 |  14120 al 14129	| 	30224,30225   | 30812         | 192.168.10.174 | 192.168.10.153 |
| cs_46XXXXX1 |  14130 al 14139	| 	30226,30227   | 30813         | 192.168.10.175 | 192.168.10.154 |
| cs_20XXXXX7 |  14140 al 14149	| 	30228,30229   | 30814         | 192.168.10.176 | 192.168.10.155 |
| cs_77XXXXX4 |  14150 al 14159	| 	30230,30231   | 30815         | 192.168.10.177 | 192.168.10.156 |

Ports in ```docker.ugr.es```  are redirected to ```389``` and ```636``` (i.e: first ```30208``` -> ```389``` ; second ```30209``` -> ```636```).


### Next steps

Once understood the scheme of work and access to the servers, the next thing to do is work with Docker containers on ```bahia.ugr.es```

[Starting docker](../Docker/starting_docker.md)



