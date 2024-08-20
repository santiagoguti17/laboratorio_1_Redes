# laboratorio_1_Redes
# README: Configuración de Red y Simulación

## 1. Comprensión de los Elementos de la Red

### Router Inalámbrico (WRT300N Wireless Router)
- **Función Principal:** Es el núcleo de la red WLAN, encargado de enrutar el tráfico entre dispositivos locales e Internet. Posee dos direcciones IP: una para la red local (192.168.0.1) y otra para la red externa (208.67.220.1), permitiéndole actuar como intermediario entre ambas.
- **Capacidades:** Ofrece conectividad inalámbrica para dispositivos móviles y cableada para dispositivos como la PC y la laptop, reflejando un escenario común en un hogar moderno.

### Dispositivos en la red WLAN
- **PC, Laptop, Tablet, Smartphone:** Cada dispositivo tiene una dirección IP estática asignada manualmente, lo que asegura una IP fija y evita conflictos de direcciones. Sin embargo, en redes más grandes, la asignación manual puede ser tediosa, recomendándose la implementación de DHCP para simplificar el proceso.

### Cable Modem (Cable Modem0)
- **Función:** Conecta la red local con el proveedor de servicios de internet (ISP). Convierte las señales digitales del router en señales aptas para transmisión a través de la red del ISP.

### Cloud (Cloud0)
- **Simulación de Internet:** Representa la conexión a Internet en la simulación, conectando la red doméstica al servidor remoto de DisneyPlus, simulando el tráfico que pasaría por la red pública.

### Servidor (Server-PT)
- **Servidor DNS y HTTP:** Configurado para manejar:
  - **DNS (Domain Name System):** Resuelve el dominio disneyplus.com en una dirección IP (208.67.220.220), facilitando que los dispositivos locales encuentren el servidor web.
  - **HTTP (Hypertext Transfer Protocol):** Proporciona contenido web a los dispositivos clientes al acceder a disneyplus.com.

## 2. Tipos de Redes

### LAN (Red de Área Local)
- **Características:** Conecta dispositivos dentro de un área limitada, como un hogar. Todos los dispositivos en la red azul están conectados dentro de la misma LAN, permitiendo una comunicación rápida y eficiente.
- **Ventajas:** Facilita el compartir recursos como impresoras, archivos y la conexión a Internet.

### WLAN (Red de Área Local Inalámbrica)
- **Características:** Extiende los principios de una LAN pero sin cables, ideal para hogares con dispositivos móviles.
- **Beneficios:** Proporciona flexibilidad y movilidad, permitiendo el acceso a Internet desde cualquier parte de la casa.

### WAN (Red de Área Amplia)
- **Características:** Conecta múltiples redes LAN a través de grandes distancias. En la simulación, la WAN conecta la red local con el servidor de DisneyPlus a través del Cloud y el Cable Modem.
- **Importancia:** Permite el acceso a recursos y servicios en Internet, como DisneyPlus.

## 3. Topologías de Red

### Topología Estrella
- **Características:** Todos los dispositivos están conectados a un punto central (el router inalámbrico). Los datos pasan por el router antes de llegar a su destino.
- **Ventajas:** 
  - **Facilidad de administración:** Un dispositivo con problemas no afecta a los demás.
  - **Escalabilidad:** Es fácil agregar más dispositivos.
- **Desventajas:** Si el router falla, toda la red pierde conectividad.

### Otras Topologías
- **Bus, Anillo, Malla:** Aunque existen otras topologías, la estrella es la más práctica para un hogar debido a su simplicidad y eficiencia.

## 4. Arquitecturas y Servicios

### DNS (Domain Name System)
- **Función:** Traduce nombres de dominio en direcciones IP, esencial para la navegación web.
- **Implementación:** El servidor DNS resuelve disneyplus.com a 208.67.220.220, permitiendo la conexión sin conocer la IP exacta.

### DHCP (Dynamic Host Configuration Protocol)
- **Función:** Asigna direcciones IP dinámicamente, eliminando la necesidad de configurarlas manualmente. Es útil en redes más grandes o con dispositivos que se conectan y desconectan con frecuencia.
- **Recomendación:** Considerar implementar DHCP para mejorar la escalabilidad y gestión de la red.

### Arquitectura Cliente-Servidor
- **Modelo:** Los dispositivos del hogar actúan como clientes que solicitan recursos (como contenido de DisneyPlus) desde un servidor central.
- **Beneficios:** Centraliza la gestión de recursos y permite a los clientes acceder sin necesidad de almacenar grandes cantidades de datos localmente.

## 5. Protocolos y Modelos

### TCP/IP (Protocolo de Control de Transmisión/Protocolo de Internet)
- **Función:** Permite la comunicación en redes como Internet. TCP garantiza la transmisión fiable de datos, mientras que IP se encarga de enrutar los datos.
- **Aplicación:** TCP/IP asegura la correcta transmisión de datos entre el cliente y el servidor de DisneyPlus.

### Modelo OSI (Open Systems Interconnection)
- **Capas Relevantes:**
  - **Capa Física:** Conexiones físicas y medios de transmisión.
  - **Capa de Enlace de Datos:** Transmisión de datos entre dos nodos conectados.
  - **Capa de Red (IP):** Maneja direcciones IP.
  - **Capa de Transporte (TCP):** Asegura la transmisión confiable de datos.
  - **Capa de Aplicación (HTTP):** Maneja los servicios de red utilizados por los usuarios finales.

## Recomendaciones Adicionales
- **Seguridad:** Implementar cifrado WPA2 en el router inalámbrico para proteger la WLAN.
- **Monitoreo de Red:** Utilizar herramientas de monitoreo de tráfico para asegurar un rendimiento óptimo de la red.
