<template>
<div class="input-siswa">
 <div class="content">
    <div class="wrapper">
       <div class="title">
           <p>Form Pendaftaran siswa </p>
       </div>
      <form @submit.prevent="getDataFromForm">    
        <div class="field">
          <input type="text1" required v-model="nama">
          <label>Nama lengkap</label>
        </div>
         <div class="field">
          <input type="text2" required v-model="Nis">
          <label>Nis</label>
        </div>
        <div class="field">
          <input type="text" required v-model="TempatTanggalLahir">
          <label>Tempat, Tanggal.lahir</label>
        </div>

        <div class="Jeniskelamin">
          <form method="get">
            <h5> Jenis kelamin: </h5>
            <input id="Laki-Laki" type="radio" name="Jeniskelamin" value="Laki-Laki" v-model="Jeniskelamin"><p>Laki-Laki</p>
            <input class="perempuan" type="radio" name="Jeniskelamin" value="Perempuan" v-model="Jeniskelamin"><p> Perempuan</p>
          </form>
        </div>

        <div class="field">
          <input type="text" required v-model="alamat">
          <label>Alamat</label>
        </div><br>
        <div class="agama">
          <h5> Agama: </h5>
          <select v-model="agama" >
            <option disabled value="">Please select one</option>
            <option>islam</option>
            <option>katolik</option>
            <option>protestan</option>
            <option>Hindu</option>
            <option>Budha</option>
            <option>Khongmuchu</option>
          </select>
        </div><br><br><br>

        <div class="kelas">
          <h5> Kelas : </h5>
          <select v-model="kelas">
            <option disabled value="">Please select one</option>
            <option>XI RPL 1</option>
            <option>Xi RPL 2</option>
            <option>XI TKJ 1</option>
            <option>XI TKJ 2</option>
            <option>XI MM 1</option>
            <option>XI MM 2</option>
          </select>      
        </div><br><br>

        <div class="pelajaran">
          <h5> pelajaran yang disukai:</h5><br><br><br>
          <form method="get">
            <table >

            <input type="checkbox" name="checkbox1" value="Mtk" v-model="pelajaran">
            <label for="checkbox1">Mtk</label>
              <input type="checkbox" name="checkbox2" value="Bahasa-Indonesia" v-model="pelajaran">
            <label for="checkbox2">Bahasa Indonesia</label>
              <input type="checkbox" name="checkbox3" value="Bahasa-Inggris" v-model="pelajaran">
            <label for="checkbox3">Bahasa Inggris</label><br>
              <input type="checkbox" name="checkbox4" value="IPA" v-model="pelajaran">
            <label for="checkbox4">IPA</label>
              <input type="checkbox" name="checkbox5" value="PPKN" v-model="pelajaran">
            <label for="checkbox5">PPKN</label>
              <input type="checkbox" name="checkbox6" value="Bahasa-Sunda" v-model="pelajaran">
            <label for="checkbox6">Bahasa Sunda</label><br>
              <input type="checkbox" name="checkbox7" value="Olahraga" v-model="pelajaran">
            <label for="checkbox7">Olahraga</label>
              <input type="checkbox" name="checkbox8"  value="PKK" v-model="pelajaran">
            <label for="checkbox8">PKK</label>
                  <input type="checkbox" name="checkbox9" value="Agama" v-model="pelajaran">
            <label for="checkbox9">Agama</label>
              </table>
           </form>
        </div>
        <div class="field">
          <input type="submit" name="tombol" value="Daftar" >
        </div>
   
      </form>
    </div>
 </div>  
</div>
</template>

<style>
@import url('https://fonts.googleapis.com/css?family=Poppins:400,500,600,700&display=swap');

.input-siswa {
    display: flex;
    justify-content: center;
    margin-top: 30px;
}

.content {
    width: 70%;
}

.wrapper{
  width:1000px;
  background:#fff;
  border-radius: 15px;
  box-shadow: 10px 15px 20px rgba(0,0,0,0.1);
  height: 900px;
}

.wrapper .title{
  font-size: 35px;
  font-weight: 600;
  text-align: center;
  line-height: 100px;
  color:black;
  user-select: none;
}
.wrapper form{
  padding:10px 30px 50px 30px;

}
.wrapper form .field{
  height:50px;  
  width:100%;
  margin-top:15px;
  position: relative;
}

