Status: done

Implementa una nueva venta de login, mas moderna, con las opciones de login en un costado y una imagen representativa de el otro costado.

Agrega un boton de contacto con los owner de la aplicacion

## Implementation Notes

Implemented and pushed to the following branches:
- Backend (`consorcio-unido`): `new-login`
- Frontend (`consorcio-unido-ui`): `new-login`

### Changes Made:

**Frontend (consorcio-unido-ui):**
- Modern two-column layout with login form on the right and decorative image on the left
- Responsive design using Material-UI Grid
- Contact button that opens a modal dialog
- Contact form with fields for name, email, and message
- Updated styling with gradient background

**Backend (consorcio-unido):**
- New endpoint: `POST /sendContactMessage`
- Added `send_contact_message` method in LoginService
- Integrated EmailService to send contact messages to administrators
- Contact message formatting for email