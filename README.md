# Banner

Banner is a simple [triweb app](https://triweb.com) (TWA) that allows you to setup a static website directly from your domain control panel.
No external servers or coding experience is needed as **the website theme and texts are configured entirely through the DNS TXT records**.

## Demos

- **Default theme: https://banner.triweb.dev/**
-  https://aerial.banner.triweb.dev/
-  https://dimension.banner.triweb.dev/ 

## Getting Started

To deploy the Banner app on your domain (e.g., `www.mydomain.com`), follow these steps:

1. **Point your domain at a triweb relay server** 
    
    Log in to your domain control panel and set up a CNAME record pointing your domain to a triweb relay server, e.g.,:

    ```
    www.mydomain.com            CNAME   triweb.io.
    ```

2. **Deploy the Banner TWA** 
 
    While still in your domain's control panel, add TXT records under the `_triweb.` subdomain to deploy the Banner app and configure it with the desired theme and text:

    ```
    _triweb.www.mydomain.com    TXT     "app banner/themes/default"
    _triweb.www.mydomain.com    TXT     "[h1] Welcome to my personal website"
    _triweb.www.mydomain.com    TXT     "[p] I love cats and rabbits"
    ```

    For a comprehensive list of themes and their configurations, take a look into the [themes directory](https://github.com/triweb/triweb-apps-banner/tree/master/themes/).


3. **Visit your new website** 
    
    That's all - your new website is published. To see it in action, visit your domain.


## Troubleshooting

Encountering issues? Here are some common problems and solutions:

- **DNS Propagation Delay:** DNS changes might take up to 48 hours to propagate worldwide. If your website isn't accessible immediately, please wait and try again later.
- **Incorrect DNS Configuration:** Ensure that your TXT and CNAME records are correctly set up. Typos or incorrect values can prevent your website from loading. You can online tools such as [mxtoolbox](https://mxtoolbox.com/DNSLookup.aspx) to check DNS records.

## FAQ

**Q: Can I use custom domains with Banner?**  
A: Yes, Banner, just like any TWA, supports custom domains. Just configure your domain's DNS settings as shown in the setup guide.

**Q: How can I change my website's theme?**  
A: To change your theme, update the `_triweb.` TXT record for your domain that begins with `app` keyword with the path to the new theme's manifest file.
