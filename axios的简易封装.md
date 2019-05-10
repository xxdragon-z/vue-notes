# axios封装
* ## 使用axios,你需要npm install axios
* ### 设置axios的各种属性
<pre><code>
import axios from 'axios'
//设置跨域
axios.defaults.withCredentials = true
//设置默认的请求地址
axios.defaults.baseURL=''
</code></pre>
* ### 分装请求类型
<pre><code>
export const getRequest = (url) => {
  console.info(url)
    return axios.get(url).then(result => result.data)
  }

export const PUT = (url, params) => {
  return axios.put(url, params).then(res => res.data)
}

export const DELETE = (url, params) => {
  return axios.delete(url, {params: params}).then(res => res.data)
}

export const PATCH = (url, params) => {
  return axios.patch(url, params).then(res => res.data)
}
export const POST = (url, params) => {
  console.info(url + '++++++++' + params)
  return axios.post(url, params).then(res => res.data)
}
</code></pre>