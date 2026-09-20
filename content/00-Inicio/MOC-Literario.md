---
title: "MOC — Laboratorio literario"
conocimiento: 64
lastmod: 2026-09-20
---

# MOC — Laboratorio literario

Analogías y motivos narrativos (**≠ evidencia**). Capítulo canónico: [[Cap-06-01-Medea-Damnatio-Rehen|Capítulo 6.1. Laboratorio literario: Medea, damnatio memoriae y el menor como rehén]] (**v1.54** · conocimiento **64**).

**Regla:** la metáfora aclara; **no tipifica** PAS/SAP. Meland dual ([@meland2026love]): no silenciar IPV ni negar PABs.

## Núcleo mítico / clásico

| Motivo | Forma | Cap-06 |
|--------|-------|--------|
| **Medea** | Venganza vía hijos; *philia*; maternidad atípica | §2.1–2.3b |
| **Deméter / Perséfone** | Rapto de la hija; madre buscadora; pacto cíclico de tiempo | §2.6 |
| **Oresteia** | Hijo entre relatos parentales; venganza → Areópago | §2.7 |
| **Telémaco / Odisea** | Padre ausente; suplentes; patetismo→ironía | §2.8 |
| *Damnatio memoriae* | Borrado ritual del nombre | §2.5 |
| Rehén | Menor como garantía emocional/procesal | §5.3 |
| Árbol a la sombra | Autoestima / meta-etnografía PA | [@roysland2026meta] |
| Amor condicionado | Meland | [@meland2026love] |

## Ficción / AV — mapa rápido (no tipicidad)

**Interferencia / PABs / corte:** Daudet §2.3c · Hawthorne §2.3d · McGee §2.3e · Sánchez §2.3f · Polak §2.3g · Egizii §2.3h · Josse §2.3i · Matthews §2.3j · Whitaker *You* §2.3k · Godly §2.3n · Aconis §2.3o · Burke §2.3p · Frost §2.3q · Lonie §2.3r · Bailey §2.3s · Adams §2.3t · Richardson §2.3u · Cross §2.3v · Olmos §2.3w · Salomón §2.3x · Gentile §2.3y · *Arrancamiento* §2.3z · W5 §2.3aa · Talbusch §2.3ab · Conway §2.3ac · Klune §2.3ad · Avieli §2.3ae · Riqueni §2.3l · *Querer* §2.3m (IPV).

**Bloque sustracción internacional (§2.3af–ak):** Trottner · Alan · Galbraith · Meyer · Khashoggi · ViDja — pareja Deméter; corredor Cap-01-03/04 (SRE/HCCH).

**Bloque alegaciones / mentira / alto conflicto (§2.3al–ao):** Bagdad · Whitaker *Nothing but the Truth* · Eddy *Splitting* · Delaney *Believe Me* — pareja Cap-01-03 (CIS/Smit); **prohibido** monopolio de género.

## Índice por polo (laboratorio dual)

| Polo ilustrado en trama | Ejemplos Cap-06 |
|-------------------------|-----------------|
| Madre no favorecida / buscadora | Egizii · Godly · Aconis · Lonie · Deméter · Trottner · *Arrancamiento* (advocacy IPV) |
| Padre no favorecido | McGee · Matthews · Whitaker *You* · Burke · Salomón |
| Actor de interferencia materno | Daudet · Polak · Sánchez · Matthews |
| Actor de interferencia paterno | Hawthorne · Egizii · Godly |
| POV menor | Polak · Trottner |

## Regla de etiquetado

Todo enlace aquí = dispositivo narrativo en el capítulo de origen (`#vf/literario`). Stats de blurbas/PASG **nunca** como tasa del Libro Vivo.

<!-- sync:mermaid-boot -->
<script type="module">
/* Quartz OFM mermaid: cold-load + SPA. Re-query after await (DOM swap). */
(async () => {
  if (window.__vfMermaidBoot) return;
  window.__vfMermaidBoot = true;
  const ready = () => {
    const center = document.querySelector(".center");
    return center ? [...center.querySelectorAll("code.mermaid")] : [];
  };
  let mermaid = null;
  let painting = false;
  const ensure = async () => {
    if (mermaid) return mermaid;
    const mod = await import(
      "https://cdnjs.cloudflare.com/ajax/libs/mermaid/11.4.0/mermaid.esm.min.mjs"
    );
    mermaid = mod.default;
    return mermaid;
  };
  const paint = async () => {
    if (painting) return;
    let nodes = ready().filter((n) => !n.querySelector("svg"));
    if (!nodes.length) return;
    painting = true;
    try {
      const m = await ensure();
      // Quartz SPA may replace .center while mermaid loads
      nodes = ready().filter((n) => !n.querySelector("svg"));
      if (!nodes.length) return;
      for (const n of nodes) {
        n.removeAttribute("data-processed");
      }
      const dark =
        document.documentElement.getAttribute("saved-theme") === "dark";
      m.initialize({
        startOnLoad: false,
        securityLevel: "loose",
        theme: dark ? "dark" : "base",
      });
      nodes = ready().filter((n) => !n.querySelector("svg"));
      if (!nodes.length) return;
      await m.run({ nodes });
    } catch (err) {
      console.warn("[vf mermaid-boot]", err);
    } finally {
      painting = false;
    }
  };
  const tryPaint = () => {
    paint().catch(() => {});
  };
  document.addEventListener("nav", tryPaint);
  document.addEventListener("themechange", tryPaint);
  tryPaint();
  for (const ms of [50, 200, 600, 1500, 3000]) {
    setTimeout(tryPaint, ms);
  }
  const mo = new MutationObserver(() => {
    if (ready().some((n) => !n.querySelector("svg"))) tryPaint();
  });
  if (document.body) {
    mo.observe(document.body, { childList: true, subtree: true });
  } else {
    document.addEventListener("DOMContentLoaded", () => {
      mo.observe(document.body, { childList: true, subtree: true });
    });
  }
})();
</script>
<!-- /sync:mermaid-boot -->
