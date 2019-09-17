# PyMetaMap-Windows-support

Code taken from 'https://github.com/AnthonyMRios/pymetamap/tree/master/pymetamap' and modified
Very raw but working first version of the code. Below code does not work with sents, only works with files.

Changed the package to print the output to a file instead of returning concepts

from pymetamap import MetaMap

Have to get instance using 'metamap14.bat'        
Change .... in the below path to where your UMLS is installed        

mm=MetaMap.get_instance(r'....\UMLS\public_mm\bin\metamap14.bat')


filename = f, contains the text you need to classify/process        
output of the process will be written to out_filename        
All other options are still available to use as the standard package        

concepts, error=mm.extract_concepts(filename = f, out_filename = f + '_out')


You will always get an error and you can ignore with try except block
