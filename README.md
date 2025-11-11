# Config Repository

Repositorio centralizado de configuraciones para microservicios del Sistema de Gestión de Pedidos.

## Estructura

```
config-repo/
├── ms-productos-dev.yml      # Configuración desarrollo ms-productos
├── ms-productos-docker.yaml  # Configuración Docker ms-productos
├── ms-productos-qa.yml       # Configuración QA ms-productos
├── ms-productos-prod.yml     # Configuración producción ms-productos
├── ms-pedidos-dev.yml        # Configuración desarrollo ms-pedidos
├── ms-pedidos-docker.yaml    # Configuración Docker ms-pedidos
├── ms-pedidos-qa.yml         # Configuración QA ms-pedidos
├── ms-pedidos-prod.yml       # Configuración producción ms-pedidos
├── gateway-service.yaml      # Configuración desarrollo gateway
├── gateway-service-docker.yaml # Configuración Docker gateway
├── registry-service.yml      # Configuración desarrollo registry
└── registry-service-docker.yml # Configuración Docker registry
```

## Configuraciones

### Perfiles Soportados
- **dev**: Desarrollo local
- **docker**: Contenedores Docker
- **qa**: Ambiente de pruebas
- **prod**: Producción

### Configuraciones Docker
- Usan nombres de contenedor para comunicación interna
- Configuración de Eureka con `registry-service:8761`
- Base de datos PostgreSQL en contenedor separado

### Variables Importantes
- `host.docker.internal`: Acceso a BD local desde contenedores
- Nombres de servicio: `ms-productos`, `registry-service`, `config-server`

## Uso

Utilizado por **ms-config-server** para configuraciones. 
Los perfiles Docker permiten despliegue completo con `docker-compose up --build`.