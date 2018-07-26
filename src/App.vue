<template>
  <div class='container'>
    <form role='form'>
       <div class='form-group'>
         <label from='username'>用户名</label>
         <input type='text' class='form-control' placeholder='请输入用户名' v-model='username'/>
       </div>
       <div class='form-group'>
         <label from='userage'>年 龄</label>
         <input type='text' class='form-control' placeholder='请输入年龄' v-model='userage'/>
       </div>
       <div class='form-group'>
          <input type='button' class='btn btn-primary' value='添加' @click='add'/>
          <input type='button' class='btn btn-danger' value='重置' @click='reset'/>
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
       <tr class='text-center' v-for='(item,index) in myData' :key='item.id'>
         <td>{{index+1}}</td>
         <td>{{item.name}}</td>
         <td>{{item.age}}</td>
         <td>
           <button class='btn btn-danger btn-sm' @click='fnDelete(index)'>删除</button>
         </td>
       </tr>
       
       <tr v-show='myData.length!=0'>
          <td class='text-right' colspan='4'>
             <button class='btn btn-danger btn-sm' @click='fnComplete'>全部删除</button>
          </td>
       </tr>
       <tr class='text-center' v-show='myData.length==0'>
         <td colspan='4'>
           <p>输无数据......</p>
         </td>
       </tr>
     </table>

     <!--模态框-->
     <div role='dialog' class='modal' id='layer'>
     
     </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data(){
    return {
      myData:[
        
      ],
      username:'',
      userage:''
    }
  },
  methods:{
    add(){
    if(this.username!='' && this.userage!=''){
      this.myData.push({
        name:this.username,
        age:this.userage
      }),
      this.username='';
      this.userage='';


      }else{
        alert('内容不能为空!');

      }
    },
    reset(){
      this.username='';
      this.userage='';

    },
    fnDelete(index){
      this.myData.splice(index,1);


    },

    fnComplete(){
      this.myData=[]


    }
  }
}
</script>

<style>

</style>
