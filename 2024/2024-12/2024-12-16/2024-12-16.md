Vue2:

    直接通过模块名访问 $store.state.模块名.xxx
    通过 mapState 映射
    默认根级别的映射 mapstate(['xxx'])
    子模块的映射 mapstate('模块名'，「'xxx'])    需要开启命名空间

    使用模块中 getters 中的数据:
    1. 直接通过模块名访问 $store.getters['模块名/xxx']
    2. 通过 mapGetters 映射
    默认根级别的映射 mapGetters(['xxx'])
    子模块的映射 mapGetters('模块名',['xxx'])    需要开启命名空间

    目标:掌握模块中 mutation 的调用语法
    注意:默认模块中的 mutation 和 action
    载到子模块。
     会被挂载到全局，
    需要开启命名空间，才会
    调用子模块中 mutation:
    直接通过 store 调用
    $store.commit('模块名/xxx'，额外参数)
    通过 mapMutations 映射
    更新信息
    默认根级别的映射 mapMutations([xxx'])
    子模块的映射 mapMutations('模块名'，['xxx'])-需要开启命名空间
    
     action的调用语法(同理-直接类比 mutation 即可) 会被挂载到全局，
    需要开启命名空间，才会挂载到子模块。
    注意:默认模块中的 mutation 和 actior
    调用子模块中 action :
     1.直接通过 store 调用 $store.dispatch('模块名/xxx，额外参数)
    通过 mapActions 映射
    默认根级别的映射 mapActions(['xxx']
    子模块的映射 mapActions('模块名'，'xxX'])-需要开启命名空间

命令行创建vue3
注意:node.js版本>16
npm init vue@latest

// 显示的暴露组件内的属性和方法
defineExpose({})
// 父传子使用defineProps接收
defineProps({})
// 子传父使用defineEmits
defineEmits([])

基本数据类型响应化：在 Vue 3 中，ref可以用来创建基本数据类型（如number、string、boolean）
引用响应式数据：ref返回的是一个包含value属性的对象

复习:
polite
cave
go on a picnic

cow
behind
eraser
exercise
science
far
half
mid-autumn-festival
together
get together
mooncake
moon
pen pal
hobby
lost
poem
puzzle
jasmine
idea
Canberra
amazing
goal
join
factory
tired
Germany
alaska
fast
Papa Westray
Scotland
visit
sea a film
take a trip
supermarket
share
sled
film










