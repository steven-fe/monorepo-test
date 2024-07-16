在`pnpm-workspace.yaml`中定义`catalog`。

作用：将`monorepo`代码仓库中多个子项目的依赖，提升到`pnpm-workspace.yaml - catalog`中集中统一管理，便于日后将多个子项目依赖版本的升级。

## 例子：

pnpm-workspace.yaml

```yaml
packages:
  - packages/*

# Define a catalog of version ranges.
catalog:
  react: ^18.3.1
  redux: ^5.0.1
```

packages/example-app/package.json

```json
{
  "name": "@example/app",
  "dependencies": {
    "react": "catalog:",
    "redux": "catalog:"
  }
}
```

publish 后的 packages/example-app/package.json

```json
{
  "name": "@example/app",
  "dependencies": {
    "react": "^18.3.1",
    "redux": "^5.0.1"
  }
}
```
