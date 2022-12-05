<template>
    <div class="card mb-3" style="width: 30rem; margin:1rem;">
            <div class="card-header border-info" :class="backgroundheader">{{titulo}}</div>
            <div class="card-body text-bg-ligth border-ligth">
                <table class="table" :class="tablestyle">
                    <thead>
                        <tr>
                            <th scope="col">Bandera</th>
                            <th scope="col">ISO</th>
                            <th scope="col">País</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr :class="i%2==0? 'table-active':tablestyle" v-for="(itemdata,i) of tabledata" :key="i">
                            <td>
                                <img class="avatarCol" :src="require('@/assets/'+itemdata.imagen)">
                            </td>
                            <td>{{itemdata.imagen}}</td>
                            <td>{{itemdata.pais}}</td>
                        </tr> 
                    </tbody>
                </table>
            </div>
    </div>
</template>

<script>
    export default {
        name: 'MiTabla',
        props:{
            tabledata:Array,
            backgroundheader:String,
            tablestyle:String,
            titulo:String
        }
    }
</script>


<style scoped>
.tableHead{
    background-color:#19234F;
    color:#BDAA75;
}

.imparRow{
    background-color:#ffffff;
    color: #19234F;
}

.parRow{
    background-color: #BDAA75;
    color: #19234F;
}

.avatarCol{
    width: 50px;
    height: 30px;
/*     border-radius: 50%; */
}

</style>
