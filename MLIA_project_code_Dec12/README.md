# MLIA_Project_Segnet


How to run =============
● Ensure that you are using a powerful machine with the required computational power.
● We used a Rivanna instance with 4 NVIDIA A100 GPUs and 200 GB memory.
● Make sure all the python notebook code files are in the same folder
● In any one folder create the directory structure as follows
____ mlia __________ data_imgs_aug __________________ train
        |               |____________ test
        |               |____________ trainannot
        |               |____________ testannot
        |               |____________ testNoLabel 
        |_______ results
createDirectories.ipynb may be used for this after changing the base path in each mkdir command line from /home/ufh6ft.
● If you do not wish to train the model (only test it), then place the provided pre-trained model file in the results folder and after that run the MLIA_test_only.ipynb.
If you wish to train the model and then test it. Then skip this step and continue with the steps below.
●
In all 5 code python notebooks (MLIA_read_training_data.ipynb, MLIA_read_test_data.ipynb, MLIA_read_noLabel_test_data.ipynb, MLIA_gray.ipynb, MLIA_test_only.ipynb) change the values assigned to these 2 variables (if present); t4_data_path and write_to_path.
They have these values.
write_to_path = "/home/ufh6ft"
t4_data_path = "/project/mlia"
Change the value of t4_data_path to the folder with the T4_Data folder (folder of data samples provided) in it.
Change write_to_path to the directory where you created the directory structure in step 2.
●
Run the python notebooks in this order
MLIA_read_training_data.ipynb MLIA_read_test_data.ipynb MLIA_read_noLabel_test_data.ipynb MLIA_gray.ipynb MLIA_test_only.ipynb
The results are visible in the outputs for MLIA_test_only.ipynb.
MLIA_read_training_data.ipynb should take ~15 minutes to run and MLIA_gray.ipynb should take less than 1.5 hrs to run with 4 NVIDIA A100 GPUs and 200 GB memory. All other files should take less than a minute to run.
