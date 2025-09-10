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
| Status Code | Description             |
| ----------- | ----------------------- |
| 404         | Shipment does not exist |
| 500         | Internal server error   |
3. Save.  

---

### diagrams/shipment-system.png
- Place any PNG diagram here (draw.io export or simple box diagram).  

---

### sql/example-queries.sql
1. Right-click `sql` → New File → `example-queries.sql`  
2. Paste:

```sql
-- Count shipments by status
SELECT status, COUNT(*) 
FROM shipments 
GROUP BY status;

-- Find delayed shipments
SELECT id, destination, updated_at 
FROM shipments 
WHERE status = 'delayed';
