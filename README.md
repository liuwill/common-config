# 各种用到的配置文件的模版

> This Project works as a repo for all ide config

## vim配置
需要配置全局的~/.vimrc和当前项目的.ide.vim两个文件，每个项目使用自己单独的配置，全局没有任何额外配置
```
cp ./vim/.vimrc ~/.vimrc
cp ./vim/ide.vim .ide.vim
```

## eslint配置
不同的ide需要安装对应的插件之后才能使用eslint，或者命令行下eslint

### eslint规则
 - http://eslint.org/docs/rules/
 - http://blog.guowenfh.com/2016/08/07/ESLint-Rules/
 - http://www.ruanyifeng.com/blog/2016/07/yaml.html


### Visual Studio Code支持ESLint
 - https://segmentfault.com/a/1190000005030647
 - http://www.cnblogs.com/IPrograming/p/VsCodeESLint.html

### Sublime Text支持ESLint
 - http://www.jianshu.com/p/b2985ba08ec9
 - http://blog.csdn.net/lj745280746/article/details/49658249

### react.eslintrc 是react对应的eslint配置

```
npm install --save-dev babel-eslint eslint-plugin-react eslint
cp ./eslint/react.eslintrc ./eslintrc
```