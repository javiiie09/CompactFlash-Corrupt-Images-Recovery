# CompactFlash Corrupt (Recover images)

A tool made for linux to recover images from CF or other kind of memories when they get corrupted and you can't access the files.

You have to create an image (compress file) of the card and give it it to the program.
On linux, you can use de command: ```bash dd if=/dev/{card root} of=image.img bs=512.```
Usually, or in my case the card root was /dev/sdb.

Once the command has finish, it will take more or less depending on the size of the card, you have to compile the program in this repository (RecoverCF.c),
on linux: ```bash gcc RecoverCF.c -o RecoverCF```

Then take the image created before and the compiled program into a folder to extract the pictures.
```bash ./RecoverCF image.img```

The program will automatically extract all the files that it find in the compress image.

Credits: https://homes.cs.washington.edu/~oskin/saveimg.html
