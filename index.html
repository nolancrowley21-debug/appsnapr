<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>AppSnapr — On-Device AI App Builder</title>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --bg: #0d0d0d;
      --surface: #161616;
      --surface2: #1c1c1c;
      --border: #2a2a2a;
      --cyan: #00e5ff;
      --violet: #a855f7;
      --yellow: #f7c948;
      --text: #e2e2e2;
      --muted: #666;
      --code-bg: #0a0a0a;
    }

    body {
      background: var(--bg);
      color: var(--text);
      font-family: system-ui, -apple-system, sans-serif;
      height: 100vh;
      display: flex;
      flex-direction: column;
      overflow: hidden;
    }

    /* ── Header ───────────────────────────────────── */
    header {
      display: flex;
      align-items: center;
      gap: 14px;
      padding: 10px 20px;
      background: var(--surface);
      border-bottom: 1px solid var(--border);
      flex-shrink: 0;
      user-select: none;
    }
    header h1 {
      font-size: 1.05rem;
      font-weight: 800;
      background: linear-gradient(90deg, var(--cyan), var(--violet));
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      letter-spacing: 0.06em;
    }
    .header-sub {
      color: var(--muted);
      font-size: 0.75rem;
    }
    .lang-badges {
      display: flex;
      gap: 7px;
      margin-left: auto;
    }
    .badge {
      padding: 3px 11px;
      border-radius: 20px;
      font-size: 0.7rem;
      font-weight: 700;
      letter-spacing: 0.1em;
      border: 1px solid var(--border);
      color: var(--muted);
      transition: all 0.25s ease;
    }
    .badge.active-html {
      border-color: var(--cyan);
      color: var(--cyan);
      box-shadow: 0 0 10px rgba(0,229,255,0.25);
      background: rgba(0,229,255,0.06);
    }
    .badge.active-js {
      border-color: var(--yellow);
      color: var(--yellow);
      box-shadow: 0 0 10px rgba(247,201,72,0.25);
      background: rgba(247,201,72,0.06);
    }

    /* ── Prompt bar ───────────────────────────────── */
    .prompt-bar {
      display: flex;
      gap: 10px;
      padding: 11px 20px;
      background: var(--surface);
      border-bottom: 1px solid var(--border);
      flex-shrink: 0;
    }
    .prompt-bar input {
      flex: 1;
      background: var(--bg);
      border: 1px solid var(--border);
      border-radius: 8px;
      padding: 10px 14px;
      color: var(--text);
      font-size: 0.92rem;
      outline: none;
      transition: border-color 0.2s, box-shadow 0.2s;
    }
    .prompt-bar input:focus {
      border-color: var(--cyan);
      box-shadow: 0 0 0 3px rgba(0,229,255,0.08);
    }
    .prompt-bar input::placeholder { color: var(--muted); }
    .btn-generate {
      background: linear-gradient(135deg, var(--cyan), var(--violet));
      border: none;
      border-radius: 8px;
      padding: 10px 22px;
      color: #000;
      font-weight: 800;
      font-size: 0.88rem;
      cursor: pointer;
      transition: opacity 0.2s, transform 0.15s, box-shadow 0.2s;
      white-space: nowrap;
      letter-spacing: 0.02em;
    }
    .btn-generate:hover:not(:disabled) {
      opacity: 0.92;
      transform: translateY(-1px);
      box-shadow: 0 4px 20px rgba(0,229,255,0.2);
    }
    .btn-generate:disabled { opacity: 0.35; cursor: not-allowed; transform: none; }

    /* ── Example chips ────────────────────────────── */
    .examples {
      display: flex;
      align-items: center;
      gap: 7px;
      padding: 7px 20px;
      background: var(--surface);
      border-bottom: 1px solid var(--border);
      flex-wrap: wrap;
      flex-shrink: 0;
    }
    .ex-label { color: var(--muted); font-size: 0.72rem; margin-right: 2px; }
    .chip {
      background: none;
      border: 1px solid var(--border);
      border-radius: 20px;
      color: var(--muted);
      font-size: 0.72rem;
      padding: 3px 10px;
      cursor: pointer;
      transition: border-color 0.2s, color 0.2s, background 0.2s;
      font-family: inherit;
    }
    .chip:hover {
      border-color: var(--cyan);
      color: var(--cyan);
      background: rgba(0,229,255,0.05);
    }

    /* ── Panels ───────────────────────────────────── */
    .panels {
      display: flex;
      flex: 1;
      overflow: hidden;
      min-height: 0;
    }
    .panel {
      flex: 1;
      display: flex;
      flex-direction: column;
      overflow: hidden;
      min-width: 0;
    }
    .panel:first-child { border-right: 1px solid var(--border); }

    .panel-header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 7px 14px;
      background: var(--surface2);
      border-bottom: 1px solid var(--border);
      font-size: 0.7rem;
      font-weight: 700;
      letter-spacing: 0.12em;
      color: var(--muted);
      flex-shrink: 0;
    }
    .btn-icon {
      background: none;
      border: 1px solid var(--border);
      border-radius: 6px;
      color: var(--text);
      font-size: 0.72rem;
      padding: 4px 10px;
      cursor: pointer;
      transition: border-color 0.2s, color 0.2s, background 0.2s;
      font-family: inherit;
      font-weight: 600;
    }
    .btn-icon:hover { border-color: var(--cyan); color: var(--cyan); }
    .btn-icon:disabled { opacity: 0.3; cursor: not-allowed; }

    /* ── Code panel ───────────────────────────────── */
    #code-panel {
      margin: 0;
      border-radius: 0;
      background: var(--code-bg);
      flex: 1;
      overflow: auto;
      padding: 16px 18px;
      font-size: 0.8rem;
      line-height: 1.65;
      tab-size: 2;
      min-height: 0;
    }
    #code-el {
      font-family: 'Fira Code', 'Cascadia Code', 'Consolas', monospace;
      white-space: pre-wrap;
      word-break: break-word;
    }
    .streaming #code-el { color: #b0b0b0; }

    .placeholder-msg {
      color: var(--muted);
      font-size: 0.82rem;
      font-style: italic;
      font-family: system-ui, sans-serif;
    }

    /* ── Preview panel ────────────────────────────── */
    #preview-iframe {
      flex: 1;
      border: none;
      background: #fff;
      display: block;
      min-height: 0;
    }

    .btn-download {
      background: linear-gradient(135deg, var(--cyan), var(--violet));
      border: none;
      border-radius: 7px;
      padding: 8px 18px;
      color: #000;
      font-weight: 800;
      font-size: 0.78rem;
      cursor: pointer;
      transition: opacity 0.2s, transform 0.15s;
      letter-spacing: 0.02em;
    }
    .btn-download:hover:not(:disabled) { opacity: 0.85; transform: translateY(-1px); }
    .btn-download:disabled { opacity: 0.3; cursor: not-allowed; }

    /* ── Loading overlay ──────────────────────────── */
    #loading-overlay {
      position: fixed;
      inset: 0;
      background: rgba(10,10,10,0.97);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: 18px;
      z-index: 100;
      backdrop-filter: blur(4px);
    }
    #loading-overlay h2 {
      font-size: 1.5rem;
      font-weight: 800;
      background: linear-gradient(90deg, var(--cyan), var(--violet));
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      letter-spacing: 0.06em;
    }
    #loading-overlay .loading-sub {
      color: var(--muted);
      font-size: 0.9rem;
    }
    .progress-wrap {
      width: 340px;
      height: 5px;
      background: var(--border);
      border-radius: 3px;
      overflow: hidden;
    }
    #progress-bar {
      height: 100%;
      width: 0%;
      background: linear-gradient(90deg, var(--cyan), var(--violet));
      border-radius: 3px;
      transition: width 0.4s ease;
    }
    #loading-status {
      color: #555;
      font-size: 0.78rem;
      min-height: 1.2em;
      max-width: 340px;
      text-align: center;
      line-height: 1.4;
    }
    .loading-note {
      font-size: 0.72rem;
      color: #3a3a3a;
      max-width: 300px;
      text-align: center;
      line-height: 1.5;
    }

    /* ── Edit bar ────────────────────────────────────── */
    #edit-bar {
      display: none;
      align-items: center;
      gap: 10px;
      padding: 10px 20px;
      background: var(--surface);
      border-top: 1px solid var(--border);
      flex-shrink: 0;
    }
    #edit-bar .edit-label {
      font-size: 0.75rem;
      font-weight: 700;
      color: var(--violet);
      white-space: nowrap;
      letter-spacing: 0.05em;
    }
    #edit-input {
      flex: 1;
      background: var(--bg);
      border: 1px solid var(--violet);
      border-radius: 8px;
      padding: 9px 14px;
      color: var(--text);
      font-size: 0.9rem;
      outline: none;
      transition: border-color 0.2s, box-shadow 0.2s;
      font-family: inherit;
    }
    #edit-input:focus {
      border-color: var(--cyan);
      box-shadow: 0 0 0 3px rgba(168,85,247,0.12);
    }
    #edit-input::placeholder { color: var(--muted); }
    #btn-edit {
      background: linear-gradient(135deg, var(--violet), var(--cyan));
      border: none;
      border-radius: 8px;
      padding: 9px 20px;
      color: #000;
      font-weight: 800;
      font-size: 0.86rem;
      cursor: pointer;
      transition: opacity 0.2s, transform 0.15s;
      white-space: nowrap;
      font-family: inherit;
    }
    #btn-edit:hover:not(:disabled) { opacity: 0.88; transform: translateY(-1px); }
    #btn-edit:disabled { opacity: 0.35; cursor: not-allowed; transform: none; }

    /* ── WebGPU error ─────────────────────────────── */
    #webgpu-error {
      display: none;
      position: fixed;
      inset: 0;
      background: var(--bg);
      align-items: center;
      justify-content: center;
      flex-direction: column;
      gap: 14px;
      text-align: center;
      padding: 40px;
      z-index: 200;
    }
    #webgpu-error .err-icon { font-size: 2.5rem; }
    #webgpu-error h2 { color: #f87171; font-size: 1.15rem; }
    #webgpu-error p { color: var(--muted); max-width: 420px; line-height: 1.65; font-size: 0.9rem; }
    #webgpu-error a { color: var(--cyan); text-decoration: none; }
    #webgpu-error a:hover { text-decoration: underline; }
    #webgpu-error code {
      background: var(--surface);
      padding: 2px 6px;
      border-radius: 4px;
      font-size: 0.85em;
      color: var(--yellow);
    }
  </style>

  <!-- Prism.js syntax highlighting -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism-tomorrow.min.css" />
  <script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/components/prism-core.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/plugins/autoloader/prism-autoloader.min.js"></script>
