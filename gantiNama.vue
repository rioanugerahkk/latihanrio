<template>
    <div class="gantiNama">
        <table>
            <h3>Ubah Nama Siswa</h3>
            <p>Nama Sebelumnya : </p>
            <input type="text" >
            <p>Nama Baru </p> 
            <input type="text">
            <p>Masukan Ulang Nama Baru </p>
            <input type="text"><br><br>
            <input type="submit" name="tombol" value="Save" v-on:click ="Save">
        </table>
    </div>
</template>

<style scoped>
.gantiNama table{
 margin-left: 10px;
 margin-top: 100px;
}
.gantiNama table h3{
 text-align: center;
}
.gantiNama table p {
    margin-bottom: 5px;
}
.gantiNama table input{
    margin-bottom: -5px;
}
.gantiNama table input[type="submit"]{
  color:#fff;
  border:none;
  padding-left:0;
  font-size: 20px;
  font-weight: 500;
  cursor: pointer;
  background:  rgb(0, 89, 255);
  transition:all 0.3s ease;
  border-radius: 6px;
}

.gantiNama table input[type="submit"]:hover{
background-color: rgb(42, 226, 42);
}
</style>