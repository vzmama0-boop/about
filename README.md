<head>
<meta charset="UTF-8">
<title>About Me</title>

<style>
  :root {
    --black: #0F0F0F;
    --brown: #6B4F3F;
    --soft-brown: #A0785A;
    --off-white: #EDE6DF;
  }

  body {
    background: var(--black);
    color: var(--off-white);
    font-family: Arial, sans-serif;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  /* BUTTON */
  #aboutBtn {
    background: var(--brown);
    color: var(--off-white);
    border: none;
    padding: 12px 24px;
    font-size: 14px;
    cursor: pointer;
    letter-spacing: 1px;
  }

  #aboutBtn:hover {
    background: var(--soft-brown);
  }

  /* MODAL */
  .modal {
    display: none;
    position: fixed;
    inset: 0;
    background: rgba(15,15,15,0.95);
  }

  .modal-content {
    background: var(--black);
    border: 1px solid var(--soft-brown);
    max-width: 400px;
    margin: 20% auto;
    padding: 25px;
  }

  .modal-content h2 {
    color: var(--brown);
    margin-bottom: 10px;
    letter-spacing: 2px;
  }

  .modal-content p {
    font-size: 14px;
    opacity: 0.9;
  }

  .close {
    color: var(--soft-brown);
    font-size: 22px;
    float: right;
    cursor: pointer;
  }

  .close:hover {
    color: var(--brown);
  }
</style>
</head>

<body>

<!-- Button -->
<button id="aboutBtn">About Me</button>

<!-- Modal -->
<div id="aboutModal" class="modal">
  <div class="modal-content">
    <span class="close">&times;</span>
    <h2>About Me</h2>
    <p>
     Hi I am Vzmama. I enjoy car culture and created this platform to share 
  automotive experiences and events with others who appreciate it.
    </p>
  </div>
</div>

<script>
  const btn = document.getElementById("aboutBtn");
  const modal = document.getElementById("aboutModal");
  const close = document.querySelector(".close");

  btn.onclick = () => modal.style.display = "block";
  close.onclick = () => modal.style.display = "none";

  window.onclick = (e) => {
    if (e.target === modal) modal.style.display = "none";
  };
</script>

</body>
