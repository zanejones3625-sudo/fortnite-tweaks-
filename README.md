# fortnite-tweaks-# fortnite-tweaks-:root {
  color-scheme: dark;
  --ink: #f5f1e8;
  --acid: #d8f53b;
  --orange: #ff744b;
  --line: rgba(245, 241, 232, 0.32);
}

* {
  box-sizing: border-box;
}

html,
body {
  margin: 0;
  min-height: 100%;
  background: #11130f;
}

body {
  color: var(--ink);
  font-family: "Space Mono", monospace;
}

.hero {
  isolation: isolate;
  min-height: 100svh;
  overflow: hidden;
  position: relative;
  display: grid;
  align-items: end;
  padding: clamp(2rem, 6vw, 5.5rem);
}

.hero__video,
.hero__scrim {
  height: 100%;
  inset: 0;
  position: absolute;
  width: 100%;
}

.hero__video {
  background: #25291e;
  border: 0;
  height: 56.25vw;
  left: 50%;
  min-height: 100%;
  min-width: 100%;
  pointer-events: none;
  top: 50%;
  transform: translate(-50%, -50%);
  width: 177.78vh;
  z-index: -2;
}

.hero__scrim {
  background:
    linear-gradient(90deg, rgba(10, 13, 8, 0.88) 0%, rgba(10, 13, 8, 0.48) 42%, rgba(10, 13, 8, 0.16) 100%),
    linear-gradient(0deg, rgba(10, 13, 8, 0.74) 0%, transparent 58%);
  z-index: -1;
}

.hero__content {
  max-width: 44rem;
  animation: rise-in 800ms cubic-bezier(0.2, 0.8, 0.2, 1) both;
}

.eyebrow {
  color: var(--acid);
  font-size: 0.7rem;
  letter-spacing: 0.08em;
  margin: 0 0 1.25rem;
  text-transform: uppercase;
}

h1 {
  font-family: "Barlow Condensed", sans-serif;
  font-size: clamp(5rem, 15vw, 12rem);
  font-weight: 900;
  letter-spacing: 0;
  line-height: 0.76;
  margin: 0;
  text-transform: uppercase;
}

h1 span {
  color: var(--orange);
}

.hero__copy {
  font-size: clamp(0.8rem, 1.4vw, 1rem);
  margin: 2rem 0 1.75rem;
}

.hero__link {
  align-items: center;
  border-bottom: 1px solid var(--acid);
  color: var(--ink);
  display: inline-flex;
  font-size: 0.75rem;
  gap: 1rem;
  padding: 0 0 0.7rem;
  text-decoration: none;
  text-transform: uppercase;
  transition: color 180ms ease, gap 180ms ease;
}

.hero__link:hover {
  color: var(--acid);
  gap: 1.4rem;
}

.hero__status {
  align-items: center;
  border-top: 1px solid var(--line);
  color: rgba(245, 241, 232, 0.72);
  display: flex;
  font-size: 0.65rem;
  gap: 0.6rem;
  justify-self: end;
  margin: 0;
  padding-top: 0.75rem;
  text-transform: uppercase;
  width: min(16rem, 30vw);
}

.hero__status span {
  background: var(--acid);
  border-radius: 50%;
  box-shadow: 0 0 0 0.25rem rgba(216, 245, 59, 0.16);
  height: 0.45rem;
  width: 0.45rem;
}

@keyframes rise-in {
  from { opacity: 0; transform: translateY(1.5rem); }
  to { opacity: 1; transform: translateY(0); }
}

@media (max-width: 600px) {
  .hero {
    padding: 2rem 1.5rem;
  }

  .hero__status {
    bottom: 2rem;
    position: absolute;
    right: 1.5rem;
    width: auto;
  }
}

@media (prefers-reduced-motion: reduce) {
  .hero__content { animation: none; }
  .hero__link { transition: none; }
}

.tutorial {
  min-height: 100svh;
  padding: clamp(2rem, 6vw, 5rem);
}

.tutorial__header {
  align-items: end;
  display: flex;
  justify-content: space-between;
  margin: 0 auto 2.5rem;
  max-width: 72rem;
  gap: 2rem;
}

.tutorial__back {
  color: var(--acid);
  font-size: 0.7rem;
  text-decoration: none;
  text-transform: uppercase;
}

