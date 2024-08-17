## Conectar Dispositivo Bluetooth desde la Terminal

1. **Iniciar Servicio Bluetooth:**
   ```bash
   sudo systemctl start bluetooth
   sudo systemctl enable bluetooth
   ```

2. **Abrir `bluetoothctl`:**
   ```bash
   bluetoothctl
   ```

3. **Habilitar el Bluetooth:**
   ```bash
   power on
   ```

4. **Hacer el Adaptador Detectable:**
   ```bash
   discoverable on
   ```

5. **Buscar Dispositivos:**
   ```bash
   scan on
   ```

6. **Emparejar y Conectar:**
   ```bash
   pair XX:XX:XX:XX:XX:XX
   connect XX:XX:XX:XX:XX:XX
   ```

7. **Confiar en el Dispositivo:**
   ```bash
   trust XX:XX:XX:XX:XX:XX
   ```

8. **Finalizar Escaneo:**
   ```bash
   scan off
   ```

9. **Salir de `bluetoothctl`:**
   ```bash
   exit
   ```
