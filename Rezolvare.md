# Soluție

## 1. DNS over HTTPS
Am implementat funcția aici:
```
import requests, json

headers = { 
     "Accept": "application/dns-json"
 }

def getter (_nume): 
     response = requests.get('https://cloudflare-dns.com/dns-query?name=' + _nume + '.com&type=AAAA', headers=headers)
     print (json.loads(response.text)["Answer"][0]['data'])

_nume = input("insert name : ") 
getter(_nume)
```
iar aici e un exemplu de execuție
```python
print("你好吗")
```

## 2. Traceroute

Am implementat soluția iar aici este output-ul:

### Ruta către IP1
```
IP11 - Oraș, Regiune, Țară
IP12 - Oraș, Regiune, Țară
IP13 - Oraș, Regiune, Țară
...
IP1N - Oraș, Regiune, Țară
```

### Ruta către IP2
```
IP21 - Oraș, Regiune, Țară
IP22 - Oraș, Regiune, Țară
IP23 - Oraș, Regiune, Țară
...
IP2N - Oraș, Regiune, Țară
```

### Ruta către IP3
```
IP31 - Oraș, Regiune, Țară
IP32 - Oraș, Regiune, Țară
IP33 - Oraș, Regiune, Țară
...
IP3N - Oraș, Regiune, Țară
```


## 3. Reliable UDP

### Emițător - mesaje de logging
Rulăm `docker-compose logs emitator` și punem rezultatul aici:
```
....
....
....
....
....
```


### Receptor - mesaje de logging
Rulăm `docker-compose logs receptor` și punem rezultatul aici:
```
....
....
....
....
....
```
