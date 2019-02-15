<template>
  <div class="hello">
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
      msg: 'Welcome to Your Vue.js App'
    }
  },
  methods:{
    change(){
      this.msg="";
    }
  },
  mounted(){
    this.$nextTick(()=>{
      
    })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
