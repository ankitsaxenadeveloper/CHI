# CHI
Making Computers EMOLIGENT : Emotionally Intelligent
 
 
Ankit  Saxena
Tata Consultancy Services Ltd.
Meerut , Uttar Pradesh , India
+91-9568458204
ankitsaxena@acm.org


 



 
ABSTRACT
Feelings are a vital part of life and they can be expressed through emotions. This paper presents a technique named CoEmo to develop emotions in computers and make them sense, feel and express it. This paper proposes a way of making computers Emoligent : Emotionally intelligent  by enabling them sense  mood of user by capturing live video of user and to determine which mood a user is in. For this , a pattern matching algorithm that perceives face , voice tone of user and matching it against predefined set of masks for each mood is presented. This paper also presents a way to make computers synthesize voice in a particular tone to approximately match with user mood. For this , This paper uses pitch, mid tones as characteristics  of sound and alter them to produce sound in an emotional tone , thus finally making computers Emotionally Intelligent.
Author Keywords
CoEmo , Emoligent ,landmarks, making Computers emotionally intelligent.
1.	INTRODUCTION
Emotions are an integral part of life. From anything to everything emotions play a vital role to express our feelings. This paper proposes the importance of imparting feelings to computers and describe how can computers sense mood and act accordingly. One question arises, why to develop feelings in computers when our work is getting done without imparting emotions to computers. The answer is simple, as the modern computing is becoming  close to real world , emotions play a vital role in perceiving information , making decision and acting accordingly. 
So in this modern world of Artificial Intelligence , it opens a special area of reasoning and decision making in which computers can perceive environment specifically the mood of user and on the basis of that making decision and talking to user in the same emotional tone. This paper presents a technique named CoEmo which serves the same purpose of finding in which mood a user is, and then accordingly talk by synthesizing voice in same emotion.
The  technique CoEmo and is divided into 2 stages :
1)  Sensing mood of user by capturing image of user through its    actuators (webcam) and by applying a pattern matching algorithm.
2)   After calculating in which mood a user is. the next stage is to synthesize voice in same emotional tone in which a user is.
2.	RELATED WORK
This paper proposes the idea how each of the 2 stages described above can be achieved and also describes the work done for the same. On combining these two stages , computers can be made to sense and feel emotions.
2.1  Sensing Mood of User
The first stage is sensing the mood of user. For this actuator like webcam is used to capture live video of user and capturing image of user frame by frame and then applying image processing on the image captured. The algorithm of pattern matching is based on landmarks in which a face is considered as a continuous set of special points whose alignment is calculated and then compared with the mask stored in database and then it is calculated in which mood a user is.
First of all , we crop the region of interest (ROI) which is the face  of the user and then calculate the landmarks , the special set of points that outline the face and based on that matching it against the predefined set , mood value can be calculated. Here mood value means a flag value (example 1 for happy , 2 for sad , and so on ).
 
Figure 1 Identifying landmarks of major blobs on face.     Software Courtesy :  MathWorks Matlab , Original Image Courtesy : inspirasinusantara.com  
2.1.1  Algorithm
Input : The image of user captured by webcam 
1)	Find out the region of interest ,which is the face of user.
2)	Calculate special points called landmarks that outlines the face in the region of interest .
3)	Find the major blobs in the image.
4)	Find the position of eye ,lips, nose in the face and other blobs like elevated cheeks. of face.
5)	Separate each and every part determined and match with the predefined set of masks for each part.
6)	Use nearest neighbor algorithm to find the closest match between calculated and predefined landmarks.
7)	return flag value of the corresponding mood.
 
Figure 2. Capturing live video of user and saving image frame by frame to apply further processing.
2.1.2  Accuracy
Out of 100 tests done in which different faces were shown , this algorithm CoEmo returned 80 correct flag values of emotions , so this algorithm is working with 80 % accuracy.
2.2  Producing Emotional Tone
Now we have got the flag value of mood of user , in short we know in which mood a user is , now comes the stage of producing emotional tone . Based on that flag value , computers can determine the area in which it has to deal. If mood is happy , that is flag value 1 , then it will search words in the area of positivity and accordingly makes decision. Now comes the problem of producing emotional tone.
This paper uses the main 3 main characteristics of sound namely, pitch , intensity and loudness of sound. As we know , the tone of the voice produced can be modulated to express emotions and  emotion is specified by flag value calculated above. Producing voice works in 2 stages :
1)  Converting the decision or text into phonetic text.
2)   Calculating how each phoneme should be pronounced, giving      rhythms to it , called prosody.
 
Figure 2. A Sound wave modulated to produce a specific tone

The idea is to add emotion to each phoneme produced at the same time when prosody is applied. Now giving rhythms to sound can be modulated by varying the pitch, intensity and loudness thereby producing a quality sound that too in an emotional tone.Syllable can be considered as the pats of phoneme , and attenuating the pitch , loudness, intensity of that syllable according to the flag value of the corresponding emotion calculated above can modulate the tone. And when the tone gets modulated, automatically emotions can be expressed in voice. Its somewhat similar to Text To Speech with emotions in the prosody part.
3.	LIMITATIONS and FUTURE WORK
The technique discussed above requires a proper exposure to light to calculate landmarks on image and finding in which mood a user is. Proper Exposure to light is required for the algorithm to correctly identify landmarks and so to apply further processing .In addition , when modulating the rhythm of each syllable , its phoneme can alter the meaning of the word.
Future prospects include the more refined form of applying modulation to its prosody part. Furthermore Learning prospect can be applied to mood calculation algorithm , by automatically giving feedback of the error an using it to correct itself , a extension of self learning networks, thereby increasing its accuracy.
4.	CONCLUSION
By enabling computers to sense , feel and express emotions , the emotional intelligence of computers can be increased. In this way the decision making capability of computers can also be enhanced. It can be shown that according to technique CoEmo mood can be detected with 80 % accuracy. Furthermore the ability of computers to express emotions can make advancement in the field of artificial intelligence and Natural Language Processing. This paper demonstrated a unique algorithm for increasing the emotional quotient of computer thereby providing them the ability of reasoning, thus making them emotionally intelligent.
5.	ACKNOWLEDEMENTS
Thanks to all who gave their comments about the idea which helped refine the algorithm .
6.	REFERENCES
1.	C. Dianne Martin , 1998. Giving Computers Emotions - Why and How. The George Washington Univ., Washington, DC.
2.	Gerald Salton , 1966. ELIZA—a computer program for the study of natural language communication between man and machine.  Cornell Univ., Ithaca, NY
3.	Auburn University Auburn  , 2008. The role of emotion in computer skill acquisition .  AL, USA
4.	Bruce A. Draper, Kyungim Baek, Marian Stewart Bartlett, J. Ross Beveridge, Recognizing faces with PCA and ICA, Computer Vision and Image Understanding.
5.	Ying-li Tian, Takeo Kanade, Jeffrey F. Cohn, Recognizing Action Units for Facial Expression Analysis, IEEE Transactions on Pattern Analysis and Machine Intelligence, 
6.	J. Fleiss. 1981 .Statistical Methods for Rates and Proportions. Wiley, New York.
7.	Seyed Mehdi Lajevardi, Margaret Lech,2008 . Averaged Gabor Filter Features for Facial Expression Recognition. 

