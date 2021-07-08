## useEffect life Cycle

```javascript
useEffect(() => {
  // 모든 값의 변화에 인지함
  console.log("component did mount");
});
useEffect(() => {
  // 최초에 한번 인지
  console.log("component did mount");
}, []); //ComponentDidMount

useEffect(() => {
  // name 값의 변화에만 인지함
  console.log("component did update");
}, [name]); //componentDidUpdate
```
