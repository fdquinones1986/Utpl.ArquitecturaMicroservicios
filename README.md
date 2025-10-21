# Taller Microservicios

Estructura:
- backend/clients
- backend/suppliers
- backend/invoices
- frontend/portal

Requisitos:
- pip install fastapi uvicorn requests

Ejecutar cada servicio (en su carpeta):
- clients: > uvicorn main:app --reload --port 8001
- suppliers: > uvicorn main:app --reload --port 8002
- invoices: > CLIENTS_URL=http://localhost:8001 uvicorn main:app --reload --port 8003

Frontend:
- Abrir frontend/portal/index.html con el navegador (o > python -m http.server 5500 y abrir http://localhost:5500)
- Configurar las URLs de cada servicio y probar los botones.

Notas de taller:
- Cada estudiante levanta un servicio diferente. Para simular fallo, uno detiene su servicio y la web debe mostrar error solo para ese servicio.
- Opcional: añadir timeouts/retries en frontend o usar un API gateway.
