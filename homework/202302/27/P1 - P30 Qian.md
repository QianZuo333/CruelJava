# 万物到C，C到汇编，汇编到机器。


# What is CS Register? What exactly is inside it? Here is a snnipet code, show me what is inside it?
```
_start:
    mov eax, 1
    xor ebx, ebx
    int 0x80

```

```
The contents of the CS register depend on the specific execution environment and operating system that is running the program. In this example, assuming that the program is running in a 32-bit Linux environment, the CS register might contain the following values:

Selector index: 0x001b
Requested privilege level: 0x03
Descriptor type: 0x08
Descriptor privilege level: 0x00
Present: 0x01
Available: 0x01
Long mode: 0x00
Default operand size: 0x01
Granularity: 0x01
Base address: 0xc0000000
```
