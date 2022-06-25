# uds-docs

Notas sobre UDS en macOS.

1. Instalar el cliente de UDS en macOS siguiendo
   la [documentación oficial](https://www.udsenterprise.com/media/filer_public/cb/da/cbda627f-61db-4b83-a1e1-6c701c7787dd/habilitar_rdp_desde_macos_-_uds_enterprise_30.pdf).

    ```
    brew install --cask xquartz
    brew install freerdp
    ```

2. Problema con `freerdp` y el permiso para el
   micrófono: [Crash on macOS Monterey · Issue #7791 · FreeRDP/FreeRDP · GitHub](https://github.com/FreeRDP/FreeRDP/issues/7791).

3. Desactivar SIP en el
   Mac: [How to disable SIP in new Apple Silicon Macs (Monterey)](https://www.alejandrofanjul.com/how-to-disable-sip-in-new-apple-silicon-macs-monterey/).

4. Darle permisos de acceso al micrófono al cliente de UDS
   usando [GitHub - DocSystem/tccutil: A macOS Permissions manager](https://github.com/DocSystem/tccutil).

    ```
    git clone https://github.com/DocSystem/tccutil.git
    
    cd tccutil
    
    sudo python tccutil.py -e --microphone -p /Applications/UDSClient.app
    ```

   > A partir de este momento el cliente de UDS se debería abrir con normalidad.
   
5. Reactivar SIP en el Mac.
