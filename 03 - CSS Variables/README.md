# **03 - CSS Variables**

## **題目**
製作一個即時調整內距、模糊、邊框色。  

## **Javascript語法**
### **dataset**
用`dataset`可以取出對象的`data-*`屬性，也等同於`getAttribute`

```javascript
<div id="test" data-sizing="px"></div>
document.querySelector('#test').dataset.sizing // 輸出px
document.querySelector('#test ').getAttribute('data-sizing'); // 輸出px
```
### **style.setProperty()**

```javascript
style.setProperty('padding', '25px');
/* 等同於 */
style.padding = '25px';
```

>參照:[MDN-setProperty](https://developer.mozilla.org/en-US/docs/Web/API/CSSStyleDeclaration/setProperty)
