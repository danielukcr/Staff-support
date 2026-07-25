<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Staff Message Panel</title>
  <style>
    :root {
      --bg: #0f172a;
      --card: #111827;
      --accent: #3b82f6;
      --accent-soft: #1d4ed8;
      --text: #e5e7eb;
      --muted: #9ca3af;
      --border: #1f2937;
      --danger: #f97373;
      --warn: #facc15;
      --success: #22c55e;
    }

    * {
      box-sizing: border-box;
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "SF Pro Text",
        "Segoe UI", sans-serif;
    }

    body {
      margin: 0;
      padding: 32px;
      background: radial-gradient(circle at top, #1f2937 0, #020617 55%);
      color: var(--text);
      display: flex;
      justify-content: center;
    }

    .app {
      width: 100%;
      max-width: 1100px;
    }

    .header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 24px;
    }

    .title {
      font-size: 24px;
      font-weight: 600;
    }

    .subtitle {
      font-size: 13px;
      color: var(--muted);
    }

    .badge {
      padding: 6px 12px;
      border-radius: 999px;
      border: 1px solid var(--border);
      background: rgba(15, 23, 42, 0.8);
      font-size: 12px;
      display: inline-flex;
      align-items: center;
      gap: 6px;
    }

    .badge-dot {
      width: 8px;
      height: 8px;
      border-radius: 999px;
      background: var(--accent);
      box-shadow: 0 0 0 4px rgba(59, 130, 246, 0.25);
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
      gap: 16px;
    }

    .section {
      background: linear-gradient(145deg, #020617, #0b1120);
      border-radius: 16px;
      border: 1px solid var(--border);
      padding: 16px;
      box-shadow: 0 18px 40px rgba(0, 0, 0, 0.55);
      backdrop-filter: blur(16px);
    }

    .section-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 10px;
    }

    .section-title {
      font-size: 14px;
      font-weight: 600;
      letter-spacing: 0.03em;
      text-transform: uppercase;
      color: var(--muted);
    }

    .section-tag {
      font-size: 11px;
      padding: 4px 8px;
      border-radius: 999px;
      background: rgba(31, 41, 55, 0.8);
      color: var(--muted);
    }

    .message {
      position: relative;
      margin-bottom: 10px;
      padding: 10px 12px;
      border-radius: 12px;
      background: rgba(15, 23, 42, 0.9);
      border: 1px solid rgba(31, 41, 55, 0.9);
      display: flex;
      gap: 10px;
      align-items: flex-start;
    }

    .message-icon {
      width: 22px;
      height: 22px;
      border-radius: 999px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 13px;
      background: rgba(31, 41, 55, 0.9);
      flex-shrink: 0;
    }

    .message-content {
      font-size: 13px;
      line-height: 1.4;
    }

    .message-footer {
      font-size: 11px;
      color: var(--muted);
      margin-top: 4px;
    }

    .copy-btn {
      margin-left: auto;
      padding: 6px 10px;
      border-radius: 999px;
      border: 1px solid rgba(55, 65, 81, 0.9);
      background: rgba(15, 23, 42, 0.9);
      color: var(--muted);
      font-size: 11px;
      display: inline-flex;
      align-items: center;
      gap: 6px;
      cursor: pointer;
      transition: all 0.15s ease;
    }

    .copy-btn span {
      font-size: 12px;
    }

    .copy-btn:hover {
      border-color: var(--accent);
      color: var(--accent);
      background: rgba(15, 23, 42, 1);
      transform: translateY(-1px);
    }

    .copy-btn.copied {
      border-color: var(--success);
      color: var(--success);
    }

    .copy-btn.copied span {
      transform: scale(1.1);
    }

    .pill-row {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-top: 8px;
    }

    .pill {
      font-size: 11px;
      padding: 4px 8px;
      border-radius: 999px;
      background: rgba(31, 41, 55, 0.9);
      color: var(--muted);
    }

    .accent-warn {
      color: var(--warn);
    }

    .accent-danger {
      color: var(--danger);
    }

    .accent-success {
      color: var(--success);
    }

    @media (max-width: 720px) {
      body {
        padding: 18px;
      }
      .header {
        flex-direction: column;
        align-items: flex-start;
        gap: 8px;
      }
    }
  </style>
