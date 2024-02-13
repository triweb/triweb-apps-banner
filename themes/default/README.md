# Default Theme

**Theme identifier:** `default`

A minimalistic theme that can be used to build simple webpages.

![Default theme](preview.png)

## Live demo

You can access a preview of this theme on [banner.triweb.dev](https://banner.triweb.dev/).<br/>
[Click here](https://mxtoolbox.com/SuperTool.aspx?action=txt%3a_triweb.banner.triweb.dev&run=toolpage) to see the live TXT records that are used for this preview. 

## Example domain configuration

```
www.mydomain.example            CNAME   triweb.io.

_triweb.www.mydomain.example    TXT     "app banner/themes/default"

_triweb.www.mydomain.example    TXT     "meta-title Triweb Banner - default theme"
_triweb.www.mydomain.example    TXT     "meta-description Publish simple websites directly from your domain control panel in minutes!"

_triweb.www.mydomain.example    TXT     "[h1] Hello world!"
_triweb.www.mydomain.example    TXT     "[h2] This website was set up and launched directly through the domain control panel %F0%9F%AA%84"

_triweb.www.mydomain.example    TXT     "[p][0] If you have a domain name, you can also use [Triweb Banner](https://triweb.com/apps/banner) to create, publish, and edit basic websites directly from your domain control panel, **without the need for web servers, hosting providers, or any coding kn" "owledge.** Plus, an amazing feature - once someone visits your site, it becomes accessible even in offline mode."
_triweb.www.mydomain.example    TXT     "[p][1] [Take a look](https://mxtoolbox.com/SuperTool.aspx?action=txt%3a_triweb.banner.triweb.dev&run=toolpage) at how this website was made - everything, including its theme, texts, and buttons was set up using [DNS TXT records](https://en.wikipedia.org/w" "iki/TXT_record)."

_triweb.www.mydomain.example    TXT     "[btn][0] Set up on your domain"
_triweb.www.mydomain.example    TXT     "[btn][0] href=https://triweb.com/apps/banner style=primary"
_triweb.www.mydomain.example    TXT     "[btn][1] See available themes"
_triweb.www.mydomain.example    TXT     "[btn][1] href=https://github.com/triweb/triweb-apps-banner/tree/master/themes/"

```

## Available customization slots

This theme has following customization slots:

### h1

**Name:**       h1<br/>
**Value:**      A main heading that appears above the text<br/>
**Options:**    `color` (default black)<br/>
**Example TXT records:** 
```
"[h1] color=black"
"[h1] Hello World!"
```

### h2

**Name:**       h2<br/>
**Value:**      A sub-heading that appears above the text<br/>
**Options:**    `color` (default black)<br/>
**Example TXT record:** ```"[h2] Welcome to my website color=#f0f0f0"```

### p

**Name:**       p<br/>
**Value:**      One or more paragraphs of text formatted with markdown<br/>
**Options:**    - none -<br/>
**Example TXT records:** 
```
"[p][0] A first paragraph of text."
"[p][2] A second paragraph with **bold** text and a [link](/)."
```

### btn

**Name:**       btn<br/>
**Value:**      One or more action buttons that appear below the text<br/>
**Options:**    `href` (the target URL), `style` (one of: primary, secondary)<br/>
**Example TXT records:**
```
[btn][0] View my GitHub profile
[btn][0] href=https://github.com/ style=primary
[btn][1] Send me an email
[btn][1] href=mailto:me@mydomain.example
```

### sidebar

**Name:**       sidebar<br/>
**Value:**      The look and feel of the sidebar<br/>
**Options:**    `color` (background color), `img` (URL of the image)<br/>
**Example TXT records:**
```
[sidebar] color=red img=https://somedomain.example/image.png
```
