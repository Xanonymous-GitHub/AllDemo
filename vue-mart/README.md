# vue-mart

#### 技术栈: vue vuex vue-router cube-ui

> 拦截器的制作
```js
//  拦截请求
import axios from 'axios'

export default function(){
    axios.interceptors.request.use((config)=>{
        const token = localStorage.getItem('token')
        if(token){
            config.headers.token = token;
        }
        return config;
    })
}
```