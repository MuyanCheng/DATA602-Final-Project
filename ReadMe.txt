get_id.py and Get_ID_Cleaned.jpynb are the same in concept but I have removed all the unnessary code from get_id.py to obtain Get_ID_Cleaned.jpynb
	Get the list of zip code from www.ciclt.net and store them in a list
	Use the list of Zip codes to obtain the list of Vehicle IDs
	Remove all the dupilcated vehicle IDs and store them in a txt file
detail.py and detail_Cleaned.jpynb are again, the same in concept and detail_Cleaned.jpynb is the cleaned version of detail.py
	Read in the txt file containing all the vehicle IDs
	Write the details into a csv file to be processed. 
The raw training data is stored in these csv files: data1.csv, data2.csv, data3.csv, data4.csv, data5.csv, data6.csv.
Final_Preprocessing.ipynb is used to preprocess the this raw data. During preprocessing, it:
	performs EDA on the dataset.
	fill the missing value, creates data_afterFillna.csv file.
	implements normalization, creates data_afterNorm.csv file.
	encodes all the categorical features, creates data_forModel.csv file.
Final_Buildingmodel.ipynb is used to build a model and train the model. It:
	builds a neural network with linear, normalization, dropout layers, and uses residual connection.
	uses AdamW to optimize this neural network with learning_rate = 0.02 and learning rate decay.
	trains this model for 2000 epoches, creates the plots to show how MSE loss changes over epoches.
	save the model parameters in model_dict.pt file.
Final_MakePrediction&Dashboard.ipynb is used to make predictions over the test data full_test_data.csv and create a dashboard. It:
	creates a function to preprocesses the test data.
	builds a neural network and load the parameters from model_dict.pt.
	uses this model to make predictions on the test data.
	creates a dashboard to show statistics information of the dataset, the model performance, and can predicts car price based on specific inputs.
These codes read and write lots of files, please make sure that the file paths are correct when running them.
