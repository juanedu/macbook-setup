# macbook-setup

## MBP Initial Setup

Durante la configuracion inicial, conectarse al wifi de turno e ingresar el Apple ID cuando sea necesario.

Setear huellas para Touch ID (opcional si la MB cuenta con el dispositivo)

Omitir configuracion de Apple Pay

Luego de reinstalar macOS, comprobar que no haya actualizaciones pendientes del SO.
- System Preferences - Software Update

Configurar TimeMachine

## Configuración 

TODO: Automatizar con defaults y dotfiles

Deshabilitar Photos sync hacia iCloud
- System Preferences - Apple ID - iCloud - Photos

Finder:
- Preferences - Sidebar - habilitar Home folder, ocultar Tags
- View - Show status bar
- Shift+Cmd+. - para mostrar/ocultar archivos ocultos
- Mantener Option - muestra el path bar

Trackpad:
- Tap to Click
- App exposé

Accessibility:
- Pointer control - Tracked options - Enable dragging (opcional)

Security & Privacy:
- Require password immediately…
- Advanced… - Require an admin pwd…
- Firewall - Turn On firewall

Dock & Menu bar:
- Auto hide and show the Dock

Keyboard:
- Touch Bar shows function keys
  - Si no tiene Touch Bar: Use F1, F2, etc. as standard function keys
- Ajustar Key repeat (fast) y Delay until repeat (short)
- Text - Deshabilitar “Correct spelling automatically”
- Cambiar double (") y single quotes (')

Display:
- Night Shift - Sunset to Sunrise

Time Machine:
- Show Time Machine in menu bar

-----

Instalar HomeBrew (http://brew.sh)

Instalar ansible
- brew install ansible

TODO: Resolver provisionamiento de keys ssh para clonar repos. Quizas haya que hacer dos corridas de ansible: una para bajar los config files (ej: dropbox o icloud), y otra para ejecutar las tareas de configuracion de las apps copiando los archivos

Crear una carpeta 'code' en el home y clonar este repositorio
- git clone https://github.com/juanedu/macbook-setup.git

ansible-galaxy install -r requirements.yml
ansible-playbook main.yml --ask-become-pass


Instalar iTerm2 (vía brew)
- Closing - deshabilitar confirmaciones de Quit
- Duplicar el profile default y hacerlo nuevo default
    - Windows - ajustar ancho y alto
    - Text - Underline cursor + Blinking



——---

Webs:

https://nartc.me/blog/macos-dev-setup
https://sourabhbajaj.com/mac-setup/
https://www.robinwieruch.de/mac-setup-web-development/

