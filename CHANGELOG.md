# @coongro/kit-rentals

## 0.4.0

### Minor Changes

- El kit trae roles para los empleados del negocio

  Cuatro roles combinables (se suman si una persona tiene varios): **Operación completa** (por defecto: todo lo del kit, el que reciben los usuarios que ya existían), **Consulta** (ver sin modificar), **Cobranzas** (consulta más cobrar alquileres y registrar cobros) y **Mantenimiento** (gestionar órdenes de trabajo). Ninguno administra usuarios, plugins ni configuración: eso es del dueño. Los roles se asignan desde la pantalla de Usuarios de Coongro Standalone.

### Patch Changes

- El Panel de alquileres encabeza la sección principal del menú

  El Panel de `leases` no tenía sección asignada en el kit y quedaba suelto en el sidebar. Ahora
  abre la sección principal, primero.

## 0.3.0

### Minor Changes

- fcdfa82: feat: kit de gestión de alquileres v1 (COONG-275)

  El paraguas del kit: instala y organiza los cinco plugins que lo componen —propiedades, contratos,
  índices, cobranza y mantenimiento— y ordena el menú en las cuatro secciones con las que se trabaja
  un mes de alquileres: Patrimonio, Alquileres, Cobranza y Operación.

  Como todo kit, no tiene lógica propia: son dependencias y organización.

### Patch Changes

- 061d88c: fix: el kit no muestra «Cobros» ni «Caja» (COONG-275)

  Los dos vienen de `billing` y duplicaban el concepto de cobrar: el kit ya tiene
  su propia «Cobranzas», que es la que entiende de contratos, períodos y ajustes.

  Se ocultan con `hidden` en los `menuAssignments` del kit, así que `billing`
  queda intacto y sus menús siguen apareciendo en cualquier otro kit que lo
  instale. `hidden` saca el ítem del sidebar, no la vista: las pantallas siguen
  existiendo y siendo alcanzables — es organización del menú, no control de
  acceso.
