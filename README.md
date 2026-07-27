# CI-CD
Core Concepts - CI vs CD

1. Continuous Integration (CI) — Integración Continua
Cada vez que haces push, el pipeline automáticamente compila (build) y corre los tests.
- Objetivo: detectar código roto en minutos, no días.
- Sin CI, podrías tardar semanas en descubrir que tu cambio rompió algo que otro compañero hizo — con CI, te enteras en el siguiente push.
- Aquí es donde vive el famoso "check verde/rojo" en un Pull Request.

2. Continuous Delivery (CD - Entrega Continua)
Un paso más allá de CI: además de construir y testear, el pipeline deja el artefacto siempre listo para desplegar.
- La diferencia clave: un humano decide cuándo hacer clic en "deploy".
- El código está probado y empaquetado, pero el despliegue a producción es una acción manual/consciente.

3. Continuous Deployment (CD - Despliegue Continuo)
Mismo pipeline, pero sin el humano en el medio: si todos los checks pasan (build ✅ + tests ✅), se despliega automáticamente a producción.
- Es el nivel máximo de automatización.
- Requiere mucha confianza en tu suite de tests, porque no hay revisión manual antes de producción.

CI:                    build + test (automático)
CD (Delivery):         build + test + package listo → [humano hace clic] → deploy
CD (Deployment):       build + test + package listo → deploy (automático)
