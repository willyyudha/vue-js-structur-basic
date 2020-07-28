<template>
    <div id="app">
        <div class="container">
            <div class="row header mb-5 p-3">
                <div class="col-lg-12">
                    <h3>What I Do Today</h3>
                </div>
            </div>
            <div class="row content">
                <div class="col-lg-12">
                    <div class="pekerjaan-rumah">
                        <div class="row">
                            <div v-for="task in tasks" v-bind:key="task.id"  class="mb-3 tugas col-lg-12 text-left">
                                <itemTugas :testopervariabel="task.status" v-bind:task="task"/>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>

    import 'bootstrap/dist/css/bootstrap.css';
    import ItemTugas from '../components/ItemTugas';

    export default {
        name : 'ToDoList',
        data : function (){
           return {
               tasks : [
                   {
                       id   : 1,
                       name : 'Bersihkan tempat tidur',
                       status : false
                   },
                   {
                       id : 2,
                       name : 'Bersihkan toilet',
                       status : false
                   },
                   {
                       id : 3,
                       name : 'Bersihkan diri',
                       status : false
                   }
               ]
           }
        },
        components: {
            ItemTugas
        }
    }
</script>
<style scoped>
    #app {
        font-family: "Avenir","Helvetica","Arial","sans-serif";
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: darkslateblue;
        margin-top: 60px;
    }
    .header {
        background: seagreen;
    }
    .header h2 {
        margin-bottom: 0;
    }

    .tugas {
        margin-bottom: 20px;
    }

    .tugas .item {
        font-size: 18px;
        text-align: left;
    }
</style>
