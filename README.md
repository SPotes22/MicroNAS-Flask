#  microNAS

**microNAS** es un servidor NAS (Network Attached Storage) ligero desarrollado en Python con Flask. Permite subir, listar, leer y eliminar archivos según el rol del usuario, ideal para proyectos académicos o pruebas en red local. solo redirigiendo un puerto , (Por defecto 8000)

---

## 🚀 Instrucciones de instalación

1. **Clona el repositorio o descarga el `.zip`:**

```bash
git clone https://github.com/tuusuario/microNAS.git
cd microNAS
```

2. **Crea una carpeta llamada `archivos` en la raíz del proyecto:**

```bash
mkdir archivos
```

3. **Crea un entorno virtual (opcional pero recomendado):**

```bash
python -m venv venv
```

> Puedes llamar la carpeta `venv` para que esté excluida automáticamente por `.gitignore`.

4. **Activa el entorno virtual:**

- En Linux/macOS:
  ```bash
  source venv/bin/activate
  ```
- En Windows:
  ```bash
  venv\Scripts\activate
  ```

5. **Instala las dependencias:**

```bash
pip install -r requirements.txt
```

6. **Ejecuta la aplicación:**

```bash
python app.py
```

---

## Roles y Credenciales

| Rol      | Permisos                     | Usuario    | Contraseña   |
|----------|------------------------------|------------|--------------|
| Admin    | Subir, listar, borrar        | `admin`    | `admin123`   |
| Cliente  | Subir y listar               | `cliente`  | `cliente123` |
| Usuario  | Solo puede leer archivos     | `usuario`  | `usuario123` |

---


# Futuras Versiones (ON DEVELOPMENT)

## 🗃️ Organización del sistema de archivos

microNAS soporta dos modelos opcionales para la gestión de archivos:

### 1. Sistema por carpetas raíz (por usuario)
```
/archivos/
├── admin/
├── cliente/
└── usuario/
```

- Se crea una subcarpeta por usuario para mantener su espacio privado o compartido según configuración.

### 2. Sistema basado en nodos y árboles (experimental)
- Organización jerárquica de archivos en forma de árbol.
- Ideal para estructuras más complejas o visualización en GUI.
- Puedes extender este modelo a futuro con una base de datos de nodos (JSON o SQL).

---

##  Notas adicionales

- El entorno virtual `venv/` está excluido por defecto gracias al archivo `.gitignore`.
- El sistema incluye autenticación segura basica todavía (bycrypt).
- Se recomienda no subir archivos sensibles.

---

## 🧾 Licencia

Este proyecto está licenciado bajo una Licencia derivada de GNU GPLv3.

> Todo software, modificación o herramienta que derive de este código también deberá mantenerse como **software libre y abierto**, de acuerdo con la filosofía GNU.

Consulta el archivo [LICENSE](LICENSE) incluido para más detalles.

---

## ✨ Créditos

Desarrollado por Santiago Potes Giraldo.  
Proyecto educativo y de uso local.
