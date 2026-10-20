# REFERENCES — Backend Architecture & Design

Usa `sets-framework/docs/REFERENCE_POLICY.md` para evaluar autoridad, vigencia y adecuación. Consulta una fuente para resolver una pregunta concreta; esta lista no prescribe un stack ni una ruta de lectura lineal.

## Referencias técnicas

- **Java Platform Specifications:** https://docs.oracle.com/javase/specs/ — semántica de lenguaje/JVM según versión.
- **Spring Framework Reference:** https://docs.spring.io/spring-framework/reference/ — contratos y comportamiento del framework; no es arquitectura universal.
- **PostgreSQL Documentation:** https://www.postgresql.org/docs/ — transacciones, aislamiento, locking, índices, replicación y operación.
- **Apache Kafka Documentation:** https://kafka.apache.org/documentation/ — solo cuando Kafka sea una opción pertinente.
- **Azure Architecture Center — API Design:** https://learn.microsoft.com/en-us/azure/architecture/microservices/design/api-design — diseño de contratos de API.
- **Google SRE Books:** https://sre.google/books/ — confiabilidad, operación e incidentes.
- **OWASP Cheat Sheet Series:** https://cheatsheetseries.owasp.org/ — controles y riesgos de seguridad de aplicaciones.

## Libros útiles según la pregunta

- Martin Kleppmann, *Designing Data-Intensive Applications* — sistemas de datos, replicación y consistencia.
- Michael T. Nygard, *Release It!* — resiliencia y fallos en producción.
- Sam Newman, *Building Microservices* — límites, integración y operación de servicios; contrastar sus recomendaciones con el contexto.
- John Ousterhout, *A Philosophy of Software Design* — modularidad y complejidad.

Distingue la documentación de una herramienta, el comportamiento de una versión concreta y el principio arquitectónico. Verifica las versiones vigentes cuando una recomendación dependa de ellas.
