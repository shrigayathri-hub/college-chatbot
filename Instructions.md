# Follow this after cloning this repo & use it

## Virtual Environment

Try either of these methods :

1. `pip install virtualenv`
2. `virtualenv venv`

--- OR ---
 
in VS Code, run `Ctrl+Shift+P` ,s earch for _Create environment_ & create one. **But don't tick the `requirements.txt`**

## Installations (in terminal)

1. `pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118`
   **Note** : I have used CUDA (GPU) so torch versions have `+cu116` written.
2. `pip install nltk spacy flask flask_sqlalchemy`
3. `python -m spacy download en_core_web_sm`
4. `pip install thinc wheel`

## Running the flask Server

1. In terminal run this command `cd flask_server`
2. In terminal run this command `set FLASK_APP=university.__init__.py`
3. then go to `college-enquiry-chatbot\flask_server\university\routes.py` file & uncomment `db.create_all()` in `hello_world` method
4. in terminal run this command `flask run` & open the browser & see the website working
5. go to `/teachers` url in browser & add some teachers
6. similiarly add some Courses, Students & holiday (more details later...)

## Training the Neural network

1. In terminal run this command `cd ..`
2. In terminal run this command `set FLASK_APP=run.py`
3. In terminal run this command `py train.py`

## Finally you can use the project

1. In terminal run this command `flask run --host=0.0.0.0 --port=5000`


i have mentioned the basic of what my project do , so i need a detailed conservation like content to present for my final year project presenetaion to faculty make sure i sound technical and straight on pont delivery in indain tone, the project titile is : CHATBOT SYSTEM FOR COLLEGE INFORMATION AND SUPPORT, give literature survey with reference papers, AIM & OBJECTIVES OF THE PROJECT (Problem Statement) ,scope of the project , need for the currenet study , feasibility analysis, proposed methodology, CHOICE  OF  COMPONENTS  /  MODULES  / METHODS/TECHNIQUES EQUIPMENT  USED FOR  PROJECT DEVELOPMENT, design and software architecture , novelty of the project, 
Chatbot for College Support Desk and Enquiry

My project is an intelligent chatbot system designed to automatically understand and respond to user queries related to college support and enquiry., it focus on semester result based on student roll no , holiday as for particular year with pdf output , syllabus for course in pdf output , faculty available , campus & infrastructure details  , fee detail , admission related queriries ---join date , appplication form , course available with duration.

The system receives a user’s message in natural language through a web-based chat interface.

It processes the message using Natural Language Processing techniques:

Tokenization to split the sentence into words.

Stemming to reduce words to their root form.

Bag-of-Words (BoW) converts the sentence into a fixed-size numeric vector.

The processed data is passed into a Feedforward Neural Network (FNN) model which classifies the user’s intention by predicting a specific intent tag.

The system applies a confidence threshold and returns the predefined response associated with the predicted intent tag.

Responses can be plain text, links to files, or URLs for additional actions.

The entire system is connected via a Flask REST API, allowing interaction between frontend and backend in real time.

The neural network is trained using labeled datasets of intents, optimized with the Adam algorithm and CrossEntropy Loss to achieve efficient and accurate predictions.
