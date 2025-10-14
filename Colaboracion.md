
# Gestión de código por invitación

- Para equipos pequeños.
- Los desarrolladores se conocen
- 🧨 **EL colaborador puede tocar la rama principal!!**

## Cómo Invitar a colaborador

- Se accede a settings, Colaborators y se manda la invitación
- El invitado puede comprobar su correo de gitghub o en la propia
bandeja de notificaciones internas de Github


---

# Gestión de código con Pull Request 

- Para equipos medios / grandes
- El colobarorador nunca toca la rama del desarrollo principal
- 🩹Sólo las personas con permisos deniegan/aprueban los cambios
  

## 👥 Escenario

Utilizaremos un proyecto donde trabajan dos desarrolladores:

- **Desarrollador A (rmsvdp)**: Crea el repositorio y será el encargado de aprobar cambios.
- **Desarrollador B (race8086)**: Contribuye al desarrollo.

---

## 🧭 Objetivo

El proyecto se desarrollará de forma conjunta, pero el Desarrollador B propone cambios sin modificar directamente el código principal (`main`).  
El Desarrollador B, deberá hacer un FORK del proyecto principal y trabajar con él.
Para eso se usa un **Pull Request (PR)**.

---

## :gear: Flujo de Trabajo

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
2. Aparecerá un mensaje: **Compare & pull request** → clic.
3. Verifica EL SENTIDO: (`race8086:nueva-rama`) hacia `rmsvdp:main`.
4. Escribe un título y descripción.
5. Haz clic en **Create pull request** 

---

### 6. Desarrollador A revisa el Pull Request
1. Entra al repositorio original y abre la pestaña **Pull Requests**.
2. Revisa los cambios, comenta o aprueba.Click en el commit y seguir indicaciones
3. Si todo está bien, clic en **Merge pull request** → **Confirm merge**.

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

## 💡 Consejos
- Usa nombres de ramas descriptivos.
- Evita **Pull Request** grandes
- Desarrollador A puede activar **Branch Protection Rules** para exigir revisiones antes de hacer merge.
- Si el repo es **privado**, el dueño debe añadir colaboradores desde **Settings → Collaborators**.


