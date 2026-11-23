```aura width=800 height=330
<div style={{ position: 'relative', display: 'flex', width: '100%', height: '100%', background: '#111111', borderRadius: 24, border: '1px solid rgba(255,255,255,0.1)', overflow: 'hidden', fontFamily: 'Geist' }}>
  <style>{`
    @keyframes drift-a { 0%, 100% { transform: translate(0, 0) scale(1); } 50% { transform: translate(-150px, 70px) scale(1.2); } }
    @keyframes drift-b { 0%, 100% { transform: translate(0, 0) scale(1); } 50% { transform: translate(170px, -60px) scale(1.15); } }
    @keyframes drift-c { 0%, 100% { transform: translate(0, 0) scale(1); } 50% { transform: translate(-110px, -90px) scale(1.25); } }
    #blob-a, #blob-b, #blob-c { transform-box: fill-box; transform-origin: center; }
    #blob-a { animation: drift-a 8s ease-in-out infinite; }
    #blob-b { animation: drift-b 10s ease-in-out infinite; }
    #blob-c { animation: drift-c 7s ease-in-out infinite; }
    @media (prefers-reduced-motion: reduce) { #blob-a, #blob-b, #blob-c { animation: none; } }
  `}</style>

  <svg width="800" height="330" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="gold" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(224,169,137,0.55)" />
        <stop offset="100%" stopColor="rgba(224,169,137,0)" />
      </radialGradient>
      <radialGradient id="rose" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(196,96,118,0.5)" />
        <stop offset="100%" stopColor="rgba(196,96,118,0)" />
      </radialGradient>
      <radialGradient id="amber" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(240,190,120,0.32)" />
        <stop offset="100%" stopColor="rgba(240,190,120,0)" />
      </radialGradient>
    </defs>
    <ellipse id="blob-a" cx="640" cy="60" rx="300" ry="220" fill="url(#gold)" />
    <ellipse id="blob-b" cx="110" cy="300" rx="280" ry="200" fill="url(#rose)" />
    <ellipse id="blob-c" cx="430" cy="320" rx="240" ry="160" fill="url(#amber)" />
  </svg>

  <div style={{ position: 'relative', display: 'flex', width: '100%', height: '100%', padding: '40px 40px 38px 40px', justifyContent: 'center', alignItems: 'center' }}>
    <div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center' }}>
      <span style={{ fontFamily: 'GeistMono', fontSize: 12, letterSpacing: 1.4, color: '#E0A989' }}>HI, I'M</span>
      <span style={{ fontFamily: 'SpaceGrotesk', fontSize: 74, lineHeight: 1, letterSpacing: -1.2, color: '#EDEDED', marginTop: 12 }}>justseiji</span>
      <span style={{ fontFamily: 'GeistMedium', fontSize: 17.5, color: '#E0A989', marginTop: 16 }}>AI-Assisted Developer · Web Apps & Testing Tools</span>
      <span style={{ fontSize: 15, lineHeight: 1.5, color: '#A3A3A3', marginTop: 10 }}>Turning ideas into working apps, with AI helping me move faster.</span>
    </div>
  </div>
</div>
```

```aura width=800 height=130
<div style={{ position: 'relative', display: 'flex', flexDirection: 'column', alignItems: 'center', justifyContent: 'center', width: '100%', height: '100%', background: '#111111', borderRadius: 24, border: '1px solid rgba(255,255,255,0.1)', overflow: 'hidden', fontFamily: 'Geist' }}>
  <style>{`
    @keyframes sweep { 0%, 100% { transform: translate(-220px, 0); } 50% { transform: translate(220px, 0); } }
    @keyframes sweep-back { 0%, 100% { transform: translate(200px, 0); } 50% { transform: translate(-200px, 0); } }
    #glow-a { animation: sweep 7s ease-in-out infinite; }
    #glow-b { animation: sweep-back 9s ease-in-out infinite; }
    @media (prefers-reduced-motion: reduce) { #glow-a, #glow-b { animation: none; } }
  `}</style>
  <svg width="800" height="130" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="gold" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(224,169,137,0.6)" />
        <stop offset="100%" stopColor="rgba(224,169,137,0)" />
      </radialGradient>
      <radialGradient id="rose" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(196,96,118,0.5)" />
        <stop offset="100%" stopColor="rgba(196,96,118,0)" />
      </radialGradient>
    </defs>
    <ellipse id="glow-a" cx="400" cy="140" rx="280" ry="110" fill="url(#gold)" />
    <ellipse id="glow-b" cx="400" cy="-10" rx="260" ry="100" fill="url(#rose)" />
  </svg>
  <div style={{ position: 'relative', display: 'flex', fontFamily: 'SpaceGrotesk', fontSize: 30, letterSpacing: -0.6 }}>
    <span style={{ color: '#EDEDED' }}>Have an idea? Let's build something</span>
    <span style={{ color: '#E0A989', marginLeft: 8 }}>useful.</span>
  </div>
  <span style={{ position: 'relative', fontSize: 14, color: '#A3A3A3', marginTop: 8 }}>See my work, or reach me on LinkedIn or by email.</span>
</div>
```

```aura width=166 height=44 link="https://jisei.vercel.app/" inline align=center
<div style={{ display: 'flex', alignItems: 'center', justifyContent: 'center', width: 150, height: 44, marginLeft: 8, background: '#1A1A1A', border: '1px solid rgba(224,169,137,0.35)', borderRadius: 999, fontFamily: 'GeistMedium', fontSize: 14, color: '#EDEDED' }}>
  <img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgc3Ryb2tlPSIjRTBBOTg5IiBzdHJva2Utd2lkdGg9IjIiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI+PGNpcmNsZSBjeD0iMTIiIGN5PSIxMiIgcj0iMTAiLz48cGF0aCBkPSJNMiAxMmgyMCIvPjxwYXRoIGQ9Ik0xMiAyYTE1LjMgMTUuMyAwIDAgMSA0IDEwIDE1LjMgMTUuMyAwIDAgMS00IDEwIDE1LjMgMTUuMyAwIDAgMS00LTEwIDE1LjMgMTUuMyAwIDAgMSA0LTEweiIvPjwvc3ZnPg==" width={16} height={16} />
  <span style={{ marginLeft: 8 }}>Portfolio</span>
</div>
```

```aura width=166 height=44 link="https://www.linkedin.com/in/seijil/" inline align=center
<div style={{ display: 'flex', alignItems: 'center', justifyContent: 'center', width: 150, height: 44, marginLeft: 8, background: '#1A1A1A', border: '1px solid rgba(224,169,137,0.35)', borderRadius: 999, fontFamily: 'GeistMedium', fontSize: 14, color: '#EDEDED' }}>
  <img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0iIzRDOUJFOCIgZD0iTTIwLjQ0NyAyMC40NTJoLTMuNTU0di01LjU2OWMwLTEuMzI4LS4wMjctMy4wMzctMS44NTItMy4wMzctMS44NTMgMC0yLjEzNiAxLjQ0NS0yLjEzNiAyLjkzOXY1LjY2N0g5LjM1MVY5aDMuNDE0djEuNTYxaC4wNDZjLjQ3Ny0uOTQ4IDEuNjM3LTEuOTUgMy4zNy0xLjk1IDMuNjAxIDAgNC4yNjcgMi4zNyA0LjI2NyA1LjQ1NXY2LjI4NnpNNS4zMzcgNy40MzNjLTEuMTQ0IDAtMi4wNjMtLjkyNi0yLjA2My0yLjA2NSAwLTEuMTM4LjkyLTIuMDYzIDIuMDYzLTIuMDYzIDEuMTQgMCAyLjA2NC45MjUgMi4wNjQgMi4wNjMgMCAxLjEzOS0uOTI1IDIuMDY1LTIuMDY0IDIuMDY1em0xLjc4MiAxMy4wMTlIMy41NTVWOWgzLjU2NHYxMS40NTJ6TTIyLjIyNSAwSDEuNzcxQy43OTIgMCAwIC43NzQgMCAxLjcyOXYyMC41NDJDMCAyMy4yMjcuNzkyIDI0IDEuNzcxIDI0aDIwLjQ1MUMyMy4yIDI0IDI0IDIzLjIyNyAyNCAyMi4yNzFWMS43MjlDMjQgLjc3NCAyMy4yIDAgMjIuMjIyIDBoLjAwM3oiLz48L3N2Zz4=" width={16} height={16} />
  <span style={{ marginLeft: 8 }}>LinkedIn</span>
</div>
```

```aura width=166 height=44 link="mailto:seiji.workmail@gmail.com" inline align=center
<div style={{ display: 'flex', alignItems: 'center', justifyContent: 'center', width: 150, height: 44, marginLeft: 8, background: '#1A1A1A', border: '1px solid rgba(224,169,137,0.35)', borderRadius: 999, fontFamily: 'GeistMedium', fontSize: 14, color: '#EDEDED' }}>
  <img src="data:image/svg+xml;base64,PHN2ZyBmaWxsPSIjRUE0MzM1IiByb2xlPSJpbWciIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48dGl0bGU+R21haWw8L3RpdGxlPjxwYXRoIGQ9Ik0yNCA1LjQ1N3YxMy45MDljMCAuOTA0LS43MzIgMS42MzYtMS42MzYgMS42MzZoLTMuODE5VjExLjczTDEyIDE2LjY0bC02LjU0NS00LjkxdjkuMjczSDEuNjM2QTEuNjM2IDEuNjM2IDAgMCAxIDAgMTkuMzY2VjUuNDU3YzAtMi4wMjMgMi4zMDktMy4xNzggMy45MjctMS45NjRMNS40NTUgNC42NCAxMiA5LjU0OGw2LjU0NS00LjkxIDEuNTI4LTEuMTQ1QzIxLjY5IDIuMjggMjQgMy40MzQgMjQgNS40NTd6Ii8+PC9zdmc+" width={16} height={16} />
  <span style={{ marginLeft: 8 }}>Email</span>
</div>
```
