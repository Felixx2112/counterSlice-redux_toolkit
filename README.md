## Reducers

- la mot function co ban

```c
const initValue = { value: 0 };
const rootReducer = (state = initValue, action) => {
switch (action.type) {
case "INCREMENT":
return {
...state,
value: state.value + 1,
};

    default:
      return state;

}
};
```

## **LUU Y:**

- Gia tri cua state moi luon luon duoc tinh toan dua tren gia tri cua state truoc do. State la tham so thu nhat con action la tham so thu 2(neu co)

- Khong bao gio duoc thay doi gia tri cua state hien tai ma chung ta se thuc hien dong lenh 'immutability',ma chung ta tao mot phien ban copy va cap nhap gia tri mong muon

_ACTIONS_

`Action la mot object co cac thuoc tinh: type, payload`

```c
const INCREMENT = {
type: "INCREMENT",
// payload: 1,
};
```

_Action creators_

```c
const incrementCreator = (data) => {
return {
type: "INCREMENT",
payload: data,
};
};

incrementCreator(10);
```

_DISPATCH_

`La mot function`

```c
const dispatch = (action) => {};

dispatch(incrementCreator(10));
```
