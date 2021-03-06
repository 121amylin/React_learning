#### 01_用CDN引用React 
- [Add React to a Website](https://reactjs.org/docs/add-react-to-a-website.html)

----
#### 02_JSX
- {}，類似ES6的字符串模板。可以在 JSX 的大括號中寫入任何合法的 JavaScript expression
- 可以在屬性中使用大括號來嵌入一個 JavaScript expression。
  例如：style屬性值要用{{}}包起來，style={{color:'red'}}。外層大括號是指指在程式哩，第二層是指object物件
  *不要在嵌入 JavaScript expression 作為屬性的時候同時使用引號或是大括號。

- 可以嵌套使用
- className
- JSX 防範注入攻擊
- JSX 表示物件，JSX 編譯為呼叫 React.createElement() 的程式


----
#### 03_Render Element
- 建立 React 應用程式最小的單位是 element。
  *觀察範例:03_Render_Element.html，Elements 面板DOM更新的狀態
- React 只更新必要的 Element


----
#### 04_Components and Props
- component 就像是 JavaScript 的 function，它接收任意的參數（稱之為「props」）並且回傳描述畫面的 React element。
-  可以使用function 或是 class 來宣告 component
```javascript
      function Welcome(props) {
        return <h1>Hello, {props.name}</h1>
      }
```
   *用class要注意this的使用
```javascript
      class Welcome2 extends React.Component {
        render() {
          return <h1>Hello, {this.props.name}</h1>;
        }
      }
```
- React.Fragment    (Fragment 碎片) 
- Props 是唯讀的，所有的 React component 都必須像 Pure function 一般保護他的 props


----
#### 05_State and Lifecycle
##### 生命週期
- componentDidMount() 方法會在 component 被 render 到 DOM 之後才會執行(component Did Mount 組件確實掛載了)
- componentWillUnmount() 方法會在 component 被銷毀之前執行
- [React与vue的生命周期对照](https://blog.csdn.net/jean850218/article/details/80799497)
- [[Day 08] React lifeCycle 生命週期](https://ithelp.ithome.com.tw/articles/10234998)

##### setState
```javascript=
this.setState((state, props) => {
  return { ...一個新的物件 };
});

```

- [setState注意事項](https://zh-hant.reactjs.org/docs/state-and-lifecycle.html#using-state-correctly)
- [【React.js入門 - 12】 state 與 詳解setState語法](https://ithelp.ithome.com.tw/articles/10219561)

##### component
- component 被定義成 class 而不是 function的時候，render要用自閉合標籤<xxx/>，不能用function
- 05_State and Lifecycle.html


----
#### 06_Handling Events
##### 條件渲染
- if else
- 表達式
- If 與 && 邏輯運算子
- 三元運算子
- return null ， 防止 Component Render
