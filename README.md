# Ant_Forest  

![AF_Pic](https://github.com/SuperMonster003/Ant_Forest/blob/master/Github_Material/AF_Pic_361%C3%97103.png?raw=true)
###### 蚂蚁森林能量收取工具 (基于Auto.js)

******
### 使用说明
******
1. 下载"Ant_Forest_Project"目录  
2. 将目录中的全部文件 (或目录本身) 放置于手机存储    
3. 使用"Auto.js"运行"Ant_Forest.js"文件  
4. 欢迎使用并反馈
> 手机存储目录推荐"Auto.js"默认可识别目录 (如 `/sdcard/Scripts/` 或 `/sdcard/脚本/` )  
"Auto.js"版本不低于 `4.1.0 Alpha5`

******
### 功能简介
******
* 收取好友能量
* 帮收好友能量 (可开关)
* 收取自己的能量 (可在指定时间范围内循环收取)
* 能量收取结果统计/展示 ~~(floaty方式)~~  
* 多任务排队机制  
** 代码灵感来源 [e1399579](https://github.com/e1399579/autojs)  
* ~~多语言支持/智能切换~~
* 黑名单机制  
** 黑名单自动管理  (由"能量保护罩"触发)  
** ~~用户自行管理黑名单  (可从列表选取而无需手动输入)~~  
** 黑名单解除剩余时间提示 (控制台)  
* ~~配置向导~~  
* 信息加密存储  
** 自动生成"密文映射"字典文件  
** 使用密文存储账户信息/解锁密码等敏感信息  
** 请妥善保管"密文映射"字典文件
* ~~账户智能切换~~  
~~** 防止其他账户 (如支付宝小号) 意外收取 (需录入主账户信息)~~  
~~** 信息录入向导~~  
~~** 主账户收取完毕可自动切换之前的账户 (如果有此账户信息)~~  
* 自动解锁屏幕  
** 解锁模块来源 [e1399579](https://github.com/e1399579/autojs)  
** 可结合 `Xposed Edge Pro` 或 `Tasker` 实现定时启动  
~~** 可通过配置向导页面实现解锁密码录入~~  
* 适应恶劣条件  
** 脚本在恶劣条件下仍可正常运行或识别异常 (网络条件较差/意外来电/支付宝异常退出/广告弹窗等)  
* ###### 其他功能详见[使用说明书](https://github.com/SuperMonster003/Ant_Forest/blob/master/Ant_Forest_Project/Documents/Ant_Forest_User_Manual.md)


******
### 版本历史
******
  
# v1.1.1
##### 2019/03/20 
* `修复` 文件依赖关系
* `修复` 密文工具
* `优化` 文件结构

# v1.1.0
###### 2019/03/19 - 脚本可用性暂未测试 
* `新增` 自动检测/生成/引用本地"密文映射"文件
* `移除` 指定账户智能切换功能 (暂时关闭)
* `修复` 收取完毕返回好友列表时 当前屏幕信息没有及时处理即开始滑屏
* `灵动` 账户智能切换 (账户录入 已录入账户的选择/信息更新) 
* `灵动` 使用密文解析工具时若发现"密文映射"文件异常 及时报错 

# v1.0.0
###### 2019/03/19 - 此版本依赖设备本地密文映射文件 因此暂不可用
* `新增` 自动收取好友能量 (基于Auto.js控件/颜色识别)
* `新增` 自动帮收好友能量
* `新增` 可在指定时间范围内不间断检测自己的能量 (感谢 [e1399579](https://github.com/e1399579/autojs))
* `新增` 自动解锁屏幕 (感谢 [e1399579](https://github.com/e1399579/autojs))
* `新增` 脚本排队机制 (感谢 [e1399579](https://github.com/e1399579/autojs))
* `新增` 脚本运行结束后智能关屏 (感谢 [e1399579](https://github.com/e1399579/autojs))
* `新增` 脚本运行结束后智能保留/结束APP进程
* `新增` 自动切换APP语言 (目前暂时统一切换为简体中文)
* `新增` 若当前用户不是指定账户 (主账户) 则自动切换为主账户 (需录入账户信息)
* `新增` 可显示/关闭能量罩的剩余时间 (因黑名单系统未完成 暂未投入使用)
* `新增` 可显示/关闭收取/帮收好友能量的详细信息
* `新增` 可分别显示收取自己能量的总数与收取好友能量的总数
* `新增` 将Auto.js的日志保存在指定的文件中 (Auto.js v4.1.0版本以上)
* `优化` 精简部分无用的方法
* `优化` 脚本部分参数可供用户自行配置 (目前只可在脚本文件中配置)
* `优化` 部分参数值可以自动修正/修复 
* `优化` 恶劣条件下 (不稳定的互联网连接等) 的脚本稳定性 
* `优化` 收取能量时 先保证能量收取成功 然后立即返回 (稳定性/高效率) 
* `优化` 帮收能量时 若能量帮收成功 立即返回 (高效率) 
* `优化` 线程循环展开列表 节约滑动好友列表时"加载中"的时间 (高效率) 
* `优化` 线程监视好友列表底部 一旦进入屏幕 立即停止列表滑动 (高效率) 
* `优化` 优化好友列表滑动的稳定性 
* `灵动` 能量罩用户黑名单功能实现 (目前只是空壳)
* `灵动` 脚本使用说明文档 (包含使用细节和注意事项)
* `灵动` ~~自动生成并引用本地"密文映射"字典~~ v1.1.0
* `灵动` ~~本地"密文映射"加解密工具~~ v1.1.0
* `灵动` 主要方法的JSDoc注释
* `灵动` 可用于配置脚本的UI界面 (高交互性)
* `灵动` 帮收好友能量增加精准性及效率
* `灵动` 登录主账户之前记录当前用户信息 脚本结束后恢复登录 (需录入账户信息)
* `灵动` 额外文件的生成/存取不受机型限制
* `灵动` 语言智能切换且可供用户配置
* `灵动` 使用Floaty方式替代Toast消息显示
* `灵动` 好友数量小于10的异常处理
* `灵动` shell强制结束APP的替代方案 (避免经常出现的几秒钟黑屏)
