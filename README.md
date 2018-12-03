# Grammar-Error-Detection-and-Classification
## Task Description  

## Detect the grammatical errors given the input sentences and classify them into an error type.  
 
### Task 1: Error Detection 
    - Given tokens of a sentence, determine if a grammatical error exists due to that token. 
 
### Task 2: Error Classification 

    - Once the error is detected in a sentence, you must classify this error into one of the 28 classes of error types. 
    Please find the description of error types in table 1 of the paper here
   
   
## Dataset description  
You are provided the following files
Data/ 
1) train.txt   
2) dev.txt 
3) dev_results.txt 
4) dev_correction_results.txt 

Each line in the data file contains a word, optionally it’s correction and the error category. 
  1) Each line in `train.txt` is of the form - Word [Correction] [ErrorCategory] 
  2) Each line in `dev.txt` is of the form - Word 
  3) Whereas, each line in `dev_results.txt` is of the form - Word [Error Category] 

Following instances occur in the files 
  1) If the correction replaces the original text at the given location, it should fix the grammatical error. 
    Example 
      - there 
      - are is SVA 
      - very 
      - limited 
      - spaces space Nn 
      - for 
      - us 
  2) But If the correction is `-`, deletion of Word should fix the grammatical error. 
     Example 
      - by 
      - achieving 
      - a 
      - better 
      - usage 
      - of 
      - the - ArtOrDet 
      - land 
  3) If the Word is `-` inserting the Correction in the original text would fix the error. 
    Example 
      - this 
      - _ has Vt 
      - caused 
      - problem problems Nn 
  4) In some sentences, corrections happen on a span of tokens. In this case, corrections and its types repeat until the phrase      with the error ends. 
     In this example, corrections for on, its, way, to are same. This means that the phrase “on its way to” must be replaced          with the correction “its process of” to fix the grammatical error. 
      - china 
      - has 
      - been 
      - eagerly 
      - speeding 
      - up 
      - on its process of Wci 
      - its its process of Wci 
      - way its process of Wci 
      - to its process of Wci 
      - industrialization 
