# Take Home Exam
TM Natalia Khaidanova (2778662)

- save_munual_examples.py contains code for saving the test instances defined in the file and their gold labels as .json files. The output is four .json test files: 
Caused-motion.json,
Polysemy.json, 
ARG0 idioms.json, and
ARG1 idioms.json.
Note! The files are saved to the Data folder. So make sure you have it, otherwise you need to adapt the code. 

- extend_some_examples.py contains code for extending the test instances defined in the file using Transformers fill-mask pipeline, and saving unique extended instances and their gold labels as .json files. The output is five .json test files: 
Instrument+Theme.json,
Benefactive.json,
Passive voice.json,
Left-out predicate.json, and
Left-out Theme.json.
Note! The files are saved to the Data folder. So make sure you have it, otherwise you need to adapt the code. 

- utils.py contains the code necessary to run save_munual_examples.py and extend_some_examples.py.

- test_models.py contains the code for evaluating the pretrained structured-prediction-srl-bert and structured-prediction-srl models on the defined .json test files. The output is the failure rate of each model for each .json test file, the number of fully correct predictions per .json test file. The test instances, gold labels, and predictions of each model are saved as new .json files. 
Note! The files are saved to the Output folder. So make sure you have it, otherwise you need to adapt the code. 

- error_analysis.py contains the code for performing basic error analysis. Note! The code makes use of the Output folder. So make sure you have it, otherwise you need to adapt the code. 

- Data folder contains .json test files that are outputs of the code defined in save_munual_examples.py and extend_some_examples.py. 

- Output folder contains .json test files with the predictions of the pretrained structured-prediction-srl-bert and structured-prediction-srl models.

Make sure you have installed the packages listed in requirements.txt. 

If you want to replicate the results, delete all files in the Output folder, run test_models.py and error_analysis.py. 

If you want to test the code, delete all files in the Data and Output folders, then run save_munual_examples.py, extend_some_examples.py, test_models.py, and error_analysis.py in the specified order. Note! The results will not be replicated as some .json test files in the Data folder were manually reduced or/and adapted before running test_models.py.  
