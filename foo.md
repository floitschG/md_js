---
---

# foo

<div id='template'></div>
<script>
var url = window.location.pathname
var id = /\/([^\/]+)\.html$/.exec(url)[1];
document.title = id;

function reqListener () {
  var data = this.responseText;
  var json = JSON.parse(data);
  document.querySelector('#template').innerHTML =
    "template: " + json[id].template_EN + "</br>" +
    "type: " + json[id].type + "</br>"
//    + "<iframe src='https://github.com/floitschG/md_js/wiki/" + id + "' >" +
//    "your browser doesn't support iframes</iframe>";
}

var oReq = new XMLHttpRequest();
oReq.addEventListener("load", reqListener);
oReq.open("GET", "ids.json");
oReq.send();
</script>

## Examples

```
foo(2, 3, 5);
```

## Stackoverflow links
[http://www.example.com]
