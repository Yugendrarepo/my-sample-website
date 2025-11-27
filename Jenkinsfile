<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Yugendra’s Simple Project — Jenkins + Webhook + Docker (Interview Demo)</title>
  <style>
    :root{
      --bg1:#0f172a;--bg2:#0b1220;--accent:#7c3aed;--accent-2:#06b6d4;
      --muted:rgba(255,255,255,0.75);--mono:"Courier New",monospace;
      --radius:12px;--container-max:1100px;
    }
    *{box-sizing:border-box}
    body{
      margin:0;font-family:Inter,system-ui,-apple-system,"Segoe UI",Roboto,Arial;
      background:linear-gradient(180deg,var(--bg1),var(--bg2));
      color:#e6eef8;line-height:1.45;min-height:100vh;
      -webkit-font-smoothing:antialiased;-moz-osx-font-smoothing:grayscale;
    }
    .wrap{max-width:var(--container-max);margin:36px auto;padding:28px;}
    header{display:flex;gap:20px;align-items:flex-start;margin-bottom:20px;}
    .logo{width:72px;height:72px;border-radius:14px;
      background:linear-gradient(135deg,var(--accent),var(--accent-2));
      display:flex;align-items:center;justify-content:center;font-weight:700;color:white;
      box-shadow:0 8px 30px rgba(12,12,40,0.6);flex-shrink:0;font-size:22px;}
    h1{font-size:28px;margin:0}
    p.lead{margin:6px 0 0;color:var(--muted);font-size:14px}
    .sub{color:var(--muted);font-size:13px;margin-top:6px}
    .badge{background:rgba(255,255,255,0.06);padding:5px 10px;border-radius:8px;font-size:12px;color:#fff;border:1px solid rgba(255,255,255,0.06);margin-right:8px;display:inline-block}
    .grid{display:grid;grid-template-columns:1fr 360px;gap:22px;margin-top:22px}
    @media(max-width:980px){.grid{grid-template-columns:1fr}}
    .card{background:linear-gradient(180deg,rgba(255,255,255,0.02),rgba(255,255,255,0.01));padding:22px;border-radius:var(--radius);box-shadow:0 8px 30px rgba(2,6,23,0.6);border:1px solid rgba(255,255,255,0.03);margin-bottom:16px}
    .section-title{font-size:18px;margin-top:6px;margin-bottom:12px;font-weight:600;display:flex;align-items:center;gap:10px;border-left:4px solid var(--accent);padding-left:10px}
    .code{background:rgba(255,255,255,0.06);padding:14px;border-radius:10px;font-family:var(--mono);font-size:13px;overflow-x:auto;white-space:pre;border:1px solid rgba(255,255,255,0.04);color:#eaf2ff;margin-top:8px}
    .small{color:var(--muted);font-size:13px}
    .flow{display:flex;gap:12px;align-items:center;justify-content:space-between;flex-wrap:wrap;margin-top:12px}
    .flow .step{background:linear-gradient(180deg,rgba(255,255,255,0.015),rgba(255,255,255,0.01));padding:12px;border-radius:10px;flex:1 1 150px;text-align:center;border:1px solid rgba(255,255,255,0.03);font-weight:600}
    .flow .arrow{width:28px;text-align:center;color:var(--muted)}
    .kbd{background:rgba(255,255,255,0.04);padding:4px 8px;border-radius:6px;font-family:var(--mono);font-size:13px;border:1px solid rgba(255,255,255,0.03)}
    footer{margin-top:18px;text-align:center;color:var(--muted);font-size:13px}
    @media(max-width:600px){
      .wrap{padding:18px;margin:18px auto}
      .logo{width:60px;height:60px;font-size:18px}
      h1{font-size:22px}
      .badge{font-size:11px;padding:4px 8px}
      .card{padding:16px}
      .section-title{font-size:16px}
      .flow .step{flex:1 1 100%}
      .flow .arrow{display:none}
      .code{font-size:12px}
    }
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <div class="logo">YP</div>
      <div style="flex:1">
        <h1>Yugendra’s Simple Project</h1>
        <p class="lead">Interview-ready demo: CI/CD using <strong>GitHub → Webhook → Jenkins → Docker → Ngrok</strong></p>
        <p class="sub">Created by <strong>Yugendra Prasad</strong> — a small, practical project to demonstrate automation and live demo skills.</p>
        <div style="margin-top:10px">
          <span class="badge">Interview Project</span>
          <span class="badge">CI / CD</span>
          <span class="badge">Jenkins</span>
          <span class="badge">Docker</span>
        </div>
      </div>
    </header>

    <div class="grid">
      <main>
        <div class="card">
          <div class="section-title">What this project shows</div>
          <p class="small">A one-page site that documents how I built this profile. The repo contains <code class="kbd">index.html</code> (this page) and a <code class="kbd">Dockerfile</code>. Pushing to GitHub triggers Jenkins (via webhook) which builds and deploys the image to port <strong>8081</strong>.</p>
        </div>

        <div class="card">
          <div class="section-title">🚀 End-to-End Flow (Short)</div>
          <div class="small">Commit → GitHub (push) → GitHub webhook → Jenkins job → Docker image build → Stop old container → Run new container on host port 8081 → Ngrok (optional) for public demo.</div>

          <div style="margin-top:12px" class="small"><strong>Commands / snippets</strong></div>

          <h4 style="margin-top:10px">Index (minimal)</h4>
          <div class="code">&lt;!doctype html&gt;
&lt;html&gt;&lt;head&gt;&lt;meta charset="utf-8"&gt;&lt;meta name="viewport" content="width=device-width,initial-scale=1"&gt;&lt;title&gt;Yugendra's Simple Project&lt;/title&gt;&lt;/head&gt;&lt;body&gt;&lt;h1&gt;Hello from Yugendra's Simple Project&lt;/h1&gt;&lt;/body&gt;&lt;/html&gt;</div>

          <h4 style="margin-top:10px">Dockerfile</h4>
          <div class="code">FROM nginx:alpine
COPY index.html /usr/share/nginx/html/index.html</div>

          <h4 style="margin-top:10px">Jenkinsfile</h4>
          <div class="code">pipeline {
  agent any
  stages {
    stage('Checkout'){ steps { git branch: 'main', url: 'https://github.com/Yugendrarepo/my-sample-website' } }
    stage('Build'){ steps { sh 'docker build -t sample-website .' } }
    stage('Stop'){ steps { sh 'docker stop sample-container || true'; sh 'docker rm sample-container || true' } }
    stage('Run'){ steps { sh 'docker run -d --name sample-container -p 8081:80 sample-website' } }
  }
  post { success { echo 'deployed' } failure { echo 'failed' } }
}</div>

          <h4 style="margin-top:10px">Ngrok (demo)</h4>
          <div class="code">ngrok http 8081</div>

        </div>

        <div class="card">
          <div class="section-title">Verification & Deploy steps</div>
          <ol class="small">
            <li>Save this updated <code class="kbd">index.html</code> into your repo and commit.</li>
            <li>If Jenkins builds from the repo automatically, push to GitHub so webhook triggers the Jenkins pipeline.</li>
            <li>Or locally rebuild & redeploy the Docker image:</li>
          </ol>

          <div class="code"># from repo root
docker build -t sample-website .
docker stop sample-container || true
docker rm sample-container || true
docker run -d --name sample-container -p 8081:80 sample-website
# verify
docker ps
docker logs -f sample-container
curl http://localhost:8081</div>

          <div style="margin-top:8px" class="small">If Jenkins handles build/deploy, just push and check Jenkins console for completion; then verify <code class="kbd">http://localhost:8081</code> or the ngrok URL.</div>
        </div>

        <div class="card">
          <div class="section-title">Troubleshooting</div>
          <ul class="small">
            <li>Still seeing old content? Do a hard refresh (Ctrl+F5) or clear cache — browsers often cache static index.html.</li>
            <li>If Jenkins runs but page is unchanged, confirm Jenkins actually pulled the new commit (check pipeline console & workspace files).</li>
            <li>If ngrok URL shows old content, restart ngrok after redeploy.</li>
          </ul>
        </div>

        <div class="card">
          <div class="section-title">Final note</div>
          <p class="small">This page is intentionally minimal and interview-ready — created by <strong>Yugendra Prasad</strong>. Use the ngrok link to show a live demo during interviews.</p>
        </div>
      </main>

      <aside>
        <div class="card">
          <div class="section-title">Project summary</div>
          <p class="small">This page documents how the project was created and deployed. Repo: <a href="https://github.com/Yugendrarepo/my-sample-website" style="color:#bfefff">github.com/Yugendrarepo/my-sample-website</a></p>
        </div>

        <div class="card" style="margin-top:16px">
          <div class="section-title">Author</div>
          <p class="small"><strong>Yugendra Prasad</strong><br>DevOps Engineer</p>
        </div>
      </aside>
    </div>

    <footer>© 2025 • Interview demo by <strong>Yugendra Prasad</strong></footer>
  </div>
</body>
</html>
