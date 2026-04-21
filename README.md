# 🗳️ Resultados Presidenciales Perú 2026

Dashboard en tiempo real de resultados electorales de ONPE.

## Setup en 3 pasos

### 1. Crear el repositorio en GitHub
- Crea un nuevo repo público (ej: `elecciones-2026`)
- Sube todos estos archivos manteniendo la estructura de carpetas

### 2. Activar GitHub Pages
- Ve a **Settings → Pages**
- Source: `Deploy from a branch`
- Branch: `main` / carpeta: `/ (root)`
- Guarda → en ~1 minuto tendrás tu URL: `https://TU-USUARIO.github.io/elecciones-2026`

### 3. Activar permisos de escritura para el workflow
- Ve a **Settings → Actions → General**
- En "Workflow permissions" selecciona **"Read and write permissions"**
- Guarda

### 4. Ejecutar el workflow por primera vez
- Ve a **Actions → Fetch ONPE Data → Run workflow**
- Esto pobla la carpeta `data/` con los JSONs reales
- Desde ahí corre automáticamente cada 5 minutos

## Estructura
```
├── index.html              # Dashboard principal
├── data/
│   ├── participantes.json  # Actualizado por GitHub Actions
│   ├── totales.json        # Actualizado por GitHub Actions
│   └── meta.json           # Timestamp de última actualización
└── .github/
    └── workflows/
        └── fetch-onpe.yml  # Cron job cada 5 minutos
```

## Fuente
Datos oficiales: https://resultadoelectoral.onpe.gob.pe
