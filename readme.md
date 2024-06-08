## Attack Model Training and Evaluation

The four tasks are in four separate notebooks(membership_inference_task_cifar_res, membership_inference_task_cifar_mobilenetv2, membership_inference_task_tiny_res, membership_inference_task_tiny_mobilenetv2). Each of them follow the same structure:
- Data loading
    - Loading libraries
    - Mounting the drive (if using google colab)
    - Loading the shadow dataset and creating train and test dataloaders
- Shadow Model Training
    - Loading the target model and training on the shadow data
    - Loading already trained shadow model
    - Evaluating the shadow model on test data
- Attack Model Training
    - generating data for the attack model using the shadow model
    - training the attack model on the generated data
- Attack Model Evaluation
    - load the target model
    - load evaluation data
    - create evaluation dataset for attack model using the target model on the evaluation data
    - evaluate the attack model on the evaluation dataset
    - evaluate the attack model
    - save the trained attack model

## Generating Predictions on Test Data
To generate predictions on test data, I have used the notebook - test_output_generator. In the notebook there are four separate cells for generating test predictions for each of the tasks. Each section follows the same structure:            
- Data loading
- Target Model Loading
- Generating test dataset for attack model using the target model
- Loading the previously trained attack model
- Generating predictions on the test dataset
- Saving the predictions
