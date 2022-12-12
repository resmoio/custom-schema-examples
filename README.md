# Resmo Custom Data Resource/Schema Examples

## Example JSON schema for an employee
[Example JSON Schema](schema.json)

## Resource event (single)
[Valid example of payload](payload.json)
```
curl --request POST \
  --url https://id.resmo.app/integration/custom-data/event/YOUR_TABLE_NAME_HERE \
  --header 'Content-Type: application/json' \
  --header 'X-Ingest-Key: YOUR_INTEGRATION_INGEST_KEY_HERE' \
  --data 'PAYLOAD_HERE'
```

## Resource event (bulk)
[Valid example of payload](bulk-payload.json)
```
curl --request POST \
  --url https://id.resmo.app/integration/custom-data/bulk-event/YOUR_TABLE_NAME_HERE \
  --header 'Content-Type: application/json' \
  --header 'X-Ingest-Key: YOUR_INTEGRATION_INGEST_KEY_HERE' \
  --data 'PAYLOAD_HERE'
```

## Delete a resource
To remove resources with ids: ID1, ID2, ID3:
```
curl --request DELETE \
  --url https://id.resmo.app/integration/custom-data/YOUR_TABLE_NAME_HERE?resourceIds=ID1,ID2,ID3 \
  --header 'X-Ingest-Key: YOUR_INTEGRATION_INGEST_KEY_HERE'
```