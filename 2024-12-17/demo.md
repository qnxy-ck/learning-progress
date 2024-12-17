- ## 上午

Pinia是替代了Vuex的状态管理工具
1.提供更加简单的API(去掉了 mutat@ners
2.提供符合，组合式风格的API(和 Vue3 新语法统一)
3.去掉了 modules 的概念，每一个 store 都是一个独立的模块
使用storeToRe 解构不会数据结构不会丢失响应性,方法解构不会丢失响应性
如: const {count, msg} = storeToRefs(countStore);
安装插件 nmp i pinia-plugin-persistedstate
// 持久化插件的使用需要再main.js 创建实例 并挂载到
// 导入持久化插件
import persist from "pinia-plugin-persistedstate";
// 创建pinia实例
const pinia = createPinia()
// 挂载
app.use(pinia.use(persist))

使用:
persist:true //开启当前模块的持久化
key: 更改本地存储的键名
paths: [] // 用于指定需要持久化的数据,不使用默认开启整个模块持久化

- ## 下午
- 观看FastJson
- 实例对象和List集合, map集合转JSON字符串
- JSON.toString
- 实例对象和List集合, map集合的JSON字符串反序列化
- 调用parseObject将map数组反序列化
  传递参数,TypeReference类型,在TypeReference类的泛型中,传递转后的Map集合
  如: Map<String,Student〉 map = JSON,parseObject(jsonString, new TypeReference<Map<String,Student>>(){}):
- parseArray将List数组反序列化
  先传递json格式字符串、传递转换后的集合的泛型的class对象
  如: List<Student> list=JSON. parseArray(jsonString, Student.class);
-

SerializerFeature是枚举注解:
SerializerFeature属性用在方法上(如: JSON.toJSONString(实例对象, SerializerFeature. WriteMapNullValue))
WriteMapNullValue 是否输出值为null的字段,默认为false
WriteNullListAsEmpty List字段如果为null,输出为[],而非null
WriteNullStringAsEmpty 字符类型字段如果为null,输出为”“,而非null
WriteNullNumberAsZero 数值字段如果为null,输出为0,而非null
WriteNullBooleanAsFalse Boolean字段如果为null,输出为false,而非null

@JSonField注解
该注解作用于方法上,字段上和参数上,可在序列化和反序列化时进行特性功能定制:
注解属性:name 序列化后的名字
注解属性:ordinal序列化后的顺序
注解属性:format 序列化后的格式(如: YYYY-MM--dd)
注解属性:serialize 是否序列化该字段
注解属性:deserialize 是否反序列化该字段
注解属性:serialzeFeatures 序列化时的特性定义

@JSonType注解
该注解作用于类上,对该类的字段进行序列化和反序列化时的特性功能定制,
注解属性:includes 要被序列化的字段.
注解属性:orders 序列化后的顺序
注解属性:serialzeFeatures 序列化时的特性定义