</head>
<body>

  <!-- ── WebGPU error screen ───────────────────────────── -->
  <div id="webgpu-error">
    <div class="err-icon">⚠️</div>
    <h2>WebGPU Not Available</h2>
    <p>
      AppSnapr runs a real AI model directly on your GPU — no server, no API key needed.
      Please open this file in <a href="https://www.google.com/chrome/" target="_blank">Chrome 113+</a>
      and make sure <strong>Hardware Acceleration</strong> is enabled in
      <code>Settings → System</code>.
    </p>
    <p style="margin-top:6px;">
      You can also enable WebGPU at <code>chrome://flags/#enable-unsafe-webgpu</code>.
    </p>
  </div>

  <!-- ── Loading overlay ───────────────────────────────── -->
  <div id="loading-overlay">
    <h2>⚡ AppSnapr</h2>
    <p class="loading-sub">Loading AI model onto your device...</p>
    <div class="progress-wrap">
      <div id="progress-bar"></div>
    </div>
    <div id="loading-status">Initializing...</div>
    <p class="loading-note">
      First visit downloads ~2.2 GB to your browser cache.
      After that, the model loads instantly — no internet needed.
    </p>
  </div>

  <!-- ── Header ────────────────────────────────────────── -->
  <header>
    <h1>⚡ AppSnapr</h1>
    <span class="header-sub">On-device AI &nbsp;·&nbsp; No account &nbsp;·&nbsp; No server</span>
    <div class="lang-badges">
      <span class="badge" id="badge-html">HTML</span>
      <span class="badge" id="badge-js">JS</span>
    </div>
  </header>

  <!-- ── Prompt bar ─────────────────────────────────────── -->
  <div class="prompt-bar">
    <input
      id="prompt-input"
      type="text"
      placeholder='Describe your app — e.g. "a snake game", "a budget tracker", "a password generator"'
      autocomplete="off"
      spellcheck="false"
    />
    <button class="btn-generate" id="btn-generate" disabled>Generate ▶</button>
  </div>

  <!-- ── Example chips ──────────────────────────────────── -->
  <div class="examples">
    <span class="ex-label">Try:</span>
    <button class="chip" onclick="fillPrompt('a snake game')">snake game</button>
    <button class="chip" onclick="fillPrompt('a to-do list app')">to-do list</button>
    <button class="chip" onclick="fillPrompt('a countdown timer')">countdown timer</button>
    <button class="chip" onclick="fillPrompt('a budget expense tracker')">expense tracker</button>
    <button class="chip" onclick="fillPrompt('a password generator')">password generator</button>
    <button class="chip" onclick="fillPrompt('a drawing canvas app')">drawing canvas</button>
    <button class="chip" onclick="fillPrompt('a pomodoro focus timer')">pomodoro timer</button>
    <button class="chip" onclick="fillPrompt('a BMI calculator')">BMI calculator</button>
  </div>

  <!-- ── Main panels ────────────────────────────────────── -->
  <div class="panels">

    <!-- Code panel -->
    <div class="panel">
      <div class="panel-header">
        <span>CODE</span>
        <button class="btn-icon" id="btn-copy">Copy</button>
      </div>
      <pre id="code-panel"><code id="code-el" class="language-html"><span class="placeholder-msg">Your generated code will appear here...</span></code></pre>
    </div>

    <!-- Preview panel — always a live running app -->
    <div class="panel">
      <div class="panel-header">
        <span>LIVE PREVIEW</span>
        <button class="btn-download btn-icon" id="btn-download" disabled>⬇ Download</button>
      </div>
      <iframe id="preview-iframe" sandbox="allow-scripts allow-forms allow-modals"></iframe>
    </div>

  </div>

  <!-- ── Edit bar ──────────────────────────────────────────── -->
  <div id="edit-bar">
    <span class="edit-label">✏️ Edit:</span>
    <input
      id="edit-input"
      type="text"
      placeholder='Tell the bot what to change — e.g. "make it dark mode", "add a reset button", "fix the bug where..."'
      autocomplete="off"
      spellcheck="false"
    />
    <button id="btn-edit">Apply ▶</button>
  </div>

  <!-- ── Main script ────────────────────────────────────── -->
  <script type="module">
    import * as webllm from 'https://esm.run/@mlc-ai/web-llm';

    // ── Model ──────────────────────────────────────────────
    // Qwen2.5-Coder-7B is purpose-built for code — much better app quality.
    // Requires ~4 GB VRAM. If it fails to load, fall back to the smaller model below.
    const MODEL_ID = 'Qwen2.5-Coder-7B-Instruct-q4f16_1-MLC';
    // const MODEL_ID = 'Phi-3.5-mini-instruct-q4f16_1-MLC'; // fallback for low VRAM

    // ── DOM refs ───────────────────────────────────────────
    const overlay      = document.getElementById('loading-overlay');
    const statusEl     = document.getElementById('loading-status');
    const progressEl   = document.getElementById('progress-bar');
    const btnGen       = document.getElementById('btn-generate');
    const webgpuErr    = document.getElementById('webgpu-error');
    const codePanel    = document.getElementById('code-panel');
    const codeEl       = document.getElementById('code-el');
    const previewFrame = document.getElementById('preview-iframe');
    const btnDownload  = document.getElementById('btn-download');
    const btnCopy      = document.getElementById('btn-copy');
    const editBar      = document.getElementById('edit-bar');
    const editInput    = document.getElementById('edit-input');
    const btnEdit      = document.getElementById('btn-edit');

    // ── State ──────────────────────────────────────────────
    let engine      = null;
    let currentCode = '';
    let currentLang = 'html';

    // ── System prompts ─────────────────────────────────────
    // Always outputs a single self-contained HTML file so the preview
    // is always a live, usable, interactive app in the iframe.
    const SYSTEM_PROMPT = `You are a senior web developer. Output a single self-contained HTML file for the requested app.

FORMAT RULES (critical):
- Line 1: LANG: JS  (or LANG: HTML for purely static pages)
- Line 2: <!DOCTYPE html>
- Then: the complete HTML. Nothing else. No markdown fences, no explanation, no comments outside the code.

CODE RULES:
- All CSS and JS must be inline inside the HTML file. Zero external dependencies.
- Every feature must be fully implemented — no placeholders, no "TODO", no mock data.
- The app must work perfectly the first time with no errors.

QUALITY RULES — this is the most important section:
- Use a polished dark UI by default: dark backgrounds (#0f0f0f or similar), vibrant accent colors, smooth CSS transitions.
- Typography: use system fonts or Google Fonts (loaded via @import in the <style> tag).
- Layout: use CSS Grid or Flexbox properly. Everything must be aligned and spaced well.
- Games: must have a game loop, score, game over screen, restart button, and responsive controls.
- Tools/calculators: must have clear labels, input validation, and formatted output.
- Timers: must actually count, have start/pause/reset, and display MM:SS format.
- Lists/trackers: must support adding, completing, and deleting items, with data persisting via localStorage.
- Every button must have a hover state. Every input must have a focus style.
- No plain white backgrounds. No default browser styles left unstyled.`;

    const EDIT_PROMPT = `You are a web developer editing an existing single-file HTML app based on the user's request.
Rules:
1. Output ONLY the complete updated HTML file. Start directly with <!DOCTYPE html> — no LANG: header, no markdown fences, no explanation.
2. Apply the requested change precisely. Keep everything else working exactly as it was.
3. The entire file must remain fully functional after your edit.`;

    // ── WebGPU check ───────────────────────────────────────
    if (!navigator.gpu) {
      overlay.style.display = 'none';
      webgpuErr.style.display = 'flex';
      throw new Error('WebGPU not available');
    }

    // ── Engine init ────────────────────────────────────────
    function onProgress(report) {
      if (report.text) statusEl.textContent = report.text;
      if (typeof report.progress === 'number') {
        progressEl.style.width = Math.min(100, report.progress * 100).toFixed(1) + '%';
      }
    }

    async function initEngine() {
      try {
        engine = await webllm.CreateMLCEngine(MODEL_ID, {
          initProgressCallback: onProgress,
        });
        overlay.style.display = 'none';
        btnGen.disabled = false;
        window._appsnaprReady = true;
      } catch (err) {
        statusEl.textContent = '❌ ' + (err.message || 'Failed to load model');
        console.error('[AppSnapr] Engine init error:', err);
      }
    }

    initEngine();

    // ── Badge helper ───────────────────────────────────────
    function setActiveBadge(lang) {
      document.getElementById('badge-html').className = 'badge' + (lang === 'html' ? ' active-html' : '');
      document.getElementById('badge-js').className   = 'badge' + (lang === 'js'   ? ' active-js'   : '');
    }

    // ── Clean model output ─────────────────────────────────
    // Models often wrap output in ```html ... ``` despite instructions.
    // Strip fences, stray LANG: lines, and leading whitespace.
    function cleanCode(raw) {
      let s = raw.trim();
      // Strip any leading LANG: line the streaming loop didn't catch
      s = s.replace(/^LANG:\s*\S+\s*\n?/i, '').trim();
      // Strip opening fence: ```html, ```javascript, ``` etc.
      s = s.replace(/^```[\w]*\s*\n?/, '').trim();
      // Strip closing fence
      s = s.replace(/\n?```\s*$/, '').trim();
      // Truncate anything after </html> — catches trailing 0s and model noise
      const closeHtml = s.lastIndexOf('</html>');
      if (closeHtml !== -1) s = s.slice(0, closeHtml + 7);
      return s.trim();
    }

    // ── Syntax highlight ───────────────────────────────────
    function highlightCode(lang) {
      const prismLang = lang === 'js' ? 'javascript' : 'markup';
      codeEl.className = 'language-' + prismLang;
      codeEl.textContent = currentCode;
      if (window.Prism) Prism.highlightElement(codeEl);
    }

    // ── Download ───────────────────────────────────────────
    function downloadCode() {
      if (!currentCode) return;
      const blob = new Blob([currentCode], { type: 'text/html' });
      const url  = URL.createObjectURL(blob);
      const a    = Object.assign(document.createElement('a'), { href: url, download: 'app.html' });
      document.body.appendChild(a);
      a.click();
      a.remove();
      URL.revokeObjectURL(url);
    }

    btnDownload.addEventListener('click', downloadCode);

    // ── Copy ───────────────────────────────────────────────
    btnCopy.addEventListener('click', async () => {
      if (!currentCode) return;
      try {
        await navigator.clipboard.writeText(currentCode);
        btnCopy.textContent = 'Copied!';
        setTimeout(() => { btnCopy.textContent = 'Copy'; }, 1600);
      } catch {
        btnCopy.textContent = 'Failed';
        setTimeout(() => { btnCopy.textContent = 'Copy'; }, 1600);
      }
    });

    // ── Fill prompt (called by chips) ──────────────────────
    window.fillPrompt = function(text) {
      document.getElementById('prompt-input').value = text;
      document.getElementById('prompt-input').focus();
    };

    // ── Generate ───────────────────────────────────────────
    async function generate(prompt) {
      if (!engine) return;

      // Reset UI
      btnGen.disabled      = true;
      btnGen.textContent   = '⏳ Generating...';
      btnDownload.disabled = true;
      codeEl.textContent   = '';
      codeEl.className     = 'language-html';
      codePanel.classList.add('streaming');
      currentCode = '';
      currentLang = 'html';
      setActiveBadge('');
      previewFrame.src = 'about:blank';

      let buffer       = '';
      let langDetected = false;

      try {
        const stream = await engine.chat.completions.create({
          messages: [
            { role: 'system', content: SYSTEM_PROMPT },
            { role: 'user',   content: 'Build this app: ' + prompt },
          ],
          stream:      true,
          temperature: 0.25,
          max_tokens:  4096,
        });

        for await (const chunk of stream) {
          if (chunk.choices[0]?.finish_reason) break;
          const delta = chunk.choices[0]?.delta?.content;
          if (typeof delta !== 'string' || !delta) continue;
          buffer += delta;

          // Detect LANG: header from first line
          if (!langDetected) {
            const newlineIdx = buffer.indexOf('\n');
            if (newlineIdx !== -1) {
              const firstLine = buffer.slice(0, newlineIdx).trim();
              if (firstLine.startsWith('LANG:')) {
                const tag = firstLine.replace('LANG:', '').trim().toLowerCase();
                currentLang = (tag === 'js' || tag === 'javascript') ? 'js' : 'html';
                setActiveBadge(currentLang);
                buffer = buffer.slice(newlineIdx + 1);
              }
              langDetected = true;
            }
          }

          currentCode = buffer;
          codeEl.textContent = buffer;
        }

      } catch (err) {
        codeEl.textContent = '// Error: ' + err.message;
        console.error('[AppSnapr] Generation error:', err);
      }

      // Finalize — clean output, highlight, load live preview
      currentCode = cleanCode(currentCode);
      codePanel.classList.remove('streaming');
      highlightCode(currentLang);

      // Use a Blob URL for the iframe — more reliable than srcdoc for local files
      if (currentCode) {
        const blob = new Blob([currentCode], { type: 'text/html' });
        const url  = URL.createObjectURL(blob);
        // Revoke previous blob URL to avoid memory leaks
        if (previewFrame._blobUrl) URL.revokeObjectURL(previewFrame._blobUrl);
        previewFrame._blobUrl = url;
        previewFrame.src = url;
        btnDownload.disabled = false;
      }

      btnGen.disabled    = false;
      btnGen.textContent = 'Generate ▶';
      if (currentCode) editBar.style.display = 'flex';
    }

    // ── Generate edit ──────────────────────────────────────
    async function generateEdit(request) {
      if (!engine || !currentCode) return;

      btnEdit.disabled    = true;
      btnEdit.textContent = '⏳ Editing...';
      btnGen.disabled     = true;
      codeEl.textContent  = '';
      codePanel.classList.add('streaming');
      previewFrame.src    = 'about:blank';

      let buffer = '';

      try {
        const stream = await engine.chat.completions.create({
          messages: [
            { role: 'system', content: EDIT_PROMPT },
            { role: 'user',   content: `Current code:\n${currentCode}\n\nEdit request: ${request}` },
          ],
          stream:      true,
          temperature: 0.2,
          max_tokens:  4096,
        });

        for await (const chunk of stream) {
          if (chunk.choices[0]?.finish_reason) break;
          const delta = chunk.choices[0]?.delta?.content;
          if (typeof delta !== 'string' || !delta) continue;
          buffer += delta;
          codeEl.textContent = buffer;
        }

      } catch (err) {
        codeEl.textContent = '// Edit error: ' + err.message;
        console.error('[AppSnapr] Edit error:', err);
      }

      // Finalize
      currentCode = cleanCode(buffer);
      codePanel.classList.remove('streaming');
      highlightCode(currentLang);

      if (currentCode) {
        const blob = new Blob([currentCode], { type: 'text/html' });
        const url  = URL.createObjectURL(blob);
        if (previewFrame._blobUrl) URL.revokeObjectURL(previewFrame._blobUrl);
        previewFrame._blobUrl = url;
        previewFrame.src = url;
      }

      btnEdit.disabled    = false;
      btnEdit.textContent = 'Apply ▶';
      btnGen.disabled     = false;
      editInput.value     = '';
    }

    // ── Event wiring ───────────────────────────────────────
    btnGen.addEventListener('click', () => {
      const prompt = document.getElementById('prompt-input').value.trim();
      if (prompt) generate(prompt);
    });

    document.getElementById('prompt-input').addEventListener('keydown', e => {
      if (e.key === 'Enter') {
        const prompt = e.target.value.trim();
        if (prompt && !btnGen.disabled) generate(prompt);
      }
    });

    btnEdit.addEventListener('click', () => {
      const request = editInput.value.trim();
      if (request) generateEdit(request);
    });

    editInput.addEventListener('keydown', e => {
      if (e.key === 'Enter') {
        const request = editInput.value.trim();
        if (request && !btnEdit.disabled) generateEdit(request);
      }
    });
  </script>

</body>
</html>
