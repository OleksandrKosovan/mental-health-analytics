# Mental health analytics

### Dataset Information

This dataset is from a 2014 survey that measures attitudes towards mental health and frequency of mental health disorders in the tech workplace. 

### This dataset contains the following data:

- Timestamp
- Age
- Gender
- Country
- state: If you live in the United States, which state or territory do you live in?
- self_employed: Are you self-employed?
- family_history: Do you have a family history of mental illness?
- treatment: Have you sought treatment for a mental health condition?
- work_interfere: If you have a mental health condition, do you feel that it interferes with your work?
- no_employees: How many employees does your company or organization have?
- remote_work: Do you work remotely (outside of an office) at least 50% of the time?
- tech_company: Is your employer primarily a tech company/organization?
- benefits: Does your employer provide mental health benefits?
- care_options: Do you know the options for mental health care your employer provides?
- wellness_program: Has your employer ever discussed mental health as part of an employee wellness program?
- seek_help: Does your employer provide resources to learn more about mental health issues and how to seek help?
- anonymity: Is your anonymity protected if you choose to take advantage of mental health or substance abuse treatment resources?
- leave: How easy is it for you to take medical leave for a mental health condition?
- mental_health_consequence: Do you think that discussing a mental health issue with your employer would have negative consequences?
- phys_health_consequence: Do you think that discussing a physical health issue with your employer would have negative consequences?
- coworkers: Would you be willing to discuss a mental health issue with your coworkers?
- supervisor: Would you be willing to discuss a mental health issue with your direct supervisor(s)?
- mental_health_interview: Would you bring up a mental health issue with a potential employer in an interview?
- phys_health_interview: Would you bring up a physical health issue with a potential employer in an interview?
- mental_vs_physical: Do you feel that your employer takes mental health as seriously as physical health?
- obs_consequence: Have you heard of or observed negative consequences for coworkers with mental health conditions in your workplace?
- comments: Any additional notes or comments

# Questions to answer:

> How does the frequency of mental health illness and attitudes (other factors in datasets) towards mental health vary by geographic location?

> What are the strongest predictors of mental health illness treatment?



# Answers

### 1.Сonclusions from the visualization:

- The largest number of respondents from the United States. They are relatively equally distributed. UK and Canada are too.
- But indicators for other countries are not enough.
- So, we can't say that it depends on the location.We dont have enough information
- We need to pay attention on correlation with country. (no_employees: 0.31) , (work_interfere: -0.39)


### 2.We need to pay attention on next correlation:

(coworkers / phys_health_consequence: 0.57), (mental_health_consequence: 0.51), (treatment / family_history: 0.49), (coworkers / leave: -0.577)

I use LightgbmClassifier for prediction consequences for coworkers with mental health conditions in your workplace. So, this model takes into account the following indicators:

- age
- no_employees
- leave
- work_interfere


### Some visualizations:

![alt text](https://2.bp.blogspot.com/-G2feM1Rwox0/WzTYqx57wJI/AAAAAAAAAGA/7cQH_OvPQCwXQyXPp8kH2r7voE67d4zeACLcBGAs/s640/Plot%2B3.png)

![alt text](https://2.bp.blogspot.com/-Bm_2MgWgrNM/WzTYqwF5aXI/AAAAAAAAAF8/V357kCQr8BojxgR7XCYqmjxCYzw4fZ01wCLcBGAs/s640/Plot%2B5.png)

![alt text](https://2.bp.blogspot.com/-cm4nKcNYSXY/WzTYqyvCJTI/AAAAAAAAAGE/bOiXBFoP8ZIs46rUiy2geZaYcewIFH6MACLcBGAs/s640/Screenshot%2Bfrom%2B2018-06-28%2B15-12-27.png)
