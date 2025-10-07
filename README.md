<<<<<<< HEAD
<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>शुभ दीपावली</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Noto Sans Devanagari', 'Arial', sans-serif;
            background: linear-gradient(135deg, #1a0033 0%, #4a0080 50%, #ff6b00 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow-x: hidden;
            position: relative;
        }

        /* Animated background diyas */
        .diya {
            position: absolute;
            width: 30px;
            height: 30px;
            background: radial-gradient(circle, #ffaa00 0%, #ff6600 70%, transparent 100%);
            border-radius: 50%;
            animation: float 6s ease-in-out infinite;
            opacity: 0.6;
            filter: blur(2px);
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px) translateX(0px); }
            25% { transform: translateY(-20px) translateX(10px); }
            50% { transform: translateY(-10px) translateX(-10px); }
            75% { transform: translateY(-25px) translateX(5px); }
        }

        .container {
            max-width: 800px;
            width: 90%;
            background: rgba(255, 255, 255, 0.95);
            border-radius: 30px;
            padding: 60px 40px;
            text-align: center;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.4);
            position: relative;
            z-index: 10;
            animation: slideIn 1s ease-out;
        }

        @keyframes slideIn {
            from {
                opacity: 0;
                transform: translateY(-50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .diya-icon {
            font-size: 80px;
            margin-bottom: 20px;
            animation: glow 2s ease-in-out infinite;
        }

        @keyframes glow {
            0%, 100% { 
                filter: drop-shadow(0 0 10px #ff6600);
                transform: scale(1);
            }
            50% { 
                filter: drop-shadow(0 0 25px #ff6600);
                transform: scale(1.1);
            }
        }

        h1 {
            color: #d4002a;
            font-size: 48px;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
            animation: colorChange 3s ease-in-out infinite;
        }

        @keyframes colorChange {
            0%, 100% { color: #d4002a; }
            50% { color: #ff6600; }
        }

        /* Timer Section */
        .timer-section {
            background: linear-gradient(135deg, #ff6600 0%, #d4002a 100%);
            color: white;
            padding: 25px;
            border-radius: 20px;
            margin: 30px 0;
            box-shadow: 0 10px 30px rgba(255, 102, 0, 0.3);
        }

        .timer-title {
            font-size: 24px;
            margin-bottom: 15px;
            font-weight: bold;
        }

        .timer-display {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
        }

        .timer-box {
            background: rgba(255, 255, 255, 0.2);
            padding: 15px 20px;
            border-radius: 15px;
            min-width: 80px;
            backdrop-filter: blur(10px);
        }

        .timer-number {
            font-size: 36px;
            font-weight: bold;
            display: block;
        }

        .timer-label {
            font-size: 14px;
            opacity: 0.9;
            margin-top: 5px;
        }

        .input-section {
            margin: 30px 0;
        }

        input {
            width: 100%;
            max-width: 400px;
            padding: 15px 20px;
            font-size: 18px;
            border: 3px solid #ff6600;
            border-radius: 15px;
            outline: none;
            transition: all 0.3s ease;
            font-family: 'Noto Sans Devanagari', 'Arial', sans-serif;
        }

        input:focus {
            border-color: #d4002a;
            box-shadow: 0 0 20px rgba(255, 102, 0, 0.3);
            transform: scale(1.02);
        }

        .greeting {
            font-size: 28px;
            color: #333;
            margin: 30px 0;
            line-height: 1.6;
            font-weight: 600;
        }

        .greeting-name {
            color: #ff6600;
            font-size: 36px;
            display: block;
            margin: 10px 0;
            animation: bounce 2s ease-in-out infinite;
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        .message {
            font-size: 20px;
            color: #555;
            line-height: 1.8;
            margin: 30px 0;
            padding: 20px;
            background: linear-gradient(135deg, #fff5e6 0%, #ffe6cc 100%);
            border-radius: 15px;
            border-left: 5px solid #ff6600;
        }

        .decorative-lights {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin: 30px 0;
        }

        .light {
            width: 20px;
            height: 20px;
            border-radius: 50%;
            animation: blink 1.5s ease-in-out infinite;
        }

        .light:nth-child(1) { background: #ff0000; animation-delay: 0s; }
        .light:nth-child(2) { background: #ffaa00; animation-delay: 0.3s; }
        .light:nth-child(3) { background: #00ff00; animation-delay: 0.6s; }
        .light:nth-child(4) { background: #0088ff; animation-delay: 0.9s; }
        .light:nth-child(5) { background: #ff00ff; animation-delay: 1.2s; }

        @keyframes blink {
            0%, 100% { opacity: 1; transform: scale(1); }
            50% { opacity: 0.3; transform: scale(0.8); }
        }

        .share-section {
            margin-top: 40px;
            padding-top: 30px;
            border-top: 2px dashed #ff6600;
        }

        .share-btn {
            background: linear-gradient(135deg, #ff6600 0%, #d4002a 100%);
            color: white;
            border: none;
            padding: 15px 40px;
            font-size: 18px;
            border-radius: 30px;
            cursor: pointer;
            margin: 10px;
            transition: all 0.3s ease;
            font-weight: bold;
            box-shadow: 0 5px 15px rgba(255, 102, 0, 0.3);
            display: inline-flex;
            align-items: center;
            gap: 10px;
        }

        .whatsapp-btn {
            background: linear-gradient(135deg, #25D366 0%, #128C7E 100%);
        }

        .share-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(255, 102, 0, 0.5);
        }

        .whatsapp-btn:hover {
            box-shadow: 0 8px 20px rgba(37, 211, 102, 0.5);
        }

        .share-btn:active {
            transform: translateY(0);
        }

        .firework {
            position: absolute;
            width: 5px;
            height: 5px;
            border-radius: 50%;
            animation: explode 2s ease-out infinite;
        }

        @keyframes explode {
            0% {
                opacity: 1;
                transform: translate(0, 0) scale(1);
            }
            100% {
                opacity: 0;
                transform: translate(var(--tx), var(--ty)) scale(0);
            }
        }

        @media (max-width: 768px) {
            .container {
                padding: 40px 20px;
            }
            h1 {
                font-size: 36px;
            }
            .greeting-name {
                font-size: 28px;
            }
            .message {
                font-size: 18px;
            }
            .timer-display {
                gap: 10px;
            }
            .timer-box {
                min-width: 70px;
                padding: 10px 15px;
            }
            .timer-number {
                font-size: 28px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="diya-icon">🪔</div>
        <h1>✨ शुभ दीपावली ✨</h1>
        
        <div class="decorative-lights">
            <div class="light"></div>
            <div class="light"></div>
            <div class="light"></div>
            <div class="light"></div>
            <div class="light"></div>
        </div>

        <!-- Timer Section -->
        <div class="timer-section">
            <div class="timer-title">🎆 दीपावली में  🎆</div>
            <div class="timer-display">
                <div class="timer-box">
                    <span class="timer-number" id="days">00</span>
                    <div class="timer-label">दिन</div>
                </div>
                <div class="timer-box">
                    <span class="timer-number" id="hours">00</span>
                    <div class="timer-label">घंटे</div>
                </div>
                <div class="timer-box">
                    <span class="timer-number" id="minutes">00</span>
                    <div class="timer-label">मिनट</div>
                </div>
                <div class="timer-box">
                    <span class="timer-number" id="seconds">00</span>
                    <div class="timer-label">सेकंड</div>
                </div>
              <div>  </div>
            </div>
          <div>  </div>
          <div class="timer-title">समय बाकी </div>
        </div>
        <div style="font-size: 18;color:#f74905;font-weight: bold; ">आपका नाम यहां लिखो</div>
        <div class="input-section">
            <input type="text" id="nameInput" placeholder="अपना नाम यहाँ लिखें..." />
        </div>
        <div style="font-size: 18;color:#f74905;font-weight: bold; ">आपका नाम यहां लिखो</div>
        <div class="greeting">
            <span class="greeting-name" id="greetingName">आपका नाम</span>
            <div> की तरफ से दिवाली की हार्दिक शुभकामनाएं ! 🎆</div>
        </div>

        <div class="message">
            <p>🪔 आपको और आपके परिवार को दीपावली की हार्दिक शुभकामनाएं! 🪔</p>
            <p>इस दीपों के त्यौहार पर आपके जीवन में खुशियों और समृद्धि का उजाला हो। माँ लक्ष्मी आपको धन-धान्य से भर दें और भगवान गणेश आपके सभी विघ्नों को दूर करें।</p>
            <p>आइए इस खूबसूरत त्यौहार को प्यार, खुशी और ढेर सारी मिठाइयों के साथ मनाएं! 🎇✨</p>
            <p><strong>शुभ दीपावली! 🙏</strong></p>
            <p style="margin-top: 15px; font-style: italic;">दीप जले, मन में उमंग हो,<br>घर में सुख-समृद्धि का संग हो,<br>हर दिशा से आए खुशियों की बहार,<br>दीपावली आपके जीवन में लाए उजाला अपार!</p>
        </div>

        <div class="share-section">
            <p style="color: #666; margin-bottom: 15px; font-size: 18px;">अपने प्रियजनों के साथ शुभकामनाएं साझा करें!</p>
            <button class="share-btn whatsapp-btn" onclick="shareWhatsApp()">
                <span style="font-size: 24px;">📱</span> WhatsApp पर भेजें
            </button>
            
            <button class="share-btn" onclick="copyLink()">
                <span style="font-size: 20px;">🔗</span> लिंक कॉपी करें
            </button>
        </div>
    </div>

    <script>
        // Diwali 2025 date (October 20, 2025)
        const diwaliDate = new Date('2025-10-20T00:00:00').getTime();

        function updateTimer() {
            const now = new Date().getTime();
            const distance = diwaliDate - now;

            if (distance < 0) {
                document.getElementById('days').textContent = '00';
                document.getElementById('hours').textContent = '00';
                document.getElementById('minutes').textContent = '00';
                document.getElementById('seconds').textContent = '00';
                document.querySelector('.timer-title').textContent = '🎉 शुभ दीपावली! 🎉';
                return;
            }

            const days = Math.floor(distance / (1000 * 60 * 60 * 24));
            const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((distance % (1000 * 60)) / 1000);

            document.getElementById('days').textContent = String(days).padStart(2, '0');
            document.getElementById('hours').textContent = String(hours).padStart(2, '0');
            document.getElementById('minutes').textContent = String(minutes).padStart(2, '0');
            document.getElementById('seconds').textContent = String(seconds).padStart(2, '0');
        }

        updateTimer();
        setInterval(updateTimer, 1000);

        // Create floating diyas
        for (let i = 0; i < 15; i++) {
            const diya = document.createElement('div');
            diya.className = 'diya';
            diya.style.left = Math.random() * 100 + '%';
            diya.style.top = Math.random() * 100 + '%';
            diya.style.animationDelay = Math.random() * 6 + 's';
            diya.style.animationDuration = (Math.random() * 4 + 4) + 's';
            document.body.appendChild(diya);
        }

        // Handle name input
        const nameInput = document.getElementById('nameInput');
        const greetingName = document.getElementById('greetingName');

        // Get name from URL parameter
        const urlParams = new URLSearchParams(window.location.search);
        const nameFromUrl = urlParams.get('n');
        
        if (nameFromUrl) {
            nameInput.value = nameFromUrl;
            greetingName.textContent = nameFromUrl;
        }

        nameInput.addEventListener('input', function() {
            const name = this.value.trim();
            greetingName.textContent = name || 'आपका नाम';
        });

        // WhatsApp share function
        function shareWhatsApp() {
            const name = nameInput.value.trim() || 'दोस्त';
            const url = window.location.origin + window.location.pathname + '?n=' + encodeURIComponent(name);
            const message = `🪔 *शुभ दीपावली !* 🪔\n\nआपको और आपके परिवार को ${name} की तरफ से दीपावली की हार्दिक शुभकामनाएं!\n\nयह विशेष शुभकामना संदेश देखें:\n${url}`;
            
            const whatsappUrl = `https://wa.me/?text=${encodeURIComponent(message)}`;
            window.open(whatsappUrl, '_blank');
        }

        // Copy link function
        function copyLink() {
            const name = nameInput.value.trim() || 'दोस्त';
            const url = window.location.origin + window.location.pathname + '?n=' + encodeURIComponent(name);
            
            navigator.clipboard.writeText(url).then(() => {
                alert('लिंक कॉपी हो गया! अपने दोस्तों और परिवार के साथ शेयर करें! 🎉');
            }).catch(() => {
                prompt('इस लिंक को कॉपी करें:', url);
            });
        }

        // Create fireworks effect
        function createFirework() {
            const colors = ['#ff0000', '#ffaa00', '#00ff00', '#0088ff', '#ff00ff', '#ffff00'];
            const firework = document.createElement('div');
            firework.className = 'firework';
            firework.style.background = colors[Math.floor(Math.random() * colors.length)];
            firework.style.left = Math.random() * 100 + '%';
            firework.style.top = Math.random() * 100 + '%';
            firework.style.setProperty('--tx', (Math.random() - 0.5) * 200 + 'px');
            firework.style.setProperty('--ty', (Math.random() - 0.5) * 200 + 'px');
            document.body.appendCShild(firework);
            
            setTimeout(() => firework.remove(), 2000);
        }

        setInterval(createFirework, 500);
    </script>
</body>
</html>
