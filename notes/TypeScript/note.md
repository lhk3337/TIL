# Typescript에서 Object Destructure 와 props 설정 하기

```typescript
interface AppProps {
  name: string;
  age: string;
}
const Info = (props: AppProps) => {
  const { name, age } = props; //구조 분해 할당
  return (
    <>
      <div>My name is {name}</div>
      <div>I am {age} years old.</div>
    </>
  );
};
const App = () => {
  return (
    <>
      <Info name="Holim" age="24" />
      <Info name="ABC" age="20" />
    </>
  );
};
export default App;
```
