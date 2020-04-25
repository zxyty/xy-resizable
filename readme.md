### 使用方式
```jsx
<Resizeable
    showGuideLine
    direction={["right", "bottom"]}
    enableResizing
    getGuideLineParent={() => document.body}
>
    <div style={{ width: "80%", margin: "10px 0", background: "yellow" }}>
    test
    </div>
</Resizeable>
```

### API
```ts
interface ResizeableProps {
  direction?: DirectionType | Array<DirectionType>;
  // 显示resize指导线
  showGuideLine?: boolean;
  // 指定resize指导线挂载的dom元素
  getGuideLineParent?: (currDom: HTMLElement) => any;
  onResizeEnd?: (
    resizedX: number,
    resizedY: number,
    initWidth: number,
    initHeight: number,
    currDom: HTMLElement
  ) => void;
  // 是否resize的同时修改dom size
  enableResizing?: boolean;

  children?: React.ReactNode;
}
```