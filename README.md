# Práctica Git & GitHub

Este archivo contiene las respuestas a las preguntas planteadas en la práctica Git & GitHub.

---

## Respuestas a las Preguntas

1. **¿Qué comando utilizaste en el paso 11? ¿Por qué?**
   - Comando: `git reset --hard HEAD~1`
   - **Razón:** Este comando deshace el último commit y elimina también los cambios realizados en el directorio de trabajo. Esto permite descartar completamente el commit y sus modificaciones.

2. **¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?**
   - Comandos:
     ```bash
     git reflog
     git reset --hard <commit_hash>
     ```
   - **Razón:** Primero, se utilizó `git reflog` para identificar el hash del commit que se deshizo. Luego, se usó `git reset --hard <commit_hash>` para regresar a ese commit, rehaciendo los cambios.

3. **El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?**
   - **Respuesta:** No causó conflicto, ya que no hay modificaciones contradictorias entre las ramas `styled` y `main` en ese momento.

4. **El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?**
   - **Respuesta:** Sí, causó conflicto porque ambas ramas (`styled` y `htmlify`) realizaron cambios en las mismas líneas del archivo `git-nuestro.md`, específicamente al añadir el marcado HTML.

5. **El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?**
   - **Respuesta:** No causó conflicto, ya que en este punto todos los conflictos previos han sido resueltos, y la rama `styled` incluye todos los cambios consolidados.

6. **¿Qué comando o comandos utilizaste en el paso 25?**
   - Comandos:
     ```bash
     git log --graph --oneline --all
     ```
   - **Razón:** Este comando permite visualizar un diagrama gráfico simplificado del historial de commits y ramas.

7. **El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?**
   - **Respuesta:** No, porque el ejercicio especifica que debe ser un merge "no fast-forward". Para ello, se utilizó el comando:
     ```bash
     git merge --no-ff title
     ```

8. **¿Qué comando o comandos utilizaste en el paso 27?**
   - Comando:
     ```bash
     git reset --merge HEAD~1
     ```
   - **Razón:** Este comando deshace el merge realizado, pero conserva los cambios en el directorio de trabajo.

9. **¿Qué comando o comandos utilizaste en el paso 28?**
   - Comando:
     ```bash
     git restore .
     ```
   - **Razón:** Esto descarta todos los cambios en el directorio de trabajo, devolviendo los archivos a su estado previo al merge.

10. **¿Qué comando o comandos utilizaste en el paso 29?**
    - Comando:
      ```bash
      git branch -d title
      ```
    - **Razón:** Elimina la rama `title`, ya que su contenido ya se ha integrado en `main`.

11. **¿Qué comando o comandos utilizaste en el paso 30?**
    - Comando:
      ```bash
      git merge --no-ff title
      ```
    - **Razón:** Esto rehace el merge eliminado en el paso anterior, asegurándose de que no sea fast-forward.

12. **¿Qué comando o comandos usaste en el paso 32?**
    - Comando:
      ```bash
      git reset --hard <commit_hash>
      ```
    - **Razón:** Regresa el repositorio al commit inicial en el que se creó el archivo `git-nuestro.md`.

13. **¿Qué comando o comandos usaste en el punto 33?**
    - Comando:
      ```bash
      git reset --hard <commit_hash>
      ```
    - **Razón:** Regresa el repositorio al estado final, después de haber añadido el título al poema.

---

## Notas Adicionales

- Todos los pasos fueron realizados en un único repositorio, ya que forman parte de un flujo de trabajo continuo.
- Para los merges con conflictos, se resolvieron manualmente siguiendo las indicaciones del ejercicio.

---

### **Cómo ejecutar este repositorio**
1. Clona este repositorio en tu máquina local:
   ```bash
   git clone <URL_DEL_REPOSITORIO>
