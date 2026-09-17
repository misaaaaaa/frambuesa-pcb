# frambuesa-pcb

## biblioteca local de KiCad

Las partes JLCPCB elegidas para una revisión se listan en `bom.csv` de esa carpeta
(ej. `frambuesa-rev-a/bom.csv`, mismas columnas que el inventario de
[partes-jlcpcb](https://github.com/piruetasxyz/partes-jlcpcb)). Para generar la
biblioteca local de KiCad (símbolos, huellas y modelos 3D) a partir de esas partes:

```bash
cd frambuesa-rev-a
python3 /ruta/a/partes-jlcpcb/generar_biblioteca.py --bom bom.csv --output bibliotecas/frambuesa-rev-a
```

Ajusta `/ruta/a/partes-jlcpcb` a donde tengas clonado ese repositorio. Requiere su
entorno virtual activado (ver su README). Después,
agrega `bibliotecas/` como ruta de biblioteca en KiCad (Preferencias → Administrar
bibliotecas de símbolos/huellas).
