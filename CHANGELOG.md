
## 更新记录

### 2020-10-27 更新

版本：1.0.1 内测版

1. 新增页面解释类型文档可用
2. 新增原型图类型文档可用
3. 新增区域编辑导航跳转可用

### 2020-10-28 更新

版本：1.0.4 内测版

1. 新增详细使用文档
2. 文件位置和弹窗参数可以用户自定义
3. 修复弹窗文档未销毁问题
4. 修复弹窗 z-index 不够导致被覆盖
5. 修复没有#app 导致无法挂载

### 2020-11-08 更新

版本：1.0.8 内测版

1. 弹窗位置改为 13 种
2. 弹窗位置自定义
3. UI 改版优化
4. 弹窗可拖拽缩放
5. 去掉部分自定义参数
6. 修复弹窗不跟随滚动
7. 修复 z-index 层级和目标 dom 不一致

### 2020-11-26 更新

版本：1.1.3 稳定版

1. 可以自定义判断环境的函数
2. 修复面板 url 跳转问题，缓存当前状态
3. 重构 ui 面板 service、controller、modal
4. 删除自定义 dom 接入(使用概率推算极低)
5. 去掉弹窗尺寸自定义，使用最小弹窗大小策略
6. 修复同一 dom 同一类型弹窗位置重叠问题
7. 修改接入方式和说明文档

### 2020-12-04 更新

版本：1.1.4 正式版

1. 更新说明文档
2. 自定义环境函数返回值简写兼容处理

### 2020-12-09 更新

版本：2.0.0 内测版

1. 新增操作手册功能
2. 新增用户引导功能
3. 新增初始化参数：是否遮罩
4. 新增用户引导自定义方法
5. 更新说明文档

### 2020-12-15 更新

版本：2.0.1 内测版

1. 操作手册改为全局存储和读取，新增热点标签，选中跳到该操作手册第一步所在页面
2. 用户引导从面板移除
3. 用户引导通过 EasyDoc.xxx 调用，用户可控制上一步下一步是否显示，新增关闭用户引导 API
4. 更新说明文档

### 2020-12-23 更新

版本：2.0.2 内测版

1. 新增操作手册热门目录页面
2. 操作手册改为全局存储和读取，新增热点标签，选中跳到该操作手册第一步所在页面
3. 操作手册跳转之后保持状态
4. hover 触发

### 2020-12-30 更新

版本：2.0.3 内测版

1. 权限属性(auth)之前必须是全大写'DEVELOPMENT' | 'TEST' | 'PRODUCTION'，现在可以使用兼容小写 'dev' | 'test' | 'pro'
2. 操作手册添加权限属性(auth)限制
3. 一个 docId 在一个页面默认只会查询出一个 dom 节点并生成弹窗，如果想要查询出多个 dom 节点，请设置该节点属性 noUnique=true
4. 新增操作手册全局 API EasyDoc.jumpManualStep 和 EasyDoc.manualNextStep，用于代码控制操作手册的跳转和下一步操作，减轻用户操作负担
5. 引入方式调整，不再使用 new EasyDoc，改为 EasyDoc.init()
6. 操作手册的每个步骤可能没有 dom 节点，只有说明，所以 nodes 属性改为可选属性
7. 初始化参数 env 的值修改为 字符串或函数，去掉'NODE_ENV' 和 'URL', 默认使用 URL 判断，具体请看上面使用说明
8. 操作面板新增拖拽和钉住功能，拖出来固定高度 50%，只有操作手册的情况下高度全部上移
9. 在操作步骤中增加属性 linkManualName，实现从操作手册跳转到其他操作手册功能

### 2020-01-04 更新

版本：2.0.5 正式版

1. 拖拽操作优化
2. 页面说明类型可使用 html
3. jumpManualStep 参数修改 public static jumpManualStep(stepIdx: number, manualName?: string, timeout = 1000): void
4. 新增全局 api limitManualJumpStep(stepIdx: number, limitManualName: string, timeout = 1000)

### 2020-01-05 更新

版本：2.0.6 优化版

1. docId、doc-id、docid、data-docId、data-doc-id、data-docid 可以兼容使用
2. doc、edit 类型的节点可以自定义 width、height

### 2020-01-05 更新

版本：2.0.7 优化版

1. 页面刷新时，操作手册复现动画两次优化为一次
2. 文本内 a 链接颜色改为主题色橙色
3. 拖拽文字修改并移到右下角，动画优化

### 2020-01-05 更新

版本：2.0.9 优化版

1. 拖拽优化

### 2020-01-08 更新

版本：2.0.10 优化版

1. 不选中操作手册时操作手册被遮挡修复
2. 用户引导被初始化冲突修复
3. 操作手册为空时有空白修复

### 2020-01-11 更新

版本：2.0.12 优化版

1. dev 环境读取 manuals 也会存入缓存
2. 操作手册高度问题修复

### 2020-01-20 更新

版本：2.0.13 优化版

1. auth 判断逻辑修改
2. 增加首次加载小标标提示（页面重新加载提示）
3. 增加路径黑名单

### 2021-02-03 更新

版本：2.0.14 优化版

1. 增加首次加载小标标提示（session 存储提示）

### 2021-05-21 更新

版本：2.1.3 优化版
1. 可视化配置json
2. 所有节点添加可选zIndex属性，用于指定层叠顺序

### 2021-06-28 更新

版本：2.1.9 优化版
1. 页面文档类型左侧标题样式调整
2. 新增项目文档类型
3. 节点收缩后不随下拉滚动而自动展开
4. 新增请求地址前缀参数

### 2021-07-03 更新

版本：2.1.10 优化版
1. 新增参数hasEasyDocJSON hasManualsJSON hasProjectsJSON，在没有对应的json时赋值false,可以避免控制台network请求报错
2. 简化接入初始参数；去掉pageInterval
3. 右上角删除用户引导
4. 更新接入说明

### 2021-07-05 更新

版本：2.1.12 优化版
1. 项目文档或页面文档过宽改为随页面大小自适应
2. 项目文档增加版本参数，修改版本重新弹窗
3. 新增Easydoc宣传链接

### 2021-11-19 更新
版本：2.2.0 优化版
1. vue2重写dom操作
2. 用户引导bugfix
3. 加载报错new Error改成 console.error
