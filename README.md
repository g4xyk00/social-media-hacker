# Social Media Hacker
This repository stores the scripts used to protect user privacy or provide additional features on social media. 

## Facebook
### Remove Facebook Click Identifier (fbclid)
```javascript
//Updated: 30 Jan 2020

var link=document.getElementsByTagName('a');
for (var i = 0; i<link.length; i++){ 
	if(link[i].href.includes("fbclid")){
		if(link[i].href.includes("?u=http")){
				var l = link[i].href.split('%3F')[0];
				link[i].href = l;
		}
	}
}
```
