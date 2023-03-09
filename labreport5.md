# Lab Report 5

In enjoyed lab report 3 and researching various options to a command so for this lab I will be researching options for the `grep` command

# Option 1: `grep -H`

Source: [grep manual](https://man7.org/linux/man-pages/man1/grep.1.html)

**Example 1**
```
grep -H Paris ch1.txt
```
**Output:** 
```
ch1.txt:For our purposes, we can represent growing product diversity in the form of a “fashion triangle” (Figure 1.1). Apparel items at the very top of this triangle include dresses from Paris, Milan, and New York runways, which represent a very small share of apparel sold. The majority of fashion products also have a short selling life—usually one season—but are produced for a broader market. At the triangle’s bottom are basic products that remain in a retailer’s or manufacturer’s collection for several years, such as men’s white dress shirts or underwear. Basics -historically constituted the majority of apparel products sold. In the middle of the triangle are fashion-basic products, typically variants on a basic item but containing some fashion element (such as stonewashed jeans or khaki pants with pleats or trim). This expanding center of the fashion triangle indicates where the industry is headed. Because a growing percentage of basic apparel items have some fashion content, fashion-basic products are driving product proliferation.
```

This command is looking in the directory `written_2/non-fiction/OUP/Abernathy` and looking for the word Paris in the file named "ch1.txt." This command is helpful because it allows us to display the file name that we are searching in in the output.

**Example 2**
```
grep -H Milan ch1.txt
```
**Output:** 
```
ch1.txt:For our purposes, we can represent growing product diversity in the form of a “fashion triangle” (Figure 1.1). Apparel items at the very top of this triangle include dresses from Paris, Milan, and New York runways, which represent a very small share of apparel sold. The majority of fashion products also have a short selling life—usually one season—but are produced for a broader market. At the triangle’s bottom are basic products that remain in a retailer’s or manufacturer’s collection for several years, such as men’s white dress shirts or underwear. Basics -historically constituted the majority of apparel products sold. In the middle of the triangle are fashion-basic products, typically variants on a basic item but containing some fashion element (such as stonewashed jeans or khaki pants with pleats or trim). This expanding center of the fashion triangle indicates where the industry is headed. Because a growing percentage of basic apparel items have some fashion content, fashion-basic products are driving product proliferation.
```

This command is looking in the directory `written_2/non-fiction/OUP/Abernathy` and looking for the word Milan in the file named "ch1.txt." This command is helpful because it allows us to display the file name that we are searching in in the output.

# Option 2: `grep -n`

Source: [grep manual](https://man7.org/linux/man-pages/man1/grep.1.html)

**Example 1**
```
grep -n Paris ch1.txt
```
**Output:** 
```
33:For our purposes, we can represent growing product diversity in the form of a “fashion triangle” (Figure 1.1). Apparel items at the very top of this triangle include dresses from Paris, Milan, and New York runways, which represent a very small share of apparel sold. The majority of fashion products also have a short selling life—usually one season—but are produced for a broader market. At the triangle’s bottom are basic products that remain in a retailer’s or manufacturer’s collection for several years, such as men’s white dress shirts or underwear. Basics -historically constituted the majority of apparel products sold. In the middle of the triangle are fashion-basic products, typically variants on a basic item but containing some fashion element (such as stonewashed jeans or khaki pants with pleats or trim). This expanding center of the fashion triangle indicates where the industry is headed. Because a growing percentage of basic apparel items have some fashion content, fashion-basic products are driving product proliferation.
```

This command is looking in the directory `written_2/non-fiction/OUP/Abernathy` for the word Paris in the file "ch1.txt." This option displays the line number in the output and is helpful because it tells us exactly what line the word we are looking for is on.

**Example 2**
```
grep -n Milan ch1.txt         
```
**Output:** 
```
33:For our purposes, we can represent growing product diversity in the form of a “fashion triangle” (Figure 1.1). Apparel items at the very top of this triangle include dresses from Paris, Milan, and New York runways, which represent a very small share of apparel sold. The majority of fashion products also have a short selling life—usually one season—but are produced for a broader market. At the triangle’s bottom are basic products that remain in a retailer’s or manufacturer’s collection for several years, such as men’s white dress shirts or underwear. Basics -historically constituted the majority of apparel products sold. In the middle of the triangle are fashion-basic products, typically variants on a basic item but containing some fashion element (such as stonewashed jeans or khaki pants with pleats or trim). This expanding center of the fashion triangle indicates where the industry is headed. Because a growing percentage of basic apparel items have some fashion content, fashion-basic products are driving product proliferation.
```

This command is looking in the directory `written_2/non-fiction/OUP/Abernathy` for the word Milan in the file "ch1.txt." This option displays the line number in the output and is helpful because it tells us exactly what line the word we are looking for is on.

# Option 3: `grep -c`

Source: [grep manual](https://man7.org/linux/man-pages/man1/grep.1.html)

**Example 1**
```
grep -c Milan ch1.txt
```
**Output:** `1`

This command is looking in the directory `written_2/non-fiction/OUP/Abernathy` for the word Milan in the file "ch1.txt." This option is useful because it tells us how many occurrences the word has.

**Example 2**
```
grep -c Paris ch1.txt
```
**Output:** `1`

This command is looking in the directory `written_2/non-fiction/OUP/Abernathy` for the word Paris in the file "ch1.txt." This option is useful because it tells us how many occurrences the word has

# Option 4: `grep -o`

Source: [grep manual](https://man7.org/linux/man-pages/man1/grep.1.html)

**Example 1**
```
grep -o Paris ch1.txt
```
**Output:** `Paris`

This command is looking in the directory `written_2/non-fiction/OUP/Abernathy` for the word Paris in the file "ch1.txt." This option is useful because it displays just the occurrences of the word instead of displaying an entire paragraph.

**Example 2**
```
grep -o proliferation ch1.txt
```
**Output:** 
```
proliferation
proliferation
proliferation
proliferation
proliferation
proliferation
```

This command is looking in the directory `written_2/non-fiction/OUP/Abernathy` for the word "proliferation" in the file "ch1.txt." This option is useful because it displays just the occurrences of the word instead of displaying an entire paragraph.
