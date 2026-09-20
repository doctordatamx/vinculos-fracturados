---
title: "Changelog del libro"
obra: "Vinculos-Fracturados"
---

# Changelog del libro

El registro canónico vive en [[changelog-libro]] (`metodologia/changelog-libro.md`).

Esta nota existe para publicación web / navegación desde el libro.

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
