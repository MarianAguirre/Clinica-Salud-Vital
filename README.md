# Red del Caso Práctico 1: Clínica Salud Vital

---

## 🏥 Descripción General

La **Clínica Salud Vital** es una institución médica de tamaño reducido que atiende pacientes con un enfoque moderno, apoyándose en tecnologías para mejorar la gestión y seguridad de la información clínica. El área de Tecnologías de la Información (TI) implementa y mantiene un sistema electrónico de historial clínico y citas, el cual debe estar disponible tanto localmente como mediante acceso remoto seguro.

---

## 📦 Contenido

- [Objetivos de la Red](#objetivos-de-la-red)
- [Departamentos](#departamentos)
- [Direcciones IP y Subredes](#direcciones-ip-y-subredes)
- [Roles e Integrantes](#roles-e-integrantes)
- [Riesgos a Evaluar](#riesgos-a-evaluar)

---

## 🎯 Objetivos de la Red

- Implementar una **topología eficiente y segura** que conecte todas las áreas de la clínica.
- Establecer un **servidor local** que contenga la base de datos de pacientes y funcione como centro de almacenamiento del sistema clínico.
- Garantizar **acceso remoto cifrado** para médicos desde ubicaciones externas autorizadas.
- Implementar **mecanismos de respaldo semanal automatizados**.
- Aplicar medidas de seguridad que minimicen riesgos como accesos no autorizados o pérdida de información.

---

## 🧩 Departamentos

### 🖥️ Desarrollo
- Encargado del mantenimiento del sistema electrónico de historial clínico y citas.
- Cuenta con acceso al servidor para implementar actualizaciones.

### 🛠️ Soporte Técnico
- Brinda mantenimiento a los dispositivos de red y estaciones de trabajo.
- Supervisa la conectividad interna y el acceso remoto.

### 🧾 Administración
- Accede al sistema clínico para la gestión de agendas, altas, y cobros.
- No tiene privilegios sobre el servidor, pero requiere conectividad estable.

---

## 🌐 Direcciones IP y Subredes

### Subredes Establecidas (Ejemplo)

| Subred               | Rango IP             | Departamento    | VLAN |
|----------------------|----------------------|------------------|------|
| 192.168.10.0/24      | 192.168.10.1 - .254  | Administración   | 10   |
| 192.168.20.0/24      | 192.168.20.1 - .254  | Soporte Técnico  | 20   |
| 192.168.30.0/24      | 192.168.30.1 - .254  | Desarrollo       | 30   |
| 192.168.100.0/30     | 192.168.100.1 - .2   | Servidor Local   | 99   |
| 192.168.200.0/30     | 192.168.200.1 - .2   | Enlace a Router  | N/A  |

### Servidor Local

- IP: `192.168.100.2`
- Servicios: Base de Datos, Sistema Clínico, Respaldos

---

## 👥 Roles e Integrantes

| Nombre             | Rol                    | Actividad Principal                                 |
|--------------------|------------------------|-----------------------------------------------------|
| Daniel         | Admin de Red           | Diseño y configuración de la red                    |
| Cristo Fer       | Especialista en Seguridad | Implementación de firewalls y controles de acceso |
| Trabajador anonimo    | Técnico Soporte        | Configuración de dispositivos y solución de fallos |
| Marian       | Desarrolladora         | Gestión del sistema clínico                        |

---

## ⚠️ Riesgos a Evaluar

1. **Acceso no autorizado a datos médicos sensibles**  
   ➤ Implementar ACLs, VLANs, y autenticación robusta (VPN, credenciales seguras).

2. **Pérdida de información por fallos del servidor**  
   ➤ Establecer copias de seguridad automáticas y redundancia local.

3. **Ataques de ransomware o malware**  
   ➤ Uso de firewalls, actualizaciones periódicas y capacitación a usuarios.

---

## 📸 Captura de la Infraestructura en Packet Tracer

![image](https://github.com/user-attachments/assets/17394d18-1718-459d-ac43-1b05eb53397f)


---

## 📂 Archivos del Proyecto

- `topologia-clinica-salud-vital.pkt`
- `configuracion-switches.txt`
- `configuracion-router.txt`
- `README.md`

---

## 📢 Notas Finales

Este proyecto refleja una implementación básica pero segura y funcional de una clínica pequeña que puede escalarse a futuro con más servicios, nuevos departamentos o incluso integración con sistemas de salud externos.

---

