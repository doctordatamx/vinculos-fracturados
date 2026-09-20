---
title: "MOC — Evidencia"
---

# MOC — Evidencia

**Target alcanzado:** registry **1442** · papers **1450** · oleada 3 (escuela/CODIP, OA PA, SciELO judicial) 2026-09-19.  
Orquestador: `scripts/expand_corpus_vinculos.py` · SciELO/OpenAlex caps.

## Estado (actualizar con)

```bash
python3 -c "import json; print(len(json.load(open('metodologia/ingest-registry.json'))['entries']))"
```

## Capítulos (16) · orden temático por parte

| Capítulo | Eje |
|----------|-----|
| [[Cap-01-01-Genealogia-SAP-Interferencia-Vicaria|Capítulo 1.1. Del SAP a la interferencia y la violencia vicaria]] | Genealogía (v0.14 · Lee-Maturana / Portilla) |
| [[Cap-01-02-Redefinicion-CDN-Neurociencia|Capítulo 1.2. Derechos del Niño y neurociencia del apego]] | CDN / apego (v1.3 · conocimiento 103 · HPA/OT) |
| [[Cap-01-03-Estadistica-Mapa-Evidencia|Capítulo 1.3. Mapa estadístico: prevalencia y base rates]] | Estadística (v1.12 · pack MX + compartida condicional §2.8) |
| [[Cap-02-01-Trauma-Ruptura-Vinculo|Capítulo 2.1. Trauma de ruptura forzada]] | Trauma (v1.3 · conocimiento 103 · HPA/OT) |
| [[Cap-02-02-Evaluacion-Medicion-PABs|Capítulo 2.2. Evaluación y medición (comportamientos parentales alienantes, escalas)]] | Medición (v1.2 · Casullo/Cerqueira/López) |
| [[Cap-03-01-Lealtad-Memoria-Gatekeeping|Capítulo 3.1. Lealtad forzada, memoria y gatekeeping]] | Mecanismos (v1.2 · conocimiento 80) |
| [[Cap-03-02-Apego-Divorcio-Separacion|Capítulo 3.2. Apego, divorcio y separación]] | Apego–divorcio (v1.2 · conocimiento 80) |
| [[Cap-03-03-Alto-Conflicto-Terapia-Reunificacion|Capítulo 3.3. Alto conflicto, terapia y reunificación]] | Terapia (v1.2 · Balmer/Poustie sistemas) |
| [[Cap-03-04-Control-Coercitivo-Familia|Capítulo 3.4. Control coercitivo, familia y custodia]] | Control coercitivo (v1.2 · conocimiento 80) |
| [[Cap-03-05-Evaluacion-Custodia-Forense|Capítulo 3.5. Evaluación de custodia y peritaje forense]] | Peritaje (v1.5 · SAID / Faller) |
| [[Cap-04-01-Medidas-Cautelares-Sesgo|Capítulo 4.1. Cautelares, presunción y victimización institucional]] | Cautelares (v1.3 · BIC/Ruiz/Herrera) |
| [[Cap-04-02-Jurisprudencia-Mexicana-SCJN|Capítulo 4.2. Jurisprudencia mexicana (Suprema Corte)]] | Suprema Corte (v1.7 · perfiles OJJDP/HCCH) |
| [[Cap-04-03-IPV-Custodia-Denuncias|Capítulo 4.3. Violencia de pareja, custodia y denuncias]] | Violencia de pareja–custodia (v1.4 · sustracción int.) |
| [[Cap-05-01-Asimetrias-Denuncia-Dogma|Capítulo 5.1. Asimetrías, denuncia instrumental y dogma]] | Política (v1.5 · SAID syndrome) |
| [[Cap-06-01-Medea-Damnatio-Rehen|Capítulo 6.1. Medea, damnatio y el menor como rehén]] | Literario (v1.13 · Sarmet / Jacobs) |
| [[Cap-07-01-Escuela-Consejeria-Logro|Capítulo 7.1. Escuela, consejería y logro]] | Escuela / ERIC (v1.2 · CODIP/Wolchik/Botha) |


## Prioridad metodológica

1. Meta / systematic review  
2. Longitudinal / psicometría / N grande  
3. Empírico  
4. Jurisprudencia  
5. Opinión (baja)

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
