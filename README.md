### apiserver-gin
基于gin的api服务端脚手架。
对于新手学习使用gin搭建go服务端项目，熟悉项目规划，了解生产项目结构和细节设计感觉会有很大帮助。
本项目依然是按照单体项目布局来做的，后面会完善多模块项目推荐的布局(比如一个项目既有app端server，又有管理后台server)。

### 待完善
- Dockerfile

### 目前整合组件及实现功能
- 加入viper使用yml配置文件来配置项目信息，启动时指定不同的配置文件
```html
eg.
go run main.go -c test.yml
```
- 集成gorm 并自定义JsonTime 解决Json序列化和反序列化只支持UTC时间的问题（可以自定义时间格式）  
提供了部分demo，可以按照demo在项目中直接使用。
- 整合redis，开箱即用，通过yml文件对redis进行配置
- 整合zap，lumerjack 完善日志输出，日志分割。
- 集成jwt，提供demo代码，自定义授权失败成功等的响应格式，跟全局api响应格式统一
- 实现session管理
- md5, bcrypt和uuid生成工具包
- 应用统一封装响应格式，参照笔者参与的大型项目经验和规范。
- 项目全局错误码封装，go的error处理。
- 应用统一入口日志记录中间件实现，日志log_id透传。
- 添加makefile，可以使用make 命令进行编译，打包。
- 完善了项目版本管理，使用make命令编译后的项目可以方便跟踪线上发布版本
- 其他一些坑，后续会出一系列配置与使用教程。
### 项目使用文档 ，完善中......，敬请期待。
