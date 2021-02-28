<template>
<div class="output-siswa">
      <div class="title">
           <p>Informasi siswa</p>
       </div>
  <table class="table1">
    <p>Nama:  {{ $route.query.nama }}</p>
    <p>Nis: {{ $route.query.Nis }}</p>
    <p>Tempat, Tanggal.Lahir:{{$route.query.TempatTanggalLahir}}</p>
    <p>Jeniskelamin:{{ $route.query.Jeniskelamin}}</p>
    <p>Alamat:{{ $route.query.alamat}}</p>
    <p>Agama:{{$route.query.agama}}</p>
    <p>Kelas:{{$route.query.kelas}}</p>
    <p>Pelajaran yang disukai:</p> 
    <table class="Pelajaran" border="1">
        <tr>
            {{$route.query.pelajaran}}
        </tr>
       
    </table>

  </table>

 
</div>

</template>

<style>
.title{
  font-size: 35px;
  font-weight: 600;
  text-align: center;
  line-height: 100px;
  color:black;
  user-select: none;
}

.table1{
 margin-left: 15px;
 box-shadow: 11px 11px 19px -4px rgba(0,0,0,0.57);
}

table{
    margin-top: -10px; 
    height: 30px;
}
</style>

<script>
</script>