### The developed scripts are described here
`set PYTHONPATH=C:\temp\CA\2B\src` This is to set the execution directory for all the commands

#### Scripts for overall, model and expert system evaluation
1. `CampaignOutcome.py`: Usage: `python CampaignOutcome.py "original_data\cust_actual_merged.csv\" cust_actual_merged_best` will sort the input data with the status and the score columns, 
generated from the classification model and expert system respectively and select the top 400 customers to be targeted for the campaign. 
The file is generated in the `results` folder with the list of 400 customers.

2. `Results_Evaluate.py`: Usage:`python Results_Evaluate.py results\cust_actual_merged_best.csv` will compare the status and the scores from the input file and generate a confusion matrix and mean absolute error respectively. 
It also generates a CSV file inside `results` folder that has the difference for each record in the input.

#### Notebook to generate test predictions (on the list of 4000 records)
1. The notebook `5.TestPredictions.ipynb` will generate the predictions for the product to be purchased by the 4000 customers. 
The `model_to_use` parameter in the second cell needs to be provided which is the H5 file storing the trained model.

Best profit attainable: 1238 - customer details here: KE5108-CA1-Part2\results\best_possible_campaign.csv