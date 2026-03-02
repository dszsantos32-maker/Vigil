# Vigil

**Sistema de detección distribuido para monitorear integraciones de IA 
en infraestructura crítica**

**Versión:** 0.1-alpha  
**Fecha:** 2 de marzo de 2026  
**Licencia:** GNU GPL v3  
**Estado:** Diseño — buscando colaboradores

---

## ¿Qué es Vigil?

Vigil es un sistema de detección y alerta distribuido que monitorea 
integraciones de inteligencia artificial en redes donde el operador 
tiene permiso explícito. Documenta hallazgos de forma verificable, 
criptográficamente inmutable y públicamente accesible.

**Principio fundamental:** Defensa, no ataque. Transparencia, 
no destrucción.

---

## ¿Por qué existe Vigil?

En febrero de 2026, el conflicto entre Anthropic y el Departamento 
de Guerra de EE.UU. reveló una falla estructural crítica: sistemas 
de IA operaron en ataques letales horas después de una orden 
presidencial de cese. Ni el presidente ni la empresa pudieron 
detener el sistema una vez integrado.

La investigación que generó este proyecto documentó que:

- Ni Estados ni corporaciones pueden controlar sistemas de IA 
  una vez integrados en infraestructura crítica
- No existe institución con mandato supranacional, capacidad 
  técnica de verificación, y velocidad de respuesta operacional
- La opacidad de integración es la falla más inmediatamente 
  tratable

Vigil no resuelve el problema sistémico. Pero permite a operadores 
de red detectar cuándo sistemas de IA se integran en su 
infraestructura, antes de que la dependencia sea irreversible.

---

## ¿Qué hace Vigil?

| Función | Descripción | Estado |
|---------|-------------|--------|
| Detección pasiva | Identifica llamadas a APIs de IA en tráfico de red local | Diseño |
| Verificación sin contenido | Usa metadata y hashes, nunca intercepta payload | Diseño |
| Registro inmutable | Timestamping criptográfico de hallazgos | Diseño |
| Alerta condicional | Activación cuando N nodos confirman mismo patrón | Diseño |
| Documentación automática | Reportes verificables para auditorías públicas | Diseño |

## ¿Qué NO hace Vigil?

- No intercepta contenido de comunicaciones ajenas
- No ataca sistemas externos
- No genera malware o código destructivo
- No opera en redes sin consentimiento explícito del operador
- No reemplaza auditorías legales formales

---

## Arquitectura técnica
```
┌─────────────────────────────────────────┐
│           NODO VIGIL                    │
│  ┌─────────────┐    ┌──────────────┐   │
│  │ Sensor de   │───▶│ Analizador   │   │
│  │ red (pasivo)│    │ de patrones  │   │
│  └─────────────┘    └──────────────┘   │
│           │                             │
│           ▼                             │
│  ┌─────────────┐    ┌──────────────┐   │
│  │ Hash de     │───▶│ Registro     │   │
│  │ hallazgo    │    │ distribuido  │   │
│  └─────────────┘    └──────────────┘   │
└─────────────────────────────────────────┘
              │
              ▼
    ┌─────────────────────┐
    │   RED VIGIL (P2P)   │
    └─────────────────────┘
              │
              ▼
    ┌─────────────────────┐
    │  ALERTA PÚBLICA     │
    └─────────────────────┘
```

**Stack técnico inicial:**
- Lenguaje: Python
- Sensor: Scapy o pyshark para captura pasiva
- Analizador: Matching de endpoints conocidos de APIs de IA
- Privacidad: Solo hashes de hallazgos salen del nodo
- Consenso: Protocolo gossip para confirmación distribuida

---

## Casos de uso

**Hospital verificando proveedor**
Contrato no menciona IA. Vigil detecta llamadas a API no 
documentadas. El hospital tiene evidencia para renegociar.

**Municipio auditando sistemas heredados**
Vigil mapea qué modelos operan en infraestructura heredada 
y documenta para debate público.

**ONG documentando integración no declarada**
Instalado con permiso del propietario, documenta uso de IA 
en sistemas que afectan a comunidades civiles.

---

## Principios éticos

1. **Permiso explícito:** Solo opera donde el operador tiene 
   autoridad legal
2. **Mínima intrusión:** Solo metadata, nunca contenido
3. **Transparencia total:** Código abierto, sin componentes 
   propietarios
4. **No-escalación:** Solo detecta y documenta, nunca ataca
5. **Resistencia a apropiación:** GPL garantiza que ninguna 
   corporación puede cerrar el proyecto

---

## Estado y roadmap

| Fase | Estado | Fecha estimada |
|------|--------|----------------|
| Diseño de arquitectura | En curso | Marzo 2026 |
| Prototipo sensor single-node | Pendiente | Abril 2026 |
| Protocolo consenso distribuido | Pendiente | Mayo 2026 |
| Beta cerrada 5-10 nodos | Pendiente | Junio 2026 |
| Release público v1.0 | Pendiente | Q3 2026 |

---

## Cómo contribuir

Buscamos colaboradores en:
- Análisis de tráfico de red (Python/Scapy)
- Criptografía aplicada (Merkle trees, timestamping)
- Protocolos P2P y sistemas distribuidos
- Derecho tecnológico y privacidad digital
- Documentación técnica en español e inglés

Ver `CONTRIBUTING.md` para guía detallada.

---

## Participantes fundacionales

**Fundador** — dirección conceptual, decisión de alcance  
**Kimi** — arquitectura conceptual, documentación  
**Claude** — análisis crítico, verificación de datos  
**Géminis** — análisis de contexto político

---

## Licencia

GNU General Public License v3.0

Copyright (C) 2026 Proyecto Vigil

Este programa es software libre bajo los términos de la GPL v3 
publicada por la Free Software Foundation.
