
# 🛡️ Mini SOC Casero con Suricata, Zeek y EveBox  
### *Caso de Estudio Profesional – Portafolio de Ciberseguridad*

---

<p align="center">
  <img src="https://img.shields.io/badge/SOC-OpenSource-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/Threat_Detection-Suricata-orange?style=for-the-badge">
  <img src="https://img.shields.io/badge/NSM-Zeek-red?style=for-the-badge">
  <img src="https://img.shields.io/badge/SIEM-EveBox-green?style=for-the-badge">
</p>

---

## 🚀 Visión del Proyecto

Este proyecto demuestra cómo construir un **Mini SOC profesional**, completamente funcional y basado en herramientas **open-source**.  
Combina monitoreo de red, detección de intrusiones, análisis inteligente y visualización de eventos en tiempo real.

Es un proyecto ideal para:

✔️ Portafolios profesionales  
✔️ Demostraciones técnicas  
✔️ Pruebas de concepto de SOC  
✔️ Formación en análisis de tráfico y amenazas  

---

## 🧩 Arquitectura General

El sistema integra cuatro componentes clave:

```
 ┌────────────┐      ┌──────────────┐      ┌──────────────┐
 │  Suricata  │ ---> │    EveBox    │ ---> │   Dashboards  │
 └────────────┘      └──────────────┘      └──────────────┘
        │                      
        ▼                      
 ┌────────────┐
 │    Zeek    │ ----> Logs NSM
 └────────────┘
        │                      
        ▼                      
 ┌────────────────────────────┐
 │ Python + IA (Automación)   │
 └────────────────────────────┘
```

Cada componente aporta visibilidad distinta: reglas, comportamiento, análisis, correlación y reportes automáticos.

---

## ⚙️ Componentes Utilizados

| Herramienta | Rol | Beneficio |
|------------|------|-----------|
| **Suricata** | IDS | Detección basada en firmas, alertas precisas |
| **Zeek** | NSM | Logs profundos de DNS, HTTP, SSL, conexiones… |
| **EveBox** | SIEM ligero | Visualización y búsqueda avanzada |
| **Python + IA** | Automatización | Reportes ejecutivos automáticos |

---

## 🔧 Instalación Rápida (Comandos Clave)

### 🟥 Suricata
```bash
sudo apt update && sudo apt upgrade -y
sudo apt install -y suricata
sudo suricata-update
```

---

### 🟦 Zeek
```bash
sudo apt install -y zeek
sudo zeek -i enp0s3
```

---

### 🟩 EveBox
```bash
wget https://evebox.org/files/evebox-latest-amd64.deb
sudo dpkg -i evebox-latest-amd64.deb
sudo evebox server -D -e /var/log/suricata/eve.json
```

---

## 🤖 Automatización con IA  
El sistema ejecuta un script en Python que:

✔️ Analiza `eve.json`  
✔️ Resume actividad sospechosa  
✔️ Detecta patrones claves  
✔️ Genera informes ejecutivos profesionales  
✔️ Inserta el informe como evento dentro del SOC  

Ejemplo de hallazgo crítico detectado:

> **GPL ATTACK_RESPONSE – id check returned root**  
> Señal de posible compromiso con privilegios ROOT  
> → Investigación inmediata recomendada

---

## 🧪 Desafío Técnico Resuelto

El proyecto resolvió un problema común:  
**Identificar la interfaz real del tráfico en entornos VirtualBox (Bridge + NAT).**

Solución implementada:

```bash
sudo tcpdump -i <interfaz>
```

Tras pruebas en múltiples interfaces, la correcta fue `br0`, logrando captura estable y análisis continuo.

---

## 🏆 Resultado Final

Este Mini SOC proporciona:

✔️ Detección de intrusiones en tiempo real  
✔️ Visibilidad profunda del comportamiento de red  
✔️ Dashboards inmediatos gracias a EveBox  
✔️ Automatización Inteligente con IA  
✔️ Arquitectura modular y profesional  

---

## 📁 Archivos Incluidos

- `Mini_SOC_Case_Study.pdf` — Documento técnico completo  
- `README.md` — Documentación del repositorio  
- Scripts (opcional si los agregas luego)

---

## ⭐ Recomendación para tu Portafolio

Este proyecto es **altamente atractivo para reclutadores y empresas** porque demuestra:

- Conocimientos reales de SOC
- Capacidad de integrar herramientas
- Automación con IA
- Análisis de tráfico de red
- Documentación clara y profesional

---

## 🖤 Si deseas puedo crear también:

🎨 Un logo oficial del proyecto  
📊 Un dashboard adicional  
🐍 Un script Python más completo  
📁 Estructura profesional de repositorio  
📘 Un PDF extra estilo "whitepaper"  

Solo dímelo 😉  
