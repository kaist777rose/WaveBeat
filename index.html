<!DOCTYPE html>  
<html lang="en">  
<head>  
<meta charset="UTF-8">  
<meta name="viewport" content="width=device-width, initial-scale=1.0">  
<title>WaveBeat — Audio Visualizer</title>  
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Syne:wght@700;800&display=swap" rel="stylesheet">  
<style>  
:root{  
  --bg:#030308;  
  --surface:#0c0c18;  
  --border:#1e1e3a;  
  --accent:#7c3aed;  
  --accent2:#06b6d4;  
  --accent3:#f59e0b;  
  --text:#f0f0ff;  
  --muted:#6b7280;  
  --success:#10b981;  
}  
*{margin:0;padding:0;box-sizing:border-box;}  
html{scroll-behavior:smooth;}  
body{  
  background:var(--bg);color:var(--text);  
  font-family:'Space Mono',monospace;  
  min-height:100vh;  
  overflow-x:hidden;  
}  
  
/* **──** Animated background **──** */  
body::before{  
  content:'';position:fixed;inset:0;z-index:0;  
  background:  
    radial-gradient(ellipse 80% 50% at 20% 20%, rgba(124,58,237,.12) 0%, transparent 60%),  
    radial-gradient(ellipse 60% 40% at 80% 80%, rgba(6,182,212,.1) 0%, transparent 60%),  
    radial-gradient(ellipse 50% 60% at 50% 50%, rgba(245,158,11,.04) 0%, transparent 70%);  
  animation:bgPulse 8s ease-in-out infinite alternate;  
  pointer-events:none;  
}  
@keyframes bgPulse{  
  0%{opacity:.7;}  
  100%{opacity:1;}  
}  
  
/* Grid overlay */  
body::after{  
  content:'';position:fixed;inset:0;z-index:0;pointer-events:none;  
  background-image:linear-gradient(rgba(124,58,237,.04) 1px,transparent 1px),linear-gradient(90deg,rgba(124,58,237,.04) 1px,transparent 1px);  
  background-size:40px 40px;  
}  
  
.container{position:relative;z-index:1;max-width:700px;margin:0 auto;padding:40px 24px 100px;}  
  
