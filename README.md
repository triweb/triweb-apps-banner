# Banner

Banner is a simple [triweb app](https://triweb.com) (TWA) that allows you to setup a static website directly from your domain control panel.
No external servers or coding experience is needed as the website theme and texts are configured entirely through the DNS TXT records.

To deploy the Banner app to your domain (e.g., `www.mydomain.com`), please login to its control panel and add following records:

```
# Point your domain at a selected triweb relay server by creating a CNAME record:
www.mydomain.com            CNAME   triweb.io.

# Deploy the Banner app, and configure it with desired theme and texts
# by adding TXT records under the `_triweb.` subdomain:    
_triweb.www.mydomain.com    TXT     "app https://raw.githubusercontent.com/triweb/triweb-apps-banner/master/manifest.json"
_triweb.www.mydomain.com    TXT     "theme default"
_triweb.www.mydomain.com    TXT     "[h1] Welcome to my personal website"
_triweb.www.mydomain.com    TXT     "[p] I love cats and rabbits"
```

To see all available themes and their slots, see [triweb-apps-banner/themes](https://github.com/triweb/triweb-apps-banner/tree/master/themes/)

To see the Banner TWA in action, visit https://banner.triweb.dev/ 

## Customizations

You can [fork the Banner app repository on GitHub](https://github.com/triweb/triweb-apps-banner/fork), change or customize themes, 
and point your domain at the customized fork like below:

```
www.mydomain.com            CNAME   triweb.io.   
_triweb.www.mydomain.com    TXT     "app https://raw.githubusercontent.com/your-github-username/your-fork-name/master/manifest.json"
```
