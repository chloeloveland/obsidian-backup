Cache memory is a high-speed, low-capacity [[memory]] which is used within the [[CPU]]. It allows faster operation by placing commonly accessed data close to the rest of the CPU.

> [!Info] Principle of locality
> If a particular storage location is referenced, it is likely that nearby memory location will be referenced soon

## Direct mapped cache
- The simplest cache is <mark class="hltr-orange">**direct-mapped**</mark>
- If a byte is present in cache, it can only be in **one place**
- Cache contains 2k lines/entries
- Each line contains 32 bytes of data
- Each line also contains a <mark class="hltr-yellow">16 bit TAG</mark> and <mark class="hltr-green">1 validation bit</mark>
- The <mark class="hltr-green">validation bit</mark> is 1 if there is <mark class="hltr-green">real data</mark> in that line
- The <mark class="hltr-yellow">TAG</mark> contains the 16 most significant bits of the actual address of the data contained in that line

