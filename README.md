# 各种用到的配置文件的模版

> This Project works as a repo for all ide config

* [vim配置](#vim)
* [eslint配置](#eslint)
* [babel配置babelrc](#babel)
* [设置环境变量](#env)
* [网络相关配置](#network)
* [travis ci配置](#travis)

## <h2 id="vim">vim配置</h2>

需要配置全局的~/.vimrc和当前项目的.ide.vim两个文件，每个项目使用自己单独的配置，全局没有任何额外配置

```shell
cp ./vim/.vimrc ~/.vimrc
cp ./vim/ide.vim .ide.vim
```

## <h2 id="eslint">eslint配置</h2>

不同的ide需要安装对应的插件之后才能使用eslint，或者命令行下eslint

### eslint规则

* [http://eslint.org/docs/rules/](http://eslint.org/docs/rules/)
* [http://blog.guowenfh.com/2016/08/07/ESLint-Rules/](http://blog.guowenfh.com/2016/08/07/ESLint-Rules/)
* 阮一峰文章[http://www.ruanyifeng.com/blog/2016/07/yaml.html](http://www.ruanyifeng.com/blog/2016/07/yaml.html)


### Visual Studio Code支持ESLint

* [https://segmentfault.com/a/1190000005030647](https://segmentfault.com/a/1190000005030647)
* [http://www.cnblogs.com/IPrograming/p/VsCodeESLint.html](http://www.cnblogs.com/IPrograming/p/VsCodeESLint.html)

### Sublime Text支持ESLint

* [http://www.jianshu.com/p/b2985ba08ec9](http://www.jianshu.com/p/b2985ba08ec9)
* [http://blog.csdn.net/lj745280746/article/details/49658249](http://blog.csdn.net/lj745280746/article/details/49658249)

### react.eslintrc 是react对应的eslint配置

```bash
npm install --save-dev babel-eslint eslint-plugin-react eslint
cp ./eslint/react.eslintrc ./eslintrc
OR
cp ./eslint/mocha.eslintrc.yml ./eslintrc.yml
```

## <h2 id="babel">babel配置babelrc</h2>

在项目根目录创建`.babelrc`文件

参考阮一峰博客[http://www.ruanyifeng.com/blog/2016/01/babel.html](http://www.ruanyifeng.com/blog/2016/01/babel.html)

```bash
cp ./babelrc/es6.babelrc .babelrc
cp ./babelrc/react.babelrc .babelrc
```

## <h2 id="env">设置环境变量</h2>

### 方法一：设置.bashrc

```bash
echo .bashrc > ~/.bashrc

OR

cp .bashrc ~/.bashrc

#关闭重新打开终端
```

### 方法二：编辑/etc/profile

```bash
echo -e "\n#[REDIS_HOME]\nset REDIS_HOME=/usr/home/redis/bin\nexport REDIS_HOME\n" >> /etc/profile

source /etc/profile
#[REDIS_HOME]
set REDIS_HOME=/usr/home/redis/bin
export REDIS_HOME
## 效果

```

## <h2 id="network">网络相关配置</h2>

### 修改系统的hosts配置

系统hosts设置配置文件`/etc/hosts`

```bash
echo -e "\n127.0.0.1 dev-redis\n" >> /etc/hosts
```

## <h2 id="travis">travis ci设置</h2>

github集成的持续集成

```bash
cp ./travis-ci/gradle.travis.yml .travis.yml

OR

cp ./travis-ci/node.travis.yml .travis.yml
```

## nginx

## redis

## supervisor

## editorconfig
