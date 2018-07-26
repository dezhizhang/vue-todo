<template>
  <div class='container'>
    <form role='form'>
       <div class='form-group'>
         <label from='username'>用户名</label>
         <input type='text' class='form-control' placeholder='请输入用户名'/>
       </div>
       <div class='form-group'>
         <label from='userage'>年 龄</label>
         <input type='text' class='form-control' placeholder='请输入年龄'/>
       </div>
       <div class='form-group'>
          <input type='button' class='btn btn-primary' value='添加'/>
          <input type='button' class='btn btn-danger' value='重置'/>
       </div>
    </form>
    <hr/>
    <div class='h2 text-center text-info'>用户信息表</div>
     <table class='table table-bordered'>

       <tr class='text-center'>
         <th>序号</th>
         <th>姓名</th>
         <th>年龄</th>
         <th>操作</th>
       </tr>
       <tr class='text-center'>
         <td>1</td>
         <td>张德志</td>
         <td>28</td>
         <td>
           <button class='btn btn-danger btn-sm'>删除</button>
         </td>
       </tr>
       <tr class='text-center'>
         <td>2</td>
         <td>刘德华</td>
         <td>22</td>
         <td>
           <button class='btn btn-danger btn-sm'>删除</button>
         </td>
       </tr>
       <tr class='text-center'>
         <td>3</td>
         <td> 周华建</td>
         <td>33</td>
         <td>
           <button class='btn btn-danger btn-sm'>删除</button>
         </td>
       </tr>
       <tr>
          <td class='text-right' colspan='4'>
             <button class='btn btn-danger btn-sm'>全部删除</button>
          </td>
       </tr>
       <tr class='text-center'>
         <td colspan='4'>
           <p>输无数据......</p>
         </td>
       </tr>
     </table>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>

</style>
