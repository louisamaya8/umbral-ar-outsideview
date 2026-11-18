# umbral-ar-outsideview

<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>A la cARta Demo</title>

  <script type="module"
    src="https://unpkg.com/@google/model-viewer/dist/model-viewer.min.js">
  </script>

  <style>

    *{
  margin:0;
  padding:0;
  box-sizing:border-box;
}

body{
  background:
  radial-gradient(circle at top, #1a1a1a 0%, #090909 60%);
  color:white;
  font-family: Arial, sans-serif;
  overflow:hidden;
}

.top-ui{
  width:100%;
  padding-top:40px;
  text-align:center;
  position:absolute;
  z-index:10;
}

.logo{
  width:78%;
  max-width:520px;
  margin-bottom:12px;
}

.subtitle{
  font-size:17px;
  color:rgba(255,255,255,0.88);
  letter-spacing:0.3px;
  padding:0 24px;
}

.gold-line{
  width:70%;
  max-width:460px;
  height:2px;
  margin:22px auto 0 auto;

  background:linear-gradient(
    90deg,
    rgba(0,0,0,0),
    #c9a34d,
    rgba(0,0,0,0)
  );

  box-shadow:0 0 18px rgba(201,163,77,0.7);
}

model-viewer{
  width:100%;
  height:100vh;

  --poster-color: transparent;

  background:
  radial-gradient(circle at center,
  #1e1e1e 0%,
  #0b0b0b 80%);
}

.ar-button{

  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:18px;

  background:rgba(12,12,12,0.92);

  color:white;

  border:2px solid rgba(212,175,55,0.75);

  border-radius:999px;

  padding:22px 30px;

  width:88%;
  max-width:620px;

  position:absolute;

  /* AQUI ESTÁ LA MAGIA */
  bottom:90px;

  left:50%;
  transform:translateX(-50%);

  backdrop-filter:blur(10px);

  box-shadow:
  0 0 22px rgba(212,175,55,0.22),
  0 10px 35px rgba(0,0,0,0.55);

  cursor:pointer;

  transition:0.25s;
}

.ar-button:hover{
  transform:translateX(-50%) scale(1.02);

  box-shadow:
  0 0 32px rgba(212,175,55,0.45),
  0 12px 40px rgba(0,0,0,0.6);
}

.ar-button:active{
  transform:translateX(-50%) scale(0.97);
}

.icon-wrap{
  width:64px;
  height:64px;

  min-width:64px;

  border-radius:50%;

  border:2px solid rgba(212,175,55,0.7);

  display:flex;
  align-items:center;
  justify-content:center;

  box-shadow:
  0 0 18px rgba(212,175,55,0.35);
}

.icon-wrap img{
  width:34px;
  height:34px;
  object-fit:contain;
}

.button-text{
  flex:1;
  text-align:left;
}

.button-title{
  font-size:32px;
  font-weight:800;
  line-height:1;
  color:#f4d27a;
  letter-spacing:1px;
  margin-bottom:6px;
}

.button-subtitle{
  font-size:18px;
  color:rgba(255,255,255,0.88);
}

.arrow{
  font-size:42px;
  color:#f4d27a;
  font-weight:bold;
  margin-right:6px;
}

@media(max-width:768px){

  .button-title{
    font-size:22px;
  }

  .button-subtitle{
    font-size:15px;
  }

  .ar-button{
    padding:18px 22px;

    /* MÁS espacio todavía en móvil */
    bottom:110px;
  }

  .icon-wrap{
    width:56px;
    height:56px;
    min-width:56px;
  }

  .arrow{
    font-size:34px;
  }

  .subtitle{
    font-size:15px;
  }

}

  </style>
</head>

<body>

  <div class="top-ui">

    <!-- CAMBIA logo.png POR TU LOGO -->
  
    <img src="logo.png" class="logo">

    <div class="subtitle">
@@ -249,30 +249,30 @@

      <div class="icon-wrap">

        <!-- CAMBIA icono.png POR TU LOGO -->
      
        <img src="icono.png">

      </div>

      <div class="button-text">

        <div class="button-title">
          PRESIONA AQUÍ
        </div>

        <div class="button-subtitle">
          para ver el platillo en tu mesa
        </div>

      </div>

      <div class="arrow">
        ›
      </div>

    </button>

  </model-viewer>

</body>
</html>
