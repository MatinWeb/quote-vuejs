<template>
    <div class="col-sm-6 col-md-4 col-lg-3 my-3">
        <div class="panel">
            <div class="panel-body">
                <slot></slot>
                <button class="btn btn-primary" @click="removeThis">Remove</button>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    methods:{
        removeThis(){
            this.$emit('removeThisQuote')
        }
    }
}
</script>
<style scoped>

.panel{
  padding: 10px 15px;
  border: 1px solid #a1a0a088;
  border-radius: 5px;
  box-shadow: 0px 0px 10px 1px #a29f9f;
}
.panel-body{
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-family: 'Arizonia', cursive;
        font-size: 24px;
        color: #6e6e6e;
}

.panel:hover{
  transform: scale(1.05);
  background-color: #a29f9f50;
}

</style>