/* **──** Header **──** */  
.header{  
  padding:48px 0 56px;  
  display:flex;flex-direction:column;align-items:center;text-align:center;  
}  
.logo-mark{  
  display:flex;align-items:center;gap:14px;margin-bottom:12px;  
}  
.logo-icon{  
  width:44px;height:44px;  
  background:linear-gradient(135deg,var(--accent),var(--accent2));  
  border-radius:12px;display:flex;align-items:center;justify-content:center;  
  font-size:22px;box-shadow:0 0 30px rgba(124,58,237,.5);  
  animation:iconPulse 3s ease-in-out infinite;  
}  
@keyframes iconPulse{  
  0%,100%{box-shadow:0 0 30px rgba(124,58,237,.5);}  
  50%{box-shadow:0 0 50px rgba(124,58,237,.8),0 0 80px rgba(6,182,212,.3);}  
}  
.logo-text{  
  font-family:'Syne',sans-serif;  
  font-size:clamp(32px,6vw,52px);  
  font-weight:800;letter-spacing:-2px;  
  background:linear-gradient(135deg,#fff 0%,var(--accent2) 50%,var(--accent) 100%);  
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;  
}  
.tagline{  
  font-size:11px;letter-spacing:4px;color:var(--muted);  
  text-transform:uppercase;margin-top:4px;font-weight:800;  
}  
  
/* **──** Card **──** */  
.card{  
  background:var(--surface);  
  border:1px solid var(--border);  
  border-radius:16px;padding:24px;margin-bottom:16px;  
  position:relative;overflow:hidden;  
  transition:border-color .3s;  
}  
.card::before{  
  content:'';position:absolute;inset:0;border-radius:16px;  
  background:linear-gradient(135deg,rgba(124,58,237,.05),transparent 60%);  
  pointer-events:none;  
}  
.card:hover{border-color:rgba(124,58,237,.4);}  
  
.card-label{  
  font-size:9px;letter-spacing:4px;color:var(--accent2);  
  text-transform:uppercase;font-weight:800;  
  margin-bottom:16px;display:flex;align-items:center;gap:10px;  
}  
.card-label::after{content:'';flex:1;height:1px;background:linear-gradient(90deg,var(--border),transparent);}  
  
/* **──** Drop zone **──** */  
.drop{  
  border:1px dashed rgba(124,58,237,.4);border-radius:10px;  
  padding:32px 16px;text-align:center;cursor:pointer;  
  transition:all .25s;background:rgba(124,58,237,.04);  
  position:relative;overflow:hidden;  
}  
.drop::before{  
  content:'';position:absolute;inset:0;  
  background:linear-gradient(135deg,rgba(124,58,237,.08),rgba(6,182,212,.08));  
  opacity:0;transition:opacity .25s;  
}  
.drop:hover::before,.drop.over::before{opacity:1;}  
.drop:hover{border-color:rgba(124,58,237,.8);}  
.drop.active{border:1px solid var(--accent);background:rgba(124,58,237,.08);}  
.drop.over{border-color:var(--accent2);background:rgba(6,182,212,.06);}  
.drop-ico{font-size:30px;display:block;margin-bottom:10px;opacity:.7;}  
.drop-sub{font-size:11px;color:var(--muted);letter-spacing:1px;font-weight:800;}  
.drop-name{font-size:11px;color:var(--accent2);margin-top:8px;word-break:break-all;display:none;font-weight:700;}  
.drop.active .drop-name{display:block;}  
.drop.active .drop-sub{display:none;}  
input[type=file]{display:none;}  
  
/* **──** Settings grid **──** */  
.settings{display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-top:4px;}  
.s-item{background:rgba(255,255,255,.02);border:1px solid var(--border);padding:14px;border-radius:10px;}  
.s-item.full{grid-column:1/-1;}  
.s-lbl{font-size:8px;letter-spacing:3px;color:var(--muted);text-transform:uppercase;margin-bottom:8px;display:block;font-weight:700;}  
select,input[type=text],textarea{  
  background:rgba(255,255,255,.04);border:1px solid var(--border);  
  color:var(--text);font-family:'Space Mono',monospace;font-size:11px;font-weight:700;  
  padding:9px 12px;width:100%;outline:none;  
  transition:border-color .2s;-webkit-appearance:none;border-radius:7px;  
}  
select:focus,input[type=text]:focus,textarea:focus{border-color:var(--accent);}  
select option{background:#0c0c18;color:#f0f0ff;}  
textarea{resize:vertical;min-height:80px;line-height:1.7;}  
  
/* **──** Color row **──** */  
.clr-row{display:flex;gap:8px;align-items:center;}  
.clr-box{width:36px;height:36px;border:1px solid var(--border);flex-shrink:0;cursor:pointer;position:relative;overflow:hidden;border-radius:8px;}  
.clr-box input[type=color]{position:absolute;inset:-4px;width:calc(100%+8px);height:calc(100%+8px);opacity:0;cursor:pointer;border:none;padding:0;}  
.clr-fill{width:100%;height:100%;pointer-events:none;}  
.clr-row input[type=text]{flex:1;}  
  
/* **──** Wave style **──** */  
.wave-styles{display:flex;gap:7px;flex-wrap:wrap;}  
.ws{  
  flex:1;min-width:70px;padding:10px 4px;text-align:center;  
  border:1px solid var(--border);border-radius:8px;  
  font-size:9px;font-weight:700;letter-spacing:1px;  
  color:var(--muted);cursor:pointer;background:transparent;  
  transition:all .2s;text-transform:uppercase;font-family:'Space Mono',monospace;  
}  
.ws:hover{border-color:var(--accent);color:var(--text);}  
.ws.sel{border-color:var(--accent);background:rgba(124,58,237,.15);color:var(--accent2);}  
  
/* **──** Theme chips **──** */  
.theme-chips{display:flex;gap:8px;flex-wrap:wrap;margin-top:4px;}  
.chip{width:30px;height:30px;border-radius:50%;cursor:pointer;border:2px solid transparent;transition:all .2s;flex-shrink:0;}  
.chip:hover{transform:scale(1.15);}  
.chip.sel{border-color:#fff;transform:scale(1.2);box-shadow:0 0 12px rgba(255,255,255,.3);}  
  
/* **──** Logo section **──** */  
.logo-preview{display:none;margin-top:12px;align-items:center;gap:12px;}  
.logo-preview.show{display:flex;}  
.logo-preview img{height:44px;max-width:130px;object-fit:contain;border:1px solid var(--border);border-radius:8px;background:rgba(255,255,255,.05);padding:4px;}  
.logo-pos-row{display:flex;gap:6px;flex-wrap:wrap;margin-top:10px;}  
.lp{  
  font-size:9px;font-weight:700;letter-spacing:1px;padding:7px 12px;  
  border:1px solid var(--border);border-radius:7px;cursor:pointer;  
  color:var(--muted);background:transparent;transition:all .2s;  
  font-family:'Space Mono',monospace;  
}  
.lp:hover{border-color:var(--accent);color:var(--text);}  
.lp.sel{border-color:var(--accent);background:rgba(124,58,237,.15);color:var(--accent2);}  
  
/* **──** Lyrics **──** */  
.lyric-toggle{display:flex;align-items:center;gap:10px;margin-bottom:12px;cursor:pointer;}  
.lyric-toggle input[type=checkbox]{width:16px;height:16px;accent-color:var(--accent);cursor:pointer;}  
.lyric-toggle span{font-size:10px;font-weight:800;color:var(--text);letter-spacing:2px;text-transform:uppercase;}  
.lyric-body{display:none;}  
.lyric-body.show{display:block;}  
  
/* **──** Badge **──** */  
.badge{  
  font-size:8px;letter-spacing:2px;color:var(--accent3);  
  background:rgba(245,158,11,.15);border:1px solid rgba(245,158,11,.4);  
  padding:2px 8px;margin-left:6px;font-weight:800;border-radius:4px;  
}  
  
/* **──** Range slider **──** */  
input[type=range]{  
  width:100%;margin-top:6px;  
  accent-color:var(--accent);  
  -webkit-appearance:none;height:4px;border-radius:2px;  
  background:var(--border);outline:none;  
}  
input[type=range]::-webkit-slider-thumb{  
  -webkit-appearance:none;width:16px;height:16px;border-radius:50%;  
  background:var(--accent);cursor:pointer;box-shadow:0 0 8px rgba(124,58,237,.6);  
}  
  
/* **──** Preview **──** */  
.preview-wrap{  
  margin-top:16px;border:1px solid var(--border);  
  border-radius:10px;overflow:hidden;background:#000;display:none;  
}  
.preview-wrap.show{display:block;}  
.preview-wrap canvas{width:100%;display:block;}  
  
/* **──** Progress **──** */  
.prog-wrap{margin-top:16px;display:none;}  
.prog-wrap.show{display:block;}  
.prog-lbl{font-size:8px;letter-spacing:3px;color:var(--muted);margin-bottom:8px;font-weight:700;text-transform:uppercase;}  
.prog-track{height:2px;background:var(--border);overflow:hidden;border-radius:2px;}  
.prog-bar{  
  height:100%;  
  background:linear-gradient(90deg,var(--accent),var(--accent2));  
  width:0%;transition:width .35s;border-radius:2px;  
  box-shadow:0 0 8px rgba(124,58,237,.8);  
}  
.prog-bar.anim{width:30%;animation:scan 1.2s ease-in-out infinite;}  
@keyframes scan{0%{transform:translateX(-200%)}100%{transform:translateX(500%)}}  
.prog-msg{font-size:12px;color:var(--muted);margin-top:10px;font-weight:800;}  
.prog-msg.ok{color:var(--success);}  
.prog-msg.err{color:#ef4444;}  
  
/* **──** Buttons **──** */  
.btn-convert{  
  width:100%;  
  background:linear-gradient(135deg,var(--accent),#5b21b6);  
  color:#fff;border:none;font-family:'Syne',sans-serif;  
  font-size:18px;font-weight:800;letter-spacing:4px;  
  text-transform:uppercase;padding:20px;cursor:pointer;  
  border-radius:12px;margin-bottom:14px;  
  transition:all .25s;position:relative;overflow:hidden;  
  box-shadow:0 4px 30px rgba(124,58,237,.4);  
}  
.btn-convert::before{  
  content:'';position:absolute;inset:0;  
  background:linear-gradient(135deg,rgba(255,255,255,.1),transparent);  
  opacity:0;transition:opacity .25s;  
}  
.btn-convert:hover::before{opacity:1;}  
.btn-convert:hover{transform:translateY(-2px);box-shadow:0 8px 40px rgba(124,58,237,.6);}  
.btn-convert:active{transform:translateY(0);}  
.btn-convert:disabled{  
  background:linear-gradient(135deg,#2a2a4a,#1e1e3a);  
  color:var(--muted);cursor:not-allowed;transform:none;  
  box-shadow:none;  
}  
  
.btn-dl{  
  display:none;width:100%;  
  background:transparent;color:var(--success);  
  border:1px solid var(--success);font-family:'Space Mono',monospace;  
  font-size:13px;font-weight:700;letter-spacing:4px;  
  padding:17px;cursor:pointer;text-align:center;  
  text-decoration:none;transition:all .25s;  
  margin-bottom:14px;border-radius:12px;  
  box-shadow:0 0 20px rgba(16,185,129,.15);  
}  
.btn-dl.show{display:block;}  
.btn-dl:hover{background:rgba(16,185,129,.1);box-shadow:0 0 30px rgba(16,185,129,.3);}  
  
.btn-reset{  
  font-size:10px;color:var(--muted);letter-spacing:3px;font-weight:800;  
  cursor:pointer;text-align:center;display:block;width:100%;  
  transition:color .2s;text-transform:uppercase;background:none;border:none;  
  font-family:'Space Mono',monospace;padding:8px;  
}  
.btn-reset:hover{color:var(--text);}  
  
.fmt-note{  
  font-size:10px;color:var(--muted);margin-top:12px;  
  text-align:center;line-height:1.8;font-weight:800;  
}  
  
/* **──** Footer **──** */  
.footer{  
  text-align:center;margin-top:60px;padding-top:24px;  
  border-top:1px solid var(--border);  
}  
.footer-logo{  
  font-family:'Syne',sans-serif;font-size:20px;font-weight:800;letter-spacing:-1px;  
  background:linear-gradient(135deg,#fff,var(--accent2));  
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text;  
}  
.footer-sub{font-size:9px;letter-spacing:3px;color:var(--muted);margin-top:4px;font-weight:800;}  
  
@media(max-width:520px){.settings{grid-template-columns:1fr;}}  
</style>  
</head>  
<body>  
  
<div class="container">  
  
  <!-- Header -->  
  <div class="header">  
    <div class="logo-mark">  
      <div class="logo-icon">🌊</div>  
      <div class="logo-text">WaveBeat</div>  
    </div>  
    <div class="tagline">// Audio Visualizer · MP3 to MP4 · No Server</div>  
  </div>  
  
  <!-- Audio -->  
  <div class="card">  
    <div class="card-label">Audio File</div>  
    <div class="drop" id="mp3Zone">  
      <span class="drop-ico">**♫**</span>  
      <span class="drop-sub">MP3 · WAV · M4A · AAC — Click or Drag</span>  
      <span class="drop-name" id="mp3Name"></span>  
      <input type="file" id="mp3Input">  
    </div>  
  </div>  
  
  <!-- Background Image -->  
  <div class="card">  
    <div class="card-label">Background Image <span class="badge">OPTIONAL</span></div>  
    <div class="drop" id="bgImgZone">  
      <span class="drop-ico">🖼</span>  
      <span class="drop-sub">JPG · PNG · WEBP — Click or Drag</span>  
      <span class="drop-name" id="bgImgName"></span>  
      <input type="file" id="bgImgInput">  
    </div>  
    <div id="bgThumbWrap" style="display:none;margin-top:12px;">  
      <img id="bgThumbImg" style="width:100%;max-height:80px;object-fit:cover;border:1px solid var(--border);border-radius:8px;opacity:.8;" src="" alt="">  
      <div style="display:flex;justify-content:space-between;align-items:center;margin-top:10px;">  
        <span class="s-lbl" style="margin:0;">Darkness</span>  
        <span style="font-size:11px;color:var(--accent2);font-weight:700;" id="dimVal">65%</span>  
      </div>  
      <input type="range" id="dimSlider" min="0" max="95" value="65">  
      <button id="bgClearBtn" style="margin-top:10px;width:100%;background:transparent;border:1px solid var(--border);color:var(--muted);font-family:'Space Mono',monospace;font-size:10px;font-weight:700;letter-spacing:3px;padding:8px;cursor:pointer;border-radius:8px;text-transform:uppercase;transition:all .2s;" onmouseover="this.style.borderColor='#7c3aed'" onmouseout="this.style.borderColor=''">✕ Remove Image</button>  
    </div>  
  </div>  
  
  <!-- Watermark -->  
  <div class="card">  
    <div class="card-label">Watermark / Logo <span class="badge">OPTIONAL</span></div>  
    <div class="drop" id="logoZone">  
      <span class="drop-ico">💧</span>  
      <span class="drop-sub">PNG (transparent background recommended)</span>  
      <span class="drop-name" id="logoName"></span>  
      <input type="file" id="logoInput" accept="image/*">  
    </div>  
    <div class="logo-preview" id="logoPreview">  
      <img id="logoThumb" src="" alt="logo">  
      <div style="flex:1;">  
        <span class="s-lbl">Size</span>  
        <input type="range" id="logoSize" min="5" max="30" value="12">  
        <div style="display:flex;justify-content:space-between;font-size:10px;color:var(--accent2);font-weight:700;margin-top:2px;">  
          <span>Small</span><span id="logoSizeVal">12%</span><span>Large</span>  
        </div>  
      </div>  
    </div>  
    <div class="logo-pos-row" id="logoPosRow" style="display:none;">  
      <div class="lp" data-pos="tl">↖ Top Left</div>  
      <div class="lp" data-pos="tr">↗ Top Right</div>  
      <div class="lp sel" data-pos="br">↘ Bottom Right</div>  
      <div class="lp" data-pos="bl">↙ Bottom Left</div>  
      <div class="lp" data-pos="bc">↓ Bottom Center</div>  
    </div>  
    <button id="logoClearBtn" style="display:none;margin-top:10px;width:100%;background:transparent;border:1px solid var(--border);color:var(--muted);font-family:'Space Mono',monospace;font-size:10px;font-weight:700;letter-spacing:3px;padding:8px;cursor:pointer;border-radius:8px;text-transform:uppercase;">✕ Remove Logo</button>  
  </div>  
  
  <!-- Settings -->  
  <div class="card">  
    <div class="card-label">Settings</div>  
    <div class="settings">  
  
      <div class="s-item full">  
        <span class="s-lbl">Track Title (auto-filled · editable)</span>  
        <input type="text" id="songTitle" placeholder="Enter track title">  
      </div>  
  
      <div class="s-item full">  
        <span class="s-lbl">Artist Name</span>  
        <input type="text" id="songArtist" placeholder="Artist name (optional)">  
      </div>  
  
      <div class="s-item">  
        <span class="s-lbl">Resolution</span>  
        <select id="resSelect">  
          <option value="1920,1080">1920 × 1080 (FHD)</option>  
          <option value="1280,720" selected>1280 × 720 (HD)</option>  
          <option value="854,480">854 × 480</option>  
          <option value="640,360">640 × 360</option>  
        </select>  
      </div>  
  
      <div class="s-item">  
        <span class="s-lbl">Bitrate</span>  
        <select id="brSelect">  
          <option value="4000000">Best · 4 Mbps</option>  
          <option value="2500000" selected>High · 2.5 Mbps</option>  
          <option value="1500000">Medium · 1.5 Mbps</option>  
          <option value="800000">Low · 0.8 Mbps</option>  
        </select>  
      </div>  
  
      <div class="s-item">  
        <span class="s-lbl">Background Color</span>  
        <div class="clr-row">  
          <div class="clr-box">  
            <div class="clr-fill" id="clrFill" style="background:#030308"></div>  
            <input type="color" id="clrPicker" value="#030308">  
          </div>  
          <input type="text" id="clrText" value="#030308" maxlength="7">  
        </div>  
      </div>  
  
      <div class="s-item">  
        <span class="s-lbl">Visualizer Style</span>  
        <div class="wave-styles">  
          <div class="ws" data-style="bars">**▊** Bars</div>  
          <div class="ws" data-style="mirror">⬡ Mirror</div>  
          <div class="ws" data-style="line">〰 Line</div>  
          <div class="ws sel" data-style="circle">**◎** Circle</div>  
          <div class="ws" data-style="heart">♥ Heart</div>  
        </div>  
      </div>  
  
      <div class="s-item full">  
        <span class="s-lbl">Color Theme</span>  
        <div class="theme-chips" id="themeChips">  
          <div class="chip sel" data-theme="cyan"   style="background:linear-gradient(135deg,#00e5ff,#0066ff)"></div>  
          <div class="chip"     data-theme="gold"   style="background:linear-gradient(135deg,#ffd700,#ff6600)"></div>  
          <div class="chip"     data-theme="purple" style="background:linear-gradient(135deg,#bf5fff,#ff3cac)"></div>  
          <div class="chip"     data-theme="green"  style="background:linear-gradient(135deg,#00ff88,#00ccaa)"></div>  
          <div class="chip"     data-theme="red"    style="background:linear-gradient(135deg,#ff4444,#ff8800)"></div>  
          <div class="chip"     data-theme="white"  style="background:linear-gradient(135deg,#ffffff,#aaccff)"></div>  
        </div>  
      </div>  
  
      <div class="s-item full">  
        <span class="s-lbl">Output Filename</span>  
        <input type="text" id="fname" value="output" placeholder="output">  
      </div>  
  
    </div>  
  
    <!-- Lyrics -->  
    <div style="margin-top:18px;padding-top:16px;border-top:1px solid var(--border);">  
      <label class="lyric-toggle">  
        <input type="checkbox" id="lyricsEnabled">  
        <span>🎵 Show Lyrics (optional)</span>  
      </label>  
      <div class="lyric-body" id="lyricBody">  
        <div class="s-lbl" style="margin-bottom:6px;">Lyrics — one line per row (in order)</div>  
        <textarea id="lyricsText" placeholder="First lyric line&#10;Second lyric line&#10;Third lyric line&#10;..."></textarea>  
        <div style="margin-top:10px;display:flex;align-items:center;gap:10px;">  
          <span class="s-lbl" style="margin:0;white-space:nowrap;">Lyric Color</span>  
          <div class="clr-box" style="width:30px;height:30px;">  
            <div class="clr-fill" id="lyricClrFill" style="background:#ffffff"></div>  
            <input type="color" id="lyricClrPicker" value="#ffffff">  
          </div>  
          <input type="text" id="lyricClrText" value="#ffffff" maxlength="7" style="width:100px;">  
        </div>  
      </div>  
    </div>  
  
    <!-- Preview -->  
    <div class="preview-wrap" id="previewWrap">  
      <canvas id="previewCanvas"></canvas>  
    </div>  
  
    <!-- Progress -->  
    <div class="prog-wrap" id="progWrap">  
      <div class="prog-lbl">// Status</div>  
      <div class="prog-track"><div class="prog-bar" id="progBar"></div></div>  
      <div class="prog-msg" id="progMsg"></div>  
    </div>  
  </div>  
  
  <button class="btn-convert" id="btnConvert" disabled>CONVERT</button>  
  <a class="btn-dl" id="btnDl">⬇ DOWNLOAD</a>  
  <button class="btn-reset" id="btnReset">↺ Reset</button>  
  <p class="fmt-note" id="fmtNote"></p>  
  
  <!-- Footer -->  
  <div class="footer">  
    <div class="footer-logo">WaveBeat</div>  
    <div class="footer-sub">// Audio Visualizer · Runs 100% in your browser · No uploads · Free</div>  
  </div>  
  
</div>  
  
<script>  
(function(){  
'use strict';  
let mp3File=null,outUrl=null,bgImg=null,logoImg=null;  
let waveStyle='circle',colorTheme='cyan',logoPos='br';  
let gradHue=0;  
  
const THEMES={  
  cyan:  {a:'#00e5ff',b:'#0066ff',glow:'rgba(0,229,255,',  text:'#00e5ff'},  
  gold:  {a:'#ffd700',b:'#ff6600',glow:'rgba(255,215,0,',   text:'#ffd700'},  
  purple:{a:'#bf5fff',b:'#ff3cac',glow:'rgba(191,95,255,',  text:'#cc88ff'},  
  green: {a:'#00ff88',b:'#00ccaa',glow:'rgba(0,255,136,',   text:'#00ff88'},  
  red:   {a:'#ff4444',b:'#ff8800',glow:'rgba(255,68,68,',   text:'#ff6666'},  
  white: {a:'#ffffff',b:'#aaccff',glow:'rgba(255,255,255,',  text:'#ffffff'},  
};  
  
const $=id=>document.getElementById(id);  
const mp3Zone=$('mp3Zone'),mp3Input=$('mp3Input'),mp3NameEl=$('mp3Name');  
const bgImgZone=$('bgImgZone'),bgImgInput=$('bgImgInput'),bgImgName=$('bgImgName');  
const bgThumbWrap=$('bgThumbWrap'),bgThumbImg=$('bgThumbImg');  
const dimSlider=$('dimSlider'),dimVal=$('dimVal'),bgClearBtn=$('bgClearBtn');  
const logoZone=$('logoZone'),logoInput=$('logoInput'),logoName=$('logoName');  
const logoPreview=$('logoPreview'),logoThumb=$('logoThumb'),logoClearBtn=$('logoClearBtn');  
const logoSize=$('logoSize'),logoSizeVal=$('logoSizeVal'),logoPosRow=$('logoPosRow');  
const resSelect=$('resSelect'),brSelect=$('brSelect'),fname=$('fname');  
const songTitle=$('songTitle'),songArtist=$('songArtist');  
const clrPicker=$('clrPicker'),clrText=$('clrText'),clrFill=$('clrFill');  
const lyricsEnabled=$('lyricsEnabled'),lyricBody=$('lyricBody'),lyricsText=$('lyricsText');  
const lyricClrPicker=$('lyricClrPicker'),lyricClrText=$('lyricClrText'),lyricClrFill=$('lyricClrFill');  
const progWrap=$('progWrap'),progBar=$('progBar'),progMsg=$('progMsg');  
const btnConvert=$('btnConvert'),btnDl=$('btnDl'),btnReset=$('btnReset'),fmtNote=$('fmtNote');  
const previewWrap=$('previewWrap'),previewCanvas=$('previewCanvas');  
  
function mkColor(picker,text,fill){  
  function apply(h){picker.value=h;text.value=h;fill.style.background=h;}  
  apply(picker.value);  
  picker.addEventListener('input',()=>apply(picker.value));  
  text.addEventListener('input',()=>{if(/^#[0-9a-fA-F]{6}$/.test(text.value))apply(text.value);});  
  return ()=>text.value;  
}  
const getBg=mkColor(clrPicker,clrText,clrFill);  
const getLyricColor=mkColor(lyricClrPicker,lyricClrText,lyricClrFill);  
  
lyricsEnabled.addEventListener('change',()=>{lyricBody.classList.toggle('show',lyricsEnabled.checked);if(mp3File)drawStaticPreview();});  
document.querySelectorAll('.ws').forEach(btn=>{btn.addEventListener('click',()=>{document.querySelectorAll('.ws').forEach(b=>b.classList.remove('sel'));btn.classList.add('sel');waveStyle=btn.dataset.style;if(mp3File)drawStaticPreview();});});  
document.querySelectorAll('.chip').forEach(chip=>{chip.addEventListener('click',()=>{document.querySelectorAll('.chip').forEach(c=>c.classList.remove('sel'));chip.classList.add('sel');colorTheme=chip.dataset.theme;if(mp3File)drawStaticPreview();});});  
document.querySelectorAll('.lp').forEach(btn=>{btn.addEventListener('click',()=>{document.querySelectorAll('.lp').forEach(b=>b.classList.remove('sel'));btn.classList.add('sel');logoPos=btn.dataset.pos;if(mp3File)drawStaticPreview();});});  
logoSize.addEventListener('input',()=>{logoSizeVal.textContent=logoSize.value+'%';if(mp3File)drawStaticPreview();});  
  
function resizeImg(img,maxW,maxH){  
  const ow=img.naturalWidth||img.width||800,oh=img.naturalHeight||img.height||600;  
  const scale=Math.min(1,maxW/ow,maxH/oh);  
  const w=Math.round(ow*scale),h=Math.round(oh*scale);  
  const c=document.createElement('canvas');c.width=w;c.height=h;  
  c.getContext('2d').drawImage(img,0,0,w,h);return c;  
}  
  
function loadBgImg(f){  
  if(!f)return;  
  const ok=f.type.startsWith('image')||/\.(jpe?g|png|webp|gif|heic)$/i.test(f.name)||f.type==='';  
  if(!ok){alert('Please select an image file');return;}  
  const url=URL.createObjectURL(f);const img=new Image();  
  img.onload=()=>{bgImg=resizeImg(img,1920,1080);bgImgName.textContent=f.name;bgImgZone.classList.add('active');bgThumbImg.src=url;bgThumbWrap.style.display='block';if(mp3File)drawStaticPreview();};  
  img.onerror=()=>alert('Image load failed. Please try another file.');img.src=url;  
}  
bgImgZone.addEventListener('click',()=>bgImgInput.click());  
bgImgInput.addEventListener('change',e=>loadBgImg(e.target.files[0]));  
bgImgZone.addEventListener('dragover',e=>{e.preventDefault();bgImgZone.classList.add('over');});  
bgImgZone.addEventListener('dragleave',()=>bgImgZone.classList.remove('over'));  
bgImgZone.addEventListener('drop',e=>{e.preventDefault();bgImgZone.classList.remove('over');loadBgImg(e.dataTransfer.files[0]);});  
dimSlider.addEventListener('input',()=>{dimVal.textContent=dimSlider.value+'%';if(mp3File)drawStaticPreview();});  
bgClearBtn.addEventListener('click',()=>{bgImg=null;bgImgInput.value='';bgImgName.textContent='';bgImgZone.classList.remove('active');bgThumbWrap.style.display='none';bgThumbImg.src='';if(mp3File)drawStaticPreview();});  
  
function loadLogo(f){  
  if(!f)return;  
  const ok=f.type.startsWith('image')||/\.(jpe?g|png|webp|gif|heic)$/i.test(f.name)||f.type==='';  
  if(!ok){alert('Please select an image file');return;}  
  const url=URL.createObjectURL(f);const img=new Image();  
  img.onload=()=>{logoImg=resizeImg(img,600,600);logoName.textContent=f.name;logoZone.classList.add('active');logoThumb.src=url;logoPreview.classList.add('show');logoPosRow.style.display='flex';logoClearBtn.style.display='block';if(mp3File)drawStaticPreview();};  
  img.onerror=()=>alert('Image load failed.');img.src=url;  
}  
logoZone.addEventListener('click',()=>logoInput.click());  
logoInput.addEventListener('change',e=>loadLogo(e.target.files[0]));  
logoZone.addEventListener('dragover',e=>{e.preventDefault();logoZone.classList.add('over');});  
logoZone.addEventListener('dragleave',()=>logoZone.classList.remove('over'));  
logoZone.addEventListener('drop',e=>{e.preventDefault();logoZone.classList.remove('over');loadLogo(e.dataTransfer.files[0]);});  
logoClearBtn.addEventListener('click',()=>{logoImg=null;logoInput.value='';logoName.textContent='';logoZone.classList.remove('active');logoPreview.classList.remove('show');logoPosRow.style.display='none';logoClearBtn.style.display='none';logoThumb.src='';if(mp3File)drawStaticPreview();});  
  
function loadAudio(f){  
  if(!f)return;  
  const ok=f.type.startsWith('audio')||/\.(mp3|m4a|wav|aac|ogg|flac|aiff?)$/i.test(f.name)||f.type==='';  
  if(!ok){alert('Please select an audio file');return;}  
  mp3File=f;mp3NameEl.textContent=f.name;mp3Zone.classList.add('active');  
  if(!songTitle.value)songTitle.value=f.name.replace(/\.[^.]+$/,'').replace(/[-_]/g,' ');  
  btnConvert.disabled=false;drawStaticPreview();  
}  
mp3Zone.addEventListener('click',()=>mp3Input.click());  
mp3Input.addEventListener('change',e=>loadAudio(e.target.files[0]));  
mp3Zone.addEventListener('dragover',e=>{e.preventDefault();mp3Zone.classList.add('over');});  
mp3Zone.addEventListener('dragleave',()=>mp3Zone.classList.remove('over'));  
mp3Zone.addEventListener('drop',e=>{e.preventDefault();mp3Zone.classList.remove('over');loadAudio(e.dataTransfer.files[0]);});  
[clrPicker,clrText,songTitle,songArtist,resSelect,dimSlider,lyricClrPicker,lyricClrText].forEach(el=>{el.addEventListener('input',()=>{if(mp3File)drawStaticPreview();});el.addEventListener('change',()=>{if(mp3File)drawStaticPreview();});});  
lyricsText.addEventListener('input',()=>{if(mp3File)drawStaticPreview();});  
  
function drawStaticPreview(){  
  const[W,H]=resSelect.value.split(',').map(Number);  
  previewCanvas.width=W;previewCanvas.height=H;previewWrap.classList.add('show');  
  const ctx=previewCanvas.getContext('2d');  
  const fake=new Uint8Array(256);for(let i=0;i<256;i++)fake[i]=80+Math.sin(i*.3)*60+Math.random()*40;  
  const lyrics=lyricsEnabled.checked?lyricsText.value.split('\n').filter(l=>l.trim()):[];  
  drawFrame(ctx,W,H,fake,songTitle.value,songArtist.value,getBg(),colorTheme,waveStyle,0,bgImg,parseInt(dimSlider.value),logoImg,+logoSize.value,logoPos,lyrics,0,getLyricColor(),gradHue);  
}  
  
// **══════════════════════════════════════════**  
// FRAME RENDERER  
// **══════════════════════════════════════════**  
function drawFrame(ctx,W,H,data,title,artist,bg,theme,style,t,bgImage,dimPct,logo,logoSizePct,lpos,lyrics,elapsed,lyricColor,ghue){  
  const T=THEMES[theme]||THEMES.cyan;  
  if(bgImage){  
    const iw=bgImage.width||800,ih=bgImage.height||600;  
    const scale=Math.max(W/iw,H/ih);const sw=iw*scale,sh=ih*scale;  
    ctx.drawImage(bgImage,(W-sw)/2,(H-sh)/2,sw,sh);  
    ctx.fillStyle=`rgba(0,0,0,${(dimPct||65)/100})`;ctx.fillRect(0,0,W,H);  
  }else{  
    const g1=ctx.createLinearGradient(0,0,W,H);  
    const h1=ghue%360,h2=(ghue+120)%360,h3=(ghue+240)%360;  
    g1.addColorStop(0,hsl(h1,70,6));g1.addColorStop(.5,hsl(h2,80,4));g1.addColorStop(1,hsl(h3,70,8));  
    ctx.fillStyle=g1;ctx.fillRect(0,0,W,H);  
    const gr=ctx.createRadialGradient(W*.3,H*.3,0,W*.5,H*.5,H*.8);  
    gr.addColorStop(0,hsl(h1,80,12)+'55');gr.addColorStop(1,'transparent');  
    ctx.fillStyle=gr;ctx.fillRect(0,0,W,H);  
  }  
  const vig=ctx.createRadialGradient(W/2,H/2,H*.12,W/2,H/2,H*.78);  
  vig.addColorStop(0,'rgba(0,0,0,0)');vig.addColorStop(1,'rgba(0,0,0,0.68)');  
  ctx.fillStyle=vig;ctx.fillRect(0,0,W,H);  
  if(style==='circle')drawCircleViz(ctx,W,H,data,T,t);  
  else if(style==='bars')drawBars(ctx,W,H,data,T,t);  
  else if(style==='mirror')drawMirror(ctx,W,H,data,T,t);  
  else if(style==='line')drawLine(ctx,W,H,data,T,t);  
  else if(style==='heart')drawHeart(ctx,W,H,data,T,t);  
  drawText(ctx,W,H,title,artist,T,style);  
  drawTimer(ctx,W,H,elapsed,T);  
  if(lyrics&&lyrics.length>0)drawLyrics(ctx,W,H,lyrics,elapsed,lyricColor);  
  if(logo)drawLogo(ctx,W,H,logo,logoSizePct,lpos);  
}  
  
function drawCircleViz(ctx,W,H,data,T,t){  
  const cx=W/2,cy=H/2,baseR=Math.min(W,H)*.21,n=data.length;  
  ctx.save();  
  // 3 outer rings — bright and clear  
  for(let r=0;r<3;r++){  
    const ringR=baseR*(1.52+r*.22);  
    const hue=(t*60+r*120)%360;  
    const lw=Math.max(1.5,(3.5-r)*2.2*(W/1280));  
    ctx.beginPath();ctx.arc(cx,cy,ringR,0,Math.PI*2);  
    ctx.strokeStyle=hsl(hue,100,75);ctx.lineWidth=lw;  
    ctx.shadowColor=hsl(hue,100,80);ctx.shadowBlur=12*(W/1280);  
    ctx.globalAlpha=.72-r*.12;ctx.stroke();ctx.shadowBlur=0;  
  }  
  ctx.globalAlpha=1;  
  const bass=avg(data,0,8)/255,mid=avg(data,8,64)/255,energy=bass*.6+mid*.3;  
  const hMain=(t*45)%360,ringColor=hsl(hMain,100,62);  
  const pd=ctx.createRadialGradient(cx,cy,0,cx,cy,baseR*(1+energy*.35)*1.2);  
  pd.addColorStop(0,T.glow+'0.18)');pd.addColorStop(1,T.glow+'0)');  
  ctx.fillStyle=pd;ctx.beginPath();ctx.arc(cx,cy,baseR*(1+energy*.35)*1.2,0,Math.PI*2);ctx.fill();  
  ctx.beginPath();ctx.arc(cx,cy,baseR*1.12,0,Math.PI*2);  
  ctx.strokeStyle=ringColor;ctx.lineWidth=2*(W/1280);  
  ctx.shadowColor=hsl(hMain,100,75);ctx.shadowBlur=18*(W/1280);  
  ctx.globalAlpha=.7;ctx.stroke();ctx.shadowBlur=0;ctx.globalAlpha=1;  
  ctx.beginPath();ctx.arc(cx,cy,baseR*.88,0,Math.PI*2);  
  ctx.strokeStyle=hsl((hMain+180)%360,100,65);ctx.lineWidth=1.2*(W/1280);ctx.globalAlpha=.5;ctx.stroke();ctx.globalAlpha=1;  
  for(let i=0;i<64;i++){  
    const ang=(i/64)*Math.PI*2+t*.4;  
    ctx.beginPath();ctx.arc(cx+Math.cos(ang)*baseR*1.32,cy+Math.sin(ang)*baseR*1.32,1.8*(W/1280),0,Math.PI*2);  
    ctx.fillStyle=hsl((hMain+i*(360/64))%360,100,70);ctx.globalAlpha=.55;ctx.fill();  
  }  
  ctx.globalAlpha=1;  
  for(let i=0;i<n;i++){  
    const ang=(i/n)*Math.PI*2-Math.PI/2,v=data[i]/255;  
    const col=hsl((hMain+(i/n)*160)%360,100,60+v*30);  
    const x1=cx+Math.cos(ang)*baseR*.85,y1=cy+Math.sin(ang)*baseR*.85;  
    ctx.beginPath();ctx.moveTo(x1,y1);  
    ctx.lineTo(cx+Math.cos(ang)*(baseR*.85-v*baseR*.78),cy+Math.sin(ang)*(baseR*.85-v*baseR*.78));  
    ctx.strokeStyle=col;ctx.lineWidth=Math.max(1,2*(W/1280));  
    ctx.shadowColor=col;ctx.shadowBlur=v*12*(W/1280);ctx.globalAlpha=.55+v*.4;ctx.stroke();  
  }  
  ctx.shadowBlur=0;ctx.globalAlpha=1;  
  for(let i=0;i<n;i++){  
    const ang=(i/n)*Math.PI*2-Math.PI/2,v=data[i]/255;  
    const col=hsl((hMain+30+(i/n)*200)%360,100,55+v*35);  
    const x1=cx+Math.cos(ang)*baseR*1.12,y1=cy+Math.sin(ang)*baseR*1.12;  
    ctx.beginPath();ctx.moveTo(x1,y1);  
    ctx.lineTo(cx+Math.cos(ang)*(baseR*1.12+v*baseR*.55),cy+Math.sin(ang)*(baseR*1.12+v*baseR*.55));  
    ctx.strokeStyle=col;ctx.lineWidth=Math.max(1,1.8*(W/1280));  
    ctx.shadowColor=col;ctx.shadowBlur=v*14*(W/1280);ctx.globalAlpha=.6+v*.35;ctx.stroke();  
  }  
  ctx.shadowBlur=0;ctx.globalAlpha=1;  
  const cg=ctx.createRadialGradient(cx,cy,0,cx,cy,baseR*.28*(0.9+energy*.25));  
  cg.addColorStop(0,T.glow+'0.55)');cg.addColorStop(1,T.glow+'0)');  
  ctx.fillStyle=cg;ctx.beginPath();ctx.arc(cx,cy,baseR*.28*(0.9+energy*.25),0,Math.PI*2);ctx.fill();  
  for(let c=0;c<4;c++){  
    const ang=t*.8+c*Math.PI/2;  
    ctx.beginPath();ctx.moveTo(cx+Math.cos(ang)*baseR*.25,cy+Math.sin(ang)*baseR*.25);  
    ctx.lineTo(cx+Math.cos(ang)*baseR*.6,cy+Math.sin(ang)*baseR*.6);  
    ctx.strokeStyle=ringColor;ctx.lineWidth=1*(W/1280);ctx.globalAlpha=.25;ctx.stroke();  
  }  
  ctx.globalAlpha=1;ctx.restore();  
}  
  
function drawBars(ctx,W,H,data,T,t){  
  const n=Math.min(data.length,100),gap=W/n,barW=gap*.65,zoneH=H*.4,hBase=(t*50)%360;  
  ctx.save();  
  for(let i=0;i<n;i++){  
    const v=data[i]/255,bh=Math.max(3,v*zoneH),x=i*gap+(gap-barW)/2;  
    const col=hsl((hBase+i*(180/n))%360,100,55+v*30);  
    const gr=ctx.createLinearGradient(0,H/2-bh/2,0,H/2+bh/2);  
    gr.addColorStop(0,ca(col,.2));gr.addColorStop(.5,col);gr.addColorStop(1,ca(col,.2));  
    ctx.fillStyle=gr;ctx.shadowColor=col;ctx.shadowBlur=v*12*(W/1280);  
    rr(ctx,x,H/2-bh/2,barW,bh,2);ctx.fill();  
  }  
  ctx.shadowBlur=0;ctx.restore();  
}  
  
function drawMirror(ctx,W,H,data,T,t){  
  const n=Math.min(data.length,100),gap=W/n,barW=gap*.6,zoneH=H*.2,hBase=(t*50)%360;  
  ctx.save();  
  for(let i=0;i<n;i++){  
    const v=data[i]/255,bh=Math.max(2,v*zoneH),x=i*gap+(gap-barW)/2;  
    const col=hsl((hBase+i*(200/n))%360,100,55+v*30);  
    const gr=ctx.createLinearGradient(0,H/2-bh,0,H/2+bh);  
    gr.addColorStop(0,ca(col,.15));gr.addColorStop(.5,col);gr.addColorStop(1,ca(col,.15));  
    ctx.fillStyle=gr;ctx.shadowColor=col;ctx.shadowBlur=v*10*(W/1280);  
    rr(ctx,x,H/2-bh,barW,bh,2);ctx.fill();rr(ctx,x,H/2,barW,bh,2);ctx.fill();  
  }  
  ctx.shadowBlur=0;ctx.restore();  
}  
  
function drawLine(ctx,W,H,data,T,t){  
  const n=data.length,lineH=(t*40)%360;  
  ctx.save();ctx.beginPath();  
  for(let i=0;i<n;i++){const x=(i/n)*W,y=H/2+(data[i]/255-.5)*H*.35;i===0?ctx.moveTo(x,y):ctx.lineTo(x,y);}  
  ctx.strokeStyle=hsl(lineH,100,65);ctx.lineWidth=Math.max(2,3*(W/1280));  
  ctx.shadowColor=hsl(lineH,100,75);ctx.shadowBlur=16*(W/1280);ctx.lineJoin='round';ctx.stroke();  
  ctx.lineTo(W,H/2);ctx.lineTo(0,H/2);ctx.closePath();  
  ctx.fillStyle=ca(hsl(lineH,100,65),.08);ctx.shadowBlur=0;ctx.fill();ctx.restore();  
}  
  
// **──** Heart Visualizer **─────────────────────────────────**  
function drawHeart(ctx,W,H,data,T,t){  
  ctx.save();  
  const cx=W/2, cy=H*0.42;  
  const bass=avg(data,0,8)/255, mid=avg(data,8,64)/255;  
  const energy=bass*.7+mid*.3;  
  const hMain=(t*40)%360;  
  
  // **──** Side waveforms (left & right) **──────────────────**  
  const waveN=Math.min(data.length,128);  
  const waveW=W*0.38, waveH=H*0.18, waveY=cy+H*0.02;  
  
  // Left waveform (mirrored)  
  for(let i=0;i<waveN;i++){  
    const v=data[i]/255;  
    const barH=Math.max(2,v*waveH);  
    const x=cx - (i/waveN)*waveW - W*0.04;  
    const hue=(hMain+i*(180/waveN))%360;  
    const col=hsl(hue,100,60+v*30);  
    const gr=ctx.createLinearGradient(0,waveY-barH,0,waveY+barH);  
    gr.addColorStop(0,ca(col,0.1)); gr.addColorStop(0.5,col); gr.addColorStop(1,ca(col,0.1));  
    ctx.fillStyle=gr;  
    ctx.shadowColor=col; ctx.shadowBlur=v*10*(W/1280);  
    const bw=Math.max(2,(waveW/waveN)*0.7);  
    rr(ctx,x-bw/2,waveY-barH,bw,barH*2,1); ctx.fill();  
  }  
  
  // Right waveform  
  for(let i=0;i<waveN;i++){  
    const v=data[i]/255;  
    const barH=Math.max(2,v*waveH);  
    const x=cx + (i/waveN)*waveW + W*0.04;  
    const hue=(hMain+i*(180/waveN))%360;  
    const col=hsl(hue,100,60+v*30);  
    const gr=ctx.createLinearGradient(0,waveY-barH,0,waveY+barH);  
    gr.addColorStop(0,ca(col,0.1)); gr.addColorStop(0.5,col); gr.addColorStop(1,ca(col,0.1));  
    ctx.fillStyle=gr;  
    ctx.shadowColor=col; ctx.shadowBlur=v*10*(W/1280);  
    const bw=Math.max(2,(waveW/waveN)*0.7);  
    rr(ctx,x-bw/2,waveY-barH,bw,barH*2,1); ctx.fill();  
  }  
  ctx.shadowBlur=0;  
  
  // **──** Neon Heart path **─────────────────────────────────**  
  const heartSize=Math.min(W,H)*0.22*(1+energy*0.08);  
  function heartPoint(angle){  
    // Parametric heart: x=16sin³t, y=13cost-5cos2t-2cos3t-cos4t  
    const s=Math.sin(angle), s3=s*s*s;  
    const c=Math.cos(angle);  
    const hx=16*s3;  
    const hy=-(13*c - 5*Math.cos(2*angle) - 2*Math.cos(3*angle) - Math.cos(4*angle));  
    return [cx + hx*(heartSize/18), cy + hy*(heartSize/18)];  
  }  
  
  // Draw 3 layered heart outlines (outer → inner, each different color)  
  const heartLayers=[  
    {scale:1.0, hueOff:0,   alpha:0.85, lw:3.5},  
    {scale:0.82,hueOff:30,  alpha:0.6,  lw:2.5},  
    {scale:0.62,hueOff:60,  alpha:0.4,  lw:1.5},  
  ];  
  
  heartLayers.forEach(({scale,hueOff,alpha,lw})=>{  
    const hue=(hMain+hueOff)%360;  
    const col=hsl(hue,100,70);  
    ctx.beginPath();  
    for(let i=0;i<=360;i++){  
      const ang=(i/360)*Math.PI*2;  
      const s=Math.sin(ang),s3=s*s*s;  
      const c=Math.cos(ang);  
      const sz=heartSize*scale;  
      const hx=16*s3;  
      const hy=-(13*c-5*Math.cos(2*ang)-2*Math.cos(3*ang)-Math.cos(4*ang));  
      const px=cx+hx*(sz/18), py=cy+hy*(sz/18);  
      i===0?ctx.moveTo(px,py):ctx.lineTo(px,py);  
    }  
    ctx.closePath();  
    ctx.strokeStyle=col;  
    ctx.lineWidth=lw*(W/1280);  
    ctx.shadowColor=col;  
    ctx.shadowBlur=20*(W/1280);  
    ctx.globalAlpha=alpha;  
    ctx.stroke();  
    ctx.shadowBlur=0;  
  });  
  ctx.globalAlpha=1;  
  
  // **──** Glowing fill inside heart **───────────────────────**  
  ctx.beginPath();  
  for(let i=0;i<=360;i++){  
    const ang=(i/360)*Math.PI*2;  
    const s=Math.sin(ang),s3=s*s*s;  
    const c=Math.cos(ang);  
    const hx=16*s3;  
    const hy=-(13*c-5*Math.cos(2*ang)-2*Math.cos(3*ang)-Math.cos(4*ang));  
    const px=cx+hx*(heartSize*0.6/18), py=cy+hy*(heartSize*0.6/18);  
    i===0?ctx.moveTo(px,py):ctx.lineTo(px,py);  
  }  
  ctx.closePath();  
  const hfill=ctx.createRadialGradient(cx,cy-heartSize*0.05,0,cx,cy,heartSize*0.55);  
  const hue0=hMain%360;  
  hfill.addColorStop(0, hsl(hue0,80,80)+'cc');  
  hfill.addColorStop(0.5,hsl((hue0+30)%360,100,60)+'66');  
  hfill.addColorStop(1,   hsl((hue0+60)%360,100,50)+'11');  
  ctx.fillStyle=hfill;  
  ctx.globalAlpha=0.45+energy*0.2;  
  ctx.fill();  
  ctx.globalAlpha=1;  
  
  // **──** Pulsing glow halo around heart **─────────────────**  
  const halo=ctx.createRadialGradient(cx,cy,heartSize*0.3,cx,cy,heartSize*1.1);  
  halo.addColorStop(0, T.glow+(0.15+energy*0.15)+')');  
  halo.addColorStop(1, T.glow+'0)');  
  ctx.fillStyle=halo;  
  ctx.beginPath(); ctx.arc(cx,cy,heartSize*1.1,0,Math.PI*2); ctx.fill();  
  
  // **──** Water reflection below **─────────────────────────**  
  ctx.save();  
  ctx.translate(0, H);  
  ctx.scale(1,-1);  
  const refY=H-cy-heartSize*0.4;  
  const refGrad=ctx.createLinearGradient(0,refY,0,refY+heartSize*0.6);  
  refGrad.addColorStop(0, T.glow+'0.18)');  
  refGrad.addColorStop(1, T.glow+'0)');  
  // simplified reflection ripple lines  
  for(let r=0;r<6;r++){  
    const ry=refY+r*(heartSize*0.08);  
    const rw=(1-r/6)*W*0.25;  
    ctx.beginPath();  
    ctx.moveTo(cx-rw,ry); ctx.lineTo(cx+rw,ry);  
    ctx.strokeStyle=hsl((hMain+r*20)%360,100,65);  
    ctx.lineWidth=Math.max(0.5,(2-r*0.3)*(W/1280));  
    ctx.globalAlpha=0.25-r*0.03;  
    ctx.stroke();  
  }  
  ctx.globalAlpha=1;  
  ctx.restore();  
  
  ctx.restore();  
}  
  
function drawText(ctx,W,H,title,artist,T,style){  
  if(!title&&!artist)return;  
  const isCircle=(style==='circle');  
  const titleY=isCircle?H*.82:H*.18,artistY=isCircle?H*.89:H*.26;  
  ctx.save();ctx.textAlign='center';ctx.textBaseline='middle';  
  if(title){  
    const fs=Math.round(H*.052);  
    ctx.font=`700 ${fs}px 'Courier New',monospace`;  
    ctx.shadowColor=T.glow+'0.9)';ctx.shadowBlur=H*.02;ctx.fillStyle='#ffffff';  
    ctx.fillText(title,W/2,titleY,W*.82);  
  }  
  if(artist){  
    const fs2=Math.round(H*.032);  
    ctx.font=`400 ${fs2}px 'Courier New',monospace`;  
    ctx.shadowColor=T.glow+'0.6)';ctx.shadowBlur=H*.015;  
    ctx.fillStyle=T.text;ctx.globalAlpha=.9;ctx.fillText(artist,W/2,artistY,W*.75);ctx.globalAlpha=1;  
  }  
  if(title){  
    const lineY=isCircle?H*.857:H*.235;  
    ctx.shadowBlur=0;ctx.strokeStyle=T.a;ctx.lineWidth=1.5;ctx.globalAlpha=.5;  
    ctx.beginPath();ctx.moveTo(W/2-W*.07,lineY);ctx.lineTo(W/2+W*.07,lineY);ctx.stroke();ctx.globalAlpha=1;  
  }  
  ctx.restore();  
}  
  
function drawTimer(ctx,W,H,elapsed,T){  
  const mins=Math.floor(elapsed/60),secs=Math.floor(elapsed%60);  
  const str=`${String(mins).padStart(2,'0')}:${String(secs).padStart(2,'0')}`;  
  ctx.save();ctx.textAlign='center';ctx.textBaseline='middle';  
  ctx.font=`800 ${Math.round(H*.028)}px 'Courier New',monospace`;  
  ctx.shadowColor=T.glow+'0.8)';ctx.shadowBlur=H*.012;  
  ctx.fillStyle=T.text;ctx.globalAlpha=.85;ctx.fillText(str,W/2,H*.62);  
  ctx.globalAlpha=1;ctx.shadowBlur=0;ctx.restore();  
}  
  
function drawLyrics(ctx,W,H,lines,elapsed,color){  
  if(!lines||!lines.length)return;  
  const secPerLine=Math.max(2,elapsed>0?elapsed/lines.length:4);  
  const line=lines[Math.min(Math.floor(elapsed/secPerLine),lines.length-1)]||'';  
  if(!line.trim())return;  
  ctx.save();ctx.textAlign='center';ctx.textBaseline='middle';  
  ctx.font=`700 ${Math.round(H*.038)}px 'Courier New',monospace`;  
  ctx.shadowColor='rgba(0,0,0,0.9)';ctx.shadowBlur=H*.025;  
  ctx.fillStyle=color||'#ffffff';ctx.globalAlpha=.95;  
  ctx.fillText(line,W/2,H*.92,W*.88);ctx.globalAlpha=1;ctx.shadowBlur=0;ctx.restore();  
}  
  
function drawLogo(ctx,W,H,logo,sizePct,pos){  
  const maxW=W*(sizePct/100);  
  const lw=logo.width||logo.naturalWidth||100;  
  const lh=logo.height||logo.naturalHeight||100;  
  const scale=maxW/lw;  
  const dw=Math.round(lw*scale),dh=Math.round(lh*scale),pad=W*.022;  
  let x,y;  
  if(pos==='tl'){x=pad;y=pad;}else if(pos==='tr'){x=W-dw-pad;y=pad;}  
  else if(pos==='bl'){x=pad;y=H-dh-pad;}else if(pos==='bc'){x=(W-dw)/2;y=H-dh-pad;}  
  else{x=W-dw-pad;y=H-dh-pad;}  
  ctx.save();ctx.globalAlpha=.82;ctx.drawImage(logo,x,y,dw,dh);ctx.globalAlpha=1;ctx.restore();  
}  
  
function hsl(h,s,l){s/=100;l/=100;const a=s*Math.min(l,1-l);const f=n=>{const k=(n+h/30)%12;const c=l-a*Math.max(Math.min(k-3,9-k,1),-1);return Math.round(255*c).toString(16).padStart(2,'0');};return `#${f(0)}${f(8)}${f(4)}`;}  
function ca(hex,a){const r=parseInt(hex.slice(1,3),16),g=parseInt(hex.slice(3,5),16),b=parseInt(hex.slice(5,7),16);return `rgba(${r},${g},${b},${a})`;}  
function avg(arr,s,e){let sum=0;for(let i=s;i<e;i++)sum+=arr[i];return sum/(e-s);}  
function rr(ctx,x,y,w,h,r){ctx.beginPath();ctx.moveTo(x+r,y);ctx.lineTo(x+w-r,y);ctx.quadraticCurveTo(x+w,y,x+w,y+r);ctx.lineTo(x+w,y+h-r);ctx.quadraticCurveTo(x+w,y+h,x+w-r,y+h);ctx.lineTo(x+r,y+h);ctx.quadraticCurveTo(x,y+h,x,y+h-r);ctx.lineTo(x,y+r);ctx.quadraticCurveTo(x,y,x+r,y);ctx.closePath();}  
function bestMime(){const l=['video/mp4;codecs=avc1.42E01E,mp4a.40.2','video/mp4','video/webm;codecs=vp9,opus','video/webm;codecs=vp8,opus','video/webm'];for(const m of l)if(MediaRecorder.isTypeSupported(m))return m;return '';}  
function setStatus(msg,cls=''){progWrap.classList.add('show');progMsg.className='prog-msg'+(cls?' '+cls:'');progMsg.textContent=msg;}  
function setProgress(pct){progBar.className='prog-bar';progBar.style.width=pct+'%';}  
function setSpinner(){progBar.className='prog-bar anim';}  
  
let previewRaf=null;  
(function previewLoop(){gradHue=(gradHue+.25)%360;if(mp3File)drawStaticPreview();previewRaf=requestAnimationFrame(previewLoop);})();  
  
btnConvert.addEventListener('click',async()=>{  
  if(!mp3File)return;  
  btnConvert.disabled=true;btnDl.classList.remove('show');fmtNote.textContent='';  
  setSpinner();setStatus('Decoding audio...');  
  try{  
    const AC=window.AudioContext||window.webkitAudioContext;const ac=new AC();  
    const buf=await mp3File.arrayBuffer();const audioBuf=await ac.decodeAudioData(buf);  
    const[W,H]=resSelect.value.split(',').map(Number);  
    const cv=document.createElement('canvas');cv.width=W;cv.height=H;const ctx=cv.getContext('2d');  
    const analyser=ac.createAnalyser();analyser.fftSize=256;analyser.smoothingTimeConstant=.82;  
    const dataArr=new Uint8Array(analyser.frequencyBinCount);  
    const dest=ac.createMediaStreamDestination();const src=ac.createBufferSource();  
    src.buffer=audioBuf;src.connect(analyser);analyser.connect(dest);  
    const vs=cv.captureStream(30);  
    const stream=new MediaStream([...vs.getVideoTracks(),...dest.stream.getAudioTracks()]);  
    const mime=bestMime();const isMP4=mime.toLowerCase().includes('mp4');const ext=isMP4?'mp4':'webm';  
    fmtNote.textContent=isMP4?'Output: MP4 (H.264 + AAC)':'Output: WebM (playable in VLC / Chrome)';  
    const opts=mime?{mimeType:mime,videoBitsPerSecond:+brSelect.value}:{};  
    const rec=new MediaRecorder(stream,opts);const chunks=[];  
    rec.ondataavailable=e=>{if(e.data.size>0)chunks.push(e.data);};  
    const dur=audioBuf.duration;setProgress(0);setStatus('Converting... 0%');  
    let elapsed=0;const tick=setInterval(()=>{elapsed+=.5;const p=Math.min(97,Math.round(elapsed/dur*100));setProgress(p);setStatus(`Converting... ${p}%`);},500);  
    const title=songTitle.value.trim(),artist=songArtist.value.trim(),bg=clrText.value;  
    const theme=colorTheme,style=waveStyle,snapBg=bgImg,snapDim=parseInt(dimSlider.value);  
    const snapLogo=logoImg,snapLogoSize=+logoSize.value,snapLogoPos=logoPos;  
    const lyrics=lyricsEnabled.checked?lyricsText.value.split('\n').filter(l=>l.trim()):[];  
    const lyricColor=getLyricColor();  
    const startTime=ac.currentTime;let rafRunning=true,localGradHue=gradHue;  
    previewCanvas.width=W;previewCanvas.height=H;previewWrap.classList.add('show');  
    const preCtx=previewCanvas.getContext('2d');  
    function rafLoop(){  
      if(!rafRunning)return;  
      analyser.getByteFrequencyData(dataArr);  
      const t=ac.currentTime-startTime;localGradHue=(localGradHue+.5)%360;  
      drawFrame(ctx,W,H,dataArr,title,artist,bg,theme,style,t,snapBg,snapDim,snapLogo,snapLogoSize,snapLogoPos,lyrics,t,lyricColor,localGradHue);  
      preCtx.drawImage(cv,0,0);requestAnimationFrame(rafLoop);  
    }  
    rafLoop();src.start();rec.start(100);  
    await new Promise((res,rej)=>{  
      src.onended=()=>{rafRunning=false;rec.stop();vs.getTracks().forEach(t=>t.stop());};  
      rec.onstop=res;rec.onerror=e=>rej(e.error||new Error('MediaRecorder error'));  
    });  
    clearInterval(tick);setProgress(100);setStatus('✓ Done!','ok');  
    const blob=new Blob(chunks,{type:mime||'video/webm'});  
    if(outUrl)URL.revokeObjectURL(outUrl);outUrl=URL.createObjectURL(blob);  
    const n=(fname.value.trim()||'output').replace(/\.(mp4|webm)$/i,'')+'.'+ext;  
    btnDl.href=outUrl;btnDl.download=n;btnDl.textContent='⬇  DOWNLOAD  '+n.toUpperCase();  
    btnDl.classList.add('show');ac.close();  
  }catch(err){console.error(err);setProgress(0);setStatus('✕ Error: '+(err.message||String(err)),'err');}  
  finally{btnConvert.disabled=!mp3File;}  
});  
  
btnReset.addEventListener('click',()=>{  
  mp3File=null;mp3Input.value='';mp3NameEl.textContent='';mp3Zone.classList.remove('active','over');  
  bgImg=null;bgImgInput.value='';bgImgName.textContent='';bgImgZone.classList.remove('active');bgThumbWrap.style.display='none';bgThumbImg.src='';  
  logoImg=null;logoInput.value='';logoName.textContent='';logoZone.classList.remove('active');logoPreview.classList.remove('show');logoPosRow.style.display='none';logoClearBtn.style.display='none';logoThumb.src='';  
  progWrap.classList.remove('show');progBar.style.width='0%';progBar.className='prog-bar';  
  btnDl.classList.remove('show');previewWrap.classList.remove('show');  
  fname.value='output';fmtNote.textContent='';songTitle.value='';songArtist.value='';  
  lyricsEnabled.checked=false;lyricBody.classList.remove('show');lyricsText.value='';  
  if(outUrl){URL.revokeObjectURL(outUrl);outUrl=null;}btnConvert.disabled=true;  
});  
})();  
</script>  
</body>  
</html>  
