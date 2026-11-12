使用"D:\cordis"为基地，做一个类似"D:\dsh"的all in plugin的ai agent，前后端协议以及客户端基本功能参照"D:\Projects\qaqh-backend"；确保前端不知道后端到底是哪个客户端。
自行设计，要求：完全以bun运行ts为主，不允许引入0.00000000001%的nodejs或者bun的nodejs模式。原生ts运行。bun API参考"D:\bun"；环境安装了bun；其他node_module如果想抄近路可以借用dsh或者社区成熟做法。

项目宪法
1. 快速实现功能为主，测试在功能完善后可同步铺开
2. 提交信息已设置--如果无则默认使用初始提交信息
3. 全部插件模块尽可能选择最新版本，可引入rc版本
4. 前端不需要做，只做后端即可，因为我们打算打包成bun二进制作为sidecar
5. 功能侧以qaqh-backend为主，但是不允许实现它的内部冗杂结构--我相信typescript可做更轻更强。
6. loop等可抄deepseek harness，都是MIT
7. 上下文达到30%-40%时可进行handoff，使用qaqh自带的handoff文档，并且工作留痕，留到项目的docs里做类似地图索引等
8. 内存要求尽可能控制在50MB左右，因为是原生bun+ts，可能可控。 如果实在不可控，基线最高是200MB，想尽一切办法磕优化
9. 提交一定要细，每个模块或者每批改动都要提交。
