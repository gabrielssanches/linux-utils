## GRUB Select Kernel

run

```bash
grub-mkconfig | grep -iE "menuentry 'Ubuntu, with Linux" | awk '{print i++ " : "$1, $2, $3, $4, $5, $6, $7}'
```

then, in /etc/default/grub modify the GRUB_DEFAULT=0 value as per your need.

e.g.: to select list item 4

```bash
GRUB_DEFAULT="1>4"
```
