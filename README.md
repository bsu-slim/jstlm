### Java Suffix Tree Language Model

- Has several smoothing methods available, please look at extendsiong of the Smoothing class

### Installation and Usge

To run, use the command line arguments:

-text /path/to/training/file 
-test /path/to/eval/file 
-perp 

When -perp is present, it prints the perplexity of the entire corpus; when not, it prints the logProb for each sentence in the -test file.

### Extending the STLM

Other programs can use the STLM by making a SuffixTree<T> object and putting that as the only argument into a STLanguageModel<T> constructor. The T can be anything, though you MUST implement
a equals() method otherwise objects that appear the same might be treated as different (i.e., in HashMaps, etc.). 

For an example, open up STLM.java and see how a SuffixTree is trained, either line by line or individually. 

### References

If you find this useful, please cite the following paper:

```
@InProceedings{KENNINGTON12.649,
  author = {Casey Redd Kennington and Martin Kay and Annemarie Friedrich},
  title = {Suffix Trees as Language Models},
  booktitle = {Proceedings of the Eight International Conference on Language Resources and Evaluation (LREC'12)},
  year = {2012},
  month = {may},
  date = {23-25},
  address = {Istanbul, Turkey},
  editor = {Nicoletta Calzolari (Conference Chair) and Khalid Choukri and Thierry Declerck and Mehmet Uğur Doğan and Bente Maegaard and Joseph Mariani and Asuncion Moreno and Jan Odijk and Stelios Piperidis},
  publisher = {European Language Resources Association (ELRA)},
  isbn = {978-2-9517408-7-7},
  language = {english}
 }
```

