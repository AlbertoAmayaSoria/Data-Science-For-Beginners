## Write A Data Ethics Case Study

## Instructions

You've learned about various [Data Ethics Challenges](README.md#2-ethics-challenges) and seen some examples of [Case Studies](README.md#3-case-studies) reflecting data ethics challenges in real-world contexts.

In this assignment, you'll write your own case study reflecting a data ethics challenge from your own experience, or from a relevant real-world context you are familiar with. Just follow these steps:

1. `Pick a Data Ethics Challenge`. Look at [the lesson examples](README.md#2-ethics-challenges) or explore online examples like [the Deon Checklist](https://deon.drivendata.org/examples/) to get inspiration.

2. `Describe a Real World Example`. Think about a situation you have heard of (headlines, research study etc.) or experienced (local community), where this specific challenge occurred. Think about the data ethics questions related to the challenge - and discuss the potential harms or unintended consequences that arise because of this issue. Bonus points: think about potential solutions or processes that may be applied here to help eliminate or mitigate the adverse impact of this challenge.

3. `Provide a Related Resources list`. Share one or more resources (links to an article, a personal blog post or image, online research paper etc.) to prove this was a real-world occurrence. Bonus points: share resources that also showcase the potential harms & consequences from the incident, or highlight positive steps taken to prevent its recurrence.



## Rubric

Exemplary | Adequate | Needs Improvement
--- | --- | -- |
One or more data ethics challenges are identified. <br/> <br/> The case study clearly describes a real-world incident reflecting that challenge, and highlights undesirable consequences or harms it caused. <br/><br/> There is at least one linked resource to prove this occurred. | One data ethics challenge is identified. <br/><br/> At least one relevant harm or consequence is discussed briefly. <br/><br/> However discussion is limited or lacks proof of real-world occurence. | A data challenge is identified. <br/><br/> However the description or resources do not adequately reflect the challenge or prove it's real-world occurence. |

## Case study:
### Historical bias in AI recruitment filters.
1. Identified data ethics challenge
    * Primary challange: Historical bias.
    * This occurs when the data used to train a model reflects human prejudices, inequalities, or discriminatory decisions from the past. The algorithm doesn't understand what is "fair"; it only learns to replicate the patterns found within the data it is provided.
2. Example description (The real world):
#### The context
A large software company receives 5000 job applications per month. To save time, the human resources team decides to train an Artificial Inteligence model to screen the resumes (CVs) and automatically select the top 100 candidates for an interview.
#### The technical and ethical problem
To teach the AI what constitutes a "good candidate", the company feeds it the resumes of every person who has been successfully hired over the past 10 years.

Due to the historical gender gap in the tech sector, 85% of the engineeers hired by the company in the past were men. When analyzing the text, the algorithm finds that words such as "engineer", "automation", or even masculine extracurricular activities (such as "men's football club") appear frequently in "successful" resumes. Conversely, resumes from women containing phrases like "women's robotics club president" or originating from women's-only collages are penalized by the AI, simpy because the model never encountered those patterns in its historical list of successful employess.

#### Harms and unintended consequences.
* Automated discrimination: The system systematically discard highly quialified female condidates before a human recruiter evers has the chance to review their applications.
* Perpetuation of the problem: By only hiring individuals who resemble past hires, the company fails to diversify its workforce. This creates a feedback loop where future training data remains inherently biased.

#### Simple mitigation strategies to minimize impact
* Preprocessing (anonymization): Remove any gender fields, proper names, and references that reveal the applicant's gender from the dataset before the AI processes the document.
* Impact parity metric: Force the algorithm to maintain an equitable selection rate (for instance if 40% of the applicant's are women, 40% of the candidates selected by the AI must also be women)

#### Related resources
* Real-world news (The amazon case): Amazon scraps secrets AI recruiting tool thah showed bias against women \([Reuters, 2018](https://www.reuters.com/article/world/insight-amazon-scraps-secret-ai-recruiting-tool-that-showed-bias-against-women-idUSKCN1MK0AG/), [bbc, 2018](https://www.bbc.com/news/technology-45809919)\). This is the world's moust famous real-world incident where an engineering team discovered that their own model penalized resumes containing the word "women's"
* Learning tool: Google what-if tool. An interactive visual interface designed for beginners that allows users to explore how an AI model's decision shift when sensitive variables like gender or age are modified.