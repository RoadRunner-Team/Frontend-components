## 컴포넌트 구조

- Atomic Design
- 참고 : https://ui.toast.com/weekly-pick/ko_20200213/



## 사용하기

### 1 . 컴포넌트의 propTypes 확인하기

[Component].jsx 파일 하단에 보면 컴포넌트로 넘겨야하는 props를 정의해놓음.

- [Component].propTypes : 어떤 props를 넘겨야하는지 정의

- [Component].defaultProps : propTypes에 정의되어있는 props를 넘기지 않았을때의 기본값을 정의

MainButton의 경우 props로 color를 넘길 수 있음. (아래 코드 참고)

```
MainButton.propTypes = {
  color: PropTypes.oneOf(["default", "primary", "disabled", "pending"]),
};
MainButton.defaultProps = {
  color: "default",
};
```



### 2. 컴포넌트 사용하기

```
import MainButton from "@atoms/Buttons/MainButton";

<MainButton color="primary">버튼</MainButton>
```

