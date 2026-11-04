```aura width=800 height=330
<div style={{ position: 'relative', display: 'flex', width: '100%', height: '100%', background: '#F8F6F2', borderRadius: 24, border: '1px solid rgba(36,35,33,0.12)', overflow: 'hidden', fontFamily: 'Geist' }}>
  <style>{`
    @keyframes drift-a { 0%, 100% { transform: translate(0, 0); } 50% { transform: translate(-46px, 30px); } }
    @keyframes drift-b { 0%, 100% { transform: translate(0, 0); } 50% { transform: translate(40px, -26px); } }
    @keyframes drift-c { 0%, 100% { transform: translate(0, 0); } 50% { transform: translate(-30px, -34px); } }
    @keyframes pulse { 0%, 100% { opacity: 0.25; transform: scale(1); } 50% { opacity: 0; transform: scale(2.2); } }
    #blob-a { animation: drift-a 9s ease-in-out infinite; }
    #blob-b { animation: drift-b 11s ease-in-out infinite; }
    #blob-c { animation: drift-c 13s ease-in-out infinite; }
    #ring { transform-origin: 65px 274px; animation: pulse 2.4s ease-out infinite; }
    @media (prefers-reduced-motion: reduce) { #blob-a, #blob-b, #blob-c, #ring { animation: none; } }
  `}</style>

  <svg width="800" height="330" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="rose" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(214,128,150,0.42)" />
        <stop offset="100%" stopColor="rgba(214,128,150,0)" />
      </radialGradient>
      <radialGradient id="peach" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(236,170,140,0.34)" />
        <stop offset="100%" stopColor="rgba(236,170,140,0)" />
      </radialGradient>
      <radialGradient id="wine" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(150,70,95,0.22)" />
        <stop offset="100%" stopColor="rgba(150,70,95,0)" />
      </radialGradient>
    </defs>
    <ellipse id="blob-a" cx="660" cy="40" rx="280" ry="200" fill="url(#rose)" />
    <ellipse id="blob-b" cx="90" cy="320" rx="260" ry="180" fill="url(#peach)" />
    <ellipse id="blob-c" cx="430" cy="300" rx="220" ry="150" fill="url(#wine)" />
  </svg>

  <div style={{ position: 'relative', display: 'flex', width: '100%', height: '100%', padding: '40px 40px 38px 44px', justifyContent: 'space-between', alignItems: 'flex-end' }}>
    <div style={{ display: 'flex', flexDirection: 'column', width: 470 }}>
      <span style={{ fontFamily: 'GeistMono', fontSize: 12, letterSpacing: 1.4, color: '#632F3B' }}>HI, I'M</span>
      <span style={{ fontFamily: 'Bricolage', fontSize: 74, lineHeight: 1, letterSpacing: -1.2, color: '#242321', marginTop: 12 }}>Seiji Liwag</span>
      <span style={{ fontFamily: 'GeistMedium', fontSize: 17.5, color: '#632F3B', marginTop: 16 }}>AI-Assisted Developer · Web Apps & Testing Tools</span>
      <span style={{ fontSize: 15, lineHeight: 1.5, color: '#4A4743', marginTop: 10 }}>Turning ideas into working apps, with AI helping me move faster.</span>
      <div style={{ display: 'flex', alignSelf: 'flex-start', alignItems: 'center', marginTop: 22, padding: '7px 14px 7px 10px', background: 'rgba(255,255,255,0.75)', border: '1px solid rgba(36,35,33,0.12)', borderRadius: 999 }}>
        <div style={{ display: 'flex', width: 18, height: 18, flexShrink: 0 }} />
        <span style={{ fontFamily: 'GeistMedium', fontSize: 13, color: '#242321', marginLeft: 6 }}>Open to internships, OJT and junior developer roles</span>
      </div>
    </div>

    <div style={{ display: 'flex', flexDirection: 'column', width: 230, padding: '18px 20px', background: '#FFFFFF', border: '1px solid rgba(36,35,33,0.12)', borderRadius: 16, boxShadow: '0 12px 30px -14px rgba(74,35,45,0.25)' }}>
      {[
        ['STUDYING', 'BS Computer Science, Holy Angel University'],
        ['GRADUATING', '2027'],
        ['BASED IN', 'Angeles City, Philippines'],
      ].map(([k, v], i) => (
        <div key={k} style={{ display: 'flex', flexDirection: 'column', marginTop: i === 0 ? 0 : 14 }}>
          <span style={{ fontFamily: 'GeistMono', fontSize: 10, letterSpacing: 1.4, color: '#57524C' }}>{k}</span>
          <span style={{ fontFamily: 'GeistMedium', fontSize: 14, lineHeight: 1.35, color: '#242321', marginTop: 3 }}>{v}</span>
        </div>
      ))}
    </div>
  </div>

  {/* The status dot. Drawn here, over the pill, because Satori clips an SVG nested inside a rounded pill. */}
  <svg width="800" height="330" style={{ position: 'absolute', top: 0, left: 0 }}>
    <circle id="ring" cx="65" cy="274" r="4" fill="#2B6334" />
    <circle cx="65" cy="274" r="4" fill="#2B6334" />
  </svg>
</div>
```

```aura width=800 height=350
<div style={{ display: 'flex', flexDirection: 'column', width: '100%', height: '100%', padding: '32px 40px 34px 44px', background: '#FFFFFF', borderRadius: 24, border: '1px solid rgba(36,35,33,0.12)', fontFamily: 'Geist' }}>
  <span style={{ fontFamily: 'GeistMono', fontSize: 12, letterSpacing: 1.4, color: '#632F3B' }}>ABOUT ME</span>
  <span style={{ display: 'flex', fontSize: 17, lineHeight: 1.55, color: '#242321', marginTop: 12, width: 700 }}>I'm a Computer Science student who builds full-stack web apps and tools for testing software, and I lean on AI heavily throughout the process, from planning and debugging to learning new tools.</span>
  <div style={{ display: 'flex', flexWrap: 'wrap', justifyContent: 'space-between', marginTop: 24 }}>
    {[
      ['BUILDING', 'Full-stack web apps and testing tools, from workout tracking and catalog imports to browser automation'],
      ['USING', 'AI as a daily part of my workflow'],
      ['LEARNING', 'By shipping real projects'],
      ['SKILLS', 'REST APIs, authentication, databases, offline-first data sync and automated browser testing'],
    ].map(([k, v], i) => (
      <div key={k} style={{ display: 'flex', flexDirection: 'column', width: 345, minHeight: 64, marginTop: i > 1 ? 18 : 0, paddingLeft: 14, borderLeft: '2px solid rgba(214,128,150,0.7)' }}>
        <span style={{ fontFamily: 'GeistMono', fontSize: 10, letterSpacing: 1.4, color: '#57524C' }}>{k}</span>
        <span style={{ fontSize: 14, lineHeight: 1.45, color: '#4A4743', marginTop: 4 }}>{v}</span>
      </div>
    ))}
  </div>
</div>
```

```aura width=800 height=756
<div style={{ display: 'flex', flexDirection: 'column', width: '100%', height: '100%', padding: '32px 40px 34px 44px', background: '#FFFFFF', borderRadius: 24, border: '1px solid rgba(36,35,33,0.12)', fontFamily: 'Geist' }}>
  <span style={{ fontFamily: 'GeistMono', fontSize: 12, letterSpacing: 1.4, color: '#632F3B' }}>TOOLS & TECHNOLOGIES</span>
  <span style={{ display: 'flex', fontSize: 15, lineHeight: 1.5, color: '#4A4743', marginTop: 10 }}>Tools I've used in my own projects and learned through my Computer Science coursework.</span>
  {[
    ['Languages', [['TypeScript', 'typescript/3178C6'], ['JavaScript', 'javascript/E5C100'], ['Python', 'python/3776AB'], ['SQL', 'postgresql/4169E1'], ['HTML & CSS', 'html5/E34F26'], ['Dart', 'dart/0175C2'], ['Java', 'openjdk/242321'], ['PHP', 'php/777BB4']]],
    ['Web & apps', [['React', 'react/149ECA'], ['Vite', 'vite/646CFF'], ['Node.js', 'nodedotjs/5FA04E'], ['Express', 'express/242321'], ['Fastify', 'fastify/242321'], ['Tailwind CSS', 'tailwindcss/06B6D4'], ['Flutter', 'flutter/02569B'], ['FastAPI', 'fastapi/009688']]],
    ['Data & testing', [['PostgreSQL', 'postgresql/4169E1'], ['MySQL', 'mysql/4479A1'], ['Supabase', 'supabase/3ECF8E'], ['Prisma', 'prisma/2D3748'], ['Playwright', null], ['Vitest', 'vitest/6E9F18'], ['Zod', 'zod/3E67B1']]],
    ['Machine learning', [['TensorFlow', 'tensorflow/FF6F00'], ['Keras', 'keras/D00000'], ['PyTorch', 'pytorch/EE4C2C'], ['NumPy', 'numpy/013243'], ['scikit-learn', 'scikitlearn/F7931E'], ['Pillow', null]]],
    ['Deployment', [['Docker', 'docker/2496ED'], ['AWS', null], ['Vercel', 'vercel/242321'], ['Render', 'render/242321'], ['Bash', 'gnubash/4EAA25']]],
    ['Design & workflow', [['Figma', 'figma/F24E1E'], ['Git', 'git/F05032'], ['GitHub', 'github/242321'], ['Wireframing', null], ['Interface design', null]]],
    ['AI tools', [['Claude Code', 'claude/D97757'], ['Codex', 'data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0iIzI0MjMyMSIgZD0iTTIyLjI4MTkgOS44MjExYTUuOTg0NyA1Ljk4NDcgMCAwIDAtLjUxNTctNC45MTA4IDYuMDQ2MiA2LjA0NjIgMCAwIDAtNi41MDk4LTIuOUE2LjA2NTEgNi4wNjUxIDAgMCAwIDQuOTgwNyA0LjE4MThhNS45ODQ3IDUuOTg0NyAwIDAgMC0zLjk5NzcgMi45IDYuMDQ2MiA2LjA0NjIgMCAwIDAgLjc0MjcgNy4wOTY2IDUuOTggNS45OCAwIDAgMCAuNTExIDQuOTEwNyA2LjA1MSA2LjA1MSAwIDAgMCA2LjUxNDYgMi45MDAxQTUuOTg0NyA1Ljk4NDcgMCAwIDAgMTMuMjU5OSAyNGE2LjA1NTcgNi4wNTU3IDAgMCAwIDUuNzcxOC00LjIwNTggNS45ODk0IDUuOTg5NCAwIDAgMCAzLjk5NzctMi45MDAxIDYuMDU1NyA2LjA1NTcgMCAwIDAtLjc0NzUtNy4wNzI5em0tOS4wMjIgMTIuNjA4MWE0LjQ3NTUgNC40NzU1IDAgMCAxLTIuODc2NC0xLjA0MDhsLjE0MTktLjA4MDQgNC43NzgzLTIuNzU4MmEuNzk0OC43OTQ4IDAgMCAwIC4zOTI3LS42ODEzdi02LjczNjlsMi4wMiAxLjE2ODZhLjA3MS4wNzEgMCAwIDEgLjAzOC4wNTJ2NS41ODI2YTQuNTA0IDQuNTA0IDAgMCAxLTQuNDk0NSA0LjQ5NDR6bS05LjY2MDctNC4xMjU0YTQuNDcwOCA0LjQ3MDggMCAwIDEtLjUzNDYtMy4wMTM3bC4xNDIuMDg1MiA0Ljc4MyAyLjc1ODJhLjc3MTIuNzcxMiAwIDAgMCAuNzgwNiAwbDUuODQyOC0zLjM2ODV2Mi4zMzI0YS4wODA0LjA4MDQgMCAwIDEtLjAzMzIuMDYxNUw5Ljc0IDE5Ljk1MDJhNC40OTkyIDQuNDk5MiAwIDAgMS02LjE0MDgtMS42NDY0ek0yLjM0MDggNy44OTU2YTQuNDg1IDQuNDg1IDAgMCAxIDIuMzY1NS0xLjk3MjhWMTEuNmEuNzY2NC43NjY0IDAgMCAwIC4zODc5LjY3NjVsNS44MTQ0IDMuMzU0My0yLjAyMDEgMS4xNjg1YS4wNzU3LjA3NTcgMCAwIDEtLjA3MSAwbC00LjgzMDMtMi43ODY1QTQuNTA0IDQuNTA0IDAgMCAxIDIuMzQwOCA3Ljg3MnptMTYuNTk2MyAzLjg1NThMMTMuMTAzOCA4LjM2NCAxNS4xMTkyIDcuMmEuMDc1Ny4wNzU3IDAgMCAxIC4wNzEgMGw0LjgzMDMgMi43OTEzYTQuNDk0NCA0LjQ5NDQgMCAwIDEtLjY3NjUgOC4xMDQydi01LjY3NzJhLjc5Ljc5IDAgMCAwLS40MDctLjY2N3ptMi4wMTA3LTMuMDIzMWwtLjE0Mi0uMDg1Mi00Ljc3MzUtMi43ODE4YS43NzU5Ljc3NTkgMCAwIDAtLjc4NTQgMEw5LjQwOSA5LjIyOTdWNi44OTc0YS4wNjYyLjA2NjIgMCAwIDEgLjAyODQtLjA2MTVsNC44MzAzLTIuNzg2NmE0LjQ5OTIgNC40OTkyIDAgMCAxIDYuNjgwMiA0LjY2ek04LjMwNjUgMTIuODYzbC0yLjAyLTEuMTYzOGEuMDgwNC4wODA0IDAgMCAxLS4wMzgtLjA1NjdWNi4wNzQyYTQuNDk5MiA0LjQ5OTIgMCAwIDEgNy4zNzU3LTMuNDUzN2wtLjE0Mi4wODA1TDguNzA0IDUuNDU5YS43OTQ4Ljc5NDggMCAwIDAtLjM5MjcuNjgxM3ptMS4wOTc2LTIuMzY1NGwyLjYwMi0xLjQ5OTggMi42MDY5IDEuNDk5OHYyLjk5OTRsLTIuNTk3NCAxLjQ5OTctMi42MDY3LTEuNDk5N1oiLz48L3N2Zz4='], ['Gemini', 'googlegemini/8E75B2'], ['GitHub Copilot', 'githubcopilot/242321'], ['ChatGPT', 'data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0iIzI0MjMyMSIgZD0iTTIyLjI4MTkgOS44MjExYTUuOTg0NyA1Ljk4NDcgMCAwIDAtLjUxNTctNC45MTA4IDYuMDQ2MiA2LjA0NjIgMCAwIDAtNi41MDk4LTIuOUE2LjA2NTEgNi4wNjUxIDAgMCAwIDQuOTgwNyA0LjE4MThhNS45ODQ3IDUuOTg0NyAwIDAgMC0zLjk5NzcgMi45IDYuMDQ2MiA2LjA0NjIgMCAwIDAgLjc0MjcgNy4wOTY2IDUuOTggNS45OCAwIDAgMCAuNTExIDQuOTEwNyA2LjA1MSA2LjA1MSAwIDAgMCA2LjUxNDYgMi45MDAxQTUuOTg0NyA1Ljk4NDcgMCAwIDAgMTMuMjU5OSAyNGE2LjA1NTcgNi4wNTU3IDAgMCAwIDUuNzcxOC00LjIwNTggNS45ODk0IDUuOTg5NCAwIDAgMCAzLjk5NzctMi45MDAxIDYuMDU1NyA2LjA1NTcgMCAwIDAtLjc0NzUtNy4wNzI5em0tOS4wMjIgMTIuNjA4MWE0LjQ3NTUgNC40NzU1IDAgMCAxLTIuODc2NC0xLjA0MDhsLjE0MTktLjA4MDQgNC43NzgzLTIuNzU4MmEuNzk0OC43OTQ4IDAgMCAwIC4zOTI3LS42ODEzdi02LjczNjlsMi4wMiAxLjE2ODZhLjA3MS4wNzEgMCAwIDEgLjAzOC4wNTJ2NS41ODI2YTQuNTA0IDQuNTA0IDAgMCAxLTQuNDk0NSA0LjQ5NDR6bS05LjY2MDctNC4xMjU0YTQuNDcwOCA0LjQ3MDggMCAwIDEtLjUzNDYtMy4wMTM3bC4xNDIuMDg1MiA0Ljc4MyAyLjc1ODJhLjc3MTIuNzcxMiAwIDAgMCAuNzgwNiAwbDUuODQyOC0zLjM2ODV2Mi4zMzI0YS4wODA0LjA4MDQgMCAwIDEtLjAzMzIuMDYxNUw5Ljc0IDE5Ljk1MDJhNC40OTkyIDQuNDk5MiAwIDAgMS02LjE0MDgtMS42NDY0ek0yLjM0MDggNy44OTU2YTQuNDg1IDQuNDg1IDAgMCAxIDIuMzY1NS0xLjk3MjhWMTEuNmEuNzY2NC43NjY0IDAgMCAwIC4zODc5LjY3NjVsNS44MTQ0IDMuMzU0My0yLjAyMDEgMS4xNjg1YS4wNzU3LjA3NTcgMCAwIDEtLjA3MSAwbC00LjgzMDMtMi43ODY1QTQuNTA0IDQuNTA0IDAgMCAxIDIuMzQwOCA3Ljg3MnptMTYuNTk2MyAzLjg1NThMMTMuMTAzOCA4LjM2NCAxNS4xMTkyIDcuMmEuMDc1Ny4wNzU3IDAgMCAxIC4wNzEgMGw0LjgzMDMgMi43OTEzYTQuNDk0NCA0LjQ5NDQgMCAwIDEtLjY3NjUgOC4xMDQydi01LjY3NzJhLjc5Ljc5IDAgMCAwLS40MDctLjY2N3ptMi4wMTA3LTMuMDIzMWwtLjE0Mi0uMDg1Mi00Ljc3MzUtMi43ODE4YS43NzU5Ljc3NTkgMCAwIDAtLjc4NTQgMEw5LjQwOSA5LjIyOTdWNi44OTc0YS4wNjYyLjA2NjIgMCAwIDEgLjAyODQtLjA2MTVsNC44MzAzLTIuNzg2NmE0LjQ5OTIgNC40OTkyIDAgMCAxIDYuNjgwMiA0LjY2ek04LjMwNjUgMTIuODYzbC0yLjAyLTEuMTYzOGEuMDgwNC4wODA0IDAgMCAxLS4wMzgtLjA1NjdWNi4wNzQyYTQuNDk5MiA0LjQ5OTIgMCAwIDEgNy4zNzU3LTMuNDUzN2wtLjE0Mi4wODA1TDguNzA0IDUuNDU5YS43OTQ4Ljc5NDggMCAwIDAtLjM5MjcuNjgxM3ptMS4wOTc2LTIuMzY1NGwyLjYwMi0xLjQ5OTggMi42MDY5IDEuNDk5OHYyLjk5OTRsLTIuNTk3NCAxLjQ5OTctMi42MDY3LTEuNDk5N1oiLz48L3N2Zz4='], ['Antigravity', null], ['AI orchestration', null]]],
  ].map(([group, items], g) => (
    <div key={group} style={{ display: 'flex', marginTop: g === 0 ? 24 : 0, paddingTop: g === 0 ? 0 : 14, paddingBottom: 14, borderBottom: g === 6 ? 'none' : '1px solid rgba(36,35,33,0.08)' }}>
      <span style={{ fontFamily: 'GeistMono', fontSize: 11, letterSpacing: 1, color: '#57524C', width: 150, marginTop: 8 }}>{group.toUpperCase()}</span>
      <div style={{ display: 'flex', flexWrap: 'wrap', width: 566 }}>
        {items.map(([name, icon]) => (
          <div key={name} style={{ display: 'flex', alignItems: 'center', height: 30, padding: '0 12px 0 10px', margin: '0 6px 6px 0', background: '#F8F6F2', border: '1px solid rgba(36,35,33,0.1)', borderRadius: 999 }}>
            {icon
              ? <img src={icon.startsWith('data:') ? icon : 'https://cdn.simpleicons.org/' + icon} width={14} height={14} />
              : <div style={{ display: 'flex', width: 7, height: 7, margin: '0 3px 0 4px', borderRadius: 999, background: '#D68096' }} />}
            <span style={{ fontFamily: 'GeistMedium', fontSize: 13, color: '#242321', marginLeft: 7 }}>{name}</span>
          </div>
        ))}
      </div>
    </div>
  ))}
</div>
```

```aura width=800 height=120
<div style={{ position: 'relative', display: 'flex', flexDirection: 'column', alignItems: 'center', justifyContent: 'center', width: '100%', height: '100%', background: '#632F3B', borderRadius: 24, overflow: 'hidden', fontFamily: 'Geist' }}>
  <style>{`
    @keyframes glow { 0%, 100% { transform: translate(0, 0); } 50% { transform: translate(60px, 0); } }
    #glow { animation: glow 8s ease-in-out infinite; }
    @media (prefers-reduced-motion: reduce) { #glow { animation: none; } }
  `}</style>
  <svg width="800" height="120" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="footglow" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(214,128,150,0.55)" />
        <stop offset="100%" stopColor="rgba(214,128,150,0)" />
      </radialGradient>
    </defs>
    <ellipse id="glow" cx="340" cy="120" rx="300" ry="110" fill="url(#footglow)" />
  </svg>
  <span style={{ fontFamily: 'Bricolage', fontSize: 30, letterSpacing: -0.6, color: '#FFFFFF' }}>Have an idea? Let's build something useful.</span>
  <span style={{ fontSize: 14, color: 'rgba(255,255,255,0.72)', marginTop: 8 }}>Reach me on LinkedIn or by email.</span>
</div>
```

```aura width=166 height=44 link="https://www.linkedin.com/in/seijil/" inline align=center
<div style={{ display: 'flex', alignItems: 'center', justifyContent: 'center', width: 150, height: 44, marginLeft: 8, background: '#FFFFFF', border: '1px solid rgba(36,35,33,0.16)', borderRadius: 999, fontFamily: 'GeistMedium', fontSize: 14, color: '#242321' }}>
  <img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0iIzBBNjZDMiIgZD0iTTIwLjQ0NyAyMC40NTJoLTMuNTU0di01LjU2OWMwLTEuMzI4LS4wMjctMy4wMzctMS44NTItMy4wMzctMS44NTMgMC0yLjEzNiAxLjQ0NS0yLjEzNiAyLjkzOXY1LjY2N0g5LjM1MVY5aDMuNDE0djEuNTYxaC4wNDZjLjQ3Ny0uOTQ4IDEuNjM3LTEuOTUgMy4zNy0xLjk1IDMuNjAxIDAgNC4yNjcgMi4zNyA0LjI2NyA1LjQ1NXY2LjI4NnpNNS4zMzcgNy40MzNjLTEuMTQ0IDAtMi4wNjMtLjkyNi0yLjA2My0yLjA2NSAwLTEuMTM4LjkyLTIuMDYzIDIuMDYzLTIuMDYzIDEuMTQgMCAyLjA2NC45MjUgMi4wNjQgMi4wNjMgMCAxLjEzOS0uOTI1IDIuMDY1LTIuMDY0IDIuMDY1em0xLjc4MiAxMy4wMTlIMy41NTVWOWgzLjU2NHYxMS40NTJ6TTIyLjIyNSAwSDEuNzcxQy43OTIgMCAwIC43NzQgMCAxLjcyOXYyMC41NDJDMCAyMy4yMjcuNzkyIDI0IDEuNzcxIDI0aDIwLjQ1MUMyMy4yIDI0IDI0IDIzLjIyNyAyNCAyMi4yNzFWMS43MjlDMjQgLjc3NCAyMy4yIDAgMjIuMjIyIDBoLjAwM3oiLz48L3N2Zz4=" width={16} height={16} />
  <span style={{ marginLeft: 8 }}>LinkedIn</span>
</div>
```

```aura width=166 height=44 link="mailto:seiji.workmail@gmail.com" inline align=center
<div style={{ display: 'flex', alignItems: 'center', justifyContent: 'center', width: 150, height: 44, marginLeft: 8, background: '#FFFFFF', border: '1px solid rgba(36,35,33,0.16)', borderRadius: 999, fontFamily: 'GeistMedium', fontSize: 14, color: '#242321' }}>
  <img src="https://cdn.simpleicons.org/gmail/EA4335" width={16} height={16} />
  <span style={{ marginLeft: 8 }}>Email</span>
</div>
```
