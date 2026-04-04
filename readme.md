# Andes Tech

Repositorio de charlas, workshops y material compartido en los eventos de Andes Tech.

---

## Sobre Andes Tech

Andes Tech es una comunidad tecnológica de Mendoza que organiza encuentros, charlas y eventos para conectar profesionales, estudiantes y empresas del ecosistema tech.

---

## Contenido

En este repositorio vas a encontrar:

* Presentaciones (slides)
* Ejemplos de código
* Recursos y documentación
* Material complementario de las charlas

---

## Temáticas

Las charlas abarcan distintas áreas de tecnología:

* Infraestructura y Redes
* Desarrollo de Software
* Cloud y DevOps
* Inteligencia Artificial
* Blockchain y Web3
* Seguridad Informática

---

## Cómo subir tu charla (Paso a paso)

Si participaste en un evento de Andes Tech y querés compartir tu material, seguí estos pasos:

### 1. Hacer un fork del repositorio

Ingresá a este repositorio en GitHub y hacé clic en el botón **Fork** (arriba a la derecha).
Esto va a crear una copia del repositorio en tu cuenta.

---

### 2. Clonar tu fork en tu máquina

Abrí una terminal y ejecutá:

```bash
git clone https://github.com/TU-USUARIO/andestech-talks.git
cd andestech-talks
```

Reemplazá `TU-USUARIO` por tu usuario de GitHub.

---

### 3. Crear una carpeta para tu charla

Dentro del repositorio, creá una carpeta con un nombre claro y ordenado:

```bash
mkdir -p charlas/2026-03-devcafe-nombre-charla
```

Ejemplo:

```
charlas/2026-03-devcafe-llm-101/
```

Formato recomendado:

```
charlas/AÑO-MES-evento-nombre-charla
```

---

### 4. Subir el contenido de tu charla

Dentro de esa carpeta podés incluir:

* Slides (PDF, PPT, etc.)
* Código fuente
* Archivos de ejemplo
* Un archivo `README.md` explicando brevemente la charla

Ejemplo de estructura:

```
charlas/2026-03-devcafe-llm-101/
├── slides.pdf
├── codigo/
└── README.md
```

---

### 5. Agregar y commitear los cambios

Desde la terminal:

```bash
git add .
git commit -m "Agrega charla: nombre de la charla"
```

---

### 6. Subir los cambios a tu repositorio

```bash
git push origin main
```

---

### 7. Crear un Pull Request

1. Ingresá a tu repositorio en GitHub
2. Hacé clic en **"Compare & pull request"**
3. Verificá los cambios
4. Enviá el Pull Request al repositorio original de Andes Tech

---

## Eventos

Organizamos encuentros de forma regular:

* /birras → Infraestructura, redes y telco
* devcafé → Desarrollo de software
* Blockchain → Web3 y crypto
* Andes Tech Legal → Derecho y tecnología

---

## Más información

* Web: https://andestech.xyz
* Comunidad: Mendoza, Argentina
