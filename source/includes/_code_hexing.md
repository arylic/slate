# Hexed Values

> Convert a hexadecimal string representation in a human readable ASCII string.

```c
int hex_to_ascii(
    const char *pSrc, 
    unsigned char *pDst, 
    unsigned int nSrcLength, 
    unsigned int nDstLength)
{
	memset(pDst, 0, nDstLength);

	int i, j = 0;
    for (i = 0; i<nSrcLength; i+=2 ) {
		char val1 = pSrc[i];
		char val2 = pSrc[i+1];

		if ( val1 > 0x60)
			 val1 -= 0x57;
		else if (val1 > 0x40)
			 val1 -= 0x37;
		else
			val1 -= 0x30;
		
		if ( val2 > 0x60)
			val2 -= 0x57;
		else if (val2 > 0x40)
			val2 -= 0x37;
		else
			val2 -= 0x30;

		if (val1 > 15 || val2 > 15 || val1 < 0 || val2 < 0)
			return 0;

		pDst[j] = val1*16 + val2;
        j++;
	}

	return j;
}
```

> Convert a human readable ASCII string to a hexadecimal string representation.

```c
int ascii_to_hex(char* ascii_in, char* hex_out, int ascii_len, int hex_len) {
	const char hex[16] = {'0', '1', '2', '3', '4', '5', '6', '7', '8','9', 'A', 'B', 'C', 'D', 'E', 'F'};
	int i = 0;
	int ret = 0;
	
	memset(hex_out, 0, hex_len);

	while (i < ascii_len) {
		int b = ascii_in[i] & 0x000000ff; 
		hex_out[i * 2] = hex[b / 16];
		hex_out[i * 2 + 1] = hex[b % 16];
		
		++i;
		ret += 2;
	}
	
	return ret; 
}
```

As you may have noticed in some examples, there are certain values that need to be converted from a string to a hexadecimal value before sending to the API, or from a hexadecimal value to a human readable ASCII string after receiving a response. These values are marked with `[hexed string]`.

Here are two C functions, one to convert a hexadecimal string representation in a human readable ASCII string, and one function to do the opposide:
