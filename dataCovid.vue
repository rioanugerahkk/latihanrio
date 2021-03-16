<template>
<div class="cuaca">
    <div class="title">
     <h3>Data Covid 19 Di Indonesia</h3>
    </div>
    <div class="content">
     <table border="1" cellpadding="10">
        <tr>
            <td style="text-align: center;">provinsi</td>
            <td>kasus positif</td>
            <td>kasis sembuh</td>
            <td>kasus meninggal</td>
        </tr>
        <th class="provinsi">
            <tr  class="item1" v-for="item in covid" :key="item.fid">{{item.provinsi}}</tr>
        </th>
         <th>
            <tr style="color: red;" class="item"  v-for="item in covid" :key="item.fid">{{item.kasusPosi}}</tr>
        </th>
        <th>
            <tr  style="color: rgb(0, 255, 21);" class="item"  v-for="item in covid" :key="item.fid">{{item.kasusSemb}}</tr>
        </th>
        <th>
            <tr style="color:  rgba(255, 0, 0, 0.623);"   class="item" v-for="item in covid" :key="item.fid">{{item.kasusMeni}}</tr>
        </th>

    </table>
    </div>

</div>
</template>

<style scoped>
.title h3 {
 font-size: 28px;
 margin-bottom: 5px;    
}

.content table {
    float: right;
}

.content th .item{
    line-height: 19.10px;
    border-bottom: 2px solid blue;
}

.content th .item1{
    line-height: 19px;
    width: 100px;
}

.content .provinsi {
 width: 230px;
 
}


</style>

<script>
import axios from 'axios'

export default {
    data(){
         return{
             covid:[ ],
         }
    },
    created(){
        axios.get(`https://indonesia-covid-19.mathdro.id/api/provinsi/`)
        .then(res=>{
            this.apiUrl = res.config.url
            this.covid = res.data.data
        })
    },   
}
</script>