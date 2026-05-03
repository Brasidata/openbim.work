---
hide:
  - toc
---

<style>
.job-analyzer-container {
  max-width: 800px;
  margin: 0 auto;
  padding: 3rem 1.5rem;
  background: var(--md-default-bg-color);
  border-radius: 1.25rem;
  box-shadow: 0 4px 20px rgba(0,0,0,0.05);
  border: 1px solid rgba(0, 188, 212, 0.2);
  text-align: center;
}
html[data-md-color-scheme="slate"] .job-analyzer-container {
  background: var(--md-default-bg-color);
  box-shadow: 0 4px 20px rgba(0,0,0,0.25);
  border: 1px solid rgba(0, 188, 212, 0.4);
}

.job-analyzer-container h1 {
  font-size: 2rem;
  font-weight: 800;
  margin-bottom: 1rem;
  color: var(--md-default-fg-color);
}

.job-analyzer-container p.subtitle {
  font-size: 1.1rem;
  color: var(--md-default-fg-color--light);
  margin-bottom: 2rem;
}

.job-form {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
  text-align: left;
}

.form-group {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.form-group label {
  font-weight: 600;
  font-size: 0.95rem;
  color: var(--md-default-fg-color);
}

.form-control {
  width: 100%;
  padding: 1rem;
  border-radius: 0.5rem;
  border: 1px solid var(--md-default-fg-color--lightest);
  background: var(--md-default-bg-color);
  color: var(--md-default-fg-color);
  font-family: inherit;
  font-size: 1rem;
  resize: vertical;
  transition: border-color 0.2s;
}

.form-control:focus {
  outline: none;
  border-color: #00bcd4;
  box-shadow: 0 0 0 3px rgba(0, 188, 212, 0.1);
}

.toggle-group {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  cursor: pointer;
}

.toggle-group input[type="checkbox"] {
  width: 1.25rem;
  height: 1.25rem;
  cursor: pointer;
  accent-color: #00bcd4;
}

.toggle-group span {
  font-size: 0.95rem;
  color: var(--md-default-fg-color);
  user-select: none;
}

.btn-send {
  background-color: #00bcd4;
  color: #fff;
  border: none;
  padding: 1rem 2rem;
  border-radius: 999px;
  font-weight: 700;
  font-size: 1.1rem;
  cursor: pointer;
  transition: filter 0.2s;
  align-self: center;
  margin-top: 0.5rem;
}

.btn-send:hover {
  filter: brightness(0.9);
}
</style>

<div class="job-analyzer-container">
  <h1>Analisador de Vagas Open<span class="bd-accent">BIM</span></h1>
  <p class="subtitle">Cole o link da vaga ou o texto da descrição para obter uma análise completa do perfil requisitado.</p>

  <form id="job-form" class="job-form" method="POST" action="http://localhost:8080/analyze?lang=pt">
    <div class="form-group">
      <label for="job-input">Link da vaga ou texto da descrição:</label>
      <textarea id="job-input" name="job_text" class="form-control" rows="6" placeholder="https://linkedin.com/jobs/... ou cole o texto aqui"></textarea>
    </div>

    <label class="toggle-group">
      <input type="checkbox" id="auth-publish" name="auth_publish" value="true" checked>
      <span>Autorizo publicar essa vaga na nossa base de dados</span>
    </label>

    <button type="submit" class="btn-send">Enviar para Análise</button>
  </form>
</div>

<script>
  document.addEventListener("DOMContentLoaded", function() {
    var form = document.getElementById("job-form");
    if (form) {
      if (window.location.hostname === "localhost" || window.location.hostname === "127.0.0.1") {
        form.action = "http://localhost:8080/analyze?lang=pt";
      } else {
        form.action = "https://engine.openbim.work/analyze?lang=pt";
      }
    }
  });
</script>
