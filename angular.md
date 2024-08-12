# Angular

Angular.json

写真表示の設定

```typescript
"assets": [
              "src/favicon.ico",
              "src/assets"
            ],
            "styles": [
              "src/styles.css"
            ],
            "scripts": []
          },
```

## 装饰器

### @Input

@Input装饰器用于将数据从父组件传递到子组件。它允许子组件接收来自父组件的输入。这是一种实现组件之间单向数据流的方式

*只能从父组件流向子组件*

https://angular.cn/guide/components/inputs

#### input

https://angular.cn/api/core/input#

### @Output

#### $event

# Angular @Output 事件流程

1. **用户交互**
   - 用户与子组件(`UserComponent`)进行交互

2. **子组件触发事件**
   - `onSelectUser()` 方法被调用
   - 执行 `this.select.emit(this.id)`

3. **事件发射**
   - `select` EventEmitter 发出事件
   - 用户 `id` 作为事件数据被传递

4. **父组件捕获事件**
   - 父组件模板中的 `(select)="onSelectedUser($event)"` 捕获事件

5. **父组件处理事件**
   - `AppComponent` 的 `onSelectedUser(id: string)` 方法被调用
   - 接收到的 `id` 被打印到控制台

6. **数据流向**
   - 信息从子组件流向父组件
   - 保持单向数据流原则