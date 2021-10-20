## Device Main LED - Command Pair
### Get LED Status
> Command:

```plaintext
MCU+PAS+RAKOIT:LED&:
```

> Example Response:

```plaintext
MCU+PAS+LED:0&                      // LED Disabled
MCU+PAS+LED:1&                      // LED Enabled
```

This command will return a boolean state of the LED Enable/Disable Function.

Command: `MCU+PAS+RAKOIT:LED&`

Response: <br>`MCU+PAS+RAKOIT:LED:0&` LED Disabled<br>`MCU+PAS+RAKOIT:LED:1&` LED Enabled

<br><br><br>

### Set LED Status
>Command:

```plaintext
MCU+PAS+RAKOIT:LED:0&       // Disable LED
MCU+PAS+RAKOIT:LED:1&       // Enable LED
MCU+PAS+RAKOIT:LED:T&       // Toggle current LED status
```

> Example Response:

```plaintext
MCU+PAS+RAKOIT:LED:0&              // LED Disabled
MCU+PAS+RAKOIT:LED:1&              // LED Enabled
```

Enables & Disables device main LED. 

Command: `MCU+PAS+RAKOIT:LED:<bool_or_toggle>&`

Value | Description
---|---|---
`0` |  Enable
`1` |  Disable
`T` |  Toggle current LED status
<br>

Response: <br>
`MCU+PAS+RAKOIT:LED:0&` LED Disabled<br>
`MCU+PAS+RAKOIT:LED:1&` LED Enabled

