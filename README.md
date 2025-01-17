# Origin-of-Replication
<b><i>Definition of the functions used:</i></b>

1. <b><i>PatternCount</i></b>: Program to check how many times a <b>Pattern</b> appears in a <b>Text</b>

2. <b><i>FrequentWords</i></b>: Program to find the most frequent kmers <b>k</b> appearing in <b>Text</b>

3. <b><i>ReverseComplement</i></b>: Program to find the reverse complement of <b>dna</b>

4. <b><i>PatternMatching</i></b>: Program to find the starting positions of the <b>Pattern</b> in the <b>Genome</b>

5. <b><i>FindClumps</i></b>: 

We can define a k-mer as a "clump" if it appears many times within a short interval of the genome. A k-mer pattern of length <b>k</b> forms an <b>(L, t)</b> clump inside a longer string Genome <b>(Text)</b> if there is an interval of Genome of length L in which this k-mer appears at least t times
It uses the <b>Frequency Table</b> function to find the frequency of kmer of length <b>k</b> in a window of length <b>L</b>

6. <b><i>skew</i></b>: 

Skew of the genome is the difference between the total number of occurrences of G and the total number of occurrences of C. The skew diagram is defined by plotting Skew(i) (Genome) (as i ranges from 0 to |Genome|), where Skew(0) (Genome) is set equal to zero. If this nucleotide is G, then Skew(i+1)(Genome) = Skew(i)(Genome) + 1; if this nucleotide is C, then Skew(i+1)(Genome)= Skew(i)(Genome) – 1; otherwise, Skew(i+1)(Genome) = Skew(i)(Genome)
Reverse half strand = Leading strand
Forward half strand = Lagging strand
It is observed that the skew is decreasing along the reverse half-strand and increasing along the forward half-strand. Thus, the skew should achieve a minimum at the position where the reverse half-strand ends and the forward half-strand begins, which is exactly the location of ori!

7. <b><i>HammingDistance</i></b>: Program to find the number of mismatches (position wise) between two same length strings

8. <b><i>ApproximatePatMatch</i></b>: Program to find all starting positions where <b>Pattern</b> appears as a substring of <b>Text</b> with atmost <b>d</b> mismatches

9. <b><i>Neighbors</i></b>: Program to generate the set of all k-mers whose <b>Hamming distance</b> from <b>Pattern</b> does not exceed <b>d</b>

10. <b><i>FrequentWordsWithMismatches</i></b>: A better program than <b>ApproximatePatMatch</b> to count the number of times a given string has an approximate match in <b>Text</b>. For a given k-mer substring Pattern of <b>Text</b>, we need to increase 1 to the count of every k-mer of length <b>k</b> that has Hamming distance at most <b>d</b> from Pattern

11. <b><i>CountWithMismatches</i></b>: Program to count the number of times a <b>Pattern</b> appears in <b>Text</b> with <b>d</b> number of mismatches

12. <b><i>FrequentWordsWithMismatchesAndReverseComplement</i></b>: Program to find the most frequent k-mers <b>k</b> (with matches and reverse complements) in a <b>Text</b> with <b>d</b> number of mismatches

13. <b><i>FinalOri</i></b>: This program is the same as <b><i>FrequentWordsWithMismatchesAndReverseComplement</i></b> but the search is within a given <b>window_size</b> and a given <b>start_position</b>. This narrows down the search and makes the program faster