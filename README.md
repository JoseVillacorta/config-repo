# Config Repository

Repositorio centralizado de configuraciones para microservicios del Sistema de Gestión de Pedidos.

## Estructura

```
config-repo/
├── ms-productos-dev.yml    # Configuración desarrollo ms-productos
├── ms-productos-qa.yml     # Configuración QA ms-productos
├── ms-productos-prd.yml    # Configuración producción ms-productos
├── ms-pedidos-dev.yml      # Configuración desarrollo ms-pedidos
├── ms-pedidos-qa.yml       # Configuración QA ms-pedidos
└── ms-pedidos-prd.yml      # Configuración producción ms-pedidos
```

## Configuraciones

### Variables de Entorno Requeridas
- `DB_USERNAME`: Usuario de PostgreSQL
- `DB_PASSWORD`: Contraseña de PostgreSQL
- `DB_URL`: URL de conexión a BD
- `MS_PRODUCTOS_URL`: URL del microservicio productos

### Perfiles Soportados
- **dev**: Desarrollo local
- **qa**: Ambiente de pruebas
- **prd**: Producción

## Uso

Este repositorio es utilizado por el **ms-config-server** para servir configuraciones centralizadas a todos los microservicios.