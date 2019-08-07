# react-hook
Hook 就是 JavaScript函数，但是使用它们会有两个额外的规则：  
*只能在函数最外层调用 Hook。  
*不要在循环、条件判断或者子函数中调用。
只能在 React 的函数组件中调用 Hook。不要在其他 JavaScript 函数中调用。

可以在不编写 class 的情况下使用 state 以及其他的 React 特性。
```
官网
https://zh-hans.reactjs.org/docs/hooks-intro.html
```

## useState
通过在函数组件里调用它来给组件添加一些内部 state  
useState 会返回一对值：当前状态和一个让你更新它的函数
```
const [count, setCount] = useState(0);
const [fruit, setFruit] = useState('banana');
const [todos, setTodos] = useState([{ text: 'Learn Hooks' }]);
  return (
    <div>
      <p>you click {count} times</p>
      <button onClick={() => setCount(count + 1)}>Click it</button>
    </div>
  );
```
## useEffect 副作用
跟 class 组件中的 componentDidMount、componentDidUpdate 和 componentWillUnmount 具有相同的用途  
在完成对 DOM 的更改后运行你的“副作用”函数
```
// 在完成对 DOM 的更改后运行你的“副作用”函数
useEffect(() => {
// 使用浏览器的 API 更新页面标题
document.title = `You clicked ${count} times`;
});
```
