# docsify搭建指南

    这里是docsify搭建指南

[>>返回首页](/README.md)


# Step 1 快速入门
1. 官网下载 nodejs  http://nodejs.cn/download/

2. 打开命令行工具 输入命令  nmp i docsify-cli  
    (i 是安装的意思)

3. 切换到桌面文件目录 
    输入doscify init ./docs
    创建docs文件夹

4. vs code 打开目录

5. 开始写文档 
    打开README.md 输入文字 

6. 在命令行输入进入桌面目录，输入
    docsify serve docs/
    得到 http://localhost:3000   地址
    支持热更新，修改内容网页也随之变化

# Step 2 多页文档_1_链接
1. 新增 文件 名字.md     
   一个 # 表示一个一级标题 写入内容

2. 页面跳转  语法：  [>>操作指南](/guide.md)
    相应也跳转回去 （注意换行）  做好多页面博客
    （但是跳来跳去很麻烦，所以要有侧边栏）
# Step 3 多页文档_2_侧边栏

1. 要先创建 _sidebar.md

2. 侧边栏格式为  *[想显示的文字](/文档名)

3. 但还没效果 需要去 index.html 实现 loadSidebar : true

# Step 4 多页文档_3_多级目录

1. 在 sidebar写下  * 前端技术
                     * [想显示的文字](路径名)
                     * [echarts](01/echarts/)

2. 创建两个文件夹01 02 分别代表前端技术和服务器端技术
    创建文件夹Javascript  echarts

3. javascript文件夹下创建 README.md 文件 输入内容，但网页却没有显示

4. 官方文档 定制侧边栏  显示目录 小节 告诉我们要设置一个
    subMaxLevel: 2     表示二级标题

# Step 5 导航栏

1. 配置文件 DOCS 目录下新增 _navbar.md  文件
    文件内写入  _sidebar.md 一样的内容 语法非常类似
  
2. index.html  中写入  loadNavbar : true
    效果，右上角顶部导航栏 效果与侧边栏非常类似


# Step 6 封面

1. 首先通过  _coverpage.md  文件声明封面的具体内容
    复制官方内容
 
2. 在index.html   
    第一行是背景图片，输入自己喜欢图片的路径
    第二行是自己的文字和标题

    最下面会提供两个按钮，跳转页面去

3. index.html 加入 coverpage : true
    ctrl s 效果出来了

    第一个按钮可以设置到GitHub 仓库
    第二个按钮可以设置到笔记首页
    复制一下   一级标题  # Headline粘贴过来
    效果就都ok了
    
    默认下封面和首页是同时出现的
    设置只封面  index.html 加入  onlyCover : true  (or    false)

    封面和首页变成单独页面  跳转不能README一级标题了
    需要写上具体文件名称  [Get Stared](README)

