# Hexdump – Learning Summary (Cybersecurity)

This document summarizes what I learned about *hexdump and hexadecimal analysis* as part of my cybersecurity learning journey.  
Hexdump is a foundational skill for understanding how data is actually stored and processed at the binary level.

---

## 1. What Is Hexdump?
Hexdump is a method of viewing *raw binary data* in a *hexadecimal (base-16)* format along with its ASCII representation.

It helps reveal:
- Actual byte-level data
- Hidden or misleading file content
- Binary structures that normal tools abstract away

Hexdump shows *what the system sees*, not what the file extension claims.

---

## 2. Hexadecimal Basics
- Hexadecimal is *base-16*
- Digits used: 0–9 and A–F
- 0x prefix means the number is written in hexadecimal
- *2 hex digits = 1 byte*

Examples:
- 0x12 → 1 byte  
- 0x12345678 → 4 bytes  

---

## 3. ASCII and Hex Relationship
Characters are stored as *ASCII numeric values*, which appear as hex in hexdumps.

Examples:
- A → ASCII 65 → 0x41
- a → ASCII 97 → 0x61
- 0 → ASCII 48 → 0x30

Important:
> Characters are *encoded numbers*, not their visual symbols.

---

## 4. Meaning of 0x12345678
- 0x indicates hexadecimal notation
- 12345678 are hex digits
- Represents a *single numeric value*, often used as:
  - Memory addresses
  - File offsets
  - Integer values

Byte representation:


## 5. MSB and LSB (Significance)
- *MSB (Most Significant Byte)*: leftmost byte
- *LSB (Least Significant Byte)*: rightmost byte

For 0x12345678:
- MSB = 12
- LSB = 78

Rule:
> Significance depends on value contribution, not memory order.

---

## 6. Endianness
Endianness defines *byte order in memory* for multi-byte data.

### Big-endian
- MSB stored first
- Used in network byte order

### Little-endian
- LSB stored first
- Used by x86 systems (Linux, Windows)

Important notes:
- Endianness applies only to *multi-byte values*
- ASCII characters (1 byte) are not affected

---

## 7. Tools Learned

| Tool | Purpose |
|----|----|
| hexdump | Raw byte-level view |
| xxd | Beginner-friendly hex + ASCII view |
| strings | Extract readable text from binaries |
| file | Identify file type using magic numbers |
| objdump | Binary and assembly analysis |
| Wireshark | Packet-level hex inspection |

---

## 8. Why Hexdump Matters in Cybersecurity
Hexdump is essential for:
- Malware analysis
- Digital forensics
- File type verification
- Packet inspection
- Exploit development
- Understanding memory layouts

---

## 9. Key Takeaways
- Hexdump shows *bytes, not files*
- 0x indicates hexadecimal
- ASCII characters are numeric encodings
- MSB/LSB never change — storage order can
- Endianness must always be considered
- File extensions can lie; bytes do not

---

## Final Thought
> If you can read hex, you can understand what the system is really doing.

This knowledge forms the base for advanced topics such as reverse engineering, exploit development, and malware analysis.

## Basic Hexdump Commands 

hexdump -C file.bin
hexdump -C -n 64 file.bin
hexdump -C -s 128 file.bin
hexdump -C -s 128 -n 64 file.bin
hexdump -v -e '1/1 "%02x "'
echo "Hello" | hexdump -C
hexdump -C file.bin | head
hexdump -C file.bin | tail
xxd file.bin
strings file.bin
file file.bin
