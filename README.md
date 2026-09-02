# Informe financiero mensual LCC

Aplicación web estática para cargar el archivo Excel mensual y generar el informe financiero en COP y USD.

## Accesos directos

- Herramienta para compartir: https://applacalera-dev.github.io/financiero/
- Repositorio: https://github.com/applacalera-dev/financiero
- Editar las TRM: https://github.com/applacalera-dev/financiero/edit/main/trm.json
- Revisar publicaciones: https://github.com/applacalera-dev/financiero/actions
- El Excel se procesa localmente en el navegador y no se incluye en este repositorio.

## Actualizar las TRM sin editar el HTML

1. Abra [`trm.json`](https://github.com/applacalera-dev/financiero/edit/main/trm.json).
2. Busque el mes que desea actualizar.
3. Reemplace `null` por la TRM usando punto para los decimales y sin separador de miles. Ejemplo: `3250.75`.
4. Guarde el cambio directamente en la rama `main`.
5. Espere a que finalice la acción **Publicar informe en GitHub Pages**.

Al cargar un Excel, el informe consulta primero `trm.json`. Si el archivo remoto no está disponible, utiliza las tasas integradas en el HTML y solicita manualmente cualquier mes faltante.

No cambie el nombre de `trm.json`, la propiedad `trm` ni los nombres de los meses.
