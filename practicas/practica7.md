## Planteamiento del escenario

Utilizaremos un proyecto donde trabajan dos desarrolladores:

- **Desarrollador A (rmsvdp)**: Crea el repositorio y sería el encargado de aprobar cambios.
- **Desarrollador B (race8086)**: Contribuye al desarrollo.

---

## 🥇 Objetivo

El proyecto se desarrolla de forma conjunta, pero el Desarrollador B propone cambios sin modificar directamente el código principal (`main`).  
El Desarrollador B, debería hacer un **fork** del proyecto principal y trabajar con él. Cuando esté listo para subir el nuevo código, hará uso de la opción  Pull Request de gitHub.

---

## :gear: Ejemplo de Flujo de Trabajo

### 1. Inicio del desarrollo
1. Desarrollador A crea el proyecto, por ejemplo: `teamwork`.
2. Marca **Public** y crea el repositorio con un `README.md`.
3. Desarrollador B , cra **Fork** desde el repositorio del Desarrollador A
4. Clona su fork localmente:
   ```bash
   git clone https://github.com/race8086/teamwork.git
   cd proyecto-demo
   ```
---

### 2. Crear una rama de trabajo
> Nunca trabajes directamente en `main`.

1. Crea una nueva rama:
   ```bash
   git branch nueva-rama
   git checkout nueva-rama
   ```
2. Realiza los cambios necesarios.
3. Guarda y haz commit:
   ```bash
   git add .
   git commit -m "Agrego nueva funcionalidad"
   ```
---

### 3. Subir los cambios al fork
1. Sube la nueva rama:
   ```bash
   git push origin nueva-rama
   ```
---

### 4. Crear el Pull Request
1. En GitHub, entra al repositorio  (`race8086/teamwork`).
2. Aparecerá un mensaje: **Compare & pull request** 鈫?clic.
3. Verifica EL SENTIDO: (`race8086:nueva-rama`) hacia `rmsvdp:main`.
4. Escribe un t铆tulo y descripci贸n.
5. Haz clic en **Create pull request** 

---

### 6. Desarrollador A revisa el Pull Request
1. Entra al repositorio original y abre la pesta帽a **Pull Requests**.
2. Revisa los cambios, comenta o aprueba.Click en el commit y seguir indicaciones
3. Si todo est谩 bien, clic en **Merge pull request** 鈫?**Confirm merge**.

---

### 7. Mantener el fork actualizado

Si vamos a continuar contribuyendo, mantenemos actualizado nuestro fork
```bash
# Conectar el repositorio original como "upstream" (solo una vez)
git remote add upstream https://github.com/rmsvdp/teamwork.git
# Obtener los cambios del original
git fetch upstream
# Pasarse a la rama main de mi fork local
git checkout main
git merge upstream/main
# Subo los cambios al fork remoto
git push origin main
```

---
