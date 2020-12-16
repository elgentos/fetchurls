# fetchurls cache warmer

For the full README, see [here](https://github.com/adamdehaven/fetchurls).

This is a modified fork so we can (ab)use the `-e` flag to pass our own regex for everything, not just for file extensions.

Usage in the crontab for our clients (with use of the modified `-e` flag to skip `customer` and `checkout` links); 

```
# Cache warming
0 6 * * * bash fetchurls.sh -d https://domainhere.com -l /data/web/crawler -e "customer|checkout" -n
````
