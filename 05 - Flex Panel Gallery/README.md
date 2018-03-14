# **05 - Flex Panel Gallery**

## **題目**
製作一個點擊後會展開圖片的效果 

## **Javascript語法**
### **event.propertyName**
可以得知觸發`transitionend`的屬性名稱

```javascript
function toggleActive(e) {
    if (e.propertyName.includes('flex')) {
        this.classList.toggle('open-active');
    }
}
```


## **CSS語法**

### **flex 版面配置**
可以得知觸發`transitionend`的屬性名稱

### **display:flex**
把容器設成flex模式

### **flex: flex-grow flex-shrink flex-basis**
flex的簡寫，第一個為占比、第二個為壓縮值、第三個為默認尺寸

### **justify-content: center**
水平置中

### **align-items: center**
垂直置中

>參閱：[MDN-CSS Flexible Box Layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout)

>參閱：[學習 CSS 版面配置: flexbox](http://zh-tw.learnlayout.com/flexbox.html)


### **:first-child() & :last-child()**
選取first(第一個)/last(最後一個)子元素

ex  

```
<div class="panel panel1">
<p>Hey</p>
<p>Let's</p>
<p>Dance</p>
</div>
```

透過`panel > *:first-child`選取`Hey` 透過`panel > *:last-child`選取`Dance`