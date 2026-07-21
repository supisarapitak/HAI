<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport"content="width=device-width,initial-scale=1.0">
<title>AI Car Type Detetor</title>

<script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs"></script>
<script src="https://cdn.jsdelivr.net/npm/@tensorflow-models/coco-ssd"></script>

<style>
*{
  margin:0;
  padding:0;
  box-sizing:border-box;
  font-family:Segoe UI,sans-serif;
}


body{
  background:#07111f;
  color:white;
  min-height:100vh;
  text-align:center;
}

header{
  padding:20px;
  background:#0b1e35;
  box-shadow:0 0 20px cyan;
}

h1{
  color:#00ffff;
}

.container{
   padding:15px;
}

.camera-box{
   position:relative;
   width:100%;
   max-width:700px;
   margin:auto;
}

video{
  width:100%;
  border-radius:20px;
  border:2px solid cyan;
}

canvas{
  position:absolute;
  left:0;
  top:0;
  width:100%;
  height:100%;
}

.result{
   margin-top:20px;
   background:#10243e;
   padding:20px;
   border-radius:15px;
}

.detected{
   font-size:1.5rem;
   color:#00ffff;
   margin-top:10px;
}

.status{
   margin-top:10px;
   color:#8ffcff;
}
</style>
</head>
<body>

<header>
  <h1> AI Car Type Detector</h1>
  <p>Point your camera at a vehicle</p>
</header>

<div class="container">

  <div class="camera-box">
    <video id="video" autoplay playsinline></video>
    <canvas id="canvas"></canvas>
  </div>

  <div class="result">
    <h2>Detected Vehicle</h2>
    <div id="carType" class="detected">
      Waiting...
    </div>
    <div id="status" class="status">
       Loading AI Model...
       </div>
    </div>
  
  </div>

  <script>

  const video = document.getElementById("video");
  const canvas = document.getElementById("canvas");
  const ctx = canvas.getContext("2d");

  const carType = document.getElementById("carType");
  const statusText = document.getElementById("status");

  let model;

  //start Camera
  async function startCamera(){

    const stream = await navigator.mediaDevices.getUserMedia({
      video:{
        facingMode:"environment"
      }
    });

      video.srcObject = stream;

      return new Promise(resolve=>{
        video.onloadedmetadata=()=>{
          resolve();
        };
      });

    }

    // Load AI
    async function loadModel(){

      model = await cocoSsd.load();

      statusText.innerHTML =
      "AI Reary. Point camera at a vehicle.";

    }

    // Detect Vehicles
    async function detectObjects(){

      canvas.width = video.videoWidth;
      canvas.height = video.videoHeight;

    const predictions =
    await model.detect(video);

    ctx.clearRect(
      0,
      0,
      canvas.width,
      canvas.height
    );

    let vehicleFound = false;

    predictions.forEach(pred=>{

      const vehicleClasses = 
      ["car","truck","bus","motorcycle"];

      if(vehicleClasses.includes(pred.class)){

        vehicleFound = true;

        const [x,y,w,h] = pred.bbox;

        ctx.strokeStyle="#00ffff";

        ctx.lineWidth=4;

        ctx.strokeRect(x,y,w,h);

        ctx.fillStyle="#00ffff";
        ctx.font="20px Arial";

        ctx.fillText(
          pred.class.toUpperCase(),
          x,
          y-10
        );

        carType.innerHTML =
        "Detected: "+
        pred.class.toUpperCase();
      }

    });

    if(!vehicleFound){

       carType.innerHTML =
       "No vehicle detected";
    }

       requestAnimationFrame(
         detectObjects
       );
    
    }

    // Initialize
    async function init(){

      await startCamera();

      await loadModel();

      detectObjects();

    }

    init();

    </script>

    </body>
    </html>
