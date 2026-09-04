<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Account Purchase Portal</title>
  <!-- Firebase SDKs -->
  <script src="https://www.gstatic.com/firebasejs/9.22.1/firebase-app-compat.js"></script>
  <script src="https://www.gstatic.com/firebasejs/9.22.1/firebase-database-compat.js"></script>

  <style>
    * { box-sizing: border-box; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; margin: 0; padding: 0; }
    body { background-color: #121212; color: #ffffff; display: flex; justify-content: center; align-items: center; min-height: 100vh; padding: 20px; }
    .card { background: #1e1e1e; border-radius: 12px; padding: 24px; width: 100%; max-width: 400px; box-shadow: 0 4px 15px rgba(0,0,0,0.5); position: relative; }
    
    .header { display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px; }
    .help-btn { background: #333; color: #00e676; border: 1px solid #00e676; padding: 6px 12px; border-radius: 20px; cursor: pointer; font-size: 12px; }
    
    h2 { font-size: 20px; margin-bottom: 10px; color: #00e676; }
    p { font-size: 14px; color: #aaa; margin-bottom: 15px; }
    
    .step { display: none; }
    .step.active { display: block; }
    
    input, select { width: 100%; padding: 12px; margin-bottom: 15px; border-radius: 6px; border: 1px solid #333; background: #2a2a2a; color: #fff; font-size: 14px; }
    
    .btn { width: 100%; padding: 12px; background: #00e676; border: none; color: #000; font-weight: bold; border-radius: 6px; cursor: pointer; font-size: 16px; margin-top: 10px; }
    .btn-secondary { background: #444; color: #fff; margin-top: 5px; }
    
    .qr-box { text-align: center; margin: 15px 0; background: #fff; padding: 15px; border-radius: 8px; }
    .qr-box img { max-width: 180px; }
    
    .cred-display { background: #2a2a2a; border: 1px dashed #00e676; padding: 15px; border-radius: 6px; margin-top: 10px; }
    .cred-item { font-size: 14px; font-weight: bold; color: #ffffff; margin: 8px 0; display: flex; justify-content: space-between; }
    .cred-value { color: #00e676; font-family: monospace; font-size: 16px; }

    .status-badge { display: inline-block; padding: 4px 8px; border-radius: 4px; font-size: 12px; margin-bottom: 10px; font-weight: bold; }
    .pending { background: #ff9800; color: #000; }
    .active-badge { background: #00e676; color: #000; }
  </style>
</head>
<body>

<div class="card">
  <!-- Top Header with Help Option -->
  <div class="header">
    <span style="font-size: 12px; color: #888;">Panel Store</span>
    <button class="help-btn" onclick="openHelp()">💬 Help / Support</button>
  </div>

  <!-- STEP 1: Welcome -->
  <div id="step1" class="step active">
    <h2>Welcome User! 👋</h2>
    <p>Get active credentials for Free Fire, FF Max, Pokemon GO & more (1 Month Sub).</p>
    <button class="btn" onclick="nextStep(2)">Get Started</button>
  </div>

  <!-- STEP 2: Customer Info -->
  <div id="step2" class="step">
    <h2>Step 2: Customer Email</h2>
    <p>Enter your Email to register your order.</p>
    <input type="email" id="userEmail" placeholder="Enter Email" required>
    <button class="btn" onclick="nextStep(3)">Next</button>
    <button class="btn btn-secondary" onclick="nextStep(1)">Back</button>
  </div>

  <!-- STEP 3: Game Selection -->
  <div id="step3" class="step">
    <h2>Step 3: Select Game</h2>
    <p>Choose the game you need access for.</p>
    <select id="gameSelect">
      <option value="Free Fire">Free Fire</option>
      <option value="FF Max">FF Max</option>
      <option value="Pokemon GO">Pokemon GO</option>
    </select>
    <button class="btn" onclick="nextStep(4)">Next</button>
    <button class="btn btn-secondary" onclick="nextStep(2)">Back</button>
  </div>

  <!-- STEP 4: Architecture Selection -->
  <div id="step4" class="step">
    <h2>Step 4: Select Bit Version</h2>
    <p>Choose your app architecture version.</p>
    <select id="bitSelect">
      <option value="32 Bit">32-Bit</option>
      <option value="64 Bit">64-Bit</option>
    </select>
    <button class="btn" onclick="nextStep(5)">Next</button>
    <button class="btn btn-secondary" onclick="nextStep(3)">Back</button>
  </div>

  <!-- STEP 5: Payment & QR Code -->
  <div id="step5" class="step">
    <h2>Step 5: Payment (FamApp QR)</h2>
    <p>Scan QR Code & complete payment in FamApp. Click below when done.</p>
    
    <div class="qr-box">
  <!-- Aapki UPI ID (aakarshpal@fam) ka Auto QR Code -->
  <img src="https://api.qrserver.com/v1/create-qr-code/?size=200x200&data=upi://pay?pa=aakarshpal@fam&pn=aakarsh" alt="Payment QR">
  <p style="color:#000; font-weight:bold; font-size:12px; margin-top:5px;">UPI ID: aakarshpal@fam</p>
</div>

    <button class="btn" onclick="submitOrder()">Submit & Request Account</button>
    <button class="btn btn-secondary" onclick="nextStep(4)">Back</button>
  </div>

  <!-- STEP 6: Generated Credentials Display -->
  <div id="step6" class="step">
    <h2>Your Account Credentials</h2>
    <p>Status: <span id="statusBadge" class="status-badge pending">Pending Activation</span></p>
    
    <div class="cred-display">
      <div class="cred-item">
        <span>Username:</span>
        <span class="cred-value" id="dispUsername">---</span>
      </div>
      <div class="cred-item">
        <span>Password:</span>
        <span class="cred-value" id="dispPassword">---</span>
      </div>
      <div class="cred-item">
        <span>Plan:</span>
        <span class="cred-value" style="color:#fff; font-size:12px;">1 Month Subscription</span>
      </div>
    </div>

    <p style="font-size: 12px; color: #888; margin-top: 12px; text-align: center;">
      FamApp par payment verify hone par aapka account <b>Active</b> ho jayega.
    </p>
  </div>
</div>

<script>
  // --- Firebase Configuration ---
  const firebaseConfig = {
    apiKey: "AIzaSyBdNcBRZPVv9xo-gx57qbZVwnYRlBw8FLs",
    databaseURL: "https://loginform-8458e-default-rtdb.asia-southeast1.firebasedatabase.app",
    projectId: "loginform-8458e",
    storageBucket: "loginform-8458e.firebasestorage.app"
  };

  // Initialize Firebase Realtime Database
  firebase.initializeApp(firebaseConfig);
  const db = firebase.database();

  let currentStep = 1;

  function nextStep(step) {
    document.getElementById(`step${currentStep}`).classList.remove('active');
    document.getElementById(`step${step}`).classList.add('active');
    currentStep = step;
  }

  function openHelp() {
    window.open('https://t.me/YOUR_TELEGRAM_USERNAME', '_blank');
  }

// --- Auto Generate Username & Password ---
  function generateUserPass() {
    const chars = "ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789";
    let user = "user" + Math.floor(100000 + Math.random() * 900000); // e.g. user658955
    let pass = "PASS_" + Math.floor(1000 + Math.random() * 9000);
    return { user, pass };
  }

  // --- Save Order directly under /Users/{username} ---
  function submitOrder() {
    const email = document.getElementById('userEmail').value;
    const game = document.getElementById('gameSelect').value;
    const bit = document.getElementById('bitSelect').value;

    if (!email) {
      alert("Kripya pehle Email id bharein!");
      nextStep(2);
      return;
    }

    const creds = generateUserPass();

    // 1 Month Expiry Date (YYYY-MM-DD)
    const today = new Date();
    today.setMonth(today.getMonth() + 1);
    const expiryDateStr = today.toISOString().split('T')[0];

    // Reference: /Users/USERNAME (No random push key)
    const userRef = db.ref('Users/' + creds.user);

    userRef.set({
      created_by: "Aakarsh",     // Exact field name: created_by
      device_id: "",             // Empty until user logs in from device
      expiry: expiryDateStr,     // YYYY-MM-DD
      hwid: "",                  // Empty initially
      password: creds.pass,
      status: "OFF",             // Admin "active" ya "ON" karega
      email: email,              // Extra details for your reference
      game: game,
      bitVersion: bit
    }).then(() => {
      document.getElementById('dispUsername').innerText = creds.user;
      document.getElementById('dispPassword').innerText = creds.pass;
      
      // Realtime Listener on /Users/USERNAME
      listenToStatusUpdate(creds.user);

      nextStep(6);
    }).catch((error) => {
      alert("Error: " + error.message);
    });
  }

  // --- Realtime Status Listener ---
  function listenToStatusUpdate(username) {
    db.ref('Users/' + username).on('value', (snapshot) => {
      const data = snapshot.val();
      if (data) {
        const badge = document.getElementById('statusBadge');
        const st = (data.status || "").toLowerCase();
        
        if (st === "active" || st === "on" || st === "true") {
          badge.innerText = "ACTIVE (On)";
          badge.className = "status-badge active-badge";
        } else {
          badge.innerText = "Pending Activation";
          badge.className = "status-badge pending";
        }
      }
    });
  }
</script>

</body>
</html>