</head>
<body>
  <div class="app">
    <div class="header">
      <div>
        <div class="title">UKCR Staff Message Panel</div>
        <div class="subtitle">
          Click any <strong>Copy</strong> button to instantly copy that message.
        </div>
      </div>
      <div class="badge">
        <div class="badge-dot"></div>
        Live moderation toolkit
      </div>
    </div>

    <div class="grid">
      <!-- General support -->
      <div class="section">
        <div class="section-header">
          <div class="section-title">General support</div>
          <div class="section-tag">Front desk</div>
        </div>

        <div class="message">
          <div class="message-icon">👋</div>
          <div class="message-content">
            Hello! I am Senior Administrator Peely, how can I help you today?
            (If I am late say Void!)
          </div>
          <button class="copy-btn" data-text="Hello! I am Senior Administrator Peely, How can I help you today? (If I am late say Void!)">
            <span>⧉</span> Copy
          </button>
        </div>

        <div class="message">
          <div class="message-icon">💬</div>
          <div class="message-content">
            Anything else I can support you with today? If so, please state.
          </div>
          <button class="copy-btn" data-text="Anything else I can support you with today? if so please state.">
            <span>⧉</span> Copy
          </button>
        </div>

        <div class="message">
          <div class="message-icon">🌙</div>
          <div class="message-content">
            Alright! Have an amazing rest of your roleplay.
          </div>
          <button class="copy-btn" data-text="Alright! Have a amazing rest of your roleplay.">
            <span>⧉</span> Copy
          </button>
        </div>
      </div>

      <!-- Announcements -->
      <div class="section">
        <div class="section-header">
          <div class="section-title">Roleplay announcements</div>
          <div class="section-tag">Broadcast</div>
        </div>

        <div class="message">
          <div class="message-icon">☕</div>
          <div class="message-content">
            ☕ The café is now open! Come down to get a hot drink or a snack! ☕
          </div>
          <button class="copy-btn" data-text="☕ The café is now open! Come down to get a hot drink or a snack! ☕">
            <span>⧉</span> Copy
          </button>
        </div>

        <div class="message">
          <div class="message-icon">🍟</div>
          <div class="message-content">
            🍟 The Three guys is now open! Come down to get a burger or some fries!
          </div>
          <button class="copy-btn" data-text=" 🍟 The Three guys is now open! Come down to get a burger or some fries! ">
            <span>⧉</span> Copy
          </button>
        </div>

        <div class="message">
          <div class="message-icon">🚕</div>
          <div class="message-content">
            🚕 Taxi services are now available! Use the phone to direct a taxi to you! 🚕
          </div>
          <button class="copy-btn" data-text="🚕 Taxi services are now available! use the phone to direct a taxi to you! 🚕">
            <span>⧉</span> Copy
          </button>
        </div>

        <div class="message">
          <div class="message-icon accent-warn">⚠️</div>
          <div class="message-content">
            ⚠️ Please start to clear () or you will be loaded or receive moderation action.
            You have 10 seconds to comply. ⚠️
          </div>
          <button class="copy-btn" data-text="⚠️ Please start to clear () Or you will be loaded or receive moderation action. You have 10 seconds to comply. ⚠️">
            <span>⧉</span> Copy
          </button>
        </div>
      </div>

      <!-- Moderation actions -->
      <div class="section">
        <div class="section-header">
          <div class="section-title">Moderation actions</div>
          <div class="section-tag">Warnings & kicks</div>
        </div>

        <div class="message">
          <div class="message-icon accent-warn">⚠️</div>
          <div class="message-content">
            You are going to be warned for (). You are able to get 3 warnings;
            any more than that and you will be kicked.
          </div>
          <button class="copy-btn" data-text="You are going to be warned for (), You are able to get 3 warnings anymore than that you will be kicked.">
            <span>⧉</span> Copy
          </button>
        </div>

        <div class="message">
          <div class="message-icon accent-danger">⛔</div>
          <div class="message-content">
            Unfortunately, you are going to be kicked for (). Do not re-join
            before 30 minutes have passed or YOU WILL BE BANNED.
          </div>
          <button class="copy-btn" data-text="Unfortunately, you are going to be kicked for (), do not re-join before 30 minutes have passed or YOU WILL BE BANNED. ">
            <span>⧉</span> Copy
          </button>
        </div>

        <div class="message">
          <div class="message-icon accent-danger">🚫</div>
          <div class="message-content">
            Unfortunately, you are going to be banned for (). You may appeal via
            our communication server, ukcr.
          </div>
          <button class="copy-btn" data-text="Unfortunately, You are going to be banned for (), You may appeal via our communication server, ukcr. ">
            <span>⧉</span> Copy
          </button>
        </div>
      </div>

      <!-- Comms / applications -->
      <div class="section">
        <div class="section-header">
          <div class="section-title">Comms & applications</div>
          <div class="section-tag">Staff & departments</div>
        </div>

        <div class="message">
          <div class="message-icon">🛠️</div>
          <div class="message-content">
            To join the staff, simply hop into our comms, find the channel
            labelled "applications," and complete the staff application form!
          </div>
          <button class="copy-btn" data-text='To join the staff, simply hop into our comms, find the channel labelled "applications," and complete the staff application form!'>
            <span>⧉</span> Copy
          </button>
        </div>

        <div class="message">
          <div class="message-icon">🔥</div>
          <div class="message-content">
            To get whitelisted for Fire, join our comms, find the "departments"
            channel, and fill out the form.
          </div>
          <button class="copy-btn" data-text='To get whitelisted for Fire, join our comms, find the "departments" channel, and fill out the form.'>
            <span>⧉</span> Copy
          </button>
        </div>

        <div class="message">
          <div class="message-icon">🚓</div>
          <div class="message-content">
            To get whitelisted for MET, join our comms, find the channel named
            "departments," and then check out "opportunities."
          </div>
          <button class="copy-btn" data-text='To get whitelisted for MET, join our comms, find the channel named "departments," and then check out "opportunities."'>
            <span>⧉</span> Copy
          </button>
        </div>

        <div class="message">
          <div class="message-icon">🟡</div>
          <div class="message-content">
            To get whitelisted for ACC, join our comms, find the "departments"
            channel, locate ACC, and submit your application.
          </div>
          <button class="copy-btn" data-text='To get whitelisted for ACC, join our comms, find the "departments" channel, locate ACC, and submit your application.'>
            <span>⧉</span> Copy
          </button>
        </div>

        <div class="message">
          <div class="message-icon">🟢</div>
          <div class="message-content">
            To get whitelisted for NH, join our comms, find the "departments"
            channel, locate NH, and submit your application.
          </div>
          <button class="copy-btn" data-text='To get whitelisted for NH, join our comms, find the "departments" channel, locate NH, and submit your application.'>
            <span>⧉</span> Copy
          </button>
        </div>
      </div>

      <!-- Exploiter / roadworks -->
      <div class="section">
        <div class="section-header">
          <div class="section-title">Incidents</div>
          <div class="section-tag">Exploits & roadworks</div>
        </div>

        <div class="message">
          <div class="message-icon accent-success">⚡</div>
          <div class="message-content">
            ⚡ The exploiter has been banned! Sorry for any issues this has
            caused. ⚡
          </div>
          <button class="copy-btn" data-text="⚡The exploiter has been banned! Sorry for any issues this has caused. ⚡">
            <span>⧉</span> Copy
          </button>
        </div>

        <div class="message">
          <div class="message-icon">🚧</div>
          <div class="message-content">
            Hello! This roadwork is unauthorised therefore you need to clear it up.
          </div>
          <button class="copy-btn" data-text="Hello! This roadwork is unauthorised therefore you need to clear it up.">
            <span>⧉</span> Copy
          </button>
        </div>

        <div class="message">
          <div class="message-icon">🛣️</div>
          <div class="message-content">
            Hello! Freedom ave is whitelisted for NH & ACC only! Please clear this up.
          </div>
          <button class="copy-btn" data-text="Hello! Freedom ave is whitelisted for NH & ACC only! Please clear this up.">
            <span>⧉</span> Copy
          </button>
        </div>
      </div>

      <!-- Vehicles / whitelists -->
      <div class="section">
        <div class="section-header">
          <div class="section-title">Vehicles & whitelists</div>
          <div class="section-tag">Fleet control</div>
        </div>

        <div class="message">
          <div class="message-icon">🚛</div>
          <div class="message-content">
            Hello! Please change from the heavy wrecker to another vehicle as this is whitelisted.
          </div>
          <button class="copy-btn" data-text="Hello! Please change from the heavy wrecker too another vehicle as this is whitelisted.">
            <span>⧉</span> Copy
          </button>
        </div>

        <div class="message">
          <div class="message-icon">🚗</div>
          <div class="message-content">
            Hello! Please change from National Highways to Automobile Association as it's whitelisted.
          </div>
          <button class="copy-btn" data-text="Hello! please change from National highways to Automobile Association As it's whitelisted.">
            <span>⧉</span> Copy
          </button>
        </div>

        <div class="message">
          <div class="message-icon">🚙</div>
          <div class="message-content">
            Hello! Please change from ACC to Automobile Association.
          </div>
          <button class="copy-btn" data-text="Hello! please Change from ACC to Automobile Association.">
            <span>⧉</span> Copy
          </button>
        </div>
      </div>

      <!-- Avatar / uniform -->
      <div class="section">
        <div class="section-header">
          <div class="section-title">Appearance & equipment</div>
          <div class="section-tag">Avatar control</div>
        </div>

        <div class="message">
          <div class="message-icon">🧍</div>
          <div class="message-content">
            Hello! Please change your avatar as it's unrealistic. You have 1 minute
            to comply or you will be removed.
          </div>
          <button class="copy-btn" data-text="Hello! Please change your avatar as it's unrealistic. You have 1 minute to comply or you will be removed. ">
            <span>⧉</span> Copy
          </button>
        </div>

        <div class="message">
          <div class="message-icon">🔫</div>
          <div class="message-content">
            Hello! Please remove the gun as it's whitelisted to trained members.
          </div>
          <button class="copy-btn" data-text="Hello! Please remove the gun as it's whitelisted to trained members. ">
            <span>⧉</span> Copy
          </button>
        </div>

        <div class="message">
          <div class="message-icon">👕</div>
          <div class="message-content">
            Hello! Please change your uniform as it's not appropriate or whitelisted.
          </div>
          <button class="copy-btn" data-text="Hello! Please change your uniform. As it's Not appropriate or whitelisted.">
            <span>⧉</span> Copy
          </button>
        </div>

        <div class="message">
          <div class="message-icon">🚓</div>
          <div class="message-content">
            Hello! Please change your livery as it's whitelisted.
          </div>
          <button class="copy-btn" data-text="Hello! Please change your livery as it's whitelisted. ">
            <span>⧉</span> Copy
          </button>
        </div>
      </div>
    </div>
  </div>

  <script>
    document.querySelectorAll(".copy-btn").forEach((btn) => {
      btn.addEventListener("click", async () => {
        const text = btn.getAttribute("data-text") || "";
        try {
          await navigator.clipboard.writeText(text);
          btn.classList.add("copied");
          btn.innerHTML = '<span>✔</span> Copied';
          setTimeout(() => {
            btn.classList.remove("copied");
            btn.innerHTML = '<span>⧉</span> Copy';
          }, 1200);
        } catch (e) {
          // No alerts, just a subtle visual fallback
          btn.classList.add("copied");
          setTimeout(() => btn.classList.remove("copied"), 800);
        }
      });
    });
  </script>
</body>
</html>
