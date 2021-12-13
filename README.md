# wp-plugins-dict
A full wp-plugins dictionary


Updated: 28/10/2021

MD5: b602d09ef12e1f4a21f9b11eb3de000e

Fuzz each line in wp-content/plugins/

Dictionary created with the command:

```sh
for i in $(seq 1 1757); do echo "[+] Descargando pagina: $i/1757"; curl -s -X GET "https://github.com/orgs/wp-plugins/repositories?page=$i" | html2text | grep "\* \*\*\*\*" | awk '{print $3}' >> wp-plugins.txt; done
```
