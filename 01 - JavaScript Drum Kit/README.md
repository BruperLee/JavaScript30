# **01 - JavaScript Drum Kit**

## **題目**
透過JS使鍵盤按下對應的字母按鍵後，播放出對應按鍵的聲音，並同時產生一個特效

以下為學習到的新知

## **JavaScript語法**
### **element.classList**
回傳element的class值(陣列)，  
以下方法`add()`及`remove()`

```
classList.add('aaa', 'bbb', 'ccc'); //新增多個className
classList.remove('aaa', 'bbb', 'ccc'); //移除多個className
```
如果已經存在/不存在的className則會被忽略。
>其他方法:  
`toggle()`偵測是否存在這個className，存在則刪除/不存在則新增  
`contains()`偵測是否存在這個className, 返回true/false  
參閱：[MDN-Element.classList](https://developer.mozilla.org/en-US/docs/Web/API/Element/classList)

### **HTMLmediaElement(audio)**
HTML的`audio`標籤，在HTML放置如下標籤指定音源

```
<audio src="sound/boom.wav"></audio>
```
透過javascript來操作：  
`element.play()`:進行播放  
`element.currentTime`:指定播放秒數  
範例中使用`currentTime`是為了有連續觸發聲音的效果 
>參閱：[MDN-HTMLMediaElement](https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement)

### **transitionend**
當 transition 完成時會觸發此 event     
若 transition 在執行中被中斷(意指 transition 沒有真正完成)則不會觸發。

```
addEventListener('transitionend', removeTransition);
```

>參閱：[MDN-Event transitionend](https://developer.mozilla.org/en-US/docs/Web/Events/transitionend)


### **箭頭函式(Arrow Function)**
ES6的新語法

```javascript
//傳統寫法
let func1 = function(arg) { console.log('Hi, ' + arg); };
//箭頭函式寫法
let func2 = arg => console.log('Hi, ' + arg);
//補充:如果該function沒有參數要傳，要帶空括號如下
let func3 = () => console.log('Hi');
```
>參閱：[MDN-Arrow functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)

### **template literals**
模板文字，  
利用`` ` `` - 反引號(back-tick)或稱重音符(grave accent)來組合字串，  
在範圍內可利用`${}`加上變數操作

例如原本的字串+變數組合寫法：

```javascript
let str = '<div data-key="' + key + '">' +
         '<button>click me</button>' +
         '</div>';
```
改用template string來做只要

```javascript
let str = `<div data-key="${key}">
         <button>click me</button>
         </div>`;
```
用`` ` ``包住字串，利用`${}`來包變數  

>參閱：[MDN-Template literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals)

## **CSS語法**
### **display:flex**
CSS3的排版語法

```css
.keys {
    display: flex; /*要使用flex要在元素內先宣告flex*/
    flex: 1; /*這是一個簡寫，全部為flex: flex-grow｜flex-shrink｜flex-basis*/
    min-height: 100vh; /*vh代表view height, 百分比呈現*/
    align-items: center; /*宣告為flex後才有效的屬性，垂直置中*/
    justify-content: center;/*宣告為flex後才有效的屬性，水平置中*/
}
```
>參閱：[MDN-flex](https://developer.mozilla.org/en-US/docs/Web/CSS/flex)