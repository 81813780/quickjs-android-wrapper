# Change Log

## 0.19.0 *(2023-06-05)*

- 修复 `Attempt to remove non-JNI local reference` 的错误警告
- 修复 `QuickJSWrapper` 析构函数执行时可能会出现的 `use deleted global reference` 异常
- 重构 `JSCallFunction` 的绑定逻辑，避免使用 NewGlobalRef 带来的 global reference table overflow (max=51200) 异常
- 集成 GitHub Action 提升版本发布效率