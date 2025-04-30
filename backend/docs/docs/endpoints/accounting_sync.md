## Create Accounting Sync

```http
POST /api/v1/sync/invoices
```

### Request
```json
{
  "invoice_id": "inv_123",
  "accounting_provider": "evo200",
  "customer_id": "cust_456"
}
```

### Response
```json
{
  "sync_id": "sync_789",
  "accounting_id": "INV-2023-001",
  "status": "queued"
}
```

### Error Codes
| Code | Description |
|------|-------------|
| 402  | Accounting provider not connected |
| 409  | Invoice already synced |