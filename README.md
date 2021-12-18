# wp-plugins-dict
A full wp-plugins dictionary


Updated: 18/12/2021

MD5: 256a11d4434bd9e69a4a0c8b1928b235

Fuzz each line in wp-content/plugins/

Dictionary created with the command:

```sh
for i in $(seq 1 1757); do echo -e "Downloaded [$i/1757]"; curl -s -X GET "https://github.com/orgs/wp-plugins/repositories?page=$i" | html2text | grep '\* ###' | grep -oP '\[.*?\]' | awk '{print $2}' >> wp-plugins.txt; done
cat wp-plugins.txt | sort -u | sponge wp-plugins.txt
```
