# 每日任务模板

### 今日计划

#### 复习回顾

- **时间**: 早晨或开始学习前
- **内容**: 快速浏览昨日学习笔记，重点回顾不熟悉的概念。

#### 新知学习

- **上午**
    - **主题**: 写剩余项目管理系统,批量删除信息, 修改信息, 新增信息功能

- **下午**
    - **主题**: 1.修复接口 '批量删除和新增信息' bug; 2.观看spring boot 分页工具的使用
    - **资源**: JavaWeb开发教程，学习教程链接[https://www.bilibili.com/video/BV1m84y1w7Tb?spm_id_from=333.788.videopod.episodes&vd_source=73ea134d3c57c2bf237a1ff495211c28&p=140] 

#### 实践操作

#### 总结归纳

- **晚上**
    - **形式**: 学习日记或电子笔记
    - **内容**:

    1. 引入依赖: pagehelper-spring-boot-starter
    2. 配置参数(可选)
        - 如: pagehelper: page-size-zero: true // pageSize为0时，不分页查询所有结果
          helper-dialect: mysql // 指定数据库类型
          reasonable: true // 这个配置项开启了合理化分页参数,
          当设置为true时，如果pageNum小于1，它会将pageNum设置为1；如果pageSize小于1，它会将pageSize设置为默认值
          support-methods-arguments: true //
          这个允许PageHelper支持通过Mapper接口方法的参数来传递分页参数。这意味着你可以在Mapper接口的方法中直接传递Page对象或者分页参数，而不需要在每个查询前都显式地调用PageHelper.startPage方法。
          params: count=countSql // 这个配置项用于指定PageHelper在生成分页SQL时使用的参数
    3. 使用 PageHelper.startPage 方法如:
        - PageHelper.startPage(pageNum, pageSize);
          List<Entity> list = yourMapper.selectByExample();
          PageInfo<Entity> pageInfo = new PageInfo<>(list);
    4. 获取分页信息： PageInfo 对象包含了分页查询的所有相关信息，例如当前页码、总页数、总记录数等。可以通过 PageInfo
       的各种方法来获取这些信息
        - 如:private int pageNum; // 当前页
          private int pageSize; // 每页数量
          private int size; // 当前页的数量
          private int startRow; // 当前页面第一个元素在数据库中的行号
          private int endRow; // 当前页面最后一个元素在数据库中的行号
          private long total; // 总记录数
          private int pages; // 总页数
          private List<T> list; // 结果集
          private int prePage; // 前一页
          private int nextPage; // 下一页
          private boolean isFirstPage; // 是否为第一页
          private boolean isLastPage; // 是否为最后一页
          private boolean hasPreviousPage; // 是否有前一页
          private boolean hasNextPage; // 是否有下一页
          private int navigatePages; // 导航页码数
          private int[] navigatepageNums; // 所有导航页号
          private int navigateFirstPage; // 导航条上的第一页
          private int navigateLastPage; // 导航条上的最后一页
    5. 分页查询语法
        - 参数1:起始索引=(页码-1)*每页展示记录数
        - 参数2:查询返回记录数=每页展示记录数

    6. @RequestParam
        - required:指定参数是否必须。如果设置为 true，则请求中必须包含这个参数，否则会抛出异常。如果设置为 false，则参数是可选的。
        - defaultValue: 可以来设置参数的默认值. 如: @RequestParam(defaultValue ="10")Integer pageSize)
    7. @JsonFormat(pattern = "yyyy-MM-dd") 可指定返回的时间参数类型

    8. 数据库中 'Date' 类型字段在实体类中应该写成 'LocalDate' 类型
    9. 复习的英语单词:53词
       - university
       - reporter
       - museum
       - cinema
       - hospital
       - straight
       - ask
       - early
       - helmet
       - must
       - attention
       - schedule
       - dictionary
       - have a class
       - do morning exercises
       - clean a room
       - go for a walk
       - coach
       - go shopping
       - take
       - dancing
       - take a dancing class
       - when
       - usually
       - Spain
       - late
       - a.m.
       - p.m.
       - why
       - last
       - sound
       - also
       - busy
       - need
       - letter
       - island
       - always
       - go swimming
       - win
       - spring
       - summer
       - autumn
       - park
       - season
       - picnic
       - pick
       - pick apples
       - snowman
       - make a snowman
       - best
       - snow
       - good job
       - because

### 已完成任务

- [x] 批量删除和新增信息代码
- [x] 观看spring boot 分页工具的使用

### 明日计划

- 复习英语单词

## 学习资源与工具

- **工具**: IntelliJ IDEA, Git, GitHub, B站
