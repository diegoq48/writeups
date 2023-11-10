**Matryoshka Doll Forensics Challenge by SUSIE/PANDU:**

The challenge involves analyzing a set of wooden Matryoshka dolls, each containing hidden files. The initial image, "dolls.jpg," is downloaded from a provided link.

1. **Extraction Process:**
   - Use binwalk to extract hidden files: `binwalk -e dolls.jpg`.
   - Explore the extracted directory, finding "2_c.jpg" in the "base_images" folder.
   - Repeat the process on "2_c.jpg" to reveal "3_c.jpg" in a nested "base_images" directory.
   - Once again, apply binwalk to extract files, discovering "4_c.jpg" in the nested structure.

2. **Final Extraction:**
   - Use binwalk on "4_c.jpg" to uncover a compressed file, eventually revealing "flag.txt."
   - Open "flag.txt" to obtain the flag: `picoCTF{ac0072c423ee13bfc0b166af72e25b61}`.

The challenge mimics the nesting nature of Matryoshka dolls, leading to a progressively revealing extraction process.
