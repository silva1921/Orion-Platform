# Runbook - Comandos Básicos del Servidor

## Verificar memoria RAM

```bash
free -h
```

---

## Verificar discos

```bash
df -h
```

---

## Verificar procesos

```bash
ps aux
```

---

## Verificar puertos abiertos

```bash
ss -tulpn
```

---

## Verificar interfaces de red

```bash
ip a
```

---

## Verificar uso CPU y RAM

```bash
htop
```

---

## Actualizar paquetes

```bash
sudo apt update && sudo apt upgrade -y
```

---

## Verificar servicio SSH

```bash
sudo systemctl status ssh
```

