Status: done

Actualmente la UI ya tiene implementado visual de likes y corazones. 
Quiero capturar que usuario hizo ese like o corazon y guardarlo en el backend.

Realiza una implementacion limpia y ordenada. Priorizando la programacion orientada a objetos y reutiliza lo mas posible de el codigo existente.

## Implementation Notes

Implemented and pushed to the following branches:
- `consorcio-unido`: `store-likes-and-who-on-notifications`
- `consorcio-unido-ui`: `store-likes-and-who-on-notifications`

### Backend Changes
- Created `NotificationReactionModel` for storing user reactions with email and reaction type
- Implemented `NotificationReactionService` for managing reaction operations (add, remove, query)
- Added API endpoints:
  - `POST /notification/reaction` - Add or update user reaction
  - `GET /notification/reactions` - Get reaction counts and user's current reaction
- Integrated DAO layers for SQLite, PostgreSQL, and MongoDB backends
- Supports toggle behavior: same reaction type removes it, different type replaces previous

### Frontend Changes
- Updated `NotificationDetailsView` component to:
  - Load reactions from backend on component mount
  - Sync user reactions with backend via API calls
  - Integrate with UserContext to pass user email
  - Add loading state to prevent simultaneous requests
  - Display real-time reaction counts from backend
- Updated `NotificationListView` to pass user email from UserContext to child components
