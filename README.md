# forestpro-videos
dokumentasi pages wp forestpro
`<style>
html, body {
  margin: 0;
  padding: 0;
  background: black;
  overflow: hidden;
}

body.admin-bar {
  margin-top: 0 !important;
}


#wpadminbar {
  display: none !important;
}

/* Override Pagelayer biar ga ada hijau */
.pagelayer-wrap,
.pagelayer-row,
.pagelayer-col,
.pagelayer-col-holder {
  margin: 0 !important;
  padding: 0 !important;
  background: black !important;
}

.cookieadmin_re_consent {
  display: none !important;
}

/* Wrapper fullscreen */
.video-wrapper {
  width: 100vw;
  height: 100dvh;
}

/* Video */
.video-wrapper video {
  width: 100%;
  height: 100%;
  object-fit: contain; /* ganti ke cover kalau mau full crop */
  display: block;
}
</style>

<div class="video-wrapper">
  <video id="vid" autoplay playsinline controls controlsList="nodownload">
    <source id="source" src="" type="video/mp4">
  </video>
</div>

<script>
// ===== DAFTAR VIDEO =====
const base = "https://amaturalist-vault.s3.ap-southeast-3.amazonaws.com/public/";

const videos = {
  "anis-bentet-kecil": base + "anisbentetkecil.mp4",
  "burungkucing-topicokelat": base + "burungkucing-topicokelat.mp4",
  "burung-madu-hitam": base + "burungmaduhitam.mp4",
  "cikukua-kerdil": base + "cikukuakerdil.mp4",
  "cucukpanjang-perut-kuning": base + "cucukpanjangperutkuning.mp4",
  "elangalap-kelabu": base + "elangalap-kelabu.mp4",

  "isapmadu-paruhpanjang": base + "isapmadu-paruhpanjang.mp4",
  "jagal-papua": base + "jagalpapua.mp4",
  "julang-papua": base + "julangpapua.mp4",
  "kakatua-koki": base + "kakatuakoki.mp4",
  "kakatua-raja": base + "kakatuaraja.mp4",
  "kasturi-kepala-hitam": base + "kasturikepalahitam.mp4",
  "kehicap-merah-karat": base + "kehicapmerahkarat.mp4",
  "kepudang-cokelat": base + "kepudangcokelat.mp4",
  "kipasan-semak-perutputih": base + "kipasansemak-perutputih.mp4",
  "kipasan-tunggir-merah": base + "kipasantunggirmerah.mp4",
  "meliphaga-aru": base + "meliphagaaru.mp4",
  "nuri-ara-pipikuning": base + "nuriara-pipikuning.mp4",
  "nuri-kate-pusio": base + "nurikatepusio.mp4",
  "nuri-pipi-merah": base + "nuripipimerah.mp4",
  "paok-papua": base + "paokpapua.mp4",
  "paruh-sabit": base + "paruhsabit.mp4",
  "peltops-hutan": base + "peltopshutan.mp4",
  "pitohui-belang": base + "pitohuibelang.mp4",
  "pungguk-papua": base + "punggukpapua.mp4",
  "robin-belang": base + "robinbelang.mp4",
  "sikatan-kilap": base + "sikatankilap.mp4",
  "tepus-tikus-merah": base + "tepustikusmerah.mp4",
  "udang-merah-papua": base + "udangmerahpapua.mp4",
  "uncal-besar": base + "uncalbesar.mp4",
  "walikelok": base + "walikelok.mp4",
  "walik-perut-jingga": base + "walikperutjingga.mp4"
};

const params = new URLSearchParams(window.location.search);
const v = params.get("v");

// default (HARUS ADA di list)
const defaultVideo = "anis-bentet-kecil";

const selected = videos[v] ? videos[v] : videos[defaultVideo];
document.getElementById("source").src = selected;

document.getElementById("vid").load();
</script>`
