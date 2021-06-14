<template>
  
  <div @click.self="closeModal" class="overlay">
    <div @click.self="closeModal" class=" text-center row justify-content-center">
      <div class="bg-light col-10 col-md-6">
        

     <div v-if="modaltype == 'upload'" class="">
        <div class="modal-header">
           <h5 class="modal-title" id="exampleModalLabel">Upload Music</h5>
           <button @click="closeModal" type="button" class="close" data-dismiss="modal" aria-label="Close"> <span aria-hidden="true">&times;</span> </button>
          </div>
          <div class="modal-body">
            <input class="form-control" type="text">
          </div>
          <div class="modal-footer"> <button @click="closeModal" type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
            <button type="button" class="btn btn-primary">Save changes</button> 
        </div> 
      </div>
      
     <div v-if="modaltype == 'playlist'" class="">
        <div class="modal-header">
           <h5 class="modal-title" id="exampleModalLabel">Create Playlist</h5>
           <button @click="closeModal" type="button" class="close" data-dismiss="modal" aria-label="Close"> <span aria-hidden="true">&times;</span> </button>
          </div>
          <div class="modal-body">
            <input class="form-control" type="text">
          </div>
          <div class="modal-footer"> <button @click="closeModal" type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
            <button type="button" class="btn btn-primary">Save changes</button> 
        </div> 
      </div>

        
      </div>
    </div>
  </div>
  
</template>

<script>
  export default{
    props: ['modaltype'],
    
    data(){
      return{
        hide: false,
      }
    },
    
    methods:{
      closeModal(){
        //this.hide = !this.hide
        this.$emit('modal', this.hide)
      }
    }
  }
</script>

<style>
  .overlay{
    position: fixed;
    height: 100vh;
    width: 100%;
    background: rgba(0,0,0,.5);
    z-index: 999;
    left: 0;
    top: 0;
    padding: 20px 0;
  }
</style>