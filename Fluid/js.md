## Fluid variables inside JS code
If you want to use fluid variables inside a javascript block you have to wrap the plain JS code with CDATA.

```html
<script type="text/javascript">
// <![CDATA[
(function(){
// ]]>
var name = '{user.name}';
// <![CDATA[
console.log('Hello, ' + name);
// some more js code here...
})();
// ]]>
</script>
```
