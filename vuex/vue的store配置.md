# store配置

* ## 基本配置
```
import Vue from 'vue'
import Vuex from 'vuex'

Vue.use(Vuex)

// noinspection JSAnnotator
const store =new Vuex.Store({
//保存数据的区域
  state :{
    count:0
  },
  //计算函数
  mutations:{
    add(){
      this.state.count++
      console.info(this.state.count)
    },
    reduce(){
      this.state.count--
      console.info(this.state.count)
    }
  }
})
export default store
```
* ## 使用方式
```
//main.js输入以下的代码
import store from './vuex/store'
//在new Vue里添加store
new Vue({
  el: '#body',
  store,
  router,
  components: {App},
  template: '<app/>'
})

```