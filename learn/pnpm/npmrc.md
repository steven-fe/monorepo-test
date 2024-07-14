## hoist

默认值：`true`

默认情况下：将所有的依赖提升到`node_modules/.pnpm/node_modules`目录。`node_modules`中的依赖包可以软链接这个目录。

## public-hoist-pattern

默认值：`['*eslint*', '*prettier*']`

默认情况下，将会将`eslint`和`prettier`依赖包安装到顶部`node_modules`（root node_modules directory）。

## shamefully-hoist

默认值：`false`

如何设置为`true`，则会将所有的依赖包安装到顶部`node_modules`（root node_modules directory）。
