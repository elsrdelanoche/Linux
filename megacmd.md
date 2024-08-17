## Mega-cmd en Linux

**Mega-cmd** es una herramienta de línea de comandos para interactuar con el servicio de almacenamiento en la nube [MEGA](https://mega.io). Ofrece comandos para manejar archivos, directorios, y realizar tareas automatizadas desde la terminal en Linux.

### Instalación

1. **Instalación en Arch Linux:**
   ```bash
   sudo pacman -S megacmd
   ```

2. **Instalación en Ubuntu/Debian:**
   ```bash
   sudo apt update
   sudo apt install megacmd
   ```

### Uso Básico

1. **Iniciar Mega-cmd:**
   ```bash
   mega-cmd
   ```

2. **Iniciar Sesión:**
   ```bash
   mega-login TU_EMAIL TU_CONTRASEÑA
   ```

3. **Subir un Archivo:**
   ```bash
   mega-put archivo.txt /RutaRemota
   ```

4. **Descargar un Archivo:**
   ```bash
   mega-get /RutaRemota/archivo.txt
   ```

5. **Listar Archivos:**
   ```bash
   mega-ls /RutaRemota
   ```

6. **Sincronización:**
   ```bash
   mega-sync /RutaLocal /RutaRemota
   ```

7. **Salir de Mega-cmd:**
   ```bash
   exit
   ```

### Funcionalidades Avanzadas

- **Automatización de tareas**: Permite la programación de transferencias y sincronizaciones automáticas.
- **Integración de Scripts**: Mega-cmd se puede utilizar dentro de scripts bash para automatizar procesos más complejos.

### Documentación

Para más detalles, puedes consultar la [documentación oficial de Mega-cmd](https://github.com/meganz/MEGAcmd).