.wrapper form .field input{
  height:100%;
  width:50%;
  outline:none;
  font-size: 17px;
  padding-left: 20px;
  border:1px solid lightgray;
  border-radius: 25px;
  transition: all 0.3s ease;
  float: left;
}

.wrapper form .field input:focus,
form .field input:valid{
  border-color: blue;
}
.wrapper form .field label{
  position:absolute;
  top:50%;
  left:20px;
  color:#999;
  font-weight: 400;
  font-size: 17px;
  pointer-events: none;
  transform:translateY(-50%);
  transition: all 0.3s ease;
}

form .field input:focus ~ label,
form .field input:valid ~ label{
  top:0%;
  font-size: 16px;
  color: rgb(0, 89, 255);
  background:#fff;
  transform:translateY(-50%);
}

form .content{
  display:flex;
  width:100%;
  height:50px;
  font-size: 16px;
  align-items:center;
  justify-content:space-between;
}

form .content .checkbox{
  display:flex;
  align-items:center;
  justify-content:center;
}

form .content input{
  width:15px;
  height:15px;
}

.Jeniskelamin {
  margin-top: 0px;
  margin-bottom: 0px;
}

.Jeniskelamin h5{
  float: left;
  margin-left: -20px;
  color: rgb(66, 66, 66);
  
}

.Jeniskelamin input {
  float: left;
  margin-top: 24px;
  margin-left: 10px;
}
.Jeniskelamin input #Laki-Laki {
  margin-left: 10px;
}

.Jeniskelamin p {
  margin-top: 19px;
  color: #888;
  float: left;
  margin-left: 0px;
}

.Jeniskelamin form {
  margin-bottom: -0px;
}

form .content label{
  color:#262626;
  user-select: none;
  padding-left:5px;
  margin-bottom: 20px;
}

.agama h5 {
  float: left;
  margin-left: 15px;
  color: rgb(66, 66, 66);
  margin-top: 15px;
}

.agama select {
  float: left;
  margin-left: 10px;
  margin-top: 13px;
}

.kelas h5 {
  float: left;
  margin-left: 15px;
  color: rgb(66, 66, 66);
  margin-top: 7px;
}

.kelas select {
  float: left;
  margin-left: 17px;
  margin-top: 5px;
}

table{
  border:  2px solid #888;
  height: 80px;
  width: 500px;
  margin-bottom: 20px;
  text-align: left;
}

.pelajaran h5{
  float: left;
  margin-left: -43px;
  color: rgb(66, 66, 66);
  margin-top: 5px;
}

.pelajaran table{
  float: left;
  margin-top: -30px;
  margin-left: -10px;
}

.pelajaran label {
  margin-right: 10px;
}

form .content .pass-link a{
  color: blue;
}

form .field input[type="submit"]{
  color:#fff;
  border:none;
  padding-left:0;
  margin-top:-10px;
  font-size: 20px;
  font-weight: 500;
  cursor: pointer;
  background:  rgb(0, 89, 255);
  transition:all 0.3s ease;
}

form .field input[type="submit"]:hover{
    background-color: rgb(42, 226, 42);
}


form .field input[type="submit"]:active{
  transform:scale(0.95);
}
form .input-siswa-link{
  color:#262626;
  margin-top:20px;
  text-align: center;
}
form .pass-link a,
form .input-siswa-link a{
  color: blue;
  text-decoration: none;
}

</style>

<script>
export default {
  data: function(){
        return {
                     //string, number,boolean,array,object
        selectedKelas: [],
        selected: [],
        nama: '',
        Nis: '',
        TempatTanggalLahir: [],
        Jeniskelamin:[],
        alamat: "",
        agama: [],
        kelas:[],
        pelajaran: [],
        }
    },
  methods: {
    getDataFromForm:function() {
      this.$router.push({path: 'output', query: {nama: this.nama,
                                                Nis: this.Nis,
                                                TempatTanggalLahir: this.TempatTanggalLahir,
                                                Jeniskelamin: this.Jeniskelamin,
                                                alamat: this.alamat,
                                                agama: this.agama,
                                                kelas: this.kelas,
                                                pelajaran: this.pelajaran
                                                }})
    }
  }
}
</script>