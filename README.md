# Pet Adoption API

This API provides endpoints to manage pet adoption, including creating new pets, finding pets available for adoption, and managing shelter and user accounts.

## Endpoints

### Pets

#### `POST /api/pets`

Create a new pet for adoption.

**Request Body:**
```json
{
  "name": "Fluffy",
  "breed": "Persian",
  "age": 2,
  "gender": "female",
  "size": "small",
  "species": "cat",
  "description": "A beautiful Persian cat looking for a loving home.",
  "images": ["https://example.com/image1.jpg", "https://example.com/image2.jpg"],
  "status": "available",
  "shelter_id": "6163ab3f12588a8d84768d06"
}
```
**Response:**
```json
{
  "name": "Fluffy",
  "breed": "Persian",
  "age": 2,
  "gender": "female",
  "size": "small",
  "species": "cat",
  "description": "A beautiful Persian cat looking for a loving home.",
  "images": ["https://example.com/image1.jpg", "https://example.com/image2.jpg"],
  "status": "available",
  "shelter_id": "6163ab3f12588a8d84768d06",
  "_id": "6163ac9c12588a8d84768d0a",
  "created_at": "2021-10-10T00:00:00Z",
  "updated_at": "2021-10-10T00:00:00Z"
}
```

**GET /api/pets**
Get a list of all pets available for adoption.
```json
[
  {
    "name": "Fluffy",
    "breed": "Persian",
    "age": 2,
    "gender": "female",
    "size": "small",
    "species": "cat",
    "description": "A beautiful Persian cat looking for a loving home.",
    "images": ["https://example.com/image1.jpg", "https://example.com/image2.jpg"],
    "status": "available",
    "shelter_id": {
      "name": "My Shelter",
      "location": {
        "address": "123 Main St",
        "city": "Anytown",
        "state": "CA",
        "zip": "12345",
        "country": "USA"
      },
      "phone_number": "555-1234",
      "email": "shelter@example.com",
      "website": "https://example.com/shelter",
      "description": "A great place to find your new best friend.",
      "_id": "6163ab3f12588a8d84768d06"
    },
    "_id": "6163ac9c12588a8d84768d0a",
    "created_at": "2021-10-10T00:00:00Z",
    "updated_at": "2021-10-10T00:00:00Z"
  },
  {
    "name": "Max",
    "breed": "Golden Retriever",
    "age": 3,
    "gender": "male",
    "size": "medium",
    "species": "dog",
    "description": "A friendly and playful Golden Retriever.",
    "images": ["https://example.com/image3.jpg", "https://example.com/image4.jpg"],
```

