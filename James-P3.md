##James
*Problem Statement*
- I'll assume that the "Background Information" in your readme reflects your problem statement.  In which case, it is a good start.  Adding some details as far as what qualifies success would be helpful. Basically how well would you like your model to perform in order to offer it up as a viable solution?
- You did a good job of highlighting the use of this project and thus how it can be a beneficial analysis, adding some insights as far as who may benefit from a successful analysis would be useful.  

*Data Cleaning and EDA*
- Additional EDA into your n_components for your SVD would most likely have been beneficial.  By just selecting 100 components without supporting analysis you do not know if 100 components is enough to explain 80%+ of the variance in the data OR if its explaining too much and thus you are still leaving in noisy components.  
- Interesting how your EDA notebook also had your models in there.  These were more like final models as opposed to what I like to refer to as Model Based EDA(Constructing and interpreting simple models early on to better understand how the data exists.)
- While You did collect a sufficient amount of data to address your problem, as you mentioned.
- You write a good reusable function for querying the API.
- You make smart choices with how to deal with missing fields present in some API queries.
- Appropriate framing is provided for your data cleaning and EDA processes. Given that many of your steps were optimized by use of functions that with good comments, the use of extra markdown comments were not needed.
- Exploratory data analysis demonstrates consideration of goals outlined in the problem statement.

*Preprocessing and Modeling*
- Functions to automated modeling and assessment were a smart idea.
- As you choose to also looking the the confusion matrix.  You can also notice things (like with the SVD models) with respect to missclassification rates.  It seems like those models that incorporated SVD/LSA were much more likely to predict a r/liberal post as r/conservative than the other way around.
- You explored various hyperparameters for different vectorizers to numerically represent your text.
- You demonstrate proper use of stop words as a well as stemming/lemmatization.
- Nice work exploring many different models and choosing appropriate metrics for optimization.
- While you land on a couple "best" models its not clear as to which one you would choose or not choose.  You did mention that the models did not reach a desirable performance so also having stated that desired performance earlier would have been beneficial to your conclusion.
- You do an exceptional job exploring both accurate and misclassified predictions at various confidence thresholds to explore how your model works.

*Evaluation and Conceptual Understanding*
- Good work of having your model functions provide metric information apart from accuracy.  In this project analyzing confusion matrices can be very insightful to understand if missclassification is unbalanced between classes.  
- With respect to your model evaluation via metrics, a good next step is to record/include your insights about _why_ that model could have performed the way that it did.  What are the assumptions of the model and how do they compare to how the data exists?
- With the use of several models and evaluating them on accuracy and confusion matrices, you missed out on having the more _intimate_ opportunity to understand each model as far as features of importance and how they can potentially be tuned via adjusting features.

*Conclusion and Recommendations*
- In your executive summary section when talking about the highest performing models and how the text was processed.  Information about their scores is desired as far as details go.
- To be honest somehow you you managed to provide a-lot of context as far as steps and narrative aspect with not a-lot of works.  Some very detailed markdown notes and code comments really went a long way.
- There is a clear connection between analyses and conclusions.
- Given your initial problem statement to identify frequently correlated terms, it would have been a insightful act to interpret the coefficients/probabilities/feature importances of words in each model.  
- You mentioned a couple of things, such as additional data, that would be great, but I believe you could offer some modeling/data tactics you could have explored that may have been beneficial.

*Project Organization*
- Repo has some good organization for pushing to your public github but not the format for the submission.  
- Theres a folder with unused code, should either be integrated into the project or removed from the repo.  There some good stuff in there.
- Files and directories are appropriately named and all file extensions are present.

*Visualizations*
- Visualizations are good but could be better accompanied by interpretations.  
- Visualizations are typically cleanly formatted and have quick context for why they're being looked at.  
- In addition to the context of why for visualizations, I would have liked to see more of your insights gained recorded.  

*Python Syntax and Control Flow*
- Code comments are great and use of interwoven functions in order to acquire data was and excellent touch.  (Creates reusability of code.)
- I think using pickled objects was a smart choice given the considerations that you listed.
- Variables and functions have informative, human readable names.
- Clever code is efficiently implemented to meet the desired aims.

*Presentation*
- Id say your modeling function was more like a manually built pipeline.  (Probably better than SKLearn pipeline)
- That gif just ain't right.
- Nice experimentation with multiple models.  That was probably a tough learned experience, but now you know first hand, theres a point where not matter what model you throw the data at,  it won't perform any better.  And you have to go back to your data.
- Started off with a good deal of reading from and looking at your slides.
- Sentiment analysis by class would have been interesting.  

**Peers**
_Glows_
- Awesome details of your modeling techniques…want to look at how you did it further!!
- Cool modeling and I really liked that you had gone through so many models to figure out which was best
- mazingly in-depth analysis (38 models and analysis of post comments including comment depth)
- Really interesting work with creating functions to optimize models
- Good review of what told the audience and ideas for future work

_Grows_
- "Can’t think of anything"
- smile more or something, idk (edited)
- What if one post had a lot of comments?  Does that post create a bias in the dataset since it has a larger weight in the post comments dataset?
- GIF’s were fun but sometimes distracting
