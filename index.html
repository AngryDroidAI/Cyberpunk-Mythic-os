<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>CYBERPUNK NEON CRT OS v3.0 - AngryDroid Apps Integration</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Share+Tech+Mono&family=Rajdhani:wght@300;500;700&display=swap');
    
    :root {
      --neon-pink: #ff00ff;
      --neon-cyan: #00ffff;
      --neon-green: #00ff00;
      --neon-purple: #9d00ff;
      --neon-orange: #ff7700;
      --dark-bg: #0a0a14;
      --darker-bg: #050510;
      --glow-pink: 0 0 20px #ff00ff, 0 0 40px #ff00ff, 0 0 60px #ff00ff;
      --glow-cyan: 0 0 20px #00ffff, 0 0 40px #00ffff, 0 0 60px #00ffff;
      --glow-green: 0 0 20px #00ff00, 0 0 40px #00ff00, 0 0 60px #00ff00;
      --scanline: rgba(0, 255, 255, 0.05);
      --flicker: rgba(255, 0, 255, 0.1);
    }
    
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      user-select: none;
    }
    
    body {
      background: #000;
      color: var(--neon-cyan);
      font-family: 'Rajdhani', sans-serif;
      font-weight: 500;
      overflow: hidden;
      height: 100vh;
      perspective: 1000px;
      cursor: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='32' height='32' viewBox='0 0 32 32'%3E%3Ccircle cx='16' cy='16' r='14' fill='none' stroke='%2300ffff' stroke-width='2' stroke-opacity='0.8'/%3E%3Ccircle cx='16' cy='16' r='4' fill='%2300ffff' opacity='0.8'/%3E%3C/svg%3E") 16 16, auto;
    }
    
    /* === CRT SCREEN EFFECT === */
    #crt-effect {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: 10000;
      background: 
        linear-gradient(to bottom, transparent 50%, var(--scanline) 50%),
        radial-gradient(circle at 30% 30%, var(--flicker) 0%, transparent 50%),
        radial-gradient(circle at 70% 70%, var(--flicker) 0%, transparent 50%);
      background-size: 100% 4px, 200% 200%, 200% 200%;
      animation: scanlines 0.1s linear infinite, flicker 5s infinite alternate;
      mix-blend-mode: overlay;
    }
    
    #crt-glow {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: radial-gradient(circle at center, transparent 40%, rgba(0, 255, 255, 0.05) 100%);
      pointer-events: none;
      z-index: 9999;
    }
    
    /* === NEON GRID BACKGROUND === */
    #neon-grid {
      position: fixed;
      width: 200%;
      height: 200%;
      background-image: 
        linear-gradient(var(--neon-pink) 1px, transparent 1px),
        linear-gradient(90deg, var(--neon-pink) 1px, transparent 1px),
        linear-gradient(var(--neon-cyan) 1px, transparent 1px),
        linear-gradient(90deg, var(--neon-cyan) 1px, transparent 1px);
      background-size: 100px 100px, 100px 100px, 20px 20px, 20px 20px;
      background-position: -50px -50px, -50px -50px, -10px -10px, -10px -10px;
      animation: gridMove 20s linear infinite;
      opacity: 0.15;
      z-index: -3;
    }
    
    /* === CYBER MENU === */
    #cyber-menu {
      position: fixed;
      bottom: 70px;
      left: 0;
      width: 400px;
      max-height: 70vh;
      background: rgba(5, 10, 20, 0.95);
      backdrop-filter: blur(15px);
      border: 2px solid var(--neon-cyan);
      border-left: none;
      box-shadow: 
        0 0 30px var(--neon-cyan),
        inset 0 0 20px rgba(0, 255, 255, 0.1);
      display: none;
      flex-direction: column;
      z-index: 1000;
      animation: menuSlide 0.3s ease-out;
    }
    
    @keyframes menuSlide {
      from { transform: translateX(-100%); }
      to { transform: translateX(0); }
    }
    
    .menu-header {
      padding: 15px 20px;
      background: linear-gradient(90deg, rgba(0, 255, 255, 0.2), rgba(255, 0, 255, 0.2));
      border-bottom: 1px solid var(--neon-cyan);
      font-family: 'Orbitron', monospace;
      font-weight: 700;
      text-shadow: var(--glow-cyan);
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    
    .menu-categories {
      display: flex;
      background: rgba(0, 0, 0, 0.5);
      border-bottom: 1px solid var(--neon-pink);
    }
    
    .category-tab {
      padding: 10px 15px;
      cursor: pointer;
      font-family: 'Share Tech Mono', monospace;
      font-size: 12px;
      border-right: 1px solid rgba(0, 255, 255, 0.2);
      transition: all 0.3s;
    }
    
    .category-tab:hover {
      background: rgba(255, 0, 255, 0.2);
    }
    
    .category-tab.active {
      background: linear-gradient(90deg, rgba(0, 255, 255, 0.3), rgba(255, 0, 255, 0.3));
      box-shadow: inset 0 0 10px rgba(255, 0, 255, 0.5);
    }
    
    .menu-content {
      flex: 1;
      overflow-y: auto;
      padding: 10px;
    }
    
    .category-panel {
      display: none;
      grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
      gap: 10px;
      padding: 10px;
    }
    
    .category-panel.active {
      display: grid;
    }
    
    .menu-app {
      padding: 10px;
      background: rgba(0, 255, 255, 0.05);
      border: 1px solid rgba(0, 255, 255, 0.3);
      border-radius: 5px;
      cursor: pointer;
      transition: all 0.3s;
      display: flex;
      align-items: center;
      gap: 10px;
    }
    
    .menu-app:hover {
      background: rgba(255, 0, 255, 0.2);
      transform: translateX(5px);
      box-shadow: 0 0 15px var(--neon-pink);
    }
    
    .app-icon {
      font-size: 24px;
      filter: drop-shadow(0 0 5px);
    }
    
    .app-info {
      flex: 1;
    }
    
    .app-name {
      font-family: 'Share Tech Mono', monospace;
      font-size: 12px;
      font-weight: bold;
      color: var(--neon-cyan);
    }
    
    .app-category {
      font-size: 10px;
      color: var(--neon-pink);
      opacity: 0.7;
    }
    
    .app-status {
      width: 8px;
      height: 8px;
      border-radius: 50%;
      background: #ff5555;
    }
    
    .app-status.running {
      background: #00ffaa;
      box-shadow: 0 0 10px #00ffaa;
    }
    
    /* === HOLOGRAM WINDOWS === */
    .hologram-window {
      position: absolute;
      width: 800px;
      height: 600px;
      background: rgba(10, 15, 30, 0.85);
      border: 2px solid var(--neon-cyan);
      border-radius: 8px;
      backdrop-filter: blur(10px);
      box-shadow: 
        0 0 30px var(--neon-cyan),
        inset 0 0 30px rgba(0, 255, 255, 0.1);
      display: flex;
      flex-direction: column;
      z-index: 10;
      transform-style: preserve-3d;
      transition: transform 0.3s, box-shadow 0.3s;
      overflow: hidden;
      animation: hologramFloat 4s ease-in-out infinite;
    }
    
    .window-header {
      background: linear-gradient(90deg, 
        rgba(0, 255, 255, 0.2), 
        rgba(255, 0, 255, 0.2));
      padding: 15px 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 1px solid var(--neon-cyan);
      font-family: 'Orbitron', monospace;
      font-weight: 700;
      text-shadow: var(--glow-cyan);
      position: relative;
      cursor: move;
    }
    
    .window-buttons {
      display: flex;
      gap: 10px;
    }
    
    .hologram-btn {
      width: 16px;
      height: 16px;
      border-radius: 50%;
      border: 2px solid;
      cursor: pointer;
      transition: all 0.2s;
    }
    
    .hologram-btn.close {
      border-color: #ff5555;
      background: rgba(255, 85, 85, 0.2);
    }
    
    .hologram-btn.minimize {
      border-color: #ffaa00;
      background: rgba(255, 170, 0, 0.2);
    }
    
    .hologram-btn.maximize {
      border-color: #00ffaa;
      background: rgba(0, 255, 170, 0.2);
    }
    
    .hologram-btn:hover {
      transform: scale(1.2);
      box-shadow: 0 0 10px;
    }
    
    .window-content {
      flex: 1;
      overflow: hidden;
      position: relative;
    }
    
    .window-iframe {
      width: 100%;
      height: 100%;
      border: none;
      background: #000;
    }
    
    /* === DESKTOP ICONS === */
    #neon-desktop {
      position: absolute;
      width: 100%;
      height: calc(100% - 70px);
      padding: 30px;
      display: grid;
      grid-template-columns: repeat(auto-fill, 120px);
      grid-auto-rows: 140px;
      gap: 30px;
      z-index: 1;
    }
    
    .cyber-icon {
      width: 120px;
      height: 140px;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      cursor: pointer;
      transition: all 0.3s;
      position: relative;
      padding: 15px;
      border-radius: 10px;
    }
    
    .cyber-icon:hover {
      background: rgba(0, 255, 255, 0.1);
      transform: translateY(-10px) scale(1.05);
      box-shadow: var(--glow-cyan);
    }
    
    /* === TASKBAR === */
    #cyber-taskbar {
      position: fixed;
      bottom: 0;
      left: 0;
      width: 100%;
      height: 70px;
      background: rgba(5, 10, 20, 0.9);
      backdrop-filter: blur(15px);
      border-top: 2px solid var(--neon-pink);
      display: flex;
      align-items: center;
      padding: 0 30px;
      gap: 20px;
      z-index: 100;
      box-shadow: 0 -5px 30px rgba(255, 0, 255, 0.3);
    }
    
    #menu-button {
      padding: 10px 20px;
      background: rgba(0, 255, 255, 0.1);
      border: 1px solid var(--neon-cyan);
      border-radius: 5px;
      cursor: pointer;
      font-family: 'Orbitron', monospace;
      font-size: 16px;
      font-weight: 700;
      color: var(--neon-cyan);
      transition: all 0.3s;
    }
    
    #menu-button:hover {
      background: rgba(0, 255, 255, 0.3);
      box-shadow: var(--glow-cyan);
    }
    
    #taskbar-apps {
      display: flex;
      gap: 10px;
      flex: 1;
      overflow-x: auto;
      padding: 10px 0;
    }
    
    .taskbar-app {
      padding: 10px 15px;
      background: rgba(0, 255, 255, 0.1);
      border: 1px solid var(--neon-cyan);
      border-radius: 5px;
      cursor: pointer;
      font-family: 'Share Tech Mono', monospace;
      font-size: 12px;
      transition: all 0.2s;
      white-space: nowrap;
    }
    
    .taskbar-app:hover {
      background: rgba(0, 255, 255, 0.3);
      box-shadow: var(--glow-cyan);
    }
    
    .taskbar-app.active {
      background: rgba(255, 0, 255, 0.3);
      border-color: var(--neon-pink);
      box-shadow: var(--glow-pink);
    }
    
    #cyber-clock {
      font-family: 'Orbitron', monospace;
      font-size: 18px;
      color: var(--neon-pink);
      text-shadow: var(--glow-pink);
      padding: 10px 20px;
      background: rgba(255, 0, 255, 0.1);
      border: 1px solid var(--neon-pink);
      border-radius: 5px;
    }
    
    /* === ANIMATIONS === */
    @keyframes scanlines {
      from { background-position: 0 0, 0 0, 0 0; }
      to { background-position: 0 4px, 0 0, 0 0; }
    }
    
    @keyframes flicker {
      0%, 100% { opacity: 0.95; }
      50% { opacity: 0.9; }
    }
    
    @keyframes gridMove {
      0% { transform: translate(0, 0); }
      100% { transform: translate(-50px, -50px); }
    }
    
    @keyframes hologramFloat {
      0%, 100% { transform: translateY(0) rotateX(0deg); }
      50% { transform: translateY(-10px) rotateX(2deg); }
    }
    
    /* === NOTIFICATIONS === */
    .cyber-notification {
      position: fixed;
      top: 20px;
      right: 20px;
      padding: 15px 25px;
      background: rgba(10, 15, 30, 0.95);
      border-left: 4px solid var(--neon-cyan);
      border-right: 4px solid var(--neon-pink);
      font-family: 'Share Tech Mono', monospace;
      box-shadow: 
        0 0 20px var(--neon-cyan),
        0 0 20px var(--neon-pink);
      transform: translateX(120%);
      transition: transform 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
      z-index: 10000;
      max-width: 400px;
    }
    
    .cyber-notification.show {
      transform: translateX(0);
    }
    
    ::-webkit-scrollbar {
      width: 8px;
      height: 8px;
    }
    
    ::-webkit-scrollbar-track {
      background: rgba(0, 255, 255, 0.1);
      border-radius: 4px;
    }
    
    ::-webkit-scrollbar-thumb {
      background: var(--neon-cyan);
      border-radius: 4px;
      box-shadow: 0 0 10px var(--neon-cyan);
    }
  </style>
