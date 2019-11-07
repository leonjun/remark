<template>
  <div class="hello">
    
    <ul>
      <li>
        <a href="">asdfasdf</a>
      </li>
    </ul>
    <a>adfasdf</a>
    <!-- slots start -->
    <Slots>
      <template slot="header">
      <h1>头部</h1>
      </template>

      
      <p>{{msg}}</p>

      <template slot="footer">
        <p>底部</p>
      </template>
    </Slots>
    <!-- slots end -->
    <button @click="change()">click</button>
    <!-- filter component -->
    <Filt></Filt>
  </div>
  
</template>

<script>
import Slots from '@/components/slots/Slots'
import Filt from '@/components/filter/Filter'
export default {
  components:{
    Slots,
    Filt
  },
  name: 'HelloWorld',
  data () {
    return {
      mdata: {
        name: "live2d", // 模型名称
        model: "@/assets/live2d/model/tia/model.moc", // 模型文件地址
        textures: [
             "@/assets/live2d/model/tia/textures/default-costume.png", // 材质素材地址
        ]
    },
      msg: 'Welcome to Your Vue.js App'
    }
  },
  methods:{
    change(){
      this.msg="";
    },
    
  },
  mounted(){
    this.$nextTick(()=>{
      
    })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="stylus">
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type none 
  padding 0
}
li {
  display inline-block
  margin 0 10px
  a{
    color red
    text-decoration none
  }
}
a {
  
}
</style>
