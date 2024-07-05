# wp-plugins-dict
A full wp-plugins dictionary


Updated: 07/05/2024

Fuzz each line in wp-content/plugins/

Dictionary created with the command:

```sh
for i in $(seq 1 1757); do echo -e "Downloaded [$i/1757]"; curl -s -X GET "https://github.com/orgs/wp-plugins/repositories?page=$i" | html2text | grep -oP '(?<="name":").+?(?=","ow)' >> wp-plugins.txt; done
cat wp-plugins.txt | sort -u | sponge wp-plugins.txt
```
