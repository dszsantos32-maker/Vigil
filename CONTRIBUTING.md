# Cómo contribuir a Vigil

Gracias por tu interés en contribuir. Vigil es un proyecto 
de código abierto bajo GPL v3, construido por y para la 
comunidad técnica que cree en transparencia y soberanía digital.

---

## Principios de contribución

Antes de contribuir, lee y acepta estos principios:

1. **Defensa, no ataque.** Ninguna contribución puede añadir 
   capacidades ofensivas, destructivas o de vigilancia no consentida.
2. **Permiso explícito.** Todo código debe operar exclusivamente 
   en redes donde el operador tiene autoridad legal.
3. **Mínima intrusión.** Solo metadata, nunca contenido 
   de comunicaciones.
4. **Transparencia total.** Sin componentes propietarios, 
   sin dependencias cerradas.

Contribuciones que violen estos principios serán rechazadas 
independientemente de su calidad técnica.

---

## ¿Qué necesita el proyecto ahora?

### Prioridad alta
- [ ] Prototipo de sensor de red en Python (Scapy/pyshark)
- [ ] Lista verificada de endpoints de APIs de IA conocidas
- [ ] Módulo de hashing de hallazgos (privacidad por diseño)

### Prioridad media
- [ ] Protocolo de consenso distribuido (gossip protocol)
- [ ] Sistema de timestamping criptográfico
- [ ] Documentación técnica en inglés

### Prioridad baja
- [ ] Interfaz de visualización de hallazgos
- [ ] Empaquetado para Raspberry Pi
- [ ] Tests automatizados

---

## Cómo enviar una contribución

### Para código

1. Haz fork del repositorio
2. Crea una rama descriptiva:
   `git checkout -b feature/nombre-descriptivo`
3. Escribe código limpio con comentarios en español o inglés
4. Incluye tests si aplica
5. Abre un Pull Request describiendo qué hace y por qué

### Para documentación

1. Abre un Issue primero describiendo qué quieres agregar
2. Si hay consenso, procede con el Pull Request

### Para reportar bugs o proponer ideas

Abre un Issue con:
- Descripción clara del problema o propuesta
- Contexto técnico relevante
- Si es bug: pasos para reproducirlo

---

## Stack técnico actual

| Componente | Tecnología | Estado |
|------------|------------|--------|
| Lenguaje principal | Python 3.10+ | Definido |
| Sensor de red | Scapy / pyshark | Por implementar |
| Hashing | hashlib (stdlib) | Por implementar |
| Registro distribuido | Por definir | En discusión |
| Consenso P2P | Por definir | En discusión |

---

## Código de conducta

- Comunicación respetuosa y técnicamente fundamentada
- Las discusiones se basan en evidencia, no en autoridad
- Las decisiones de arquitectura las toma el fundador 
  con input de la comunidad
- No se toleran contribuciones con agenda comercial 
  o gubernamental no declarada

---

## Idiomas

El proyecto acepta contribuciones en español e inglés.
La documentación principal se mantiene en ambos idiomas.

---

## Contacto

Abre un Issue para cualquier pregunta.
El repositorio no tiene canal de comunicación privado 
por principio de transparencia.

---

*Vigil es un proyecto independiente sin financiamiento 
corporativo ni gubernamental.*
