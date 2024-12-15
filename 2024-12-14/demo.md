Vuex 
    1.state提供所有组件共享的数据
        1.1使用数据 mapState是辅助函数,可以把store中的数据自动映射到组件的计算属性中(computed)
    2.mutations可以提供修改数据的方法
        所有mutation函数，第一个参数，都是 state
        注意:mutation参数有且只能有一个，如果需要多个参数
    3.actions处理异步
         3.1使用数据 mapActions是辅助函数,可以把actions中的方法提取出来,映射到组件methods中
        注意:不能直接操作 state，操作 state，还是需要commit
    4.getters类似于计算属性    
    5.module 模块
