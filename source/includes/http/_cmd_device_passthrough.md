## Passthrough Command

It is used to forward message from HTTP to MCU, to make it possible to send direct command to the board directly. And the sub commands are same with the commands sending over TCP or UART. 

> Request format:

```html
GET /httpapi.asp?command=passthrough:<data>
```

### Parameter Description

`data` is descripted by following

Data | Description
---|---
`RAKOIT:THI:<N>`| set TREBLE tone, `<N>` range from 0~200, the real dB value is (N-100)/10.
`RAKOIT:TMI:<N>`| set MID tone, `<N>` range from 0~200, the real dB value is (N-100)/10.
`RAKOIT:TLO:<N>`| set BASS tone, `<N>` range from 0~200, the real dB value is (N-100)/10.
`RAKOIT:VBS:<N>`| set Virtual Bass enable, `<N>` range 0~1, 
`RAKOIT:EQS:<S>`| set different EQ, `<S>` could be FLAT ...
`RAKOIT:MXV:<N>`| set max volume, `<N>` range 30~100
`RAKOIT:BAL:<N>`| set balance, `<N>` range 0~200, the real value of balance is N-100
`RAKOIT:VOF:<N>`| set fixed volume, `<N>` range 0~1
`RAKOIT:LED:<N>`| set LED enable, `<N>` range 0~1
`RAKOIT:BEP:<N>`| set Beep sound enable, `<N>` range 0~1
`RAKOIT:AOM:<M>`| set Audio output mode, `<M>` could be Stereo, Mono Left, Mono Right, Mono Mixed

