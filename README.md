# 📌 Meta Ads Library API - Análisis y Automatización de Anuncios en Facebook

Este proyecto permite acceder y analizar anuncios en **Facebook Ads Library** mediante la **Graph API**. Está diseñado con fines educativos y de investigación, facilitando la consulta automatizada de anuncios según criterios como país y palabras clave.

## 🚀 Características principales
✅ **Consulta automática de anuncios** en la Biblioteca de Anuncios de Facebook.
✅ **Soporte para búsqueda por palabra clave y país** (`ads_archive`).
✅ **Almacenamiento de resultados en CSV** para análisis posterior.
✅ **Uso de tokens de autenticación** para acceder a la API.
✅ **Código modular** para futuras ampliaciones o integración con otros proyectos.

## 📜 Política de Privacidad
Este proyecto no recopila, almacena ni distribuye información personal de los usuarios. Toda la información consultada proviene de la API pública de la Biblioteca de Anuncios de Facebook y es utilizada únicamente con fines de análisis e investigación.

## 📌 Requisitos
Antes de ejecutar el proyecto, asegúrate de cumplir con los siguientes requisitos:
- Tener una cuenta en **Meta Developer** con permisos de `ads_read` activados.
- Un **token de acceso** válido para interactuar con la API de Meta.
- **Python 3.x** instalado en tu sistema.

## 🔑 Configuración del Token
Para autenticarte en la API, es necesario crear un archivo en la raíz del proyecto:
1. **Crea un archivo llamado `key.txt`**
2. **Dentro del archivo, coloca únicamente tu token de acceso de Meta**.

**Ejemplo del archivo `key.txt`:**
```
EAABsbCS1i...TuTokenAqui...
```
⚠ **No compartas tu token con nadie, ya que es privado y puede dar acceso a tu cuenta.**

## 📦 Instalación y Uso
### 1️⃣ Clonar el repositorio
```bash
git clone https://github.com/tuusuario/meta-ads-library.git
cd meta-ads-library
```

### 2️⃣ Instalar dependencias
```bash
pip install -r requirements.txt  # Si es necesario
```

### 3️⃣ Ejecutar una búsqueda
Ejemplo para buscar anuncios en El Salvador con la palabra clave "Chivo":
```python
from buscador import EjecutarBusqueda

EjecutarBusqueda("SV", "Chivo")
```
Esto generará un archivo **`resultados.csv`** con los anuncios encontrados.

## 🔍 Probando la API Manualmente
Si deseas verificar que tu token tiene los permisos adecuados, puedes ejecutar la siguiente consulta en **Graph API Explorer**:
```bash
GET https://graph.facebook.com/v18.0/me/permissions?access_token=TU_TOKEN
```
Si `ads_read` está activado, deberías ver algo como esto:
```json
{
  "data": [
    { "permission": "ads_read", "status": "granted" },
    { "permission": "public_profile", "status": "granted" }
  ]
}
```

## 🛠️ Futuras mejoras
- Implementar almacenamiento de datos en bases de datos SQL.
- Crear una interfaz gráfica para facilitar el uso.
- Automatizar búsquedas periódicas y generación de reportes.

---

📌 **Proyecto de código abierto con fines educativos.** 🚀

