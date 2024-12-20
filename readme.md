# Swahilies Payment Integration

A web application for processing payments using the ZenoPay payment gateway API.

## Features

- Payment plan selection
- Real-time payment status updates
- WebSocket integration
- Mobile money payment processing
- Responsive design
- Form validation
- Error handling

## Technical Stack

- HTML5
- CSS3 
- Vanilla JavaScript
- WebSocket
- ZenoPay API

## Configuration

1. Update the API endpoint in `script` section:
```javascript
const API_BASE_URL = 'https://zenopay-annual-meeting.onrender.com';
```

2. Payment plans are configured in the HTML:
```html
<div class="card" data-level="planName" data-amount="amount">
```

## API Integration

### Create Order
- Endpoint: `${API_BASE_URL}/create_order`
- Method: POST
- Payload:
```json
{
  "buyer_email": "string",
  "buyer_name": "string",
  "buyer_phone": "string",
  "amount": number,
  "admin_id": "string"
}
```

### Check Status
- Endpoint: `${API_BASE_URL}/check_status`
- Method: POST
- Payload:
```json
{
  "order_id": "string"
}
```

## WebSocket Events

Connects to: `wss://zenopay-annual-meeting.onrender.com/ws`
Handles real-time payment status updates.

## Setup

1. Clone repository
2. Update API endpoint if needed
3. Deploy to web server
4. Configure CORS if required

## Usage

1. Fill customer details
2. Select payment plan
3. Submit payment
4. Complete payment on mobile device
5. Wait for confirmation

## Error Handling

- Form validation errors
- API communication errors
- Payment processing errors
- WebSocket connection issues

## Security

- Input validation
- Secure WebSocket connection
- API error handling
- Phone number format validation

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)