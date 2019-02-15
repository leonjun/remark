<template>
 <div>
     
 </div>
</template>

<script>
export default {
 data() {
    return {
        lists:[1,2,3,4,5,6,7,8,9,10]
    }
 },
 components: {

 },
 
 mounted(){
      console.log(this.lists);
        let lists =this.lists.filter((list)=>{
            if(list<5){
                return list
            }
        });
        console.log(lists)
        }
}
</script>

<style scope>
</style>
