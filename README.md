# 🦄 Alke Wallet - Billetera Digital

Una aplicación web de billetera digital interactiva desarrollada con HTML, CSS, Bootstrap y jQuery como parte del bootcamp de desarrollo Front-End.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white)
![jQuery](https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white)

## 📋 Descripción

Alke Wallet es una billetera digital simulada que permite a los usuarios gestionar sus finanzas de manera intuitiva. El proyecto demuestra el uso de interacciones dinámicas, manipulación del DOM con jQuery, y diseño responsive con Bootstrap.

## ✨ Características

### 🔐 Autenticación
- Sistema de login con validación de credenciales
- Almacenamiento de sesión con localStorage
- Mensajes de error y éxito con alertas de Bootstrap

### 💰 Gestión de Saldo
- Visualización del saldo actual en tiempo real
- Actualización automática después de cada transacción
- Persistencia de datos usando localStorage

### 📥 Depósitos
- Formulario para realizar depósitos
- Botones de montos rápidos ($100, $500, $1,000, etc.)
- Validación de montos
- Confirmación visual del depósito realizado

### 📤 Envío de Dinero
- Agenda de contactos con búsqueda en tiempo real
- Agregar nuevos contactos con validación de CBU
- Enviar dinero a contactos existentes
- Validación de saldo suficiente
- Confirmación de transferencia

### 📊 Últimos Movimientos
- Historial completo de transacciones
- Filtro por tipo (Todos/Depósitos/Envíos)
- Estadísticas de totales de depósitos y envíos
- Visualización con iconos y colores diferenciados

## 🛠️ Tecnologías Utilizadas

- **HTML5**: Estructura semántica
- **CSS3**: Estilos personalizados y gradientes
- **Bootstrap 5.3.8**: Framework CSS para diseño responsive
- **jQuery 3.6.0**: Manipulación del DOM y eventos
- **LocalStorage**: Persistencia de datos del lado del cliente

## 📂 Estructura del Proyecto
```
Alke-Wallet/
│
├── login.html          # Pantalla de inicio de sesión
├── menu.html           # Menú principal con saldo
├── deposit.html        # Formulario de depósitos
├── sendmoney.html      # Envío de dinero y gestión de contactos
├── transactions.html   # Historial de movimientos
└── README.md          # Este archivo
```

## 🚀 Instalación y Uso

### Opción 1: Uso Local

1. **Clonar el repositorio**
```bash
git clone https://github.com/pibitz/Alke-Wallet.git
cd Alke-Wallet
```

2. **Abrir en el navegador**
```bash
# Simplemente abre login.html en tu navegador favorito
# O usa Live Server en VS Code
```

### Opción 2: GitHub Pages

Visita la versión desplegada en: `https://pibitz.github.io/Alke-Wallet/login.html`

## 🔑 Credenciales de Acceso

Para acceder a la aplicación, usa las siguientes credenciales:

- **Email**: `holi@poni.cl`
- **Contraseña**: `1234`

## 💡 Funcionalidades Destacadas

### Interactividad con jQuery
```javascript
// Ejemplo: Búsqueda en tiempo real de contactos
$('#searchInput').on('input', function() {
    const busqueda = $(this).val().toLowerCase();
    const filtrados = contactos.filter(c => 
        c.nombreApellido.toLowerCase().includes(busqueda)
    );
    renderizarContactos(filtrados);
});
```

### Validaciones

- ✅ Campos obligatorios en formularios
- ✅ Validación de CBU (22 dígitos numéricos)
- ✅ Validación de saldo suficiente
- ✅ Validación de montos positivos

### Persistencia de Datos

Todos los datos se almacenan en localStorage:
- Saldo de la cuenta
- Contactos
- Historial de transacciones
- Sesión del usuario

## 📱 Responsive Design

La aplicación es completamente responsive y se adapta a:
- 📱 Dispositivos móviles (< 576px)
- 📱 Tablets (576px - 768px)
- 💻 Desktop (> 768px)

## 🎨 Paleta de Colores

| Pantalla | Gradiente Principal |
|----------|-------------------|
| Login | `#ff89d6` → `#ff63bc` |
| Menú | `#baffa3` → `#ff63bc` |
| Depósito | `#8c61fa` → `#83ff95` |
| Enviar | `#fcffa5` → `#98ddff` |
| Movimientos | `#ffa0a0` → `#8bd8ff` |

## 📸 Capturas de Pantalla

### Login
![Login Screen](./screenshots/login.png)

### Menú Principal
![Menu Screen](./screenshots/menu.png)

### Depósitos
![Deposit Screen](./screenshots/deposit.png)

## 🧪 Navegación del Sistema
```
login.html
    ↓
menu.html
    ├── deposit.html → menu.html
    ├── sendmoney.html → menu.html
    └── transactions.html → menu.html
```

## 🔄 Flujo de Datos

1. **Login**: Valida credenciales → Guarda sesión en localStorage
2. **Depósito**: Incrementa saldo → Guarda en localStorage → Registra transacción
3. **Envío**: Decrementa saldo → Guarda en localStorage → Registra transacción
4. **Transacciones**: Lee desde localStorage → Renderiza con filtros

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Para cambios importantes:

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📝 Mejoras Futuras

- [ ] Integración con API REST real
- [ ] Autenticación con JWT
- [ ] Gráficos de estadísticas con Chart.js
- [ ] Exportar historial a PDF
- [ ] Notificaciones push
- [ ] Modo oscuro
- [ ] Multidioma (ES/EN)

## 👥 Autores

- **Tu Nombre** - *Desarrollo Inicial* - [@pibitz](https://github.com/pibitz)

## 📄 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE.md](LICENSE.md) para más detalles.

## 🙏 Agradecimientos

- Bootcamp Alke Wallet por el desafío
- Bootstrap por el framework CSS
- jQuery por simplificar la manipulación del DOM
- Font Awesome por los iconos (si los usas)


Link del Proyecto: [https://github.com/pibitz/Alke-Wallet](https://github.com/pibitz/Alke-Wallet)

---

⭐️ Si te gustó este proyecto, dale una estrella en GitHub!

**Hecho con 💜 por [pibitz](https://github.com/pibitz)**
