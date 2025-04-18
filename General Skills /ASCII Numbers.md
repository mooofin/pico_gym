# PicoCTF Writeup: ASCII Hex Decoding

## Challenge Description
We were given a string of hexadecimal ASCII values and asked to convert it into a readable flag.

### Given Data:
```
0x70 0x69 0x63 0x6f 0x43 0x54 0x46 0x7b 0x34 0x35 0x63 0x31 0x31 0x5f 0x6e 0x30 
0x5f 0x71 0x75 0x33 0x35 0x37 0x31 0x30 0x6e 0x35 0x5f 0x31 0x6c 0x6c 0x5f 0x74 
0x33 0x31 0x31 0x5f 0x79 0x33 0x5f 0x6e 0x30 0x5f 0x6c 0x31 0x33 0x35 0x5f 0x34 
0x34 0x35 0x64 0x34 0x31 0x38 0x30 0x7d
```

## Solution
To decode the flag, we need to convert each hexadecimal number to its ASCII character representation.

### **Python Script for Decoding**
```python
hex_values = [
    0x70, 0x69, 0x63, 0x6f, 0x43, 0x54, 0x46, 0x7b, 0x34, 0x35, 0x63, 0x31, 0x31, 0x5f, 0x6e, 0x30,
    0x5f, 0x71, 0x75, 0x33, 0x35, 0x37, 0x31, 0x30, 0x6e, 0x35, 0x5f, 0x31, 0x6c, 0x6c, 0x5f, 0x74,
    0x33, 0x31, 0x31, 0x5f, 0x79, 0x33, 0x5f, 0x6e, 0x30, 0x5f, 0x6c, 0x31, 0x33, 0x35, 0x5f, 0x34,
    0x34, 0x35, 0x64, 0x34, 0x31, 0x38, 0x30, 0x7d
]

decoded_string = ''.join(chr(h) for h in hex_values)
print(decoded_string)
```

### **Decoded Flag**
```
picoCTF{45c11_n0_qu35710n5_1ll_t311_y3_n0_l135_445d4180}
```



**Flag:** `picoCTF{45c11_n0_qu35710n5_1ll_t311_y3_n0_l135_445d4180}` 🚩
