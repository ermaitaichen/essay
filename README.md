1. 如何查看  android sdk 安装的路径
如果 android sdk已经被设置为环境变量 则可以通过命令行 set | findstr /I android 来查看
如果没有加入环境变量 则可以在我的电脑中搜索  platform-tools platform-tools 是android sdk 必不可少的文件 找到他 就找到了 android sdk 的路径了
2. React native 中的样式
React native 中并没有完整的实现 css 而是通过 javascript 来为应用添加样式
声明样式
StyleSheet.create({/* 样式 */});
使用样式
所有的核心组件都可以接受 style 属性，还可以接受数组形式的多个 style
3. React native 路由
社区主要推荐的方案是一个单独的导航库 react-navigation
下载&安装: 可以通过  yarn 和 npm 进行安装
yarn add react-navigation
npm install --save react-navigation
初始化路由栈
通过 createStackNavigator 这个类创建 路由栈
如何切换页面
跳转到新的页面
This.props.navigation.navigate( /* name of the page */ );
向  navigator stack 中推入新的 page
This.props.navigation.push( /* name of the page */ );
回退
This.props.navigation.goBack();
在路由跳转时如何传递参数 param
如何传递
This.props.navigation.navigate( ‘RouteName’, /* params */ );
如何获取
This.props.navigation.getParam( paramName, defaultValue );
如何设置
This.props.navigation.setParam(paramName, value);
如何配置导航的样式
 Static navigationOptions = {
Title: ‘’
}
4. 问题混总
unable to load script from assets 'index.android.bundle' make sure your bundle is packaged correctly or you are running a packager server

React-Native Android真机测试 -unable to load script from assets 'index.android bundle'...
解决 https://blog.csdn.net/sinat_34380438/article/details/77648476?locationNum=9&fps=1




React native tab navigator 切换时出现问题
Attempted to transition from state ‘RESPONDER_INACTIVE_PRESS_IN’to’RESPONDER_ACTIVE_LONG_PRESS_IN’,

是 debug js 模式造成的 关闭即可



5. Github 使用教程
常用命令
git add .
他会监控工作区的状态树，使用它会把工作时的所有变化提交到暂存区，包括文件内容修改(modified)以及新文件(new)，但不包括被删除的文件。
git add -u
他仅监控已经被add的文件（即tracked file），他会将被修改的文件提交到暂存区。add -u 不会提交新文件（untracked file）。（git add --update的缩写）
git add -A
是上面两个功能的合集（git add --all的缩写）
git init
初始化仓库
git status
查看仓库的状态
Git commit
保存仓库的历史记录
Git commit -m
本次提交描述
Git log
查看提交日志
Git diff
查看更改前和更改后的差别
Git branch
显示分支一览 可以将分支名列表显示 同时可以确认当前所在分支
Git checkout -b
创建、切换分支
Git merge
合并分支
Git push
将本地代码推送至远程仓库
Git pull
同步远程代码
Git remote
管理主机名
例如 git remote add origin https://..............
意思是添加一个远程仓库 代号是 origin 地址是 https: //


备注：具体可以参见这个网址的教程
https://blog.csdn.net/yanyan42/article/details/79697788
Git 提交代码五部曲
Git clone
Git status 查看当前状态
Git add .或 git add XXX
Git commit -m “”
Git pull 远程主机名 远程分支名
Git push 远程主机名 远程分支名

使用 github 过程中遇到的一个问题
首先 我在本地创建了一个仓库 (git init ) 之后我在 github 上创建一个远程仓库 我在本地仓库中添加文件 之后执行 git add .  git commit  git remote add origin https://  git push origin master 命令 保存
这是因为需要先 git pull 一下 然后再 git push 具体可以参考 https://www.cnblogs.com/code-changeworld/p/4779145.html

6. react-native-tab-navigator
底部导航栏




