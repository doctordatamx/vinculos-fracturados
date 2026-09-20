---
title: "Qué cambió en el libro — septiembre 2026"
obra: "Vinculos-Fracturados"
lastmod: 2026-09-20
fecha: "2026-09-20"
---

# Qué cambió en el libro — septiembre 2026

Resumen para lectores: temas **nuevos** o **reforzados**. No sustituye los capítulos; indica por dónde empezar.

---

## 1. México con datos (no con eslóganes)

En [[Cap-01-03-Estadistica-Mapa-Evidencia|Capítulo 1.3. Mapa estadístico: prevalencia, base rates y límites de la evidencia]] se consolidó un **pack mexicano**: violencia de pareja (ENDIREH), divorcios y custodia (Estadística de Divorcios del INEGI: quién recibe custodia, pensión, parejas del mismo sexo, factores asociados a la compartida), sustracción internacional (SRE / La Haya), y el vacío honesto de prevalencia nacional de conductas de interferencia parental (solo un estudio local débil en Saltillo).

**Qué cambia para usted:** puede citar cifras MX con fuente y año —y saber qué **no** mide cada encuesta.

---

## 2. Custodia compartida vs unilateral — con condiciones

Misma Parte I, sección nueva: la evidencia internacional (meta-análisis y revisiones: Bauserman, Baude, Nielsen, Vowels; estudios nórdicos) suele asociar la **custodia física compartida** a outcomes algo mejores que la unilateral… pero el efecto es **modesto** y **condicional**.

El libro adopta esta lectura: la compartida es pertinente si hay **seguridad**, **calidad parental**, **conflicto manejable** y **factibilidad**. No es un dogma del 50/50 ni una justificación de visitas mínimas “porque siempre se ha hecho así”. Con violencia de pareja o control coercitivo, limitar o supervisar el contacto puede ser lo correcto.

Detalle y mapa de decisión: [[Cap-01-03-Estadistica-Mapa-Evidencia|Capítulo 1.3. Mapa estadístico: prevalencia, base rates y límites de la evidencia]] §2.8 · puentes en [[Cap-03-03-Alto-Conflicto-Terapia-Reunificacion|Capítulo 3.3. Alto conflicto, terapia familiar y reunificación]] y [[Cap-03-05-Evaluacion-Custodia-Forense|Capítulo 3.5. Evaluación de custodia y peritaje forense]].

---

## 3. Mapa político por entidad (violencia / vicaria / alienación)

[[Cap-05-01-Asimetrias-Denuncia-Dogma|Capítulo 5.1. Asimetrías punitivas, denuncia instrumental y dogma de política pública]] incorpora un mapa de **asimetrías estatales**: tipificación de violencia de género / interpósita o vicaria, y cómo choca (o no) con el discurso de alienación parental. Sirve para no importar una ley de un estado como si fuera la regla nacional.

---

## 4. Peritaje familiar: más protocolos mexicanos

[[Cap-03-05-Evaluacion-Custodia-Forense|Capítulo 3.5. Evaluación de custodia y peritaje forense]] suma la guía federal OAJ de valoración de prueba psicológica, el protocolo de Tabasco y el marco SCJN para juzgar con perspectiva de infancia, además de CDMX y Edomex. El mensaje al lector: el peritaje debe ser **auditable**; “interferencia” no es atajo sindrómico.

---

## 5. Escuela: lo que sí hay y el hueco federal

[[Cap-07-01-Escuela-Consejeria-Logro|Capítulo 7.1. Escuela, consejería y logro: el menor entre hogares y aula]] aclara que **no** existe homologación SEP federal específica “divorcio × escuela”. Hay anclas (LGDNNA, protocolos locales como CDMX) y mucha evidencia ERIC sobre divorcio y logro escolar, pero casi nada sólido sobre “alienación × aula” en LATAM. La negativa a asistir (school refusal) se trata como síntoma diferencial, no como veredicto.

---

## 6. Laboratorio literario, sincronizado

[[Cap-06-01-Medea-Damnatio-Rehen|Capítulo 6.1. Laboratorio literario: Medea, damnatio memoriae y el menor como rehén]] y el [[MOC-Literario]] alinean Medea, Deméter/Perséfone, la *Oresteia* y Telémaco como **analogías** —nunca como diagnóstico. La regla no cambia: la metáfora aclara; no tipifica.

---

## 7. Genealogía del debate, versión estable

[[Cap-01-01-Genealogia-SAP-Interferencia-Vicaria|Capítulo 1.1. Genealogía crítica: Del SAP (Gardner) a la Interferencia Parental y la Violencia Vicaria]] queda como ancla de lectura: del SAP de Gardner a PABs / PCCP / violencia vicaria, sin negar IPV ni convertir todo rechazo en manipulación (doble riesgo Meland).

---

## Cómo leer esto sin perder el hilo

| Si le interesa… | Empiece por… |
|-----------------|--------------|
| Cifras y límites de la evidencia | [[Cap-01-03-Estadistica-Mapa-Evidencia|Capítulo 1.3. Mapa estadístico: prevalencia, base rates y límites de la evidencia]] |
| ¿Compartida o no? | Cap-01-03 §2.8 |
| Política / denuncias / dogmas | [[Cap-05-01-Asimetrias-Denuncia-Dogma|Capítulo 5.1. Asimetrías punitivas, denuncia instrumental y dogma de política pública]] |
| Informe pericial | [[Cap-03-05-Evaluacion-Custodia-Forense|Capítulo 3.5. Evaluación de custodia y peritaje forense]] |
| Escuela y asistencia | [[Cap-07-01-Escuela-Consejeria-Logro|Capítulo 7.1. Escuela, consejería y logro: el menor entre hogares y aula]] |
| Relatos y mitos (con cuidado) | [[Cap-06-01-Medea-Damnatio-Rehen|Capítulo 6.1. Laboratorio literario: Medea, damnatio memoriae y el menor como rehén]] |

Registro técnico interno: [[changelog-libro]].

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
