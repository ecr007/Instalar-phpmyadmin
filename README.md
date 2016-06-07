# Instalar phpmyadmin
Instalación de la ultima versión de PHPMYADMIN

# Paso 1 - Clonar phpmyadmin

```
git clone --depth=1 --branch=STABLE https://github.com/phpmyadmin/phpmyadmin.git
```

# Paso 2 - Actualizar

```
#!/bin/bash

cd /home/sites/phpmyadmin/
git pull -q origin STABLE
```

# Paso 3 - Configurar la tarea de actualización

```
# Automatically upgrade PHPMyAdmin daily (5am)
0 5 * * * /home/user/scripts/pma_update.sh >> /dev/null 2>&1
```

