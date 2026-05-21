# Server Baseline

## Información General

Servidor utilizado para el proyecto Orion Platform.

## Objetivo

Servidor on-premise destinado al aprendizaje práctico de:
- DevOps
- Observabilidad
- CI/CD
- Docker
- Networking
- Seguridad
- Infraestructura moderna


# Especificaciones del Entorno de Servidor

Este documento detalla la configuración de hardware, almacenamiento y red del nodo local.

## 1. Sistema Operativo
* **OS:** Ubuntu 24.04.4 LTS (Noble Numbat)
* **Usuario principal:** `silva19`

## 2. Memoria RAM y Swap (`free -h`)

| Tipo | Total | Usado | Libre | Compartido | Búfer/Caché | Disponible |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Memoria** | 10 Gi | 641 Mi | 8.9 Gi | 1.5 Mi | 1.4 Gi | 9.0 Gi |
| **Swap** | 4.0 Gi | 0 B | 4.0 Gi | — | — | — |

## 3. Almacenamiento en Disco (`df -h`)

| Sistema de Archivos | Tamaño | Usado | Disp. | Uso % | Montado en | Nota |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| `/dev/mapper/ubuntu--vg-ubuntu--lv` | **98G** | **7.2G** | **86G** | **8%** | `/` | Raíz principal (LVM) |
| `/dev/sda2` | 2.0G | 201M | 1.6G | 11% | `/boot` | Arranque del sistema |
| `/dev/sda1` | 1.1G | 6.2M | 1.1G | 1% | `/boot/efi` | Partición EFI |

> *Nota: Los sistemas de archivos virtuales (`tmpfs`, `efivarfs`) se han omitido para mayor claridad, operando todos por debajo del 1% de uso.*

## 4. Configuración de Red (`ip a`)

* **Interfaz de Loopback (`lo`):** `**.*.*.*/8`
* **Interfaz Cableada (`eno1`):** `DOWN` (Desconectada)
* **Interfaz Inalámbrica (`wlo1`):** `UP` (Activa)
  * **IP Privada (IPv4):** `***.***.*.*/24`
  * **MAC Address:** `**:**:**:**:db:**`

---

<details>
<summary><b>Click aquí para ver los logs originales de la terminal</b></summary>

```bash
# free -h
Mem:            10Gi       641Mi       8,9Gi       1,5Mi       1,4Gi         9Gi
Swap:          4,0Gi          0B       4,0Gi

# df -h
Filesystem                         Size  Used Avail Use% Mounted on
/dev/mapper/ubuntu--vg-ubuntu--lv   98G  7,2G   86G   8% /
/dev/sda2                          2,0G  201M  1,6G  11% /boot
/dev/sda1                          1,1G  6,2M  1,1G   1% /boot/efi

# ip a
3: wlo1: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc noqueue state UP group default qlen 1000
    inet *.*.*.*/24 metric 600 brd *.*.*.* scope global dynamic wlo1

# Herramientas Operativas Instaladas

- git
- curl
- wget
- vim
- nano
- htop
- jq
- tree
- net-tools
- fail2ban
- unzip

# Objetivo Arquitectónico Inicial

La plataforma estará compuesta por:

- Frontend Next.js
- Backend FastAPI
- PostgreSQL
- Redis
- NGINX
- Docker
- Grafana
- Prometheus
- Loki

---

# Notas Operativas

Documentación creada durante Fase 1:
Foundation & Server Setup.
