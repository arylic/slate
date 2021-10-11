# TCP API

Welcome to Arylic's TCP API developer documentation.  

MCU+PAS+RAKOIT:{message:param}&	

All commands are terminated with the special character `&`

Some Commands are Command Pairs where the same 3 character code `ABC` can be used for query/read or control/write
    `MCU+PAS+RAKOIT:ABC&` - Query or Read Values
    `MCU+PAS+RAKOIT:ABC:{parameter}&` - Control Functions or Write Values 