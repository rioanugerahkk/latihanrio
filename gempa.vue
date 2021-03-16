<template>
<div class="cuaca">
    <div class="title">
     <h3>Data Gempa Di Indonesia {{$store.state.count}}</h3>
    </div>
 <div class="content">
     <table border="2" cellpadding="10">
        <tr>
            <td>Tanggal</td>
            <td>Jam</td>
            <td>Magnitude</td>
            <td>kedalaman</td>
            <td style="text-align: center;">Wilayah</td>
            <td>Coordinate</td>
        </tr>
        <th>
            <tr class="item1" v-for="(item,index) in gempa" :key="index"> {{item.Tanggal[0]}}</tr>
        </th>
         <th>
            <tr class="item1" v-for="(item,index) in gempa" :key="index"> {{item.Jam[0]}} </tr>
        </th>
        <th>
            <tr class="item1" v-for="(item,index) in gempa" :key="index"> {{item.Magnitude[0]}}</tr>
        </th>
        <th>
            <tr  class="item1" v-for="(item,index) in gempa" :key="index"> {{item.Kedalaman[0]}} </tr>
        </th>
         <th >
            <tr   class="wilayah" v-for="(item,index) in gempa" :key="index"> {{item.Wilayah[0]}} </tr>
        </th>
         <th>
            <tr class="item1" v-for="(item,index) in gempa" :key="index"> {{item.point[0].coordinates[0]}} </tr>
        </th>
    </table>
    </div>
</div>
</template>

<style scoped>
.content table {
    width: 1150px;
    margin-left: 10px;    
}
.content table td{
    text-align: center;
}
.content .item1 {
    line-height: 25px;
}

.content .wilayah{
    color: red;
    line-height: 25px;
}

</style>

<script>
import axios from 'axios'
import xml2js from 'xml2js'
export default {
    data: function(){
        return{
                gempa: []
            }
    },
    created : function(){
        axios.get('https://data.bmkg.go.id/DataMKG/TEWS/gempadirasakan.xml')
        .then(response => {
        var self = this
        xml2js.parseString(response.data, function( err, result){
        console.log(result)
        self.gempa = result.Infogempa.gempa
    })  
  })
    }
}
</script>