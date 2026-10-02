# Una práctica sobre pip y subprocess

Este script explora cómo listar paquetes del intérprete actual y llamar a pip desde Python. También desinstala paquetes: debe leerse con especial cuidado.

## Advertencia

No lo ejecutes en el Python del sistema, en un entorno compartido ni en un proyecto con dependencias que quieras conservar. `essential_packages` es una selección fija del ejercicio, no un análisis de lo que necesita realmente tu entorno.

Confirmar con `s` ejecuta `pip uninstall -y` sobre los paquetes fuera de esa lista. No analiza dependencias, crea copias de seguridad ni ofrece simulación.

## Qué hace

Consulta `sys.executable -m pip freeze`, extrae nombres suponiendo el formato `nombre==versión`, muestra candidatos y pide confirmación antes de desinstalar.

Las instalaciones editables o mediante URL pueden no encajar con ese formato. El contador de éxitos tampoco comprueba el código de retorno de pip: puede informar como correcta una desinstalación fallida.

## Para qué conservarlo

Es un ejercicio con procesos externos, no una herramienta recomendada para limpiar entornos. Si quieres estudiar su comportamiento, utiliza únicamente un entorno virtual desechable. Para un proyecto nuevo, es más sencillo partir de un entorno limpio que reconstruir otro mediante desinstalaciones.

Esta revisión documenta los riesgos y conserva el script original. No se ha ejecutado.
