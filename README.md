# macbook-setup

## MBP Initial Setup

TODO: Automatizar configuración de apps (ansible)

TODO: ansible o homebrew para automatizar configuración? Que se necesita instalar primero para automatizar lo mas posible?

INFO: python3 ya esta incluido en macOS.

## Configuración 

Setear huellas para Touch ID

Configurar TimeMachine

Deshabilitar Photos sync hacia iCloud

Finder:
- Preferences - Sidebar - habilitar Home folder, ocultar Tags
- View - Show status bar
- Shift+Cmd+. - para mostrar/ocultar archivos ocultos
- Mantener Option - muestra el path bar

Trackpad:
- Tap to Click
- App exposé

Accessibility:
- Pointer control - Tracked options - Enable dragging

Security & Privacy:
- Require password immediately…
- Advanced… - Require an admin pwd…
- Firewall - Turn On firewall

Dock & Menu bar:
- Auto hide and show the Dock

Keyboard:
- Touch Bar shows function keys
- Ajustar Key repeat (fast) y Delay until repeat (short)
- Text - Deshabilitar “Correct spelling automatically”
- Cambiar double (") y single quotes (')

Display:
- Night Shift - Sunset to Sunrise

-----

TODO: Pasos para instalar ansible

instalar xcode-select
instalar pip3
instalar ansible

export PATH="$HOME/Library/Python/3.8/bin:/opt/homebrew/bin:$PATH"
sudo pip3 install --upgrade pip
pip3 install ansible

git clone del repo

ansible-galaxy install -r requirements.yml
ansible-playbook main.yml --ask-become-pass

——---

Instalar HomeBrew (http://brew.sh)

Instalar iTerm2 (vía brew)
- Closing - deshabilitar confirmaciones de Quit
- Duplicar el profile default y hacerlo nuevo default
    - Windows - ajustar ancho y alto
    - Text - Underline cursor + Blinking

Instalar python + ansible
- brew install python ansible

——---

Webs:

https://nartc.me/blog/macos-dev-setup
https://sourabhbajaj.com/mac-setup/
https://www.robinwieruch.de/mac-setup-web-development/

