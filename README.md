# <<React Hooks In Action>> 摘要

### useState更新object 
一般来说， usestate更适合更新单一对象， 例如
```javascript
const [someValue, setSomeValue] = React.useState(1)

// setSomeValue(newvalue)
```

但是如果我们的state是对象呢？

在`someValue`是对象的情况下， 用一下方法调用`setSomeValue`:

```javascript
setSomeValue({newValueObject})
```

会完全替代掉原来的object，哪怕只是更新对象的其中的一个field。在只需要更新对象的部分值的时候， 可以采用下面的方式, 传入一个箭头函数：

```javascript
setSomeValue((state)=> {returm {...state, field:newValue}})
```