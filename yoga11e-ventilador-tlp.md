**\# Guía rápida: Solución a ventilación excesiva en Lenovo Yoga 11e (y
equipos compactos)**

**Hola a todos. Para no hacer largo el cuento sobre lo que hice para
intentar solucionar el problema de ventilación excesiva en una Lenovo
Yoga 11e, les comparto la solución técnica definitiva.**

**Además del mantenimiento físico regular (limpieza de polvo), es
necesario instalar y permitir la ejecución de una herramienta de control
térmico que regule de forma inteligente la función del ventilador.**

**\## Paso 1: Instalación de la herramienta**

**Abre una terminal y ejecuta los siguientes comandos para actualizar
tus repositorios e instalar TLP:**

**\`\`\`bash**

**sudo apt update**

**sudo apt install tlp tlp-rdw**

**sudo tlp start**

**\`\`\`**

**\## Paso 2: Corrección de permisos de arranque**

**Si al intentar arrancar el programa notas que no aplica los cambios o
te arroja un error de servicio, significa que el sistema no lo tiene
permitido al encender. Ejecuta este comando para solucionarlo:**

**\`\`\`bash**

**sudo systemctl enable tlp.service**

**\`\`\`**

**\> \*\*Nota:\*\* Cuando la terminal te muestre que se ha creado el
\"symlink\", significa que el programa ya cuenta con los permisos
necesarios. Después de esto, reinicia tu equipo.**

**\## Recomendación de Hardware**

**Si el equipo sigue sintiéndose lento, es altamente recomendable
cambiar el viejo disco mecánico (HDD) de fábrica por un disco de estado
sólido (SSD). Esto disminuye drásticas veces el uso continuo de recursos
de lectura/escritura y, por ende, evita el sobrecalentamiento residual
que activa el ventilador al máximo.**
