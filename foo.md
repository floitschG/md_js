---
---

# foo

<div id='template'></div>
<script>
function reqListener () {
  document.querySelector('#template').innerHTML = this.responseText;
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
