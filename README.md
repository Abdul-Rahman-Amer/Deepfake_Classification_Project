# Three completed AI projects here for detecting generated AI images, text, and Audio. 

## The notebooks produce 3 models all well over 90% accurate and show a skillset in NLP (a soft model with room for deeper improvement including integrating gloVe embedding and eperimenting with different tokenizers, model tuning with grid search, as well as different sequence lengths and tokenization/stemming/lemming techniques. It's simplicity still performed very well), Image Classifcation (including Augementation and mormaliation techniques as well as data scraping), and Audio Maniupulation (including feature analysis, creating a function to turn any audio file into useable data) with complete ETL of data and soft EDA. 

# Next Steps:

### Next steps involve hyper tuning the models, pickling, and deploying them for external use with a proper front end in a front end framework such as React. Alternatively, they can be built into a flask application where the UI is directly interacting with the deployed models. Model performance trackers can be integrated my creating logging of it's performance and the most optimal way to do so would be in AWS and utilizing there logging services as well as establishing chronjobs that run developed tests and return model performance on a daily basis. 

### In addition creating a few models for different use cases will give clients flexibility on what it is they are doing including a UI where they can train pre-built models on there own data and run there own data in there unique environment for securing there data. 
