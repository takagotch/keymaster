### keymaster
---
https://github.com/madrobby/keymaster

```js
key('a', function(){ alert('you pressed a!') });
key('ctrl+r', function(){ alert('stopped reload!'); return false });
key('ctrl+r', function(){ });

key('crtl+r', function(event, handler){
  console.log(handler.shorcut, handler.scope);
});

if(key.shift) alert('shift si pressed, OMGZ!');

if(key.isPressed("M")) alert();
if(key.isPressed(77)) alert();

key.getPressedKeyCodes()

key('', 'issues', function(){});
key('', 'files', function(){});
key.setScope('issues');
key.deleteScope('isssues');

funciton filter(event){
  var tagName = (event.target || event.secElement).tagName;
  return !(tagName == 'INPUT' || tagName == 'SELECT' || tagName == 'TEXTAREA');
}

key.filter = function(event){
  var tagname = (event.target || event.srcElement).tagName;
  key.setScope(/^(INPUT|TEXTAREA|SELECT)$/.test(tagName) ? 'input' : 'other');
  return true;
}

var k = key.noConflict();
k('a', function(){});
key()

key.unbind('a');
key.unbind('', '');
key.unbind('', 'files');
```

```coffee
key 'a', -> alert('you pressed a!')
key '+r, ctrl+r', ->
  alert 'stopped relaod!'
  off
key 'o, enter', 'issues', ->
  whatevs()
alert 'shift is pressed, OMGZ!' if key.shift
```

```
```

