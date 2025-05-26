# Synthetic-Data-Generation-with-Generative-AI
Synthetic data is artificially generated data that mimics real-world data. It is created by algorithms, models, or simulations rather than being collected from actual events or real-world scenarios.
# Introduction
To get started with the task of Synthetic Data Generation, we need a dataset that we can use to feed into a Generative Adversarial Networks (GANs) model, which will be trained to generate new data samples that will be similar to the original data and the relationships between the features in the original data. I found an ideal dataset for this task, which contains daily records of insights into app usage patterns over time. Our goal will be to generate synthetic data that mimics the original dataset by ensuring that it maintains the same statistical properties while providing privacy for users’ actual usage behaviour. To create a Generative AI model using GANs for generating synthetic data, we need to:
1. Drop unnecessary columns: We will not generate the Date or App fields as they are specific identifiers. Instead, we’ll focus on Usage, Notifications, and Times opened. In case, you want to use the app column, you 2. can use the app column by converting the value of the column into numerical values.
3. Normalize the data: GANs perform better with normalized data, usually between 0 and 1.
4. Prepare the dataset for training: Ensure the remaining columns are numeric and ready for the model.

# Features
The dataset contains the following columns:
1. Date: The date of the screentime data.
2. Usage: Total usage time of the app (likely in minutes).
3. Notifications: The number of notifications received.
4. Times opened: The number of times the app was opened.
5. App: The name of the app.

# Conclusion
Here’s the process to define and train the GAN:
1. The generator will be trained to produce data similar to the normalized Usage, Notifications, and Times opened columns.
2. The discriminator will be trained to distinguish between the real and generated data.
3. Next, we will alternate between training the discriminator and the generator. The discriminator will be trained to classify real vs fake data, and the generator will be trained to fool the discriminator.
<br>
<br>
We explored the task of synthetic data generation with Generative AI using Generative Adversarial Networks (GANs). We started by preprocessing a dataset of app usage insights by focusing on features like Usage, Notifications, and Times opened, which were normalized for GAN training. The GAN architecture was built with a generator to create synthetic data and a discriminator to distinguish between real and generated data.

# Contributing
If you are interested in contributing to the project, please create a fork of the repository and submit a pull request. All contributions are welcome and appreciated.
