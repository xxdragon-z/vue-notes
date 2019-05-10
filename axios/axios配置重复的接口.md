# 封装接口
* ## 在项目中,会出现接口多页面调用的情况,可以对接口进行封装，方便调用
```
//页面导入axios自定义配置
import * as API from './axiosAPI'
//接口封装区域
export default {
//封装你的重复接口
  getRequest:(url,params)=>{
    return API.getRequest(url,params)
  }
}
```