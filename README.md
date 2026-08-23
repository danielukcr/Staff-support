<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>UKCR Staff Panel</title>

<style>
    body {
        margin: 0;
        padding: 40px;
        background: #0c0e14;
        font-family: Arial, sans-serif;
        color: #fff;
    }

    .title {
        font-size: 32px;
        font-weight: 700;
        margin-bottom: 25px;
    }

    .list {
        display: flex;
        flex-direction: column;
        gap: 18px;
        max-width: 900px;
    }

    .item {
        background: #14161f;
        border: 1px solid #232533;
        padding: 16px 20px;
        border-radius: 12px;
        display: flex;
        justify-content: space-between;
        align-items: flex-start;
        gap: 20px;
        box-shadow: 0px 0px 20px rgba(0,0,0,0.45);
    }

    .text {
        font-size: 15px;
        line-height: 1.4;
        flex: 1;
    }

    .copy {
        padding: 10px 16px;
        background: #2d4cff;
        border: none;
        border-radius: 8px;
        color: #fff;
        cursor: pointer;
        font-size: 13px;
        transition: 0.2s;
        white-space: nowrap;
    }

    .copy:hover {
        background: #4b6cff;
    }

    .reason-input {
        width: 100%;
        margin-top: 10px;
        padding: 10px;
        border-radius: 8px;
        border: 1px solid #3a3a45;
        background: #0f0f15;
        color: #fff;
        font-size: 14px;
    }
</style>
</head>

<body>

<div class="title">UKCR Staff Message Panel</div>

<div class="list">

    <!-- GENERAL SUPPORT -->
    <div class="item">
        <div class="text">Hello! I am Trainee Moderator Daniel, how can I help you today? (If I am late say Void!)</div>
        <button class="copy" onclick="copyText(this)">Copy</button>
    </div>

    <div class="item">
        <div class="text">Anything else I can support you with today? If so, please state.</div>
        <button class="copy" onclick="copyText(this)">Copy</button>
    </div>

    <div class="item">
        <div class="text">Alright! Have an amazing rest of your roleplay.</div>
        <button class="copy" onclick="copyText(this)">Copy</button>
    </div>

    <!-- ANNOUNCEMENTS -->
    <div class="item">
        <div class="text">☕ The café is now open! Come down to get a hot drink or a snack! ☕</div>
        <button class="copy" onclick="copyText(this)">Copy</button>
    </div>

    <div class="item">
        <div class="text">🍟 The Three Guys is now open! Come down to get a burger or some fries!</div>
        <button class="copy" onclick="copyText(this)">Copy</button>
    </div>

    <div class="item">
        <div class="text">🚕 Taxi services are now available! Use the phone to direct a taxi to you! 🚕</div>
        <button class="copy" onclick="copyText(this)">Copy</button>
    </div>

    <div class="item">
        <div class="text">⚠️ Please start to clear () or you will be loaded or receive moderation action. You have 10 seconds to comply. ⚠️</div>
        <button class="copy" onclick="copyText(this)">Copy</button>
    </div>

    <!-- WARN -->
    <div class="item">
        <div class="text">
            You are going to be warned for:<br>
            <input class="reason-input" placeholder="Enter reason…" oninput="updateReason(this)">
            You can receive 3 warnings; any more will result in a kick.
        </div>
        <button class="copy" onclick="copyText(this)">Copy</button>
    </div>

    <!-- KICK -->
    <div class="item">
        <div class="text">
            You are going to be kicked for:<br>
            <input class="reason-input" placeholder="Enter reason…" oninput="updateReason(this)">
            Do not re-join before 30 minutes or YOU WILL BE BANNED.
        </div>
        <button class="copy" onclick="copyText(this)">Copy</button>
    </div>

    <!-- BAN -->
    <div class="item">
        <div class="text">
            You are going to be banned for:<br>
            <input class="reason-input" placeholder="Enter reason…" oninput="updateReason(this)">
            You may appeal via our communication server, ukcr.
        </div>
        <button class="copy" onclick="copyText(this)">Copy</button>
    </div>

    <!-- COMMS -->
    <div class="item">
        <div class="text">To join the staff, hop into our comms, find "applications," and complete the form.</div>
        <button class="copy" onclick="copyText(this)">Copy</button>
    </div>

    <div class="item">
        <div class="text">To get whitelisted for Fire, join comms → departments → Fire.</div>
        <button class="copy" onclick="copyText(this)">Copy</button>
    </div>

    <div class="item">
        <div class="text">To get whitelisted for MET, join comms → departments → opportunities.</div>
        <button class="copy" onclick="copyText(this)">Copy</button>
    </div>

    <div class="item">
        <div class="text">To get whitelisted for ACC, join comms → departments → ACC.</div>
        <button class="copy" onclick="copyText(this)">Copy</button>
    </div>

    <div class="item">
        <div class="text">To get whitelisted for NH, join comms → departments → NH.</div>
        <button class="copy" onclick="copyText(this)">Copy</button>
    </div>

    <!-- INCIDENTS -->
    <div class="item">
        <div class="text">⚡ The exploiter has been banned! Sorry for any issues caused. ⚡</div>
        <button class="copy" onclick="copyText(this)">Copy</button>
    </div>

    <div class="item">
        <div class="text">Hello! This roadwork is unauthorised, please clear it up.</div>
        <button class="copy" onclick="copyText(this)">Copy</button>
    </div>

    <div class="item">
        <div class="text">Hello! Freedom Ave is whitelisted for NH & ACC only. Please clear this up.</div>
        <button class="copy" onclick="copyText(this)">Copy</button>
    </div>

    <!-- VEHICLES -->
    <div class="item">
        <div class="text">Hello! Please change from the heavy wrecker to another vehicle as this is whitelisted.</div>
        <button class="copy" onclick="copyText(this)">Copy</button>
    </div>

    <div class="item">
        <div class="text">Hello! Please change from National Highways to Automobile Association as it's whitelisted.</div>
        <button class="copy" onclick="copyText(this)">Copy</button>
    </div>

    <div class="item">
        <div class="text">Hello! Please change from ACC to Automobile Association.</div>
        <button class="copy" onclick="copyText(this)">Copy</button>
    </div>

    <!-- APPEARANCE -->
    <div class="item">
        <div class="text">Hello! Please change your avatar as it's unrealistic. You have 1 minute to comply.</div>
        <button class="copy" onclick="copyText(this)">Copy</button>
    </div>

    <div class="item">
        <div class="text">Hello! Please remove the gun as it's whitelisted to trained members.</div>
        <button class="copy" onclick="copyText(this)">Copy</button>
    </div>

    <div class="item">
        <div class="text">Hello! Please change your uniform as it's not appropriate or whitelisted.</div>
        <button class="copy" onclick="copyText(this)">Copy</button>
    </div>

    <div class="item">
        <div class="text">Hello! Please change your livery as it's whitelisted.</div>
        <button class="copy" onclick="copyText(this)">Copy</button>
    </div>

</div>

<script>
function copyText(btn) {
    const msg = btn.previousElementSibling;

    // Build final text including reason input
    let final = "";
    msg.childNodes.forEach(node => {
        if (node.nodeType === 3) {
            final += node.textContent.trim() + " ";
        }
        if (node.classList && node.classList.contains("reason-input")) {
            final += node.value.trim() + " ";
        }
    });

    navigator.clipboard.writeText(final.trim());

    btn.innerText = "Copied!";
    setTimeout(() => btn.innerText = "Copy", 900);
}
</script>

</body>
</html>
