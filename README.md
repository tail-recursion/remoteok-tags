# remoteok.io tags

Javascript to extract the top tags used for remote developer jobs on remoteok.io

```
tags = $('div[class=tag]').map(function(a,b) { return b.textContent.trim();});

counts = {}
for (i=0; i < tags.length; i++) {
    if (tags[i] in counts) {
        counts[tags[i]]+=1;
	  }
    else {
        counts[tags[i]] = 1;
	  }
}

sorted=[]
for (key in counts) {
  sorted.push([key,counts[key]]);
}
sorted.sort(function(a,b) {return a[1]<b[1]})
```
