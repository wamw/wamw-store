# &lt;wamw-store&gt;

`wamw-store` provides simple shared storage.

## Installation

```
bower install --save wamw/wamw-store
```


## Usage

`sample` will automatically save changes to its value.  
other screen/element can use the value via `wamw-store`.

```
<dom-module id="sample">
  <wamw-store name="shared-items-key" value="{{items}}"></wamw-store>
</dom-module>

<script>
  Polymer({
    is: 'sample',
    properties: {
      items: Object
    }
  });
</script>
```

## Event

### change

```
<wamw-store name="key" value="{{val}}" on-change="storeChanged">
<script>
  Polymer({
    is: 'sample',
    properties: {
      val: Object
    },
    storeChanged: function(value) {
      console.log(value);
    }
  });
</script>
```
