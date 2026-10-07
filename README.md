# Préstamos ANCO

Aplicativo web para administrar préstamos de dinero entre dos usuarios (p. ej. una pareja que presta desde una base común).

## Características

- **Dos usuarios con contraseña** (bloqueo familiar sencillo).
- **Base** (fondo disponible) y cálculo de saldo en tiempo real.
- **Préstamos** con:
  - Datos del cliente (nombre, documento, teléfono, dirección).
  - Capital prestado y **% de interés**.
  - Modalidad **cobro único** o **por cuotas** (N° y valor de cuota).
  - Fechas de desembolso y vencimiento.
  - **Foto de evidencia obligatoria** del desembolso.
- **Pagos / abonos** por cuota, interés o capital, con evidencia opcional.
- **Pantalla de inicio** con el saldo de la base y los pagos más recientes.
- **Estados automáticos**: activo / en mora / pagado.
- **Datos compartidos en la nube**: los dos usuarios ven la misma información.

## Tecnología

- Una sola página HTML (`prestamos-anco.html`), sin dependencias de servidor.
- Publicada como **Claude Artifact**, que provee:
  - `db` → base de datos compartida (préstamos, pagos, configuración).
  - `assets` → almacenamiento de las fotos de evidencia.

## Estructura

```
.
├── prestamos-anco.html   # La aplicación completa
└── README.md
```

## Uso

1. Abrir la app publicada.
2. La primera vez: crear los dos usuarios y el monto de la base.
3. Para que el segundo usuario entre desde otro dispositivo, compartir el
   artefacto **con permiso de edición** desde el menú *Compartir*.

## Notas

- La contraseña es un bloqueo de acceso sencillo, no seguridad de nivel bancario.
- No almacenar aquí información que no deba estar en la nube.
