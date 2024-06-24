


The model overview page displays real-time progress of the Fine-tuned models. 

To access the model’s overview page,  go to  **Models** > **Fine-tuned models** and click any model.

The overview page displays the following information:



* **General Information**: [This displays the model's progress status, Total time, and Author details. It also allows you to stop the fine-tuning process.](https://galeadmin-kore.github.io/docs/gale/models/fine-tune-models/images/initializing-status.png)
    * The progress statuses include Initializing, Training in progress, Testing in progress, Fine-tuning completed, Stopped, and Failed. \
**Note**: If fine-tuning fails, the status changes to "Failed." View the reason, make necessary changes, and click the Re-trigger to restart fine-tuning.
    * If necessary, you can stop the process in the middle and resume it later; then, the status is changed to “Stopped.” Click Re-trigger to initiate the fine-tuning process again from the beginning.
* **Base model information**: This section shows the base model used for fine-tuning and its source.
* **Training information**: This shows important details like training type, number of training steps, training loss, percentage of validation data, validation loss, training start time, and duration. Click the downward arrows next to the training loss and validation loss fields to see their graphical trends.
* **Test data information**: It indicates the model performance on the test dataset using the BLEU score.
* **Hardware information**: This displays CPU and GPU utilization during fine-tuning.
* **Training parameters**: Displays the summary of the parameters provided.