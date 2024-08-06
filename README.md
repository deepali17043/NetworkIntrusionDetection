# Network Intrusion Detection
Perform and evaluate Binary and Multi-Class Classification on the dataset: https://www.kaggle.com/datasets/aryashah2k/nfuqnidsv2-network-intrusion-detection-dataset/code

# Steps to run on Google Cloud
1. Upload the [dataset](https://drive.google.com/file/d/1Rru_t3Sgl415XyhKbu9iRvLl4-xTcXQQ/view?usp=sharing) to your bucket.
2. Create a folder for storing the outputs.
3. Upload the python-scripts to the bucket.
4. Create a cluster with the following configuration: ![cluster_config.png](https://github.com/deepali17043/NetworkIntrusionDetection/tree/main/images)
5. Submit a job with the python-script `project.py` and arguments:  
   i. gs link for dataset  
   ii. gs link for folder you created in step 2  
   Note: This run takes about 8 hours because of the size of the dataset.
7. Once the job is complete submit another job with the script `project_evaluating_models.py` and the same arguments as before.

# Steps to generate a sample of dataset
1. Open [ipynbs/generate_small_data.ipynb](https://github.com/deepali17043/NetworkIntrusionDetection/blob/main/ipynbs/generate_small_data.ipynb)
2. Update the sample fraction
3. Run the cells up to the cell `spark.stop()`
4. Verify that the samples are created in parts
5. update `file_path` if necessary
6. Run the remaining cells.
