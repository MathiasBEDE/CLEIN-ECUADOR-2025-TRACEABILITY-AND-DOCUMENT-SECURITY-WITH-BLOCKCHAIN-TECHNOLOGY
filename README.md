# Sistema de Gestión Documental con Streamlit

Un sistema moderno y simple para gestionar documentos con verificación de integridad mediante hash SHA-256.

## Características

- **Upload de archivos** con interfaz web amigable
- **Cálculo automático** de hash SHA-256
- **Detección automática** de tipo y versión del documento
- **Verificación de duplicados** basada en hash
- **Registro completo** con metadatos
- **Visualización en tabla** con filtros
- **Exportación a CSV**

## Cómo usar

### Opción 1: Ejecutar con script automático
1. Haz doble clic en `ejecutar_streamlit.bat`
2. Se abrirá automáticamente en tu navegador
3. ¡Listo para usar!

### Opción 2: Ejecutar manualmente
```bash
# Instalar dependencias
pip install streamlit pandas

# Ejecutar la aplicación
streamlit run app.py
```

##  Estructura del proyecto

```
HASHES/
├── app.py                  # Aplicación principal
├── ejecutar_streamlit.bat  # Script de ejecución automática
├── requirements.txt        # Dependencias de Python
├── registro_documentos.csv # Base de datos (se crea automáticamente)
└── README.md              # Este archivo
```

##  Funcionalidades principales

### 1. Upload de Archivos
- Arrastra o selecciona archivos desde tu computadora
- Formatos soportados: PDF, Word, Excel, TXT, Imágenes
- Muestra información básica del archivo

### 2. Verificación de Integridad
- Calcula hash SHA-256 automáticamente
- Detecta si el archivo ya existe en el sistema
- Alertas visuales para archivos duplicados

### 3. Detección Automática
- **Tipo de documento**: Manual, Contrato, Política, etc.
- **Versión**: Extrae automáticamente versiones del nombre
- **Nombre limpio**: Normaliza el nombre del archivo

### 4. Registro Completo
Campos disponibles:
- Hash SHA-256
- Nombre del documento
- Tipo de documento
- Fecha de creación/actualización
- Versión
- Estatus (Publicado/Editado/Borrador)
- Descripción de modificación
- Creador, Revisor, Aprobador
- No conformidad
- Auditoría

### 5. Visualización y Filtros
- Tabla interactiva con todos los registros
- Filtros por tipo, estatus y creador
- Exportación a CSV
- Métricas del sistema

##  Estados del documento

- **Publicado**: Documento nuevo registrado
- **Editado**: Documento que ya existía (mismo hash)
- **Borrador**: Documento en desarrollo
- **Vigente**: Documento activo
- **Terminado**: Documento finalizado

##  Seguridad

- Usa hash SHA-256 para verificación de integridad
- No almacena los archivos, solo metadatos
- Registro local en CSV para máxima compatibilidad

##  Requisitos técnicos

- Python 3.7+
- Streamlit
- Pandas
- Hashlib (incluido en Python)

##  Notas importantes

1. Los archivos NO se almacenan en el sistema, solo sus metadatos
2. El hash SHA-256 garantiza la detección de cualquier modificación
3. El archivo CSV se guarda en la misma carpeta del proyecto
4. La aplicación funciona completamente offline

##  Características de la interfaz

- **Responsive**: Se adapta a cualquier tamaño de pantalla
- **Intuitiva**: Flujo de trabajo paso a paso
- **Visual**: Iconos y colores para mejor experiencia
- **Rápida**: Carga instantánea y operaciones en tiempo real

##  Migración desde sistema anterior

Si tienes datos del sistema anterior (`blockchain.json`), puedes:
1. Mantener ambos sistemas
2. Usar el nuevo sistema para documentos futuros
3. Los dos sistemas son independientes

##  Soporte

Para cualquier duda o problema:
1. Verifica que Python esté instalado
2. Ejecuta `pip install streamlit pandas`
3. Usa el script `ejecutar_streamlit.bat` para facilidad

---

**Desarrollado para gestión documental simple y eficiente** 

