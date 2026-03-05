:root{
  --navy:#0b3a6f;
  --red:#c62828;
  --white:#ffffff;
  --text:#0b1220;
  --muted:#6b7280;
  --card: rgba(255,255,255,0.10);
  --glass: rgba(255,255,255,0.16);
  --border: rgba(255,255,255,0.22);
  --shadow: 0 18px 40px rgba(0,0,0,0.20);
  --radius: 18px;
}

*{ box-sizing:border-box; }
html{ scroll-behavior:smooth; }
body{
  margin:0;
  font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Arial, "Helvetica Neue", sans-serif;
  color:var(--text);
  background:#f6f8fb;
}

.container{
  width:min(1120px, calc(100% - 40px));
  margin-inline:auto;
}

/* Header */
.header{
  position:sticky;
  top:0;
  z-index:50;
  background: rgba(11,58,111,0.88);
  backdrop-filter: blur(10px);
  border-bottom:1px solid rgba(255,255,255,0.12);
}
.header__inner{
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:16px;
  padding:14px 0;
}

.brand{
  display:flex;
  align-items:center;
  gap:12px;
  text-decoration:none;
  color:white;
}
.brand__mark{
  width:42px;height:42px;
  border-radius:999px;
  display:grid;place-items:center;
  background: rgba(255,255,255,0.16);
  border:1px solid rgba(255,255,255,0.24);
  font-weight:800;
}
.brand__name{ font-weight:800; letter-spacing:.2px; }
.brand__sub{ font-size:12px; opacity:.85; letter-spacing:.8px; }

.nav{ display:flex; align-items:center; gap:14px; }
.nav__toggle{
  display:none;
  border:1px solid rgba(255,255,255,0.22);
  background: rgba(255,255,255,0.10);
  color:white;
  border-radius:12px;
  padding:8px 10px;
  cursor:pointer;
}
.nav__links{
  display:flex;
  align-items:center;
  gap:18px;
  list-style:none;
  padding:0;margin:0;
}
.nav__links a{
  color:white;
  text-decoration:none;
  font-weight:600;
  opacity:.92;
}
.nav__links a:hover{ opacity:1; text-decoration:underline; text-underline-offset:6px; }

.btn{
  display:inline-flex;
  align-items:center;
  justify-content:center;
  gap:10px;
  padding:12px 16px;
  border-radius:999px;
  text-decoration:none;
  font-weight:800;
  border:1px solid transparent;
  cursor:pointer;
  transition: transform .12s ease, filter .12s ease;
}
.btn:hover{ transform: translateY(-1px); filter: brightness(1.02); }
.btn:active{ transform: translateY(0px); }

.btn--donate{
  background: var(--red);
  color:white;
  box-shadow: 0 12px 24px rgba(198,40,40,0.28);
}
.heart{ font-size:14px; }

/* Hero */
.hero{
  position:relative;
  min-height: 82vh;
  display:flex;
  align-items:flex-end;
  padding: 64px 0 46px;
  overflow:hidden;
}
.hero__bg{
  position:absolute; inset:0;
  background-image: url("assets/hero.jpg");
  background-size: cover;
  background-position: center;
  transform: scale(1.04);
}
.hero__overlay{
  position:absolute; inset:0;
  background:
    linear-gradient(90deg, rgba(11,58,111,0.82) 0%, rgba(11,58,111,0.45) 55%, rgba(11,58,111,0.18) 100%),
    linear-gradient(0deg, rgba(0,0,0,0.34), rgba(0,0,0,0.10));
}
.hero__content{ position:relative; color:white; }
.pill{
  display:inline-flex;
  align-items:center;
  gap:10px;
  padding:10px 14px;
  border-radius:999px;
  background: rgba(255,255,255,0.14);
  border:1px solid rgba(255,255,255,0.22);
  font-weight:800;
  letter-spacing:.6px;
  margin-bottom:14px;
}

.hero__title{
  margin:0;
  font-size: clamp(38px, 4.8vw, 68px);
  line-height:1.02;
  letter-spacing:-0.8px;
  text-shadow: 0 12px 35px rgba(0,0,0,0.34);
}
.hero__title .muted{ opacity:.9; }
.hero__title .accent{
  color: var(--red);
  text-shadow: 0 14px 40px rgba(0,0,0,0.35);
}

.hero__subtitle{
  max-width: 640px;
  font-size: clamp(16px, 2vw, 20px);
  line-height:1.5;
  opacity:.95;
  margin: 16px 0 18px;
}

.hero__actions{
  display:flex;
  gap:12px;
  flex-wrap:wrap;
  margin-bottom: 18px;
}

.btn--primary{
  background: var(--red);
  color:white;
  box-shadow: 0 14px 32px rgba(198,40,40,0.26);
}
.btn--glass{
  background: rgba(255,255,255,0.18);
  color:white;
  border:1px solid rgba(255,255,255,0.26);
  backdrop-filter: blur(10px);
}
.btn--outline{
  background: transparent;
  color: var(--red);
  border: 2px solid var(--red);
}

/* Signup card */
.signup{
  margin-top: 14px;
  padding: 16px 16px 14px;
  border-radius: var(--radius);
  background: rgba(255,255,255,0.18);
  border: 1px solid rgba(255,255,255,0.28);
  backdrop-filter: blur(12px);
  box-shadow: var(--shadow);
  max-width: 620px;
}
.signup__headline{ font-weight:900; }
.signup__sub{ opacity:.92; font-size:13px; margin-top:4px; }

