<!DOCTYPE html>
<html lang="fa">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Sorvli Info</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body, html {
      height: 100%;
      overflow: hidden;
      font-family: system-ui, -apple-system, Segoe UI, Roboto, sans-serif;
      background: radial-gradient(circle at top, #0b1220, #05060a 60%, #02030a);
      color: #e5e7eb;
    }

    canvas {
      position: fixed;
      top: 0;
      left: 0;
      z-index: 0;
    }

    #overlay {
      position: relative;
      z-index: 2;
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 20px;
      gap: 20px;
    }

    .card {
      background: rgba(65, 65, 65, 0.05);
      border: 1px solid rgba(255, 255, 255, 0.10);
      padding: 40px 30px;
      border-radius: 22px;
      backdrop-filter: blur(8px);
      box-shadow: 0 20px 60px rgba(0, 0, 0, 0.6);
      max-width: 600px;
      animation: float 6s ease-in-out infinite;
    }

    h1 {
      font-size: 2.8rem;
      margin-bottom: 30px;
      background: #e5e7eb;
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    p {
      font-size: 1.1rem;
      opacity: 0.85;
      line-height: 2;
    }

    .socials {
      display: flex;
      gap: 20px;
      justify-content: center;
      margin-top: 20px;
    }

    .socials a {
      width: 46px;
      height: 46px;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 14px;
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid rgba(255,255,255,0.10);
      transition: 0.3s;
      color: white;
    }

    .socials a:hover {
      transform: translateY(-4px);
      background: rgba(255,255,255,0.12);
    }

    .socials svg {
      width: 22px;
      height: 22px;
      fill: #e5e7eb;
    }

    @keyframes float {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-10px); }
    }
  </style>
</head>
<body>

<div id="overlay">
  <div class="card">
    <h1>Hi, I'm Ali</h1>
    <p>
      I'm 18 years old and I work as a web designer and logo designer. I enjoy creating modern, clean, and user-focused digital experiences, from responsive websites to unique brand identities.

I'm always exploring new technologies and design trends to improve my skills and build better products.
      <br/>
      <br/>

     <b>You can also follow me on the platforms below to see my latest projects and updates.</b>
    </p>
    <div class="socials">
    <a href="https://t.me/sorvlix" target="_blank" title="Telegram"><svg viewBox="0 0 24 24"><path d="M9.99 15.67L9.6 21.3c.57 0 .81-.24 1.11-.54l2.66-2.55 5.52 4.04c1.01.56 1.73.27 1.98-.94l3.62-16.96c.32-1.5-.54-2.09-1.53-1.71L1.18 9.88c-1.46.57-1.44 1.39-.25 1.76l5.81 1.81L19.2 6.62c.65-.4 1.24-.18.76.22"></path></svg></a>

    <a href="#" target="_blank" title="GitHub"><svg viewBox="0 0 24 24"><path d="M12 .5C5.73.5.75 5.6.75 11.97c0 5.1 3.29 9.43 7.86 10.96.58.11.79-.26.79-.58v-2.02c-3.2.7-3.88-1.4-3.88-1.4-.52-1.36-1.28-1.72-1.28-1.72-1.05-.74.08-.72.08-.72 1.16.08 1.77 1.22 1.77 1.22 1.03 1.8 2.7 1.28 3.36.98.1-.76.4-1.28.72-1.58-2.56-.3-5.26-1.31-5.26-5.83 0-1.29.46-2.34 1.22-3.17-.12-.3-.53-1.52.11-3.17 0 0 1-.33 3.3 1.21.96-.27 1.98-.41 3-.41s2.04.14 3 .41c2.3-1.54 3.3-1.21 3.3-1.21.64 1.65.23 2.87.11 3.17.76.83 1.22 1.88 1.22 3.17 0 4.53-2.7 5.53-5.27 5.82.41.36.77 1.09.77 2.21v3.28c0 .32.21.69.8.57A11.5 11.5 0 0 0 23.25 11.97C23.25 5.6 18.27.5 12 .5z"></path></svg></a>

    <a href="#" target="_blank" title="Instagram"><svg viewBox="0 0 24 24"><path d="M7 2h10a5 5 0 0 1 5 5v10a5 5 0 0 1-5 5H7a5 5 0 0 1-5-5V7a5 5 0 0 1 5-5zm5 5.5A4.5 4.5 0 1 0 16.5 12 4.5 4.5 0 0 0 12 7.5zm6.5-1.5a1 1 0 1 0 1 1 1 1 0 0 0-1-1z"></path></svg></a>

    <a href="#" target="_blank" title="X"><svg viewBox="0 0 24 24"><path d="M18.9 2h3.1l-6.8 7.8L23 22h-6.6l-5.2-6.8L5.2 22H2l7.3-8.4L1 2h6.7l4.7 6.2L18.9 2zm-1.2 18h1.8L6.1 3.9H4.2L17.7 20z"></path></svg></a>
  </div>
  </div>

</div>

<script src="https://cdn.jsdelivr.net/npm/three@0.160.0/build/three.min.js"></script>
<script>
  const scene = new THREE.Scene();

  const camera = new THREE.PerspectiveCamera(75, window.innerWidth/window.innerHeight, 0.1, 1000);
  const renderer = new THREE.WebGLRenderer({ antialias: true, alpha: true });
  renderer.setSize(window.innerWidth, window.innerHeight);
  renderer.setPixelRatio(window.devicePixelRatio);
  document.body.appendChild(renderer.domElement);

  const geometry = new THREE.TorusKnotGeometry(10, 2.5, 200, 30);
  const material = new THREE.MeshStandardMaterial({ color: 0xffffff });
  const torusKnot = new THREE.Mesh(geometry, material);
  scene.add(torusKnot);

  const particlesGeometry = new THREE.BufferGeometry();
  const particlesCount = 800;
  const posArray = new Float32Array(particlesCount * 3);

  for (let i = 0; i < particlesCount * 3; i++) {
    posArray[i] = (Math.random() - 0.5) * 100;
  }

  particlesGeometry.setAttribute('position', new THREE.BufferAttribute(posArray, 3));

  const particlesMaterial = new THREE.PointsMaterial({
    size: 0.2,
    color: 0xe5e7eb 
  });

  const particlesMesh = new THREE.Points(particlesGeometry, particlesMaterial);
  scene.add(particlesMesh);

  const light = new THREE.PointLight(0xffffff, 1.3); 
  light.position.set(20, 20, 20);
  scene.add(light);

  scene.add(new THREE.AmbientLight(0xffffff, 1));

  camera.position.z = 40;

  let mouseX = 0, mouseY = 0;
  document.addEventListener('mousemove', (e) => {
    mouseX = (e.clientX / window.innerWidth - 0.5) * 2;
    mouseY = (e.clientY / window.innerHeight - 0.5) * 2;
  });

  function animate() {
    requestAnimationFrame(animate);

    torusKnot.rotation.y += 0.0005;
    torusKnot.rotation.x += 0.0005;

    particlesMesh.rotation.y += 0.0005;

    camera.position.x += (mouseX * 5 - camera.position.x) * 0.05;
    camera.position.y += (-mouseY * 5 - camera.position.y) * 0.05;
    camera.lookAt(scene.position);

    renderer.render(scene, camera);
  }

  animate();

  window.addEventListener('resize', () => {
    camera.aspect = window.innerWidth / window.innerHeight;
    camera.updateProjectionMatrix();
    renderer.setSize(window.innerWidth, window.innerHeight);
  });
</script>

</body>
</html>
