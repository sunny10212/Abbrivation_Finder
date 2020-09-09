# Abbrivation_Finder
Here task is to implement few functions which find the abbreviations and short forms.
Write a function read_file(filename) that receives as input a filename. The filename
includes the filepath. The function returns the entire content of the file as a single string.
Write a function find_acronyms(s) that receives as input a string s representing the text.
The function returns a list of acronyms. For our example above, find_acronyms(s) returns
the list ['GPU', 'CPU', 'IT']. Note: It is not important in which order the acronyms
appear in the returned list.
Q1 b) Find the long forms (
In this question the hard work is done: given the acronyms, your task is to find their long
form in the text. To this end, write a function find_long_forms(s, acronyms). It receives
as input a string s representing the text and a Python list of acronyms. The function returns
a dictionary d with key-value pairs, where the key is the acronym and the value is its long
form. For instance, in our example above the output is the dictionary d = {'GPU' :
'graphics processing unit', 'CPU' : None, 'IT' : None}.
You can make the following assumptions:
• The long form is found in the same sentence as the acronym itself.
• If the acronym occurs multiple times in a text, its long form is found in the first
sentence that contains the acronym.
• Every '.' (dot) marks the end of a sentence. Sentences like "I talked to the Dr. and
raised my concerns." where dots are contained within the sentence will not occur.
• The first letter of the acronym is the same letter as the first letter of the first word of
the long form. All of the letters in the acronym need to appear in the long form.
• If no long form can be found for an acronym, it is set to None (Python's None type)
as in the dictionary above.
Four examples for texts with acronyms are given in the example files
acronym_example1.txt, acronym_example2.txt etc. The corresponding tuples
of (acronym, long form) are specified in the file acronym_tuples.txt.
Q1 c) Replace acronyms by long forms 
Assume we want to make the document more self-explanatory and replace its acronyms with
their corresponding long forms. To this end, write a function replace_acronyms(s, d). It
receives as input a string s representing the text, and a dictionary d which contains <acronym
: long_form> key-value pairs as defined in Q1b). The function returns another string as
output. In this output, all acronyms in s have been replaced with their long forms. The
following rules apply:
- If an acronym has a long form, the sentence wherein the long form was defined
remains unchanged. For any other sentence, the acronym is replaced by the long form.
- If an acronym has no long form, it is not replaced anywhere.
- If you add the long form at the beginning of a sentence, make sure that its first word is
capitalised.
For instance, in our example above the output of the function is the string:
"A GPU, which stands for graphics processing unit, is different from
CPUs, says the IT expert. For some operations, a graphics processing
unit is faster than a CPU. Graphics processing units are not always
faster though."
