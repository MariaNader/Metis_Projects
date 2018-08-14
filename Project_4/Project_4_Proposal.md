## Project 4 Proposal

**Topic**

Answering Questions Based On Given Text Data



### Background

------

Each passing day more and more resources are invested in technological efforts that aim to create computers that have a higher level of autonomy and understanding of the data given to them. One such instance where this is applied is in the field *Natural Language Processing*, particularly having a machine comphrending lines of text when asked a related question to the text. A practical use of this can be expidited information search.



### Domain

------

Regarding the "comphrehension" aspect of this project, utilization of a *recurrent neural network* seems to be a viable decision. Standard machine learning libraries such as *sklearn*, *keras*, and *nltk* will be used. The training and test dataset, provided by [Stanford University](https://rajpurkar.github.io/SQuAD-explorer/), are JSON files. Each key label corresponds to an embedded dictionary, with values such as the topic of a wikipedia page, the text of each paragraph on that wikipedia page, along with a list of questions related to that wikipedia page. 



### MVP

------

The current goal is to create a model simple enough where given a subset of wikipedia pages and a subset of questions taylored for those pages, the model will be able to process / "understand" the text of the wikipedia pages' content along with the text of the questions, and return a reasonable answer. Performance of the model will be judged against a test set based on the F1 score metric. The model's y_pred will be matched with that of the y_true and scored based on how closely the text matches.

Given the wide scope and depth of such a project, scope reduction, possibly through limiting the dataset to only wikipedia pages about basketball for example, is also an option to consider.



### Known Unknowns

------

1. Implementation of recurrent neural networks has not yet been done, so timing of modeling, training, and testing is not yet known to make a sound decision on the optimal algorithms to use.
2. There is unfamiliarity working with JSON files in the realm of NLP, which will require further learning in the days to come.

### Data

------

Sample JSON snippet of entire dataset showing 1 Wikipedia page. 

```json
data = {
    wiki_page_0:{
        title: 'Beyonce',
        paragraphs:{
            1:{
                question:{
                    1: 'When did Beyonce start becoming popular?',
                    2: 'What areas did Beyonce c…hen she was growing up?'
                    },
                answers:{
                1: 'answer 1',
                2: 'answer 2'
                }
            }
        }
    }
}
```


