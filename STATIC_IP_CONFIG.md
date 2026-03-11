# Static IP Configuration for TokoCrypto API

## Dedicated Static IP (Outbound Traffic)
- **IP Address**: `167.88.158.82`
- **Type**: Dedicated IPv4 ($2/month)
- **Region**: Singapore (sin)
- **Purpose**: TokoCrypto API access

## Ingress IP (Incoming Traffic)
- **IP Address**: `149.248.219.252`
- **Type**: Dedicated IPv4 ($2/month)
- **Purpose**: Public access to proxy server

## TokoCrypto API Configuration
Add these IPs to TokoCrypto API whitelist:

1. **Outbound IP**: `167.88.158.82` (for API calls)
2. **Ingress IP**: `149.248.219.252` (if needed)

## Verification
```bash
# Test outbound IP
curl -s https://skybot-proxy.fly.dev/api/v1/time

# Check current IP
curl -s http://ipinfo.io/ip
```

## Cost
- 2x Dedicated IPv4: $4/month total
- Static IP ensures consistent API access
