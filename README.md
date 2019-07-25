## 规范说明

> 为更好的实现前端工程化、组件化、规范化，统一团队开发风格，提升开发人员规范意识，辅助开发团队输出符合规范的高质量项目，降低项目后期维护成本，特制订此文档。<br>本规范文档一经确认, 前端开发人员务必遵守此规范进行项目开发，如有错误或不适用，经团队商议确定后方可升级修订。

## 通用代码规范

-   文档编码统一为 UTF-8
-   代码缩进统一为四个空格
-   命名统一用英文(第三方库除外)
-   命名空间必须取有意义的
-   JavaScript 类、函数、方法代码说明注释规范以 [JSDoc](https://www.html.cn/doc/jsdoc/) 为标准

## 文件规范

-   文件夹及文件名采用英文单词命名规则，多个单词用中划线命名法(`Linux系统是区分大小写的，而 Windows、macOS以及 Git默认是不区分大小写的，为了统一兼容性所以不采用驼峰命名`)
-   图片文件命名多个单词使用下划线命名规则
-   公用 CSS 文件命名为 base.css，公用 JS 文件为 common.js
-   项目中的页面文件以大栏目为单位建文件夹，避免所有页面混在一起
-   文件数量多的目录，必须拆分为更细的子目录结构

## HTML

-   文档头声明统一使用 HTML5 标准
-   style、link 必须放在 head 标签，script 标签优先放 body 结束标签前
-   style、script 标签无需定义 type 标签
-   html5 废弃的标签不建议使用，如\<b>，\<u>，\<i>，\<s>分别被 \<strong> \<ins> \<em> \<del> 替换，(字体图标还是可以用 \<i> 标签)
-   标签名及属性统一使用小写，id 使用小驼峰命名，class 使用中划线命名
-   属性值统一使用双引号包裹
-   标签使用及嵌套需要符合语义化，不可随意嵌套
-   内联元素非特殊场景不可嵌套块级元素
-   殊字符(如<>&空格)尽量使用实体引用，如<(\&lt;)、>(\&gt;)、空格(\&nbsp;)、大空格(\&amp;)
-   button 元素需指明 type 属性值(在 form 表单中如不指明 type，默认为 submit，容易引起意料之外的问题)
-   设置截断或文本溢出隐藏的标签需加 title 属性
-   移动端使用 input 标签合理使用 type，text 之外还有可以选择
-   主体结构需写注释，内容两边必须包含一个空格，格式为\<!-- 内容 -->
-   避免使用相同的 name 和 id
-   属性书写顺序

    -   class
    -   id
    -   name
    -   data-\*
    -   src,for,type,href,value,max-length,max,min,pattern
    -   placeholder,title,alt
    -   aria-\*,role
    -   required,readnoly,disabled

-   功能模块命名

    -   结构

    | 功能             | 命名              | 功能     | 命名         |
    | ---------------- | ----------------- | -------- | ------------ |
    | 页头             | header            | 导航     | nav          |
    | 页面主体         | main              | 主导航   | mainbav      |
    | 页尾             | footer            | 子导航   | subnav       |
    | 容器             | container         | 顶导航   | topnav       |
    | 内容             | content           | 边导航   | sidebar      |
    | 导航             | nav               | 左导航   | leftsidebar  |
    | 侧栏             | sidebar           | 右导航   | rightsidebar |
    | 栏目             | column            | 菜单     | menu         |
    | 页面外围布局宽度 | wrapper           | 子菜单   | submenu      |
    | 左右中           | left right center | 标题     | title        |
    |                  |                   | 摘要     | summary      |
    | 标志             | logo              | 标签页   | tab          |
    | 广告             | banner            | 文章列表 | list         |
    | 登录             | login             | 提示信息 | msg          |
    | 登录条           | loginbar          | 当前的   | current      |
    | 注册             | regsiter          | 小技巧   | tips         |
    | 搜索             | search            | 图标     | icon         |
    | 功能区           | shop              | 注释     | note         |
    | 标题             | title             | 指南     | guide        |
    | 加入             | joinus            | 服务     | service      |
    | 状态             | status            | 热点     | hot          |
    | 按钮             | btn               | 新闻     | news         |
    | 滚动             | scroll            | 下载     | download     |
    | 投票             | vote              | 友情链接 | link         |
    | 合作伙伴         | partner           | 版权     | copyright    |
    | 注册             | regsiter          | 版权     | copyright    |

## CSS 篇

-   禁止使用 ID 或行为 js-前缀的 class 选择器定义样式
-   不要使用元素标签名结合 ID 或 class 进行组合
-   选择器与属性块中间留有一个空格
-   不要随意使用!important
-   不要随意使用\*选择符
-   避免使用无规律的百分比尺寸
-   大模块样式必须添加注释, 小模块适量注释
-   多个选择器公用属性块时每个选择器占一行
-   声明样式每条单独一行
-   属性声明顺序
    -   盒子模型
        -   box-sizing
    -   内容
        -   content
    -   显示属性
        -   display || visibility || opacity
    -   位置属性
        -   position top || right || bottom || left || z-index
    -   浮动属性
        -   float || clear
    -   布局属性
        -   flex-direction || flex-wrap || flex-flow || justify-content || align-items || align-content
        -   grid-columns || grid-rows
    -   多列属性
        -   columns || column-count || column-width || column-span || column-fill || column-gap || column-rule
    -   表格属性
        -   table-layout || border-collapse || border-spacing || caption-side || empty-cell
    -   大小
        -   width || max-width || min-width
        -   height || max-height || min-height
        -   margin
        -   padding
        -   border || border-radius
        -   outline
        -   overflow || clip
    -   文字系列
        -   font
        -   line-height
        -   color
        -   text-overflow
        -   text-align
        -   text-indent
        -   text-transform
        -   text-decoration
        -   text-justify
        -   text-outline
        -   text-shadow
        -   text-wrap
        -   text-emphasis
        -   vertical-align
        -   word-spacing
        -   white-space
        -   letter-spacing
        -   direction
    -   计数器
        -   counter-reset
        -   counter-increment
        -   counter()/counters()
    -   背景
        -   background
    -   其他
        -   list-style
        -   user-select
        -   resize
        -   cursor
        -   animation
        -   transform
        -   transition
        -   perspective
        -   box-shadow

## JavaScript 篇

-   变量声明避免 ES5、ES6 声明混用
-   变量命名采用小驼峰式命名规则，前缀应当是名词，如果是 boolean  类型的变量则使用 is 或 has 开头
-   函数命名规范，采用小驼峰式命名规则，前缀应当是动词，可使用常见动词约定

    | 动词          | 含义                                                | 返回值                                                |
    | ------------- | --------------------------------------------------- | ----------------------------------------------------- |
    | can           | 判断是否可执行某个动作(权限)                        | 函数返回一个布尔值。true：可执行；false：不可执行     |
    | has           | 判断是否含有某个值                                  | 函数返回一个布尔值。true：含有此值；false：不含有此值 |
    | get           | 获取某个值，如果结果为数组，命名最后需加 s 表示复数 | 函数返回一个非布尔值                                  |
    | set           | 设置某个值                                          | 无返回值、返回是否设置成功或者返回链式对象            |
    | load          | 加载某些数据                                        | 无返回值或者返回是否加载完成的结果                    |
    | count         | 获取统计值                                          | 函数返回一个数值                                      |
    | add/insert    | 插入某个值                                          | 无返回值或返回是否设置成功                            |
    | remove/delete | 删除某个值                                          | 无返回值或返回已删除的值                              |
    | update/edit   | 更新某个值                                          | 无返回值或返回更新的值                                |
    | save          | 保存某个值                                          | 无返回值或返回是否设置成功                            |

-   常量命名全部大写字母，使用下划线分割单词，力求语义表达完整清楚，不要嫌名字长
-   类、构造函数命名规范，大驼峰式命名法，首字母大写
-   形参命名规范

    | 类型　          | 　 形参命名 |
    | --------------- | ----------- |
    | 字符串          | str 或 val  |
    | 普通对象        | obj         |
    | 数组对象        | arr         |
    | Json 对象(混合) | data        |
    | 元素对象        | ele         |
    | 数字            | num         |
    | 布尔            | boo 或 flag |
    | 函数            | fun 或 fn   |
    | 请求参数集合    | params      |

-   不要在块内声明一个函数
-   单行代码注释说明规范，双斜线开始，双斜线与注释文字之间保留一个空格
-   多行代码注释说明规范，以/\*开头，\*/结尾
-   switch 的使用

    > 在一个 switch 块内，每个 case 要么通过 break/return 等来终止，要么注释说明程序将继续执行到哪一个 case 为止；
    > 在一个 switch 块内，都必须包含一个 default 语句并且放在最后，即使空代码。

-   eval 函数不要使用，不安全、效率低，使用\$.parseJSON()
-   当判断条件只有 if else 两种情况时可以用三元条件代替
-   表达异常的分支时，少用 if else 方式，使用 return

## Vue

-   参考官方[风格指南](https://cn.vuejs.org/v2/style-guide/)
