# ili-web-service-docker

```
curl -v -X POST -F "file=@data/SO_ARP_SEin_Konfiguration_20250115.ili" http://localhost:8080/ili2c/api/compile 
curl -v -X POST -F "file=@data/SO_ARP_SEin_Konfiguration_20250115.ili" http://localhost:8080/iliprettyprint/api/prettyprint 
curl -v -X POST -F "file=@data/SO_ARP_SEin_Konfiguration_20250115.ili" http://localhost:8080/iliprettyprint/api/uml -o foo.png 
```

```
curl -v -X POST -F "file=@data/SO_ARP_SEin_Konfiguration_20250115.ili" https://ili.sogeo.services/api/compile 

```asdf