.signup__form{
  display:flex;
  gap:10px;
  margin-top: 12px;
  flex-wrap:wrap;
}
.signup input{
  flex: 1 1 260px;
  padding: 12px 14px;
  border-radius:999px;
  border: 1px solid rgba(255,255,255,0.32);
  background: rgba(255,255,255,0.14);
  color:white;
  outline:none;
}
.signup input::placeholder{ color: rgba(255,255,255,0.80); }
.signup__note{ margin-top:10px; font-size:13px; opacity:.95; }

/* Sections */
.section{
  padding: 70px 0;
  background: #f6f8fb;
}
.section--alt{
  background: #eef3fa;
}
h2{
  margin:0 0 10px;
  font-size: clamp(26px, 3vw, 36px);
  letter-spacing:-0.4px;
}
.lead{
  margin:0 0 16px;
  color:#22324a;
  font-size: 18px;
  line-height:1.6;
}
p{ color:#22324a; line-height:1.7; }

.grid-2{
  display:grid;
  grid-template-columns: 1.2fr 0.8fr;
  gap: 22px;
  align-items:start;
}

.cards{
  display:grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 14px;
  margin-top: 18px;
}

.card{
  background:white;
  border: 1px solid rgba(15,23,42,0.08);
  border-radius: var(--radius);
  padding: 18px;
  box-shadow: 0 10px 24px rgba(15,23,42,0.06);
}
.card h3{ margin:0 0 8px; }
.card p{ margin:0; color:#334155; }

.photo-card{
  padding:0;
  overflow:hidden;
}
.photo-card img{
  width:100%;
  height:auto;
  display:block;
}
.photo-card__fallback{
  padding:18px;
}
.photo-card__title{ font-weight:900; }
.photo-card code{
  background:#0b3a6f10;
  padding:2px 6px;
  border-radius:8px;
}

.stats{
  display:grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 10px;
  margin-top: 16px;
}
.stat{
  background:#0b3a6f;
  color:white;
  border-radius: 16px;
  padding: 12px 14px;
}
.stat__num{ font-weight:900; }
.stat__label{ font-size:12px; opacity:.9; margin-top:4px; }

.bullets{
  margin: 14px 0 0;
  padding-left: 18px;
}
.bullets li{ margin: 8px 0; color:#334155; }

.form{
  display:grid;
  gap: 10px;
}
.form__row label{
  font-weight:800;
  font-size: 13px;
  color:#0f172a;
}
.form__row input, .form__row select{
  width:100%;
  padding: 12px 12px;
  border-radius: 14px;
  border: 1px solid rgba(15,23,42,0.12);
  outline:none;
}
.form__note{
  margin-top: 8px;
  color:#0f172a;
  font-size: 13px;
}

.link{
  color: var(--navy);
  font-weight:800;
  text-decoration:none;
}
.link:hover{ text-decoration:underline; text-underline-offset: 5px; }

.small{ font-size: 13px; color:#475569; }

/* Donate section */
.donate{
  background: linear-gradient(180deg, #0b3a6f 0%, #0b2f5a 100%);
  color:white;
}
.donate h2, .donate p{ color:white; }
.donate__inner{
  display:grid;
  grid-template-columns: 1.1fr 0.9fr;
  gap: 18px;
  align-items:center;
}
.donate__card{
  background: rgba(255,255,255,0.10);
  border:1px solid rgba(255,255,255,0.20);
  box-shadow: var(--shadow);
}
.donate__buttons{
  display:grid;
  grid-template-columns: repeat(3, 1fr);
  gap:10px;
}
.donate__fine{
  margin-top: 10px;
  opacity:.95;
}
.donate .btn--outline{
  color:white;
  border-color: rgba(255,255,255,0.45);
}

/* Footer */
.footer{
  background:#071e3a;
  color:white;
  padding: 26px 0;
}
.footer__inner{
  display:flex;
  align-items:flex-start;
  justify-content:space-between;
  gap:14px;
}
.footer__title{ font-weight:900; }
.footer__sub{ font-size:12px; opacity:.85; margin-top:4px; }
.footer__disclaimer{ font-size:12px; opacity:.85; margin-top:10px; }

.sr-only{
  position:absolute;
  width:1px;height:1px;
  padding:0;margin:-1px;
  overflow:hidden; clip:rect(0,0,0,0);
  border:0;
}

/* Responsive */
@media (max-width: 980px){
  .cards{ grid-template-columns: repeat(2, 1fr); }
  .grid-2, .donate__inner{ grid-template-columns: 1fr; }
  .stats{ grid-template-columns: 1fr; }
}

@media (max-width: 760px){
  .nav__toggle{ display:inline-flex; }
  .nav__links{
    position:absolute;
    right: 20px;
    top: 68px;
    flex-direction:column;
    background: rgba(11,58,111,0.96);
    border: 1px solid rgba(255,255,255,0.18);
    border-radius: 16px;
    padding: 12px;
    display:none;
    min-width: 200px;
  }
  .nav__links.show{ display:flex; }
  .btn--donate{ display:none; } /* keep header clean on mobile */
  .donate__buttons{ grid-template-columns: 1fr; }
}