.tutorial__heading {
  font-family: "Barlow Condensed", sans-serif;
  font-size: clamp(3.5rem, 9vw, 8rem);
  line-height: 0.8;
  margin: 0;
  max-width: 48rem;
  text-transform: uppercase;
}

.tutorial__heading span {
  color: var(--orange);
}

.tutorial__body {
  margin: 0 auto;
  max-width: 72rem;
}

.tutorial__choices {
  display: grid;
  gap: 1rem;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  margin-bottom: 4rem;
  max-width: 58rem;
}

.tutorial__choice {
  border: 1px solid var(--line);
  color: var(--ink);
  display: flex;
  flex-direction: column;
  min-height: 11rem;
  padding: 1.5rem;
  text-decoration: none;
  transition: border-color 180ms ease, transform 180ms ease;
}

.tutorial__choice:hover {
  border-color: var(--acid);
  transform: translateY(-0.25rem);
}

.tutorial__choice--paid {
  border-color: rgba(255, 116, 75, 0.62);
}

.tutorial__choice--paid:hover {
  border-color: var(--orange);
}

.tutorial__choice-label {
  color: var(--acid);
  font-size: 0.65rem;
  letter-spacing: 0.08em;
  text-transform: uppercase;
}

.tutorial__choice--paid .tutorial__choice-label {
  color: var(--orange);
}

.tutorial__choice strong {
  font-family: "Barlow Condensed", sans-serif;
  font-size: clamp(2.5rem, 5vw, 4.5rem);
  line-height: 0.9;
  margin: auto 0 1.25rem;
  text-transform: uppercase;
}

.tutorial__choice > span:last-child {
  font-size: 0.7rem;
  text-transform: uppercase;
}

.tutorial__panel {
  background: #25291e;
  border: 1px solid var(--line);
  max-width: 58rem;
  padding: clamp(2rem, 6vw, 5rem);
}

.tutorial__panel h2 {
  font-family: "Barlow Condensed", sans-serif;
  font-size: clamp(3rem, 8vw, 7rem);
  line-height: 0.85;
  margin: 0;
  text-transform: uppercase;
}

.tutorial__video {
  aspect-ratio: 16 / 9;
  background: #25291e;
  border: 1px solid var(--line);
  display: block;
  width: min(100%, 58rem);
}

.tutorial__note {
  color: rgba(245, 241, 232, 0.72);
  font-size: 0.8rem;
  line-height: 1.7;
  margin: 1.5rem 0;
  max-width: 38rem;
}

.tutorial__button {
  border-bottom: 1px solid var(--acid);
  color: var(--ink);
  display: inline-block;
  font-size: 0.75rem;
  padding-bottom: 0.7rem;
  text-decoration: none;
  text-transform: uppercase;
}

.tutorial__button:hover {
  color: var(--acid);
}

@media (max-width: 600px) {
  .tutorial__header {
    align-items: start;
    flex-direction: column-reverse;
  }

  .tutorial__choices {
    grid-template-columns: 1fr;
    margin-bottom: 3rem;
  }
}                                                                                                                                                               <!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Fortnite Tweaks</title>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@500;700;800;900&family=Space+Mono:wght@400;700&display=swap" rel="stylesheet" />
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <main class="hero">
      <iframe
        class="hero__video"
        src="https://www.youtube-nocookie.com/embed/qmv2kClUaOY?autoplay=1&mute=1&controls=0&loop=1&playlist=qmv2kClUaOY&modestbranding=1&rel=0&playsinline=1"
        title="Fortnite background video"
        allow="autoplay; encrypted-media"
        referrerpolicy="strict-origin-when-cross-origin"
      ></iframe>
      <div class="hero__scrim" aria-hidden="true"></div>
      <div class="hero__content">
        <p class="eyebrow">Performance / Precision / Play</p>
        <h1>Fortnite<br /><span>Tweaks</span></h1>
        <p class="hero__copy">Dial in your setup. Drop in sharper.</p>
        <a class="hero__link" href="tutorial.html" target="_blank" rel="noopener">Explore setup <span aria-hidden="true">↗</span></a>
      </div>
      <p class="hero__status"><span></span> Live session</p>
    </main>
  </body>
</html>
