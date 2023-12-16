# Sentiment Classification

Cource Project of "**Advanced Data Analytics**" (Score: 93)

### The aim of this project is to **construct models with diverse architectures** and **explore the efficiency of different model structures in sentiment classification**.

**Conclusion of the project:**

  1. The effectiveness of fusing global feature and local feature
  2. The effectiveness of initiating global feature extraction before local feature extraction.

(All figures are drawn by the authors, not copied from the web, which can be found in the report)

## ① BilSTM-CNN
  * Used a BiLSTM layer to extract global contextual information
  * Then employed CNN to capture local features
![image](https://github.com/Jbb-525/Sentiment-Classification/assets/88278422/0a250b68-0d52-4d7d-bd97-51701ceb35ce)


## ② TextCNN
  * Applyed 1D convolution with multiple filters of different sizes to extract local features within sentences
  * Then employed max-pooling to extract critical feature

     _**Problems**: Long-range feature extraction limitations and insensitivity to language order are noted._

 ![image](https://github.com/Jbb-525/Sentiment-Classification/assets/88278422/ac0f4098-4835-4a45-b12b-755728bfc36d)

## ③ BiLSTM
  * Applyed pad_packed_sequence & pack_padded_sequence to handle variable-length text
  * Applyed attention mechanism to extract key information in the sentence

![image](https://github.com/Jbb-525/Sentiment-Classification/assets/88278422/54710fd5-0cd4-4c11-92ed-b30d8649221a)

## ④ CNN-BiLSTM
  * Employed CNN to capture local features
  * Then used a BiLSTM layer to extract global contextual information
     
     _**Problem**: 1DCNN results in the loss of certain information from the text sequence._
     
![image](https://github.com/Jbb-525/Sentiment-Classification/assets/88278422/82c0a717-d4c3-4ab7-8bee-38a2fad05c3a)

## ⑤ Model Evaluation
  Applyed Micro Precision, Micro Recall, Micro F1 to evaluate each model
  #### BiLSTM-CNN is the BEST ONE !!
  
   ![image](https://github.com/Jbb-525/Sentiment-Classification/assets/88278422/4213ab53-5a4b-41d9-9951-4174d1409da9)





  