</head>
<body>
  <!-- CRT Effects -->
  <div id="crt-effect"></div>
  <div id="crt-glow"></div>
  
  <!-- Neon Background -->
  <div id="neon-grid"></div>
  
  <!-- Main OS Container -->
  <div id="cyber-os">
    <!-- Desktop -->
    <div id="neon-desktop">
      <!-- Desktop icons will be generated here -->
    </div>
    
    <!-- Windows will be generated here -->
  </div>
  
  <!-- Cyber Menu -->
  <div id="cyber-menu">
    <div class="menu-header">
      <span>ANGYRDROID APPS v3.0</span>
      <div style="font-size: 12px; color: var(--neon-pink);">47 APPS LOADED</div>
    </div>
    
    <div class="menu-categories">
      <!-- Categories will be generated here -->
    </div>
    
    <div class="menu-content">
      <!-- App panels will be generated here -->
    </div>
  </div>
  
  <!-- Taskbar -->
  <div id="cyber-taskbar">
    <div id="menu-button" onclick="toggleMenu()">≡ NEON MENU</div>
    
    <div id="taskbar-apps">
      <!-- Running apps will appear here -->
    </div>
    
    <div id="cyber-clock">00:00:00</div>
  </div>

  <script>
    // ====== CYBERPUNK OS ENGINE ======
    
    // System State
    let windows = [];
    let activeWindow = null;
    let appCounter = 0;
    let runningApps = new Map();
    
    // AngryDroid Apps Database (from your list)
    const angryDroidApps = [
      // Main Capsules
      {
        id: 'mythic-capsule',
        name: 'Mythic Capsule Viewer',
        url: 'https://angrydroid.neocities.org/angrydroidwebsite/',
        icon: '🌀',
        category: 'main',
        color: '#ff00ff',
        description: 'Interactive 3D capsule viewer'
      },
      
      // Development Tools
      {
        id: 'crt-terminal',
        name: 'CRT Terminal',
        url: 'https://angrydroid.neocities.org/crt/',
        icon: '🌐',
        category: 'dev',
        color: '#00ffff',
        description: 'Retro CRT terminal interface'
      },
      {
        id: 'coder',
        name: 'Code Editor',
        url: 'https://angrydroid.neocities.org/coder/',
        icon: '💻',
        category: 'dev',
        color: '#00ff00',
        description: 'HTML/CSS/JS editor with preview'
      },
      {
        id: 'html-instruct',
        name: 'HTML Instructor',
        url: 'https://angrydroid.neocities.org/html_instruct/index.HTML',
        icon: '📚',
        category: 'dev',
        color: '#ff7700',
        description: 'Interactive HTML learning'
      },
      {
        id: 'compatibility-tester',
        name: 'Compatibility Tester',
        url: 'https://angrydroid.neocities.org/website_compatibility_tester/',
        icon: '🔧',
        category: 'dev',
        color: '#9d00ff',
        description: 'Website compatibility validator'
      },
      {
        id: 'capsule-builder',
        name: 'Capsule Builder',
        url: 'https://angrydroid.neocities.org/mythic_capsule_builder/',
        icon: '📝',
        category: 'dev',
        color: '#ff0080',
        description: 'Digital time capsule creation'
      },
      {
        id: 'capsule-pro',
        name: 'Capsule Pro',
        url: 'https://angrydroid.neocities.org/mythic-capsule-pro/',
        icon: '💾',
        category: 'dev',
        color: '#0080ff',
        description: 'Advanced capsule management'
      },
      {
        id: 'tag-it',
        name: 'Tag It',
        url: 'https://angrydroid.neocities.org/tag_it/',
        icon: '🏷️',
        category: 'dev',
        color: '#80ff00',
        description: 'Tagging and categorization'
      },
      {
        id: 'code-repository',
        name: 'Code Repository',
        url: 'https://angrydroid.neocities.org/code_repository_blog/repository%20project',
        icon: '📦',
        category: 'dev',
        color: '#80ffff',
        description: 'Code version management'
      },
      {
        id: 'watermark-maker',
        name: 'Watermark Maker',
        url: 'https://angrydroid.neocities.org/watermark_maker/',
        icon: '🔖',
        category: 'dev',
        color: '#ff80ff',
        description: 'Digital watermark creation'
      },
      
      // Mythic Network
      {
        id: 'mythic-space',
        name: 'Mythic Space',
        url: 'https://angrydroid.neocities.org/mythic_space/',
        icon: '🚀',
        category: 'network',
        color: '#ffff00',
        description: 'Virtual space exploration'
      },
      {
        id: 'mythic-radar',
        name: 'Mythic Radar',
        url: 'https://angrydroid.neocities.org/mythic_radar/',
        icon: '📡',
        category: 'network',
        color: '#ff5555',
        description: 'Digital radar interface'
      },
      {
        id: 'mythic-vault',
        name: 'Mythic Vault',
        url: 'https://angrydroid.neocities.org/mythic_vault_uplink/',
        icon: '🗝️',
        category: 'network',
        color: '#55ff55',
        description: 'Secure file vault system'
      },
      {
        id: 'web-ring',
        name: 'Web Ring',
        url: 'https://angrydroid.neocities.org/web_ring/',
        icon: '🔗',
        category: 'network',
        color: '#5555ff',
        description: 'Neocities web ring navigation'
      },
      {
        id: 'swamp-blog',
        name: 'Swamp Blog',
        url: 'https://angrydroid.neocities.org/swamp_blog/',
        icon: '🪷',
        category: 'network',
        color: '#ff55ff',
        description: 'Mythic Swamp documentation'
      },
      {
        id: 'virtual-cafe',
        name: 'Virtual Cafe',
        url: 'https://angrydroid.neocities.org/mythic_virtual_cafe/',
        icon: '☕',
        category: 'network',
        color: '#ffff55',
        description: 'Virtual social space'
      },
      {
        id: 'chat',
        name: 'Mythic Chat',
        url: 'https://angrydroid.neocities.org/chat/',
        icon: '💬',
        category: 'network',
        color: '#55ffff',
        description: 'Real-time chat interface'
      },
      
      // AI & Labs
      {
        id: 'angry-ai',
        name: 'Angry AI',
        url: 'https://angrydroid.neocities.org/angry_ai/',
        icon: '🤖',
        category: 'ai',
        color: '#ff0000',
        description: 'Sarcastic AI terminal'
      },
      {
        id: 'neural-browser',
        name: 'Neural Browser',
        url: 'https://angrydroid.neocities.org/neural_browser/',
        icon: '🧠',
        category: 'ai',
        color: '#00ff00',
        description: 'Experimental neural interface'
      },
      {
        id: 'neural-chat',
        name: 'Neural Chat',
        url: 'https://angrydroid.neocities.org/neural_chat/',
        icon: '💭',
        category: 'ai',
        color: '#0000ff',
        description: 'Neural network chat'
      },
      {
        id: 'qwens-web',
        name: 'Qwen\'s Web',
        url: 'https://angrydroid.neocities.org/qwens_web/',
        icon: '🌌',
        category: 'ai',
        color: '#ff00ff',
        description: 'AI exploration interface'
      },
      {
        id: 'ai-lab',
        name: 'AI Lab',
        url: 'https://angrydroid.neocities.org/angrydroid_ai_lab/',
        icon: '🧪',
        category: 'ai',
        color: '#ffff00',
        description: 'AI experimentation lab'
      },
      {
        id: 'fungal-research',
        name: 'Fungal Research',
        url: 'https://angrydroid.neocities.org/fungal_evolution_research_suite/',
        icon: '🍄',
        category: 'ai',
        color: '#00ffff',
        description: 'Biological simulation lab'
      },
      {
        id: 'quantum-wormhole',
        name: 'Quantum Wormhole',
        url: 'https://angrydroid.neocities.org/quantum_wormhole_simulation_lab/',
        icon: '🌀',
        category: 'ai',
        color: '#ff8800',
        description: 'Quantum physics simulation'
      },
      
      // Media & Audio
      {
        id: 'media-player',
        name: 'Media Player',
        url: 'https://angrydroid.neocities.org/mythic_media_player/media_player',
        icon: '🎵',
        category: 'media',
        color: '#ff00ff',
        description: 'Custom media player'
      },
      {
        id: 'mythic-beatbox',
        name: 'Mythic Beatbox',
        url: 'https://angrydroid.neocities.org/mythic_beatbox/',
        icon: '🎧',
        category: 'media',
        color: '#00ff00',
        description: 'Interactive beatbox'
      },
      {
        id: 'keyboard-piano',
        name: 'Keyboard Piano',
        url: 'https://angrydroid.neocities.org/keyboard_piano/inde',
        icon: '🎹',
        category: 'media',
        color: '#0000ff',
        description: 'Virtual piano'
      },
      {
        id: 'sonic-oscillograph',
        name: 'Sonic Oscillograph',
        url: 'https://angrydroid.neocities.org/sonic_oscillograph77/',
        icon: '📊',
        category: 'media',
        color: '#ff8800',
        description: 'Audio visualization'
      },
      
      // Creative Projects
      {
        id: 'fortune-fairy',
        name: 'Fortune Fairy',
        url: 'https://angrydroid.neocities.org/fortune_fairy/',
        icon: '🧚',
        category: 'creative',
        color: '#ff00ff',
        description: 'Digital fortune teller'
      },
      {
        id: 'glitch-purge',
        name: 'Glitch Purge',
        url: 'https://angrydroid.neocities.org/glitch_purge/',
        icon: '⚡',
        category: 'creative',
        color: '#00ffff',
        description: 'Glitch effect generator'
      },
      {
        id: 'galactic-mayhem',
        name: 'Galactic Mayhem',
        url: 'https://angrydroid.neocities.org/galactic_mahem_neon_skies/',
        icon: '🌌',
        category: 'creative',
        color: '#00ff00',
        description: 'Space-themed game'
      },
      {
        id: 'mythic-pet',
        name: 'Mythic Pet',
        url: 'https://angrydroid.neocities.org/mythic%20pet/',
        icon: '🐾',
        category: 'creative',
        color: '#ff8800',
        description: 'Digital pet simulation'
      },
      {
        id: 'pixel-art',
        name: 'Pixel Art Shrine',
        url: 'https://angrydroid.neocities.org/pixel%20art%20shrine%20editor/',
        icon: '🎨',
        category: 'creative',
        color: '#ff00ff',
        description: 'Pixel art creation'
      },
      {
        id: 'wizards-escape',
        name: 'Wizard\'s Escape',
        url: 'https://angrydroid.neocities.org/wizards_escape/',
        icon: '🧙',
        category: 'creative',
        color: '#8800ff',
        description: 'Puzzle escape game'
      },
      {
        id: 'sticker-maker',
        name: 'Sticker Maker',
        url: 'https://angrydroid.neocities.org/mythic_sticker_maker/',
        icon: '🖼️',
        category: 'creative',
        color: '#00ff88',
        description: 'Digital sticker creation'
      },
      {
        id: 'gallery-shrine',
        name: 'Gallery Shrine',
        url: 'https://angrydroid.neocities.org/gallery_shrine/',
        icon: '🛕',
        category: 'creative',
        color: '#ff0088',
        description: 'Digital art gallery'
      },
      
      // Utilities
      {
        id: 'mythic-os',
        name: 'MythicOS',
        url: 'https://angrydroid.neocities.org/mythicos/',
        icon: '💻',
        category: 'utils',
        color: '#00ffff',
        description: 'Web-based OS interface'
      },
      {
        id: 'retro-70s-os',
        name: 'Retro 70s OS',
        url: 'https://angrydroid.neocities.org/retro_70s_crt_%20oS/',
        icon: '📺',
        category: 'utils',
        color: '#ff8800',
        description: 'Retro CRT OS simulation'
      },
      {
        id: 'mythic-calendar',
        name: 'Mythic Calendar',
        url: 'https://angrydroid.neocities.org/mythic_calendar/',
        icon: '📅',
        category: 'utils',
        color: '#00ff00',
        description: 'Digital calendar'
      },
      {
        id: 'mythic-calculator',
        name: 'Mythic Calculator',
        url: 'https://angrydroid.neocities.org/mythic_Calculator%20/',
        icon: '🧮',
        category: 'utils',
        color: '#ff00ff',
        description: 'Calculator with special functions'
      },
      {
        id: 'mythic-notepad',
        name: 'Mythic Notepad',
        url: 'https://angrydroid.neocities.org/mythic_notepad/',
        icon: '📝',
        category: 'utils',
        color: '#ffff00',
        description: 'Encrypted notepad'
      },
      {
        id: 'worldmap',
        name: 'World Map',
        url: 'https://angrydroid.neocities.org/worldmap/',
        icon: '🗺️',
        category: 'utils',
        color: '#00ffff',
        description: 'Interactive world map'
      },
      
      // Security
      {
        id: 'password-generator',
        name: 'Password Generator',
        url: 'https://angrydroid.neocities.org/passwordgenrator/',
        icon: '🔑',
        category: 'security',
        color: '#ffff00',
        description: 'Secure password generation'
      },
      {
        id: 'matrix-encryptor',
        name: 'Matrix Encryptor',
        url: 'https://angrydroid.neocities.org/matrix_encryptor/',
        icon: '🔒',
        category: 'security',
        color: '#00ff00',
        description: 'Matrix-style encryption'
      },
      {
        id: 'security-scanner',
        name: 'Security Scanner',
        url: 'https://angrydroid.neocities.org/securityscanner/',
        icon: '🛡️',
        category: 'security',
        color: '#ff0000',
        description: 'Website security scanner'
      },
      {
        id: 'security-wizard',
        name: 'Security Wizard',
        url: 'https://angrydroid.neocities.org/security_wizard/',
        icon: '🧙',
        category: 'security',
        color: '#0000ff',
        description: 'Security configuration'
      }
    ];
    
    // Category Definitions
    const categories = {
      'all': { name: 'All Apps', icon: '📱', color: '#ff00ff' },
      'main': { name: 'Main Capsules', icon: '🌀', color: '#00ffff' },
      'dev': { name: 'Development', icon: '💻', color: '#00ff00' },
      'network': { name: 'Mythic Network', icon: '🌐', color: '#ff7700' },
      'ai': { name: 'AI & Labs', icon: '🤖', color: '#9d00ff' },
      'media': { name: 'Media & Audio', icon: '🎵', color: '#ff0080' },
      'creative': { name: 'Creative', icon: '🎨', color: '#0080ff' },
      'utils': { name: 'Utilities', icon: '🛠️', color: '#80ff00' },
      'security': { name: 'Security', icon: '🔒', color: '#ff5555' }
    };
    
    // ====== INITIALIZATION ======
    function initCyberOS() {
      createDesktopIcons();
      createMenu();
      updateClock();
      showNotification('CYBERPUNK OS v3.0', '47 AngryDroid apps loaded');
      
      // Open welcome window
      setTimeout(() => openApp('mythic-capsule'), 1000);
    }
    
    // ====== MENU SYSTEM ======
    function createMenu() {
      const menuCategories = document.querySelector('.menu-categories');
      const menuContent = document.querySelector('.menu-content');
      
      // Create category tabs
      for (const [catId, catInfo] of Object.entries(categories)) {
        const tab = document.createElement('div');
        tab.className = 'category-tab';
        tab.dataset.category = catId;
        tab.innerHTML = `${catInfo.icon} ${catInfo.name}`;
        tab.style.color = catInfo.color;
        tab.onclick = () => switchCategory(catId);
        
        if (catId === 'all') tab.classList.add('active');
        menuCategories.appendChild(tab);
      }
      
      // Create category panels
      for (const [catId, catInfo] of Object.entries(categories)) {
        const panel = document.createElement('div');
        panel.id = `panel-${catId}`;
        panel.className = `category-panel ${catId === 'all' ? 'active' : ''}`;
        panel.dataset.category = catId;
        
        // Filter apps for this category
        let appsForCategory;
        if (catId === 'all') {
          appsForCategory = angryDroidApps;
        } else {
          appsForCategory = angryDroidApps.filter(app => app.category === catId);
        }
        
        // Add apps to panel
        appsForCategory.forEach(app => {
          const appElement = createMenuItem(app);
          panel.appendChild(appElement);
        });
        
        menuContent.appendChild(panel);
      }
    }
    
    function createMenuItem(app) {
      const element = document.createElement('div');
      element.className = 'menu-app';
      element.dataset.appId = app.id;
      element.onclick = () => openApp(app.id);
      
      const isRunning = runningApps.has(app.id);
      
      element.innerHTML = `
        <div class="app-icon" style="color: ${app.color}">${app.icon}</div>
        <div class="app-info">
          <div class="app-name">${app.name}</div>
          <div class="app-category">${categories[app.category].name}</div>
        </div>
        <div class="app-status ${isRunning ? 'running' : ''}"></div>
      `;
      
      return element;
    }
    
    function switchCategory(catId) {
      // Update tabs
      document.querySelectorAll('.category-tab').forEach(tab => {
        tab.classList.remove('active');
        if (tab.dataset.category === catId) {
          tab.classList.add('active');
        }
      });
      
      // Update panels
      document.querySelectorAll('.category-panel').forEach(panel => {
        panel.classList.remove('active');
        if (panel.dataset.category === catId) {
          panel.classList.add('active');
        }
      });
    }
    
    function toggleMenu() {
      const menu = document.getElementById('cyber-menu');
      menu.style.display = menu.style.display === 'flex' ? 'none' : 'flex';
    }
    
    // Close menu when clicking outside
    document.addEventListener('click', (e) => {
      const menu = document.getElementById('cyber-menu');
      const menuBtn = document.getElementById('menu-button');
      
      if (!menu.contains(e.target) && !menuBtn.contains(e.target)) {
        menu.style.display = 'none';
      }
    });
    
    // ====== APP MANAGEMENT ======
    function openApp(appId) {
      const app = angryDroidApps.find(a => a.id === appId);
      if (!app) return;
      
      // Check if app is already running
      if (runningApps.has(appId)) {
        const window = document.getElementById(`window-${appId}`);
        if (window) {
          bringToFront(window);
          return;
        }
      }
      
      // Create window
      const windowId = `window-${appId}`;
      const window = document.createElement('div');
      window.className = 'hologram-window';
      window.id = windowId;
      window.style.left = `${100 + (runningApps.size * 30)}px`;
      window.style.top = `${100 + (runningApps.size * 30)}px`;
      window.style.zIndex = 100 + runningApps.size;
      
      window.innerHTML = `
        <div class="window-header">
          <span>${app.name}</span>
          <div class="window-buttons">
            <div class="hologram-btn minimize" onclick="minimizeWindow('${windowId}')"></div>
            <div class="hologram-btn maximize" onclick="maximizeWindow('${windowId}')"></div>
            <div class="hologram-btn close" onclick="closeWindow('${windowId}')"></div>
          </div>
        </div>
        <div class="window-content">
          <iframe class="window-iframe" src="${app.url}" title="${app.name}"></iframe>
        </div>
      `;
      
      document.getElementById('cyber-os').appendChild(window);
      makeDraggable(window);
      windows.push(windowId);
      runningApps.set(appId, windowId);
      bringToFront(window);
      addToTaskbar(appId, app.name);
      updateMenuStatus(appId, true);
      
      // Hide menu
      document.getElementById('cyber-menu').style.display = 'none';
      
      showNotification('APP LAUNCHED', `${app.name} is now running`);
    }
    
    function closeWindow(windowId) {
      const window = document.getElementById(windowId);
      if (!window) return;
      
      // Find app ID
      let appId = null;
      for (const [id, winId] of runningApps.entries()) {
        if (winId === windowId) {
          appId = id;
          break;
        }
      }
      
      // Remove from system
      window.remove();
      windows = windows.filter(id => id !== windowId);
      runningApps.delete(appId);
      
      // Remove from taskbar
      const taskbarApp = document.querySelector(`[data-app-id="${appId}"]`);
      if (taskbarApp) taskbarApp.remove();
      
      // Update menu status
      if (appId) updateMenuStatus(appId, false);
      
      showNotification('APP CLOSED', 'Window terminated');
    }
    
    function minimizeWindow(windowId) {
      const window = document.getElementById(windowId);
      window.style.display = 'none';
      
      // Update taskbar
      const appId = getAppIdFromWindow(windowId);
      const taskbarApp = document.querySelector(`[data-app-id="${appId}"]`);
      if (taskbarApp) taskbarApp.classList.remove('active');
    }
    
    function maximizeWindow(windowId) {
      const window = document.getElementById(windowId);
      const isMaximized = window.style.width === '95vw';
      
      if (!isMaximized) {
        window.style.width = '95vw';
        window.style.height = '85vh';
        window.style.left = '2.5vw';
        window.style.top = '2.5vh';
      } else {
        window.style.width = '800px';
        window.style.height = '600px';
        window.style.left = '100px';
        window.style.top = '100px';
      }
      
      bringToFront(window);
    }
    
    function getAppIdFromWindow(windowId) {
      for (const [id, winId] of runningApps.entries()) {
        if (winId === windowId) return id;
      }
      return null;
    }
    
    // ====== WINDOW MANAGEMENT ======
    function makeDraggable(window) {
      const header = window.querySelector('.window-header');
      let offsetX = 0, offsetY = 0;
      
      header.addEventListener('mousedown', startDrag);
      
      function startDrag(e) {
        if (e.target.classList.contains('hologram-btn')) return;
        
        bringToFront(window);
        offsetX = e.clientX - window.offsetLeft;
        offsetY = e.clientY - window.offsetTop;
        
        document.addEventListener('mousemove', drag);
        document.addEventListener('mouseup', stopDrag);
      }
      
      function drag(e) {
        window.style.left = (e.clientX - offsetX) + 'px';
        window.style.top = (e.clientY - offsetY) + 'px';
      }
      
      function stopDrag() {
        document.removeEventListener('mousemove', drag);
        document.removeEventListener('mouseup', stopDrag);
      }
    }
    
    function bringToFront(window) {
      document.querySelectorAll('.hologram-window').forEach(w => {
        w.style.zIndex = 100;
      });
      
      window.style.zIndex = 1000;
      activeWindow = window.id;
      
      // Update taskbar
      const appId = getAppIdFromWindow(window.id);
      if (appId) {
        document.querySelectorAll('.taskbar-app').forEach(app => {
          app.classList.remove('active');
        });
        
        const taskbarApp = document.querySelector(`[data-app-id="${appId}"]`);
        if (taskbarApp) taskbarApp.classList.add('active');
      }
    }
    
    // ====== TASKBAR ======
    function addToTaskbar(appId, appName) {
      const taskbar = document.getElementById('taskbar-apps');
      
      // Check if already in taskbar
      if (document.querySelector(`[data-app-id="${appId}"]`)) return;
      
      const appElement = document.createElement('div');
      appElement.className = 'taskbar-app';
      appElement.dataset.appId = appId;
      appElement.textContent = appName;
      
      appElement.onclick = () => {
        const windowId = runningApps.get(appId);
        if (windowId) {
          const window = document.getElementById(windowId);
          if (window.style.display === 'none') {
            window.style.display = 'flex';
          }
          bringToFront(window);
        }
      };
      
      taskbar.appendChild(appElement);
    }
    
    // ====== DESKTOP ICONS ======
    function createDesktopIcons() {
      const desktop = document.getElementById('neon-desktop');
      
      // Add 6 popular apps to desktop
      const desktopApps = [
        'mythic-capsule',
        'crt-terminal',
        'fortune-fairy',
        'coder',
        'mythic-space',
        'angry-ai'
      ];
      
      desktopApps.forEach(appId => {
        const app = angryDroidApps.find(a => a.id === appId);
        if (!app) return;
        
        const icon = document.createElement('div');
        icon.className = 'cyber-icon';
        icon.onclick = () => openApp(appId);
        
        icon.innerHTML = `
          <div style="font-size: 48px; margin-bottom: 10px; color: ${app.color}; 
               filter: drop-shadow(0 0 10px ${app.color})">
            ${app.icon}
          </div>
          <div style="font-family: 'Share Tech Mono', monospace; font-size: 12px; 
               color: var(--neon-cyan); text-align: center; text-shadow: 0 0 5px var(--neon-cyan);
               background: rgba(0,0,0,0.7); padding: 5px; border-radius: 3px; max-width: 100px;">
            ${app.name}
          </div>
        `;
        
        desktop.appendChild(icon);
      });
    }
    
    // ====== UTILITIES ======
    function updateMenuStatus(appId, isRunning) {
      const menuItem = document.querySelector(`.menu-app[data-app-id="${appId}"] .app-status`);
      if (menuItem) {
        menuItem.className = `app-status ${isRunning ? 'running' : ''}`;
      }
    }
    
    function updateClock() {
      const now = new Date();
      const time = now.toLocaleTimeString('en-US', {hour12: false});
      const date = now.toLocaleDateString('en-US', { 
        weekday: 'short', 
        month: 'short', 
        day: 'numeric' 
      });
      
      document.getElementById('cyber-clock').innerHTML = `
        <div>${time}</div>
        <div style="font-size: 12px; color: var(--neon-cyan);">${date}</div>
      `;
      
      setTimeout(updateClock, 1000);
    }
    
    function showNotification(title, message) {
      const notification = document.createElement('div');
      notification.className = 'cyber-notification';
      notification.innerHTML = `
        <h4 style="color: var(--neon-pink); margin-bottom: 5px;">${title}</h4>
        <div>${message}</div>
      `;
      
      document.body.appendChild(notification);
      
      setTimeout(() => notification.classList.add('show'), 10);
      
      setTimeout(() => {
        notification.classList.remove('show');
        setTimeout(() => notification.remove(), 400);
      }, 3000);
    }
    
    // ====== INITIALIZE ======
    window.addEventListener('load', initCyberOS);
    window.addEventListener('resize', () => {
      // Handle window resize if needed
    });
  </script>
</body>
</html>
