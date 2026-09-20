---
title: "MOC — Conceptos"
---

# MOC — Conceptos

Mapa de términos operativos → [[Apendice-A-Glosario]].

## Núcleo

- Alienación parental (dinámica, no síndrome) → [[Cap-01-01-Genealogia-SAP-Interferencia-Vicaria|Capítulo 1.1. Genealogía crítica: Del SAP (Gardner) a la Interferencia Parental y la Violencia Vicaria]]
- SAP (histórico) → [[Cap-01-01-Genealogia-SAP-Interferencia-Vicaria|Capítulo 1.1. Genealogía crítica: Del SAP (Gardner) a la Interferencia Parental y la Violencia Vicaria]]
- PABs → [[Cap-02-01-Trauma-Ruptura-Vinculo|Capítulo 2.1. Trauma de ruptura forzada: apego, estrés y neurodesarrollo]]
- PCCP / RRD → [[Cap-03-01-Lealtad-Memoria-Gatekeeping|Capítulo 3.1. Lealtad forzada, manipulación de la memoria y gatekeeping]]
- Gatekeeping → [[Cap-03-01-Lealtad-Memoria-Gatekeeping|Capítulo 3.1. Lealtad forzada, manipulación de la memoria y gatekeeping]]
- Violencia vicaria → [[Cap-01-01-Genealogia-SAP-Interferencia-Vicaria|Capítulo 1.1. Genealogía crítica: Del SAP (Gardner) a la Interferencia Parental y la Violencia Vicaria]] · [[Cap-05-01-Asimetrias-Denuncia-Dogma|Capítulo 5.1. Asimetrías punitivas, denuncia instrumental y dogma de política pública]]
- Interés superior / CDN → [[Cap-01-02-Redefinicion-CDN-Neurociencia|Capítulo 1.2. Redefinición operativa: Derechos del Niño y neurociencia del apego]]
- Victimización institucional → [[Cap-04-01-Medidas-Cautelares-Sesgo|Capítulo 4.1. Medidas cautelares, presunción y victimización institucional]]

## Capítulos

- [[Cap-01-01-Genealogia-SAP-Interferencia-Vicaria|Capítulo 1.1. Genealogía crítica: Del SAP (Gardner) a la Interferencia Parental y la Violencia Vicaria]]
- [[Cap-01-02-Redefinicion-CDN-Neurociencia|Capítulo 1.2. Redefinición operativa: Derechos del Niño y neurociencia del apego]]
- [[Cap-01-03-Estadistica-Mapa-Evidencia|Capítulo 1.3. Mapa estadístico: prevalencia, base rates y límites de la evidencia]]
- [[Cap-02-01-Trauma-Ruptura-Vinculo|Capítulo 2.1. Trauma de ruptura forzada: apego, estrés y neurodesarrollo]]
- [[Cap-03-01-Lealtad-Memoria-Gatekeeping|Capítulo 3.1. Lealtad forzada, manipulación de la memoria y gatekeeping]]
- [[Cap-04-01-Medidas-Cautelares-Sesgo|Capítulo 4.1. Medidas cautelares, presunción y victimización institucional]]
- [[Cap-05-01-Asimetrias-Denuncia-Dogma|Capítulo 5.1. Asimetrías punitivas, denuncia instrumental y dogma de política pública]]
- [[Cap-06-01-Medea-Damnatio-Rehen|Capítulo 6.1. Laboratorio literario: Medea, damnatio memoriae y el menor como rehén]]

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
