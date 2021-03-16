<template>
<div class="home">
    <carousel 
    @next="next"
    @prev="prev"
    >
        <carousel-slide v-for="(slide,index) in slides" 
        :key="slide"
        :index="index"
        :visibleSlide="visibleSlide"
        :direction="direction"
        >
        <img style="width: 100%; height:400px" :src="slide"/>
        </carousel-slide>        
    </carousel>

    <div class="sejarah">
        <h1>Sejarah singkat SMKN 2 Bandung</h1>
        <p><span>SMK</span> Negeri 2 Kota Bandung berawal dari nama besar STM Negeri 1 Bandung.</p>
<p>Berdasarkan dari Surat Putusan Menteri Pendidikan, Pengadjaran, dan Kebudayaan No.3835/B.II.1951 yang tertanggal 30 Agustus 1951, diputuskan TMT <span>01 Agustus 1951</span> untuk dibuka : Sekolah Teknik Menengah (STM) Negeri (Bagian Bangunan, Mesin, dan Listrik) di Bandung.</p>
<p>Maka berdasarkan surat keputusan tersebut didirikanlah STM Negeri I Bandung pada tahun 1951 di Jl. DR.Wahidin No.2 Bandung yang dipimpin oleh :<span> W.G. Zweekhorst.</span></p>
<p>Berdasarkan surat keputusan Kepala Kanwil Departemen Pendidikan dan Kebudayaan Propinsi Jawa Barat No.148/I02.Kep/R.77 tertanggal 16-12-1977, memutuskan untuk memindahkan STM Negeri I Bandung ke Jalan Ciliwung No. 4 Bandung.</p>
<p>Pada saat itu di Jalan Ciliwung no.4 pada awalnya adalah sebuah ST Negeri 1 yang didirikan sejak zaman Belanda (tahun tidak tercatat) dan STM Negeri IV Bandung.</p>
<p>Kemudian STM Negeri IV Bandung dipindahkan ke Jalan Buah Batu Bandung.</p>
<p>Kepindahan STM Negeri 1 Bandung secara bertahap mulai tahun ajaran 1978/1979 dan secara keseluruhan berakhir pada tahun ajaran 1979/1980 secara resmi STM Negeri 1 Bandung pindah dari Jalan DR. Wahidin No.2 ke Jalan Ciliwung No.4 Bandung.</p>
<p>Perubahan nama dari STM Negeri 1 menjadi SMK Negeri 2 Bandung berdasarkan SK Mendikbud Nomor 036/O/1997, bulan Oktober 1997, angka indek 1,2,3 dst adalah diambil dari umur sekolah dihitung dari sejak berdirinya sekolah.</p>
    </div>
</div>
</template>

<style scoped>
</style>

<script>
import carousel from '../components/carousel';
import carouselSlide from '../components/carouselSlide';
export default {
    data(){
        return{
            slides:[
            "https://1.bp.blogspot.com/--o0J1Btrbpc/VFSedVNMYiI/AAAAAAAAEnM/aTSrm-hcKvU/s600/Logo-SMK-Negeri-2-Bandung-featured.png",    
            "http://foto2.data.kemdikbud.go.id/getImage/20219146/24.jpg",
            "http://foto2.data.kemdikbud.go.id/getImage/20219146/26.jpg",
            "http://foto2.data.kemdikbud.go.id/getImage/20219146/8.jpg",           
            "http://foto2.data.kemdikbud.go.id/getImage/20219146/34.jpg",
            "http://smkn2bandung.sch.id/wp-content/uploads/2020/03/feature-800x600.jpg",
            "http://smkn2bandung.sch.id/wp-content/uploads/2020/03/2.jpg",
            "http://smkn2bandung.sch.id/wp-content/uploads/2020/03/3-768x576.jpg",
            "http://smkn2bandung.sch.id/wp-content/uploads/2020/03/5-768x512.jpg",
            "https://web.kominfo.go.id/sites/default/files/KOMINFO_KUNJUNGAN%20SMKN%202%20BANDUNG_05032020_INDRA%20KUSUMA%20(1).jpg",
            "https://instagram.fiev22-1.fna.fbcdn.net/v/t51.2885-15/e35/72074135_589380325204844_8928758663577093325_n.jpg?tp=1&_nc_ht=instagram.fiev22-1.fna.fbcdn.net&_nc_cat=108&_nc_ohc=-LBQx1B_gGEAX_syzcG&oh=a5778c76814a65df31c4df73a3e14dea&oe=6075E259",
            "https://instagram.fiev22-2.fna.fbcdn.net/v/t51.2885-15/e35/71511198_158932175185730_8789972836987393007_n.jpg?tp=1&_nc_ht=instagram.fiev22-2.fna.fbcdn.net&_nc_cat=102&_nc_ohc=0sX75Y98vMkAX-Oj2tA&oh=9004234b6245f55f4b122c7e25d92453&oe=60783CB8"

            ],
            
            visibleSlide: 0,
            direction: 'left ',
        }
    },
    computed:{
      slidesLen(){
        return this.slides.length;
      }  
    },
    methods:{
        next(){
            if(this.visibleSlide >= this.slidesLen - 1){
                this.visibleSlide = 0;
            }else{
                this.visibleSlide++;
            }
            this.direction = "left"
        },
        prev(){
            if(this.visibleSlide <= 0){
                this.visibleSlide = this.slidesLen - 1;
            }else{
                this.visibleSlide--;
            }
             this.direction = "right"
        }
    },
    components : {
        carousel,
        carouselSlide,
    }
}
</script>

<style>
.sejarah p {
    text-align: left;
    font-family: 'Montserrat,sans-serif';
    margin-left: 5px;
}
.sejarah span{
    font-weight: bold;
}
</style>