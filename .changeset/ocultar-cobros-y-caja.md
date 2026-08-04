---
'@coongro/kit-rentals': patch
---

fix: el kit no muestra «Cobros» ni «Caja» (COONG-275)

Los dos vienen de `billing` y duplicaban el concepto de cobrar: el kit ya tiene
su propia «Cobranzas», que es la que entiende de contratos, períodos y ajustes.

Se ocultan con `hidden` en los `menuAssignments` del kit, así que `billing`
queda intacto y sus menús siguen apareciendo en cualquier otro kit que lo
instale. `hidden` saca el ítem del sidebar, no la vista: las pantallas siguen
existiendo y siendo alcanzables — es organización del menú, no control de
acceso.
