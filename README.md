# Facebook
### Remove Facebook Click Identifier (fbclid)
```javascript
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
