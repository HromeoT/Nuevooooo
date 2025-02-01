# Mi-Ariiiiii
San Valentín 
<!DOCTYPE html>
<html>
<head>
<title>Envelope</title>
<style>
body {
  background-color: #f0f0f0;
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  font-family: sans-serif;
}

.envelope {
  width: 200px;
  height: 150px;
  background-color: #fff;
  border: 2px solid #000;
  position: relative;
  perspective: 800px; /* Add perspective for 3D effect */
  cursor: pointer;
}

.envelope .flap {
  width: 80px;
  height: 50px;
  background-color: #fff;
  border: 2px solid #000;
  position: absolute;
  top: 0;
  right: 0;
  transform-origin: top right; /* Set transform origin for rotation */
  transform-style: preserve-3d; /* Maintain 3D effect during transformation */
  transition: transform 0.5s ease-in-out; /* Add smooth transition */
}

.envelope .flap.open {
  transform: rotateX(-120deg); /* Rotate flap when open */
}

.envelope .message {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 100%;
  height: 100%;
  background-color: #fff;
  display: none; /* Initially hide message */
  text-align: center;
  padding: 20px;
}

.envelope .message.show {
  display: block; /* Show message when envelope is open */
}
</style>
</head>
<body>

<div class="envelope">
  <div class="flap"></div>
  <div class="message">
    ¿Quieres ser mi San Valentín?
  </div>
</div>

<script>
const envelope = document.querySelector('.envelope');
const flap = document.querySelector('.flap');
const message = document.querySelector('.message');

envelope.addEventListener('click', () => {
  flap.classList.toggle('open');
  message.classList.toggle('show');
});
</script>

</body>
</html>
