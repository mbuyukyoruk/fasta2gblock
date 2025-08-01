# fasta2gblock

A web-based tool to convert FASTA sequences into tiled fragments for gene block (gBlock) synthesis. The tool reads a FASTA file or manually entered sequence and generates overlapping fragments of user-specified length and overlap. The output is provided in FASTA format, with options to copy to the clipboard or download as a file.

**Live URL**: [https://mbuyukyoruk.github.io/fasta2gblock/](https://mbuyukyoruk.github.io/fasta2gblock/)

## Preview

![workflow](image.png)

## Features
- **Input**: Paste a FASTA sequence or upload a `.fasta`, `.fa`, or `.txt` file.
- **Customizable Parameters**: Specify fragment length, overlap length, and fragment prefix.
- **Output Options**: View tiled fragments in the browser, copy to clipboard, or download as a FASTA file.
- **Adjust overlaps to achieve user-specified GC content.**
- **Avoid long repeats in fragments.**
- **Incorporate homology to vector sequences for overlap design.**

## Usage
1. Visit [https://mbuyukyoruk.github.io/fasta2gblock/](https://mbuyukyoruk.github.io/fasta2gblock/).
2. **Input a Sequence**:
   - Paste a FASTA sequence into the text area.
   - Or upload a FASTA file using the "Choose File" button.
3. **Configure Parameters**:
   - **Fragment Length**: Set the desired length of each fragment (default: 1000 bp).
   - **Overlap Length**: Set the overlap between fragments (default: 50 bp).
   - **Fragment Prefix**: Customize the prefix for fragment headers (default: "Fragment").
4. **Process and Output**:
   - Click "Process FASTA" to generate tiled fragments.
   - View the output in the browser.
   - Use "Copy to Clipboard" or "Download FASTA" to save the results.

## Example
**Input FASTA**:
```
>Sequence1
tttctttttcaacatcggctttgttaagccctaaagtatttaatttcataagatatttgtttttaaaattctac
gccgcaaaggtacgccattttttgctgaaaagaacgccataacgatagatatttctaattttagaataagcaaa
cattttgctactttattaaaaatactgcaattatatcttcagtacagaaaggatatataatggatataggaaga
atacaggaagcctcaacaaaatctattatcaaatcagcaacaaaaatatcgaaacattgcaaataatgcaatac
cacttctactactcccactcgtcccacttgtctcacctgtcccactcgtcttactaacgaaaatcaaaaataca
agcaacaaactcacattagtgaaaatatagtaattttgttttttagcaaaaagatgtatatttgcactttgttt
ttgaagaatgaatgtaaatatttgtaacatattaaatgtagaagtttcctttcaagaaaacacttggacagaga
ttactaaaaatatatccattcaacaagtgttaaatatcataaaaaaggaggaatataaaaatgtaataggaaaa
ttgcgtaatgaacttgaaaagggaaatatagaatattataatagcaataagaaaagattgccagctgttacctt
ttcaggaacatttaaaaagaaaagaactcttgattatattcaatcttataatcctattgttgttattgacatag
ataaattagataatgaggaacttgatagagtttatgatgtattagctaaagaaccctatgtacttagtttttgg
aaatcaccttcaaataaaggttttaaagggattgtacctctaaattataatactgatagtcaagattcaaactt
aattcataaatctgctttcgaaaaactatctgagtattttaaaaaagaacataatatagaacttgataagagtg
ggagcgatattacacgattatgttttatttcttctgataaagagttagttttaaaagaagaagttacttttttc
aaagttgaggatgaagatttattagataacaaaagtagtaaaactgatgaaaaaataaaacattatgttttgaa
attttctaataaaagagatgctttatataatcctaaaaataggaataaacctaaagacagaactgctatgtcga
atataattaaatatcttaaagttaaaaataaaagtataacctatagctatgccaattggtataaagtagctatg
ggaatagctaattcatttacatttgacatagggaaaaaatattttaacaaattaagtgctttagatgttggtaa
atacaattctattaattgtgaaaactttttaactgactgctatgaaatacgaaatggctctatcacgtttgcct
cgataatatatttagcaaatcagcaaggttataaaacaaaatctcaaaaaaataaaggggggttctgaagacgg
cggacaaaaacaactgtcgtaagtatcactccattaacggtaagttactgcctgagagcttaaaataggacata
aggcatatctatgtcagaatatttggtatgcaatatcaatagcgggaaccccctttattatctatgaaaccaat
agaagattttttatcagaaacagaaattataaaaagtatttgtaaaatcagagttaagctagctaagagtaggt
ctaaaaaacatttgttaaattacttaactaaaaatccaaaatataattatcatcaaagtattaaacttacaaat
gaattagaaaaacttcaatttgag
```
**Parameters**:
- Fragment Length: 100
- Overlap Length: 20
- Prefix: Fragment

**Output** (first three fragments for brevity):
```
>Fragment_1 [Sequence1 fragment 1-100]
tttctttttcaacatcggctttgttaagccctaaagtatttaatttcataagatatttgtttttaaaattctac
gccgcaaaggtacgccattttttgctga
>Fragment_2 [Sequence1 fragment 81-180]
ttttgctgaaaagaacgccataacgatagatatttctaattttagaataagcaaacattttgctactttattaa
aaatactgcaattatatcttcagtacag
>Fragment_3 [Sequence1 fragment 161-260]
cttcagtacagaaaggatatataatggatataggaagaatacaggaagcctcaacaaaatctattatcaaatca
gcaacaaaaatatcgaaacattgcaaat
```