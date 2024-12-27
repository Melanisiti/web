<template>
  <div class="container-fluid">
    <div class="row my-5">

      <div class="col-lg-12 mb-5">
        <div class="crounded-5">
          <img src="~/assets/img/guru.jpeg" alt="guru" style="width: 100%; height: 40%;"/>
        </div>
      </div>

      <div class="col-lg-12">
        <div class="sambutan rounded-5">

          <img src="~/assets/img/kepala.jpeg" alt="kepala" class="kepala-sekolah-img"/>

          <div class="sambutan-text">
            <h2>sambutan kepala sekolah</h2>
            <p>
              Assalamu'alaikum Warahmatullahi Wabarakatuh,

Salam sejahtera bagi kita semua.

Puji syukur kita panjatkan kehadirat Allah SWT atas limpahan rahmat dan karunia-Nya sehingga kita dapat terus berkarya dan berinovasi dalam memajukan dunia pendidikan, khususnya di SMKN 4 Tasikmalaya.

Sebagai salah satu sekolah kejuruan unggulan di Tasikmalaya, kami memiliki komitmen yang kuat untuk mencetak generasi muda yang tidak hanya kompeten di bidang keahlian masing-masing, tetapi juga memiliki karakter yang tangguh, integritas tinggi, serta siap bersaing di dunia industri dan dunia usaha.

Dengan dukungan tenaga pendidik yang profesional, fasilitas yang memadai, serta kurikulum berbasis kompetensi yang selalu disesuaikan dengan perkembangan dunia industri, kami yakin SMKN 4 Tasikmalaya akan terus melahirkan lulusan-lulusan yang berkualitas dan berdaya saing tinggi.

Kami juga terus berupaya menciptakan lingkungan belajar yang kondusif, inklusif, dan inovatif. Tidak hanya keterampilan teknis yang kami tekankan, tetapi juga pembentukan karakter dan pengembangan soft skills yang sangat dibutuhkan di era globalisasi ini.

Akhir kata, saya ucapkan terima kasih kepada seluruh tenaga pendidik, siswa-siswi, serta orang tua yang telah memberikan dukungan penuh untuk kemajuan sekolah ini. Mari kita bersama-sama membangun SMKN 4 Tasikmalaya menjadi sekolah yang lebih baik, unggul, dan berprestasi di masa depan.

Wassalamu'alaikum Warahmatullahi Wabarakatuh.
            </p>
            <p><strong>- kurniawan, s.pd, m.pd.</strong></p>
          </div>
        </div>
      </div>
    </div>
    </div>
</template>

<style scoped>
.card {
  height: 400px;
  box-shadow: 1px 1px 10px;
  width: 50vw;
  max-width: 10000px;
  padding-left: 100px;
  padding-right: 100px ;
}

.sambutan {
  background-color: aliceblue;
  box-shadow: 1px 1px 10px;
  padding: 20px;
}

.sambutan-content {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.kepala-sekolah-img {
  width: 150px;
  height: 150px;
  border-radius:50% ;
  object-fit: cover;
  box-shadow: 0px 2px 5px rgba(red, green, blue, alpha);
  margin-bottom: 15px;
}

.sambutan-text h2 {
  color:black;
  margin-bottom: 10px;
  font-size: 1.8rem;
}

.sambutan-text p {
  font-size: 1rem;
  line-height: 1.6;
  color: rgb(0, 0, 0);
}

.sambutan-text strong {
  color: rgb(0, 0, 0);
}
</style>