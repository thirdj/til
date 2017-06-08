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

setState에서 2번처럼 하는 건 setState 안에 props를 안 쓰거나 한 함수 안에서 setState를 연속호출만 하지 않으면 별 문제는 없음.

setState 은 비동기적 함수라서 연속으로 호출할경우에는 value 를 확신할수없어
1번 방식이 맞음.

공식 문서에서도 1번 방식을 추천 함.
