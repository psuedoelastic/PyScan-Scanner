![Pyscan](http://s28.postimg.org/usbam0pe5/pyscan.png)
## REQUIRE
* urllib2
* BeautifulSoup
* requests

## START
* Change database information
```php
$bdd = new PDO('mysql:host=localhost;dbname=pyscan', 'user', 'password');
```
* Update a Python gate
```python
panel_url = "http://localhost/pyscan/"
gate_scraper = "cmd/gate.php"
gate_scanner = "cmd/scan.php"
gate_vuln = "cmd/vuln.php"
gate_payload = "panel/api/payload.php"
gate_database = "panel/api/database.php"
```
## Upload the .SQL
```shell
mysql -u username -p database_name < file.sql
```
## Login 
![Pyscan login](http://s7.postimg.org/a7r15d2az/login2.png)
```shell
Username: root
password: toor
```

## Make payload !
![Pyscan payload](http://s22.postimg.org/6wklvc00x/payload.png)
## Test payload
```shell
python pyscan.py -u "http://exemple.com/id=2" -s -p PAYLOAD_ID
```
## Test all payload
```shell
python pyscan.py -u "http://exemple.com/id=2" -s --all
```
## Import mass link
![Pyscan import](http://s7.postimg.org/4fqgeubjf/import.png)
## Test all link
```shell
python pyscan.py --database
```