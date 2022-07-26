<template>
    <div class="grid justify-items-center">
        <br/>
        <h1 class="text-center">ToDos App </h1>
        <form @submit="addtododata" class="grid justify-items-left bg-slate-200 p-7 w-64" >
            <div>
                <input type="text" v-model="title" placeholder="Title" required/> 
            </div>
            <br/>
            <div>
                <button class=" bg-blue-600 border-1 border-black text-white p-1 rounded-md font-serif font-semibold " > Add </button>
            </div>
        </form>
    </div>
</template>
<script>


    export default{
        name : "AddToDo component",
        data(){
            return{
                title:""
            }
        },
        methods:{
            addtododata(e){
                e.preventDefault()   //this will make sure that the form is not submitted to your file 
                const newtodo = {
                    id:Date.now(),  //returns unique date
                    title:this.title,
                    completed:false  //default added by us
                }
                //send out a event
                this.$emit("add-todo", newtodo)

                //clear out input field
                this.title =""
            }
        }
    }
</script>
<style scoped>
/* form{
    width: 220px;
}
button {
    color: whitesmoke;
    background-color: red;
    float: right;

} */
</style>