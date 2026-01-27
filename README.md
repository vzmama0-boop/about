<!-- Button -->
<button id="aboutBtn">About Me</button>

<!-- Modal -->
<div id="aboutModal" class="modal">
  <div class="modal-content">
    <span class="close">&times;</span>
    <h2>About Me</h2>
    <p>
      I’m Koi Fish, a young car enthusiast capturing moments at car meets and events.
      Photography is my way to tell stories through motion, details, and atmosphere.
    </p>
  </div>
</div>/* BUTTON */
#aboutBtn {
  background-color: var(--brown);
  color: var(--off-white);
  border: none;
  padding: 10px 20px;
  cursor: pointer;
  font-size: 14px;
  border-radius: 4px;
  transition: background 0.3s;
}
#aboutBtn:hover {
  background-color: var(--soft-brown);
}

/* MODAL */
.modal {
  display: none; /* hidden by default */
  position: fixed;
  z-index: 1000;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  overflow: auto;
  background-color: rgba(15,15,15,0.95);
}

.modal-content {
  background-color: var(--black);
  margin: 15% auto;
  padding: 30px;
  border: 1px solid var(--soft-brown);
  width: 80%;
  max-width: 500px;
  color: var(--off-white);
  border-radius: 8px;
}

.modal-content h2 {
  color: var(--brown);
  margin-bottom: 15px;
}

.close {
  color: var(--soft-brown);
  float: right;
  font-size: 28px;
  cursor: pointer;
}
.close:hover {
  color: var(--brown);
}
<script>
const modal = document.getElementById("aboutModal");
const btn = document.getElementById("aboutBtn");
const span = document.getElementsByClassName("close")[0];

btn.onclick = () => {
  modal.style.display = "block";
}

span.onclick = () => {
  modal.style.display = "none";
}

window.onclick = (event) => {
  if (event.target == modal) {
    modal.style.display = "none";
  }
}
</script>
