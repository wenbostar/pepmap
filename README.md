# pepmap: peptide mapping tool

![Downloads](https://img.shields.io/github/downloads/wenbostar/pepmap/total.svg) ![Release](https://img.shields.io/github/release/wenbostar/pepmap.svg)

## Usage

```
 $ java -jar pepmap.jar
usage: Options
 -d <arg>   database file
 -h         Help
 -i <arg>   peptide file, no header line
 -o <arg>   output file
```

### Example
```java
java -jar pepmap.jar -i example/pep.txt -d example/swissprot_human_07252018.fasta -o example/out.txt
```

The input file for parameter "-i" is a peptide file like below:
```
 $ cat example/pep.txt
QFALSGSWDGTLRLWDLT
EEDLKDMGIVSKGHIIHFKS
SKFHIIHGKSVIGMDKLDEE
```

The input file for parameter "-d" is a protein sequence file in fasta format like below:
```
 $ head example/swissprot_human_07252018.fasta
>sp|Q9H9K5|MER34_HUMAN Endogenous retroviral envelope protein HEMO OS=Homo sapiens OX=9606 GN=ERVMER34-1 PE=1 SV=1
MGSLSNYALLQLTLTAFLTILVQPQHLLAPVFRTLSILTNQSNCWLCEHLDNAEQPELVF
VPASASTWWTYSGQWMYERVWYPQAEVQNHSTSSYRKVTWHWEASMEAQGLSFAQVRLLE
GNFSLCVENKNGSGPFLGNIPKQYCNQILWFDSTDGTFMPSIDVTNESRNDDDDTSVCLG
TRQCSWFAGCTNRTWNSSAVPLIGLPNTQDYKWVDRNSGLTWSGNDTCLYSCQNQTKGLL
YQLFRNLFCSYGLTEAHGKWRCADASITNDKGHDGHRTPTWWLTGSNLTLSVNNSGLFFL
CGNGVYKGFPPKWSGRCGLGYLVPSLTRYLTLNASQITNLRSFIHKVTPHRCTQGDTDNP
PLYCNPKDNSTIRALFPSLGTYDLEKAILNISKAMEQEFSATKQTLEAHQSKVSSLASAS
RKDHVLDIPTTQRQTACGTVGKQCCLYINYSEEIKSNIQRLHEASENLKNVPLLDWQGIF
AKVGDWFRSWGYVLLIVLFCLFIFVLIYVRVFRKSRRSLNSQPLNLALSPQQSAQLLVSE
```

The output file is a txt file containing the mapping result like below:
```
 $ cat example/out.txt
peptide	protein
QFALSGSWDGTLRLWDLT	sp|P63244|RACK1_HUMAN
EEDLKDMGIVSKGHIIHFKS	sp|Q9NYL2|M3K20_HUMAN
```
