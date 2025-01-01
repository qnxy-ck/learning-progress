# 每日任务模板

### 今日计划

#### 复习回顾

- **时间**: 早晨或开始学习前
- **内容**: 快速浏览昨日学习笔记，重点回顾不熟悉的概念。

#### 新知学习

- **上午**
    - **主题**: 继续昨天写spring boot + vue3的web界面,未完成功能有批量删除,增加信息的功能,修复删除单个数据bug
    - **目标**: 完成功能有批量删除,增加信息的功能

- **下午**
    - **主题**: 观看myBatis
    - **资源**:
      myBatis，学习教程链接[https://www.bilibili.com/video/BV1MT4y1k7wZ?spm_id_from=333.788.videopod.episodes&vd_source=73ea134d3c57c2bf237a1ff495211c28]

#### 实践操作

- **任务**: 实现一个简单的ArrayList增删改查功能模拟。

#### 总结归纳

- **晚上**
    - **形式**: 学习日记或电子笔记
    - **内容**: myBatis
    - 注意:

    1. 在resources创建mapper时需要将 '.'替换为 '/'如: com/cyh/mapper
    2. 特殊字符处理
        - 2.1 转义字符 如 : '<' 改成 '%lt;'
        - 2.1 CDATA区
    3. 参数占位符 使用 "#{}" 不会出现sql注入问题
    4. 动态条件查询
       4.1 <if test=""></if>逻辑表达式要写在test=""中 如<if test="status != null">status = #{status}</if>(
       status是varchar类型), 存在的问题:第一个条件不需要逻辑运算符
       4.2<where></where> 可解决if标签会出现的错误
        5. choose (when, otherwise):选择 类似于Java 中的 switch 语局
           5.1 如<choose><!--相当于switch--
           <when test="status != null"><!--相当于case-->
           status = #{status}
           </when>
           <when test="companyName != null and companyName !='!"> company_name like #{companyName}</when>
           </choose>
        6. 添加数据时主键回显 <insert id="add" useGeneratedKeys="true" keyProperty="id"></insert>
        7. <set></set>修改时使用
        8. 批量删除
           <foreach collection="array" item="id" separator=","(separator间隔符) open="("(open开始位置拼接) close=")" (
           close结束位置拼接)> #{id}   </foreach>
           mybatis会将数组参数，封装为一个Map集合
           *默认:array = 数组
           *使用@Param注解改变map集合的默认key的名称(如: @Param("ids") int[] ids)

### 已完成任务

- [x] 复删除单个数据bug

### 明日计划

- **预习明日主题**: Java IO流基础
- **实践安排**: 实现文件读写操作的代码练习
- **理论深入**: 阅读《Java核心技术卷I》第10章

## 学习资源与工具

- **教材**:《Java核心技术卷I》
- **在线课程**: [Coursera Java编程专项课程](https://www.coursera.org/specializations/java-programming)
- **工具**: IntelliJ IDEA, Git, GitHub
