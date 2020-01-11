# Breast Cancer Prediction using Flask

In this section, we have used a simple RandomForestClassifier to diagnose the breast cancer.

Creating the flask API

```
app = Flask("__name__")
```

The loadPage method calls our home.html.
```
@app.route("/")
def loadPage():
	return render_template('home.html', query="")
```

The cancerPrediction method is our POST method, which is basically called when we pass all the inputs from our front end and click SUBMIT.
```
@app.route("/", methods=['POST'])
def cancerPrediction():
```
  
The run() method of Flask class runs the application on the local development server.
```
app.run()
```


Yay, our first model is ready, let’s test our bot.
The above given Python script is executed from Python shell.

Go to Anaconda Prompt, and run the below query.
```
python app.py
```


Below message in Python shell is seen, which indicates that our App is now hosted at http://127.0.0.1:5000/ or localhost:5000
```
* Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
```


Here's our UI looks like: 

![Diagnosed](https://beingdatum.com/wp-content/uploads/2020/01/diag.PNG)
![Not Diagnosed](https://beingdatum.com/wp-content/uploads/2020/01/notdiag.PNG)