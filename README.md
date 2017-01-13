# netease-music-juke-box

一个高仿网易云音乐Web端音乐播放器

# 网易云音乐API
 - 获取某个用户的歌单    
 http://music.163.com/api/user/playlist/?uid=40652589&limit=1000&offset=0
 - 获取某个歌单的详细信息  
 http://music.163.com/api/playlist/detail?id=4000000
 - 搜索功能     
 http://music.163.com/api/search/get/ & http://music.163.com/api/suggest/web


# 技术概述
 - HTML5
 - LESS
 - JavaScript
 - ES6/ES2015
 - Babel
 - Webpack
 - jQuery
 - Gulp

# 安装步骤
## 1. clone项目
    $ git clone https://github.com/maybeShuo/netease-music-juke-box.git
## 2. 进入项目根目录
    $ cd netease-music-juke-box
## 3. 安装package.json中的devDependencies
    $ npm install -dev

# 运行步骤
## 1. 启动webpack-dev-server
    $ webpack-dev-server
## 2. 在浏览器中访问http://localhost:8080

# Glup如何运行
    $ gulp dev


# PS
如果安装了1.15.0+版本以上的webpack-dev-server,请更改webpack.config.js中的proxy：
~~~JavaScript
    proxy: {
            "/api/*": {
                "target": {
                  "host": "music.163.com",
                  "protocol": 'http:',
                  "port": 80
                },
                ignorePath: false,
                changeOrigin: true,
                secure: false,
            }
    }
~~~
