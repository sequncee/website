<script>
  //TODO:
    // export let colors = ["#ff416c", "#ff4b2b"];
  </script>
  
  <style>
@keyframes rotate {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}
@keyframes rotate {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}

.blurred-gradient {
  --size: 250px;
  --speed: 50s;
  --easing: cubic-bezier(0.8, 0.2, 0.2, 0.8);

  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: var(--size);
  height: var(--size);
  filter: blur(calc(var(--size) / 5));
  background-image: linear-gradient(hsl(158, 82%, 57%, 85%), hsl(252, 82%, 57%));
  animation: rotate var(--speed) var(--easing) alternate infinite;
  border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;
}

@media (min-width: 720px) {
  .blurred-gradient {
    --size: 500px;
  }
}
  </style>
  
  <div class="blurred-gradient"></div>

