# vue-playlist

#2.0安装
vue-cli安装
1.安装node
2.cmd中测试node和npm版本
3.node -v  (版本号在6.9以上)
4.npm -v(版本3.10以上)
5.npm install --global vue-cli(安装全局的cli)
6.装好后测试vue --version
7.装好cd到对应的项目文件夹下
8.vue init webpack vue-playlist(项目名称)
9.cd到 项目文件夹下
10.npm install
11.npm run dev

> A Vue.js project


## vue笔记

``` bash
#vue cli3.0文档
https://cli.vuejs.org/guide/

#创建vue-ant项目
#vue-ant地址 https://vue.ant.design
npm install -g @vue/cli
vue create xxx
npm i --save ant-design-vue
import Antd from 'ant-design-vue'
import 'ant-design-vue/dist/antd.css'
Vue.use(Antd)


###笔记
#命令行
git remote add origin https://github.com/leonjun/vue.git
git push -u origin master

#轮播插件
npm install --save swiper

#sass
npm install --save-dev sass-loader
npm install --save-dev node-sass

#webpack.base.conf.js的rules里面添加配置
{
  test: /\.sass$/,
  loaders: ['style', 'css', 'sass']
}

#字体图标
npm install font-awesome --save-dev
import 'font-awesome/scss/font-awesome.scss'

#mint-ui
npm i mint-ui -S
import MintUI from 'mint-ui'
import 'mint-ui/lib/style.css'
Vue.use(MintUI);
需要禁用客户端的放大缩小  user-scalable=0



#axios跨域 vue.config.js
module.exports = {
    devServer: {
        //port: 8080,
        proxy: {
            '/api': {
                target: 'https://www.apiopen.top/',  // target host
                //ws: true,  // proxy websockets 
                changeOrigin: true,  // needed for virtual hosted sites
                pathRewrite: {
                    '^/api': ''  
                }
            },
        }
    }
};

#如遇无法git
git ssh-keygen -t rsa -C "我的SSH密钥"
#去掉路径#号
mode: "history",

```
##css笔记
```bash
#css三角形
display: inline-block;
content: " ";
height: 18rpx;
width: 18rpx;
border-width: 4rpx 4rpx 0 0;
border-color: #c7c7cc;
border-style: solid;
background: linear-gradient(#ad6e01,#e79302);#渐变

```
##小程序笔记
```bash
#转换字体图标
https://transfonter.org/
#小程序
navigateBack   {delta：层数} 关闭当前页面返回
redirectTo 关闭当前页面跳转 非tabbar
navigateTo 保留当前页面跳转 非tabbar
relanuch 关闭所有页面跳转

```
##数据库笔记
``` bash
#添加字段：
alter table 表名 add 字段名 类型
#删除字段：
alter table 表名 drop column 字段名
#修改表名
alter table table_name rename table_new_name;
#查询排序
select * from xxx(表名) order by 键 desc
#删除某条数据
delete from table where  key='' 
```


For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
