# Historial de versiones

Cada vez que se termina un cambio, el juego sube de versión y se guarda una copia completa en `programa/versiones/` con el nombre `vX.Y_AAAA-MM-DD.zip`. Todos los cambios quedan apuntados en el `CHANGELOG.md`, y de ahí sale este historial.

!!! note "Cómo leer las versiones"
    - El número **X.Y** sube de uno en uno (v0.9 → v0.10 → v0.11…): **no son decimales**.
    - La **v1.00** se alcanzó con la oficina hecha entera en Blender y la música de la noche 7.
    - Faltan la **v0.78** (se saltó al numerar) y el zip de la **v0.38** (sí está en el registro de cambios).

## Para volver a una versión antigua

```bash
# 1. Descomprimir la versión en una carpeta nueva
unzip programa/versiones/v0.32_2026-10-16.zip -d prueba-v0.32

# 2. Arrancar el servidor desde esa carpeta
cd prueba-v0.32
python servidor.py
```

## Los grandes hitos

| Fecha | Versión | Hito |
|---|---|---|
| 13 oct | [v0.1](v0-1-a-v0-30.md#v01-a-v05-13-de-octubre) | Primera versión registrada: la **noche 1** jugable |
| 14 oct | [v0.7](v0-1-a-v0-30.md#v06-a-v017-14-de-octubre) | **Noche 2**: conductos de ventilación, El Insecto y El Largo |
| 15 oct | [v0.28](v0-1-a-v0-30.md#v018-a-v030-15-de-octubre) | La nave entera en **3D** con Blender |
| 16 oct | [v0.32](v0-31-a-v0-60.md#v031-a-v034-16-de-octubre) | **Noche 3** completa |
| 18 oct | [v0.35](v0-31-a-v0-60.md#v035-a-v045-18-y-19-de-octubre) | **Noche 4** con dos rutas y la llegada de **Slaimi** |
| 20 oct | [v0.46](v0-31-a-v0-60.md#v046-a-v053-20-a-22-de-octubre) | **Noche 5**: El Errante y El Dislocado |
| 21 oct | [v0.52](v0-31-a-v0-60.md#v046-a-v053-20-a-22-de-octubre) | **Rediseño** de todas las criaturas |
| 26 oct | [v0.72](v0-61-a-v0-99.md#v067-a-v077-26-y-27-de-octubre) | **Noche 6** y la primera hoja de **La Aberración** |
| 28 oct | [v0.82](v0-61-a-v0-99.md#v079-a-v099-27-a-29-de-octubre) | **Noche 7**, la noche final |
| 29 oct | [v1.00](v1-00-a-v1-38.md#v100-a-v111-29-de-octubre) | La **oficina hecha en Blender** |
| 2 nov | [v1.36](v1-00-a-v1-38.md#v128-a-v138-1-y-2-de-noviembre) | Los **4 finales** en 3D |

## Las cuatro etapas

1. **[v0.1 – v0.30 · Noches 1 y 2](v0-1-a-v0-30.md)**. El juego base: oficina, cámaras, reactor, apagones, las primeras cintas y el paso de los dibujos por código al 3D.
2. **[v0.31 – v0.60 · Noches 3 a 5](v0-31-a-v0-60.md)**. El Largo «por el oído», las taquillas, las dos rutas de la noche 4, Slaimi y el gran rediseño de las criaturas.
3. **[v0.61 – v0.99 · Noches 6 y 7](v0-61-a-v0-99.md)**. El Congelado definitivo, la sala oculta, La Aberración y la nave en llamas.
4. **[v1.00 – v1.38 · El final](v1-00-a-v1-38.md)**. La huida en 3D en tiempo real, la nave de escape y los cuatro finales.

!!! quote "La regla del proyecto"
    Cada versión se prueba antes de subirla. Si algo nuevo necesita el visto bueno (un diseño, una hoja de modelo), se marca como **PROVISIONAL** hasta que se aprueba.
