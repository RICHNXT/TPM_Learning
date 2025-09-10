# Shipment Status API

**Endpoint:**  
`GET /shipments/{id}/status`

**Description:**  
Retrieve the current status of a shipment by ID.

**Request:**  
- Path parameter: `id` (string, required)

**Response (200 OK):**
```json
{
  "shipment_id": "ABC123",
  "status": "in_transit",
  "last_update": "2025-09-09T12:34:56Z"
}