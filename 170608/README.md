### React.js setState({})
```
// 1.
this.setState(prevState => ({
  value: prevState.value - 1
}));


// 2.
this.setState({
  value: this.state.value - 1
});
```

2번의 경우 연속 호출시 버그 발생.
setState() 가 Queue 에 state 변경점을 저장해놨다가 한번에 호출 하는 방식
