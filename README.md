
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>DIGITAL FIDGETAL</title>
    
    <!-- Social Media Meta Tags -->
    <meta property="og:title" content="DIGITAL FIDGETAL">
    <meta property="og:description" content="The remedy for computertime restlessness - interactive digital fidget device">
    <meta property="og:site_name" content="DIGITAL FIDGETAL">
    <meta property="og:type" content="website">
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:title" content="DIGITAL FIDGETAL">
    <meta name="twitter:description" content="The remedy for computertime restlessness - interactive digital fidget device">
    <meta name="description" content="DIGITAL FIDGETAL - The remedy for computertime restlessness. Interactive digital fidget device with physics-based elements to help relieve stress and anxiety while using your computer.">
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        body {
            font-family: 'Space Grotesk', -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Helvetica Neue', Arial, sans-serif;
            background: #f0f0f0;
            padding: 20px 20px 40px 20px;
            touch-action: manipulation;
            transition: background 0.3s ease;
        }

        /* Glow Mode Styles */
        body.glow-mode {
            background: #0a0a0a;
        }

        .glow-mode .fidget-device {
            background: #1a1a1a !important;
            border: 3px solid #00ff00;
            box-shadow: 12px 12px 0px #003300, 0 0 20px #00ff0050;
        }

        .glow-mode .title {
            background: #0d0d0d !important;
            border: 2px solid #00ff00;
            color: #00ff00;
            box-shadow: 6px 6px 0px #003300, inset 0 0 10px #00ff0030;
            text-shadow: 0 0 10px #00ff00;
        }

        .glow-mode .title svg text:first-child {
            fill: #00ff00;
            filter: drop-shadow(0 0 5px #00ff00);
        }

        .glow-mode .title svg text:last-child {
            fill: #66ff66;
            filter: drop-shadow(0 0 3px #66ff66);
        }

        .glow-mode .module {
            background: #0d0d0d !important;
            border: 2px solid #00ff00;
            box-shadow: 6px 6px 0px #003300, 0 0 15px #00ff0030;
        }

        .glow-mode .btn {
            background: #0d0d0d;
            border: 2px solid #00ff00;
            color: #00ff00;
            box-shadow: 3px 3px 0px #003300, 0 0 8px #00ff0040;
        }

        .glow-mode .btn:hover {
            background: #1a1a1a;
            box-shadow: 3px 3px 0px #003300, 0 0 12px #00ff0060;
        }

        .glow-mode .btn:active {
            box-shadow: 1px 1px 0px #003300, 0 0 12px #00ff0060;
            transform: translate(2px, 2px);
        }

        .glow-mode .ball-track {
            background: #0d0d0d;
            border: 2px solid #00ff00;
            box-shadow: 4px 4px 0px #003300, inset 0 0 10px #00ff0020;
        }

        .glow-mode .ball {
            background: #ffff00;
            border: 2px solid #ffff00;
            box-shadow: 4px 4px 0px #666600, 0 0 15px #ffff00;
        }

        .glow-mode .wave-container {
            background: #000;
            border: 2px solid #00ff00;
            box-shadow: 4px 4px 0px #003300, 0 0 15px #00ff0040;
        }

        .glow-mode .triangle {
            background: #ff0066;
            border: 2px solid #ff0066;
            box-shadow: 3px 3px 0px #660022, 0 0 12px #ff0066;
        }

        .glow-mode .star {
            background: #ff8800 !important;
            border: 3px solid #ff8800;
            color: #000;
            box-shadow: 0 0 20px #ff8800;
        }

        .glow-mode .star-shadow {
            background: #663300;
            box-shadow: 0 0 10px #663300;
        }

        .glow-mode .square {
            border: 3px solid #00ffff;
            box-shadow: 4px 4px 0px #006666, 0 0 15px #00ffff;
        }

        .glow-mode .label {
            color: #00ff00;
            text-shadow: 0 0 5px #00ff00;
        }

        .glow-mode .nav-link {
            color: #00ff00;
            text-shadow: 0 0 5px #00ff00;
        }

        .glow-mode .nav-link:hover {
            color: #66ff66;
        }

        .nav-links {
            text-align: center;
            margin-bottom: 20px;
        }

        .nav-link {
            color: #666;
            font-size: 12px;
            font-weight: normal;
            cursor: pointer;
            text-decoration: underline;
            margin: 0 15px;
            display: inline-block;
        }

        .nav-link:hover {
            color: #333;
        }

        .modal {
            display: none;
            position: fixed;
            z-index: 10001;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.5);
            touch-action: manipulation;
        }

        .modal-content {
            background-color: white;
            margin: 10% auto;
            padding: 30px;
            border: 3px solid #333;
            border-radius: 20px;
            width: 90%;
            max-width: 500px;
            box-shadow: 12px 12px 0px #333;
            position: relative;
            font-family: 'Space Grotesk', -apple-system, BlinkMacSystemFont, sans-serif;
        }

        .video-modal-content {
            background-color: white;
            margin: 5% auto;
            padding: 40px 20px 20px 20px;
            border: 3px solid #333;
            border-radius: 20px;
            width: 90%;
            max-width: 800px;
            box-shadow: 12px 12px 0px #333;
            position: relative;
            font-family: 'Space Grotesk', -apple-system, BlinkMacSystemFont, sans-serif;
        }

        .modal h2 {
            font-size: 24px;
            font-weight: bold;
            margin-bottom: 20px;
            color: #333;
            text-align: center;
        }

        .modal ol {
            padding-left: 20px;
            line-height: 1.6;
            color: #333;
        }

        .modal li {
            margin-bottom: 12px;
            font-size: 14px;
        }

        .close {
            color: #666;
            float: right;
            font-size: 28px;
            font-weight: bold;
            cursor: pointer;
            position: absolute;
            top: 15px;
            right: 20px;
            touch-action: manipulation;
        }

        .close:hover {
            color: #333;
        }

        .video-container {
            position: relative;
            padding-bottom: 56.25%;
            height: 0;
            overflow: hidden;
            margin-top: 15px;
        }

        .video-container iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: none;
            border-radius: 8px;
        }

        #loadingScreen {
            position: fixed;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            background: white;
            z-index: 10000;
            display: flex;
            align-items: flex-start;
            justify-content: center;
            padding-top: 35vh;
            font-family: 'Space Grotesk', -apple-system, BlinkMacSystemFont, sans-serif;
        }

        #mainContent {
            opacity: 0;
            transform: scale(0.9);
            transition: opacity 0.8s ease-in, transform 0.8s ease-in;
        }

        .fidget-device {
            background: white;
            border: 3px solid #333;
            border-radius: 20px;
            padding: 20px;
            width: 450px;
            margin: 0 auto;
            max-width: calc(100vw - 40px);
            box-shadow: 12px 12px 0px #333;
            position: relative;
            overflow: hidden;
        }

        .title {
            text-align: center;
            font-size: 30px;
            font-weight: bold;
            color: #333;
            padding: 20px 10px;
            border: 2px solid #000;
            border-radius: 8px;
            margin-bottom: 20px;
            cursor: pointer;
            width: 85%;
            margin-left: auto;
            margin-right: auto;
            box-shadow: 6px 6px 0px #333;
            user-select: none;
            -webkit-user-select: none;
            -moz-user-select: none;
            -ms-user-select: none;
            background: white !important;
            touch-action: manipulation;
        }

        .module {
            border: 2px solid #333;
            border-radius: 12px;
            margin: 10px 0;
            padding: 15px;
            text-align: center;
            box-shadow: 6px 6px 0px #333;
            background: white !important;
        }

        .btn {
            background: white;
            border: 2px solid #333;
            border-radius: 6px;
            width: 32px;
            height: 32px;
            font-size: 16px;
            cursor: pointer;
            margin: 5px;
            box-shadow: 3px 3px 0px #000;
            transition: all 0.1s ease;
            user-select: none;
            -webkit-user-select: none;
            -moz-user-select: none;
            -ms-user-select: none;
            touch-action: manipulation;
        }

        .btn:hover { background: #f0f0f0; }
        .btn:active {
            box-shadow: 1px 1px 0px #000;
            transform: translate(2px, 2px);
        }

        .ball-track {
            width: 350px;
            height: 50px;
            background: #f8f8f8;
            border: 2px solid #ddd;
            border-radius: 25px;
            position: relative;
            margin: 0 auto;
            cursor: pointer;
            box-shadow: 4px 4px 0px #bbb;
            touch-action: manipulation;
        }

        .ball {
            width: 28px;
            height: 28px;
            background: #f1c40f;
            border: 2px solid #000;
            border-radius: 50%;
            position: absolute;
            top: 10px;
            left: 188px;
            cursor: grab;
            box-shadow: 4px 4px 0px #000;
            touch-action: manipulation;
        }

        .wave-container {
            width: 240px;
            height: 100px;
            background: #000;
            border: 2px solid #000;
            border-radius: 8px;
            margin: 0 auto;
            box-shadow: 4px 4px 0px #333;
            touch-action: manipulation;
        }

        .wave-canvas { width: 100%; height: 100%; border-radius: 8px; }

        .hand-container {
            width: 100%;
            height: 70px;
            position: relative;
            cursor: pointer;
            touch-action: manipulation;
        }

        .triangle {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 20px;
            height: 20px;
            background: #e74c3c;
            border: 2px solid #000;
            border-radius: 50%;
            transition: all 0.4s;
            box-shadow: 3px 3px 0px #000;
            cursor: grab;
            touch-action: manipulation;
            z-index: 100;
        }

        .triangle:active {
            cursor: grabbing;
        }

        .star {
            width: 50px;
            height: 50px;
            background: #f39c12;
            border: 3px solid #333;
            border-radius: 6px;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 32px;
            color: #fff;
            user-select: none;
            transition: transform 0.3s ease;
            position: relative;
            z-index: 2;
            touch-action: manipulation;
        }

        .star-shadow {
            position: absolute;
            top: 6px;
            left: 6px;
            width: 50px;
            height: 50px;
            background: #000;
            border-radius: 6px;
            z-index: 1;
            pointer-events: none;
        }

        .square {
            width: 40px;
            height: 40px;
            background: #27ae60;
            border: 3px solid #333;
            border-radius: 6px;
            position: absolute;
            top: 40px;
            left: 200px;
            cursor: move;
            box-shadow: 4px 4px 0px #000;
            touch-action: manipulation;
        }

        .label {
            font-size: 10px;
            color: #666;
            margin-top: 20px;
            user-select: none;
            -webkit-user-select: none;
            -moz-user-select: none;
            -ms-user-select: none;
        }

        @keyframes ripple {
            0% { width: 4px; height: 4px; opacity: 1; }
            100% { width: 40px; height: 40px; opacity: 0; }
        }

        @keyframes ballBounce {
            0% { 
                transform: scale(0) rotate(0deg); 
                opacity: 0; 
            }
            20% { 
                transform: scale(1.3) rotate(90deg); 
                opacity: 1; 
            }
            40% { 
                transform: scale(1) rotate(180deg); 
                opacity: 1; 
            }
            60% { 
                transform: scale(1.1) rotate(270deg); 
                opacity: 1; 
            }
            80% { 
                transform: scale(1) rotate(360deg); 
                opacity: 0.8; 
            }
            100% { 
                transform: scale(0) rotate(540deg); 
                opacity: 0; 
            }
        }

        @media (max-width: 480px) {
            body { padding: 10px; }
            
            .nav-links {
                margin-bottom: 15px;
            }
            
            .nav-link {
                font-size: 12px;
                margin: 0 10px;
            }
            
            .modal-content {
                margin: 20% auto;
                padding: 20px;
                width: 95%;
                box-shadow: 8px 8px 0px #333;
            }

            .video-modal-content {
                margin: 10% auto;
                padding: 30px 15px 15px 15px;
                width: 95%;
                box-shadow: 8px 8px 0px #333;
            }

            .modal h2 {
                font-size: 20px;
                margin-bottom: 15px;
            }

            .modal li {
                font-size: 13px;
                margin-bottom: 10px;
            }

            .close {
                font-size: 24px;
                top: 10px;
                right: 15px;
            }
            
            .fidget-device { 
                width: 100%; 
                padding: 15px; 
                box-shadow: 8px 8px 0px #333;
                max-width: none;
            }
            .title { 
                padding: 12px 8px; 
                box-shadow: 4px 4px 0px #333;
                font-size: 24px;
                width: 90%;
            }
            .module { 
                padding: 12px; 
                margin: 8px 0; 
                box-shadow: 4px 4px 0px #333; 
            }
            .btn { 
                width: 36px; 
                height: 36px; 
                font-size: 16px; 
                box-shadow: 2px 2px 0px #000;
                margin: 3px;
            }
            .btn:active { 
                box-shadow: 1px 1px 0px #000; 
                transform: translate(1px, 1px); 
            }
            .ball-track { 
                width: calc(100vw - 80px);
                max-width: 280px;
                height: 50px; 
                box-shadow: 3px 3px 0px #bbb; 
            }
            .ball { 
                width: 30px; 
                height: 30px; 
                top: 10px; 
                box-shadow: 3px 3px 0px #000; 
            }
            .wave-container { 
                width: calc(100vw - 140px);
                max-width: 200px;
                height: 80px; 
                box-shadow: 3px 3px 0px #333; 
            }
            .wave-canvas { 
                width: 100%; 
                height: 100%; 
            }
            .triangle { 
                width: 22px; 
                height: 22px; 
                box-shadow: 2px 2px 0px #000; 
            }
            .hand-container {
                height: 60px;
            }
            .star { 
                width: 50px; 
                height: 50px; 
                font-size: 28px; 
            }
            .star-shadow { 
                width: 50px; 
                height: 50px; 
                top: 3px; 
                left: 3px; 
            }
            #squareModule { 
                height: 160px !important; 
                padding: 12px !important; 
            }
            .square { 
                width: 35px; 
                height: 35px; 
                box-shadow: 3px 3px 0px #000; 
            }
            .label { 
                font-size: 11px; 
                margin-top: 12px; 
            }
            
            /* Nobble me mobile adjustments */
            .star + .label {
                bottom: 8px !important;
                letter-spacing: -0.5px !important;
                word-spacing: -2px !important;
                font-size: 10px !important;
                line-height: 1 !important;
            }
            
            .title svg {
                max-width: 100%;
                height: auto;
            }
            
            .title svg text:first-child {
                font-size: 22px;
            }
            
            .title svg text:last-child {
                font-size: 8px;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation Links -->
    <div class="nav-links">
        <span class="nav-link" onclick="openVideoModal()">WATCH THIS</span>
        <span class="nav-link" onclick="openModal()">READ THIS</span>
    </div>
    
    <!-- Instructions Modal -->
    <div id="instructionsModal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal()">&times;</span>
            <h2>How To Fidge</h2>
            <ol>
                <li>Get antsy at your computer.</li>
                <li>Open Digital Fidgetal in its own standalone window.</li>
                <li>Move this window to the left side of your screen.</li>
                <li>Move other windows to the right side.</li>
                <li>You're ready to begin. It's fidgie time!</li>
            </ol>
            <p style="margin-top: 20px; font-style: italic; color: #666; font-size: 12px;">*For best results, use Digital Fidgetal on a desktop computer*</p>
        </div>
    </div>
    
    <!-- Video Modal - NO TEXT HEADERS -->
    <div id="videoModal" class="modal">
        <div class="video-modal-content">
            <span class="close" onclick="closeVideoModal()">&times;</span>
            <div class="video-container">
                <iframe src="https://player.vimeo.com/video/1117285399?h=a2365272d9" allowfullscreen></iframe>
            </div>
        </div>
    </div>

    <!-- Loading Screen -->
    <div id="loadingScreen">
        <div style="text-align: center;">
            <div style="font-size: 18px; font-weight: bold; color: #333; letter-spacing: 2px; margin-bottom: 8px;">WELCOME TO</div>
            <div style="font-size: 32px; font-weight: bold; color: #333; letter-spacing: 2px;">[ DIGITAL FIDGETAL ]</div>
        </div>
    </div>

    <!-- Main Content -->
    <div id="mainContent">        
        <div class="fidget-device">
            <div class="title" onclick="handleTitleClick()">
                <svg width="320" height="40" viewBox="0 0 320 40" style="margin: 0 auto; display: block;">
                    <text x="160" y="20" font-family="'Space Grotesk', -apple-system, BlinkMacSystemFont, sans-serif" font-size="28" font-weight="900" text-anchor="middle" fill="currentColor" letter-spacing="3px">DIGITAL FIDGETAL</text>
                    <text x="160" y="39" font-family="'Space Grotesk', -apple-system, BlinkMacSystemFont, sans-serif" font-size="10" font-weight="normal" text-anchor="middle" fill="#666" letter-spacing="1.5px">the remedy for computertime restlessness</text>
                </svg>
            </div>
            
            <div class="module" style="margin-bottom: 22px;">
                <div class="ball-track" onclick="clickTrack(event)">
                    <div class="ball" id="ball"></div>
                </div>
                <div class="label">doink me</div>
            </div>
            
            <div class="module">
                <div style="display: flex; align-items: center; gap: 15px; justify-content: center;">
                    <div style="display: flex; flex-direction: column; gap: 5px;">
                        <button class="btn" onclick="changeWaveMode(-1)">•</button>
                        <button class="btn" onclick="changeWaveMode(1)">○</button>
                    </div>
                    <div class="wave-container" onclick="ripple(event)">
                        <canvas class="wave-canvas" id="canvas" width="240" height="100"></canvas>
                    </div>
                    <div style="display: flex; flex-direction: column; gap: 5px;">
                        <button class="btn" onclick="adjustWaves(1)">+</button>
                        <button class="btn" onclick="adjustWaves(-1)">-</button>
                    </div>
                </div>
                <div class="label">toon me</div>
            </div>
            
            <div style="display: flex; gap: 15px;">
                <div class="module" style="flex: 3; cursor: pointer;" onclick="bounce(event)">
                    <div class="hand-container">
                        <div class="triangle" id="triangle"></div>
                    </div>
                    <div class="label">bimp me</div>
                </div>
                
                <div class="module" style="flex: 1; position: relative; display: flex; flex-direction: column; justify-content: center; align-items: center;">
                    <div style="position: relative; margin-top: -32px;">
                        <div class="star-shadow"></div>
                        <div class="star" onclick="spinStar(this)">★</div>
                    </div>
                    <div class="label" style="position: absolute; bottom: 15px; left: 50%; transform: translateX(-50%); margin: 0;">nobble me</div>
                </div>
            </div>
            
            <div class="module" id="squareModule" style="position: relative; height: 150px; padding: 15px;">
                <div style="position: absolute; left: 15px; top: 10px; display: flex; flex-direction: column;">
                    <button class="btn" onclick="addSquare()">+</button>
                    <button class="btn" onclick="removeSquare()">-</button>
                    <button class="btn" onclick="toggleBounce()">○</button>
                </div>
                <div class="square" id="square0"></div>
                <div class="label" style="position: absolute; bottom: 15px; left: 50%; transform: translateX(-50%); margin: 0;">wubba me</div>
            </div>
        </div>
        
        <!-- Credit -->
        <div style="text-align: center; margin-top: 25px; font-size: 10px; color: #999; font-weight: normal;">MADE BY BEN 2025</div>
    </div>

    <script>
        // Modal functions
        function openModal() {
            document.getElementById('instructionsModal').style.display = 'block';
        }

        function closeModal() {
            document.getElementById('instructionsModal').style.display = 'none';
        }

        function openVideoModal() {
            document.getElementById('videoModal').style.display = 'block';
        }

        function closeVideoModal() {
            document.getElementById('videoModal').style.display = 'none';
        }

        // Close modal when clicking outside
        window.onclick = function(event) {
            const modal = document.getElementById('instructionsModal');
            const videoModal = document.getElementById('videoModal');
            if (event.target === modal) {
                modal.style.display = 'none';
            }
            if (event.target === videoModal) {
                videoModal.style.display = 'none';
            }
        }

        // Global variables
        let ballPos = 188;
        let ballVel = 0;
        let ballInterval = null;
        let dragging = false;
        let waveFreq = 5;
        let waveSpeed = 2;
        let waveColor = '#00ff00';
        let squares = [{x: 200, y: 40, vx: 3, vy: 2}];
        let nextId = 1;
        let bouncing = false;
        let starRotation = 0;
        let colors = ['white', '#333', '#e74c3c', '#3498db', '#2ecc71', '#f39c12'];
        let colorIndex = 0;
        let triangleDragging = false;
        let containerColorIndex = 0;

        // Glow mode variables
        let titleClickCount = 0;
        let titleClickTimer = null;
        let isGlowMode = false;

        // Handle title clicks for glow mode
        function handleTitleClick() {
            titleClickCount++;
            console.log('Title clicked! Count:', titleClickCount);
            
            if (titleClickTimer) clearTimeout(titleClickTimer);
            
            if (titleClickCount >= 3) {
                console.log('Activating glow mode!');
                toggleGlowMode();
                titleClickCount = 0;
            } else {
                titleClickTimer = setTimeout(() => {
                    titleClickCount = 0;
                }, 2000);
            }
        }

        function toggleGlowMode() {
            isGlowMode = !isGlowMode;
            console.log('Glow mode:', isGlowMode);
            
            if (isGlowMode) {
                document.body.classList.add('glow-mode');
                waveColor = '#00ff00';
                
                // Update square colors for glow mode
                const glowColors = ['#00ffff', '#ff0066', '#ffff00', '#00ff00', '#ff8800', '#ff00ff'];
                squares.forEach((sq, i) => {
                    const el = document.getElementById('square' + i);
                    if (el) {
                        el.style.background = glowColors[i % glowColors.length];
                    }
                });
                console.log('Glow mode activated!');
            } else {
                document.body.classList.remove('glow-mode');
                const waveColors = ['#ff0000', '#ff8800', '#ffff00', '#88ff00', '#00ff00', '#00ff88', '#00ffff', '#0088ff', '#0000ff', '#8800ff'];
                waveColor = waveColors[waveFreq - 1] || '#00ff00';
                
                // Reset square colors - keep square0 green, others use color array
                squares.forEach((sq, i) => {
                    const el = document.getElementById('square' + i);
                    if (el) {
                        if (i === 0) {
                            // Keep the original square green
                            el.style.background = '#27ae60';
                        } else {
                            // Other squares use the colors array
                            el.style.background = colors[i % colors.length];
                        }
                    }
                });
                console.log('Glow mode deactivated!');
            }
        }

        // Triple click barrel roll
        let clickCount = 0;
        let clickTimer = null;
        let isBarrelRolling = false;

        function doBarrelRoll() {
            if (isBarrelRolling) return;
            isBarrelRolling = true;
            
            const container = document.querySelector('.fidget-device');
            container.style.transition = 'transform 0.6s ease-in-out';
            container.style.transformStyle = 'preserve-3d';
            container.style.transform = 'rotateY(180deg)';
            
            setTimeout(() => {
                container.style.transform = 'rotateY(0deg)';
                setTimeout(() => {
                    container.style.transition = '';
                    container.style.transformStyle = '';
                    isBarrelRolling = false;
                }, 100);
            }, 600);
        }

        // Triple click detection (only on gray background, not Digital Fidgetal)
        document.addEventListener('click', (e) => {
            // Only count clicks on the gray background (not on the fidgetal or nav links)
            const isOnFidgetal = e.target.closest('.fidget-device') !== null;
            const isOnNavLinks = e.target.closest('.nav-links') !== null;
            const isOnModal = e.target.closest('.modal') !== null;
            
            if (!isOnFidgetal && !isOnNavLinks && !isOnModal) {
                clickCount++;
                
                if (clickTimer) clearTimeout(clickTimer);
                
                if (clickCount >= 2) {
                    doBarrelRoll();
                    clickCount = 0;
                } else {
                    clickTimer = setTimeout(() => {
                        clickCount = 0;
                    }, 250);
                }
            }
        });

        // Ball physics
        function updateBallShadow() {
            const ball = document.getElementById('ball');
            const displacement = (ballPos - 175) / 100;
            ball.style.boxShadow = `${4 + displacement * 2}px ${4 + Math.abs(displacement) * 0.5}px 0px #000`;
        }

        document.getElementById('ball').addEventListener('mousedown', e => {
            e.stopPropagation();
            dragging = true;
            e.target.style.zIndex = '9999';
        });

        document.addEventListener('mousemove', e => {
            if (dragging) {
                const rect = document.querySelector('.ball-track').getBoundingClientRect();
                const maxPos = window.innerWidth <= 480 ? Math.min(220, rect.width - 45) : 308;
                ballPos = Math.max(14, Math.min(maxPos, e.clientX - rect.left - 14));
                document.getElementById('ball').style.left = ballPos + 'px';
                updateBallShadow();
            }
        });

        document.addEventListener('mouseup', () => {
            if (dragging) {
                document.getElementById('ball').style.zIndex = '';
            }
            dragging = false;
        });

        function startBallPhysics() {
            if (ballInterval) clearInterval(ballInterval);
            ballInterval = setInterval(() => {
                if (Math.abs(ballVel) < 0.3) {
                    clearInterval(ballInterval);
                    ballInterval = null;
                    return;
                }
                ballPos += ballVel;
                const maxPos = window.innerWidth <= 480 ? Math.min(220, document.querySelector('.ball-track').offsetWidth - 45) : 308;
                ballPos = Math.max(14, Math.min(maxPos, ballPos));
                if (ballPos <= 14 || ballPos >= maxPos) ballVel *= -0.8;
                ballVel *= 0.97;
                document.getElementById('ball').style.left = ballPos + 'px';
                updateBallShadow();
            }, 16);
        }

        function clickTrack(e) {
            if (dragging) return;
            const rect = e.currentTarget.getBoundingClientRect();
            const maxPos = window.innerWidth <= 480 ? Math.min(220, rect.width - 45) : 308;
            const clickPos = Math.max(14, Math.min(maxPos, e.clientX - rect.left - 14));
            const distance = Math.abs(clickPos - ballPos);
            
            if (distance > 20) {
                ballVel = (clickPos > ballPos ? 1 : -1) * Math.min(18, 6 + distance * 0.08);
                startBallPhysics();
            }
        }

        // Wave animation
        function drawWaves() {
            const canvas = document.getElementById('canvas');
            const ctx = canvas.getContext('2d');
            const time = Date.now() * 0.01 * waveSpeed;
            
            ctx.clearRect(0, 0, 240, 100);
            ctx.strokeStyle = waveColor;
            ctx.lineWidth = 2;
            ctx.beginPath();
            
            for (let x = 0; x < 240; x++) {
                const y = 50 + Math.sin((x * 0.02 * waveFreq) + time) * 25;
                if (x === 0) ctx.moveTo(x, y);
                else ctx.lineTo(x, y);
            }
            ctx.stroke();
            requestAnimationFrame(drawWaves);
        }

        function adjustWaves(change) {
            waveSpeed = Math.max(0.5, Math.min(8, waveSpeed + change * 0.5));
        }

        function changeWaveMode(direction) {
            waveFreq = Math.max(1, Math.min(10, waveFreq + direction));
            
            if (isGlowMode) {
                // Neon glow colors for dark mode
                const glowWaveColors = ['#ff0066', '#ff3300', '#ff6600', '#ffff00', '#00ff00', '#00ffff', '#0099ff', '#6600ff', '#ff00ff', '#ff0099'];
                waveColor = glowWaveColors[waveFreq - 1] || '#00ff00';
            } else {
                // Normal colors for light mode
                const waveColors = ['#ff0000', '#ff8800', '#ffff00', '#88ff00', '#00ff00', '#00ff88', '#00ffff', '#0088ff', '#0000ff', '#8800ff'];
                waveColor = waveColors[waveFreq - 1] || '#00ff00';
            }
        }

        function ripple(e) {
            const rect = e.currentTarget.getBoundingClientRect();
            const rippleEl = document.createElement('div');
            rippleEl.style.cssText = `
                position: absolute;
                left: ${e.clientX - rect.left}px;
                top: 50px;
                width: 4px;
                height: 4px;
                background: ${waveColor};
                border-radius: 50%;
                transform: translate(-50%, -50%);
                animation: ripple 1s ease-out forwards;
                pointer-events: none;
            `;
            e.currentTarget.appendChild(rippleEl);
            setTimeout(() => rippleEl.remove(), 1000);
        }

        // Bounce function
        function bounce(e) {
            if (triangleDragging) return;
            
            const container = e.currentTarget;
            const triangle = document.getElementById('triangle');
            const rect = container.getBoundingClientRect();
            const x = e.clientX - rect.left;
            const y = e.clientY - rect.top;
            
            triangle.style.transition = 'transform 0.1s ease-out';
            triangle.style.transform = `translate(${x - container.offsetWidth/2}px, ${y - container.offsetHeight/2}px) scale(1.5)`;
            
            setTimeout(() => {
                triangle.style.transition = 'transform 0.3s ease-out';
                triangle.style.transform = 'translate(-50%, -50%) scale(1)';
                
                setTimeout(() => {
                    triangle.style.transition = 'all 0.4s';
                }, 300);
            }, 100);
        }

        // Triangle dragging
        document.getElementById('triangle').addEventListener('mousedown', function(e) {
            e.stopPropagation();
            e.preventDefault();
            triangleDragging = true;
            this.style.cursor = 'grabbing';
            this.style.transition = 'transform 0.1s ease-out';
            this.style.zIndex = '9999';
            
            document.body.style.userSelect = 'none';
            document.body.style.webkitUserSelect = 'none';
            
            const container = this.closest('.hand-container');
            const containerRect = container.getBoundingClientRect();
            
            const mouseMoveHandler = (e) => {
                if (!triangleDragging) return;
                e.preventDefault();
                e.stopPropagation();
                
                const x = e.clientX - containerRect.left - container.offsetWidth/2;
                const y = e.clientY - containerRect.top - container.offsetHeight/2;
                
                this.style.transform = `translate(${x}px, ${y}px)`;
            };
            
            const mouseUpHandler = (e) => {
                e.stopPropagation();
                this.style.cursor = 'grab';
                this.style.zIndex = '100';
                
                document.body.style.userSelect = '';
                document.body.style.webkitUserSelect = '';
                
                this.style.transition = 'transform 0.3s ease-out';
                this.style.transform = 'translate(-50%, -50%)';
                
                setTimeout(() => {
                    this.style.transition = 'all 0.4s';
                }, 300);
                
                setTimeout(() => {
                    triangleDragging = false;
                }, 50);
                
                document.removeEventListener('mousemove', mouseMoveHandler);
                document.removeEventListener('mouseup', mouseUpHandler);
            };
            
            document.addEventListener('mousemove', mouseMoveHandler);
            document.addEventListener('mouseup', mouseUpHandler);
        });

        // Star spin
        function spinStar(el) {
            const spins = 3 + Math.random() * 2;
            starRotation += spins * 360;
            
            el.style.transition = 'transform 2s ease-out';
            el.style.transform = `rotate(${starRotation}deg)`;
            el.style.background = colors[Math.floor(Math.random() * colors.length)];
            
            const shadow = el.parentElement.querySelector('.star-shadow');
            if (shadow) {
                shadow.style.transition = 'transform 2s ease-out';
                shadow.style.transform = `rotate(${starRotation}deg)`;
            }
        }

        // Title color change
        function changeColor(el) {
            colorIndex = (colorIndex + 1) % colors.length;
            el.style.color = colors[colorIndex];
        }

        // Squares functionality
        function addSquare() {
            const container = document.getElementById('squareModule');
            const square = document.createElement('div');
            square.className = 'square';
            square.id = 'square' + nextId;
            
            const maxW = container.offsetWidth - 43;
            const maxH = window.innerWidth <= 480 ? 115 : 95;
            const x = Math.random() * maxW;
            const y = Math.random() * maxH;
            
            square.style.left = x + 'px';
            square.style.top = y + 'px';
            
            // Use glow colors if in glow mode, otherwise use normal colors
            if (isGlowMode) {
                const glowColors = ['#00ffff', '#ff0066', '#ffff00', '#00ff00', '#ff8800', '#ff00ff'];
                square.style.background = glowColors[nextId % glowColors.length];
            } else {
                square.style.background = colors[nextId % colors.length];
            }
            
            container.appendChild(square);
            squares.push({x, y, vx: (Math.random() - 0.5) * 8, vy: (Math.random() - 0.5) * 8});
            makeDraggable(square, squares.length - 1);
            nextId++;
        }

        function removeSquare() {
            if (squares.length <= 1) return;
            squares.pop();
            const lastSquare = document.getElementById('square' + (nextId - 1));
            if (lastSquare) lastSquare.remove();
            nextId--;
        }

        function toggleBounce() {
            bouncing = !bouncing;
            if (bouncing) animate();
        }

        function animate() {
            if (!bouncing) return;
            squares.forEach((sq, i) => {
                const el = document.getElementById('square' + i);
                if (!el) return;
                
                const module = el.closest('.module');
                const maxW = module.offsetWidth - 43;
                const maxH = window.innerWidth <= 480 ? 115 : 105;
                
                sq.x += sq.vx;
                sq.y += sq.vy;
                
                if (sq.x <= 0 || sq.x >= maxW) sq.vx = -sq.vx;
                if (sq.y <= 0 || sq.y >= maxH) sq.vy = -sq.vy;
                
                sq.x = Math.max(0, Math.min(maxW, sq.x));
                sq.y = Math.max(0, Math.min(maxH, sq.y));
                
                el.style.left = sq.x + 'px';
                el.style.top = sq.y + 'px';
            });
            requestAnimationFrame(animate);
        }

        function makeDraggable(el, index) {
            let isDragging = false;
            
            el.addEventListener('mousedown', e => {
                if (bouncing) return;
                isDragging = true;
                
                const moveHandler = e => {
                    if (!isDragging) return;
                    const container = document.getElementById('squareModule');
                    const rect = container.getBoundingClientRect();
                    const maxW = container.offsetWidth - 43;
                    const maxH = window.innerWidth <= 480 ? 115 : 110;
                    const x = Math.max(0, Math.min(maxW, e.clientX - rect.left - 20));
                    const y = Math.max(0, Math.min(maxH, e.clientY - rect.top - 20));
                    
                    el.style.left = x + 'px';
                    el.style.top = y + 'px';
                    squares[index].x = x;
                    squares[index].y = y;
                };
                
                const upHandler = () => {
                    isDragging = false;
                    document.removeEventListener('mousemove', moveHandler);
                    document.removeEventListener('mouseup', upHandler);
                };
                
                document.addEventListener('mousemove', moveHandler);
                document.addEventListener('mouseup', upHandler);
            });
        }

        // Container color change
        let scrollAccumulator = 0;
        const scrollThreshold = 60;
        
        // Wrap effect variables (for page background scrolling)
        let wrapScrollAccumulator = 0;
        const wrapScrollThreshold = 300;
        let isWrapping = false;
        
        function changeContainerColor() {
            if (isGlowMode) return; // Don't change color in glow mode
            containerColorIndex = (containerColorIndex + 1) % colors.length;
            const container = document.querySelector('.fidget-device');
            container.style.background = colors[containerColorIndex];
        }

        function wrapFidgetal(direction) {
            if (isWrapping) return;
            isWrapping = true;
            
            const container = document.querySelector('.fidget-device');
            const originalTransform = container.style.transform;
            
            if (direction > 0) {
                container.style.transition = 'transform 0.8s cubic-bezier(0.4, 0, 0.2, 1)';
                container.style.transform = 'translateY(-100vh)';
                
                setTimeout(() => {
                    container.style.transition = 'none';
                    container.style.transform = 'translateY(100vh)';
                    
                    setTimeout(() => {
                        container.style.transition = 'transform 0.8s cubic-bezier(0.4, 0, 0.2, 1)';
                        container.style.transform = originalTransform || 'translateY(0)';
                        
                        setTimeout(() => {
                            container.style.transition = '';
                            isWrapping = false;
                        }, 800);
                    }, 20);
                }, 800);
            } else {
                container.style.transition = 'transform 0.8s cubic-bezier(0.4, 0, 0.2, 1)';
                container.style.transform = 'translateY(100vh)';
                
                setTimeout(() => {
                    container.style.transition = 'none';
                    container.style.transform = 'translateY(-100vh)';
                    
                    setTimeout(() => {
                        container.style.transition = 'transform 0.8s cubic-bezier(0.4, 0, 0.2, 1)';
                        container.style.transform = originalTransform || 'translateY(0)';
                        
                        setTimeout(() => {
                            container.style.transition = '';
                            isWrapping = false;
                        }, 800);
                    }, 20);
                }, 800);
            }
        }

        // Page background wrap effect (when scrolling outside Digital Fidgetal)
        document.addEventListener('wheel', (e) => {
            const isOverFidgetal = e.target.closest('.fidget-device') !== null;
            
            if (!isOverFidgetal && !isWrapping) {
                const scrollAmount = Math.abs(e.deltaY);
                
                wrapScrollAccumulator += scrollAmount;
                if (wrapScrollAccumulator >= wrapScrollThreshold) {
                    e.preventDefault();
                    wrapFidgetal(e.deltaY);
                    wrapScrollAccumulator = 0;
                    return;
                }
                
                setTimeout(() => {
                    wrapScrollAccumulator = Math.max(0, wrapScrollAccumulator - 50);
                }, 200);
            }
        });

        // Scroll to change container color (only on Digital Fidgetal background, not modules)
        document.querySelector('.fidget-device').addEventListener('wheel', (e) => {
            const isOverModule = e.target.closest('.module') !== null;
            const isOverTitle = e.target.closest('.title') !== null;
            
            if (!isOverModule && !isOverTitle && !isWrapping) {
                e.preventDefault();
                e.stopPropagation();
                
                scrollAccumulator += Math.abs(e.deltaY);
                if (scrollAccumulator >= scrollThreshold) {
                    changeContainerColor();
                    scrollAccumulator = 0;
                }
            }
        });
        
        document.addEventListener('click', function(e) {
            const fidgetDevice = document.querySelector('.fidget-device');
            const clickedInsideDevice = fidgetDevice.contains(e.target);
            
            if (clickedInsideDevice && 
                !dragging &&
                !triangleDragging &&
                !e.target.classList.contains('btn') && 
                !e.target.classList.contains('ball') &&
                !e.target.classList.contains('star') &&
                !e.target.classList.contains('triangle') &&
                !e.target.classList.contains('square') &&
                !e.target.closest('.wave-container') &&
                !e.target.closest('.title') &&
                !e.target.closest('.ball-track') &&
                !e.target.closest('.module')) {
                changeContainerColor();
            }
        });

        // Loading screen
        window.addEventListener('DOMContentLoaded', () => {
            setTimeout(() => {
                const loadingScreen = document.getElementById('loadingScreen');
                const mainContent = document.getElementById('mainContent');
                
                loadingScreen.style.transition = 'opacity 0.8s ease-out';
                loadingScreen.style.opacity = '0';
                
                mainContent.style.opacity = '1';
                mainContent.style.transform = 'scale(1)';
                
                setTimeout(() => {
                    loadingScreen.remove();
                }, 800);
            }, 2000);
        });

        // Initialize everything
        document.title = "DIGITAL FIDGETAL";
        drawWaves();
        makeDraggable(document.getElementById('square0'), 0);
        updateBallShadow();
        
        bouncing = false;
    </script>
</body>
</html>
