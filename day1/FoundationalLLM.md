# Foundational Large Language Models & Text Generation and Prompt Engineering

Bring life to text documents or to GitHub content.
Reinforcement learning with human feedback (RLHF):

    Question- How Gemini is using RLHF - How user feedback is used to improve the responses? How does it work? 

    Answer- LLM File tuning --> SFT and RHF 
    Supervised Finetuning (SFT): Demonstration data - to get good results. Produced by human experts for creating high quality data. 
    Reinforcement Learning with Human Feedback (RHF): Aligning models to human preferences . Make responses safer, helpful or more factually correct.

    Reward model --> For penalizing the responses, and give good scores for better answers. Human preferences are taken for reward model. 

    Question- LLM Will it interpolate from training data or it
    
     thinks beyond to make discoveries? 
        - Test time compute or inference scaling.
        - LLM is able to solve few mathematical and computer science NP problems --> Approach of it's solutioning is by doing best shot prompting --> We give a initial simple solution to LLM and ask it to make it better, LLM comes up with something new we would show it again and ask it to make it better --> Asked 1000s of time.
        - Two techniques that scale infinitely --> training and search (moment where scaling is happening for throwing compute at inference time)
    
    Question - Can small LLM be used for tasks which have extensive data/context? 
        - Distillation inference optimization techniques --> Distilling the knowledge to smaller model 
        - Multiple techniques --> Data distillation -- Use larger model to generate large amount of data for the smaller model to train them
        - Another technique --> Knowledge distillation (Fine-grain) -- Align token of smaller model to that of large model 
    
    Question - How to decide large/small LLM model can be used for an usecase?
        - Learn Ways to evaluate model performance LLM. 
        - On cases where ground truth is not available, evaluate LLM response
          Score on pair wise (take two responses for a prompt and check for the usefulness score) or take answer and prompt and check for scale of 5 how useful the response is. 
        - BLEU, ROUGE evaluation metrics
        - Open-src libraries - Example Prompt-FOO 
        - Human or auto evaluated.
    
    Question - Why step by step answering on first prompting than direct answer?
        - Chain of thought prompting: This can be done by giving examples of how to give response for the query you have. 
        - top K, top P changes can be done by resubmitting the prompt to come with varied response. 
        - Mostly the model will explain the reasoning on the inital prompt. 
    
    Question - Enum Mode - On LLM
        - Three different enums are to be given as outcome. 
        Make sure the prompt have proper data structuring.
        - Zero shot enum prompting can also be done as LLM is capable of classifying it's outcome to different enum scenarios 
        Or you need data finetuning 

Code Labs and Demos