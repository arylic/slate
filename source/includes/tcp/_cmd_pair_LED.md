## Device Main LED
### Get LED Status

> Command:

```plaintext
MCU+PAS+RAKOIT:LED&:
```

> Example Response:

```plaintext
MCU+PAS+LED:0&              // LED Disabled
MCU+PAS+LED:1&              // LED Enabled
```

This command will return a boolean state of the LED Enable/Disable Function.

<br><br><br><br><br><br><br>

### Set LED Status

> Command:

```plaintext
MCU+PAS+RAKOIT:LED:0&       // Disable LED
MCU+PAS+RAKOIT:LED:1&       // Enable LED
MCU+PAS+RAKOIT:LED:T&       // Toggle current LED status
```

> Example Response:

```plaintext
MCU+PAS+LED:0&              // LED Disabled
MCU+PAS+LED:1&              // LED Enabled
```

Enables & Disables device main LED. 

Parameter | Description
---|---|---
`0` | Disable
`1` | Enable
`T` | Toggle current LED status
