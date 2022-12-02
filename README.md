# macbook-setup

## MBP Initial Setup

Durante la configuracion inicial, conectarse al wifi de turno e ingresar el Apple ID cuando sea necesario.

Setear huellas para Touch ID (opcional si la MB cuenta con el dispositivo)

Omitir configuracion de Apple Pay

Luego de reinstalar macOS, comprobar que no haya actualizaciones pendientes del SO.
- System Preferences - Software Update
- System Preferences - General - Software Update (<- Ventura)

Configurar TimeMachine

Una vez que este configurado iCloud Drive, 

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
- Tap to Click (ver defaults)
- App exposé

Accessibility:
- Pointer control - Tracked options - Enable dragging (opcional)

Security & Privacy:
- Require password immediately…
- Advanced… - Require an admin pwd…
- Firewall - Turn On firewall

Dock & Menu bar:
- Auto hide and show the Dock (ver defaults)

Keyboard:
- Touch Bar shows function keys
  - Si no tiene Touch Bar: Use F1, F2, etc. as standard function keys
- Ajustar Key repeat (fast) y Delay until repeat (short) (ver defaults)
- Text - Deshabilitar “Correct spelling automatically” (ver defaults)
- Cambiar double (") y single quotes (')

Display:
- Night Shift - Sunset to Sunrise

Time Machine:
- Show Time Machine in menu bar

Algunos defaults:

# Disable automatic capitalization as it’s annoying when typing code
defaults write NSGlobalDomain NSAutomaticCapitalizationEnabled -bool false

# Disable smart dashes as they’re annoying when typing code
defaults write NSGlobalDomain NSAutomaticDashSubstitutionEnabled -bool false

# Disable automatic period substitution as it’s annoying when typing code
defaults write NSGlobalDomain NSAutomaticPeriodSubstitutionEnabled -bool false

# Disable smart quotes as they’re annoying when typing code
defaults write NSGlobalDomain NSAutomaticQuoteSubstitutionEnabled -bool false

# Disable auto-correct
defaults write NSGlobalDomain NSAutomaticSpellingCorrectionEnabled -bool false

# Trackpad: enable tap to click for this user and for the login screen
defaults write com.apple.driver.AppleBluetoothMultitouch.trackpad Clicking -bool true
defaults -currentHost write NSGlobalDomain com.apple.mouse.tapBehavior -int 1
defaults write NSGlobalDomain com.apple.mouse.tapBehavior -int 1

# Set a blazingly fast keyboard repeat rate
defaults write NSGlobalDomain KeyRepeat -int 1
defaults write NSGlobalDomain InitialKeyRepeat -int 10

# Finder: show all filename extensions
defaults write NSGlobalDomain AppleShowAllExtensions -bool true

# Finder: show status bar
defaults write com.apple.finder ShowStatusBar -bool true

# Automatically hide and show the Dock
defaults write com.apple.dock autohide -bool true


-----

## Ansible Playbook

Instalar HomeBrew (http://brew.sh)

Instalar ansible

    brew install ansible

+ TODO: script para instalar la key para acceder a los repos de github, bajandola de icloud (Documents/macbook-pre-setup, hasta poder encriptar las keys y dejar el repo publico.

    mkdir -m 0700 ~/.ssh
    cp -p ~/Documents/macbook-pre-setup/juanedu@github*
    (chequear permisos 0600 para private y 0644 para public)
    ssh-add ~/.ssh/juanedu@github

Crear una carpeta 'code' en el home y clonar este repositorio

    git clone git@github.com:juanedu/macbook-setup.git

TODO: Resolver provisionamiento de keys ssh para clonar repos. Quizas haya que hacer dos corridas de ansible: una para bajar los config files (ej: dropbox o icloud), y otra para ejecutar las tareas de configuracion de las apps copiando los archivos

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

https://wilsonmar.github.io/dotfiles/ (dotfiles y defaults)
https://github.com/mathiasbynens/dotfiles/blob/master/.macos (dotfiles y defaults)


