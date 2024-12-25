# Learning Flask - MNIST Digit Identification [PyTorch]
This is a project I made to help me learn Flask and how to deploy machine learning models using Flask. The project uses a neural network with the PyTorch Python package to identify digits from the MNIST dataset.

## Installation
1. Clone the repository
2. Open the terminal
3. Create a virtual environment
4. Start up the virtual environment
5. Install dependencies using `pip install -r requirements.txt`
6. Run the app using `flask run`

After doing these steps, you can visit http://127.0.0.1:5000/ in your browser and try uploading some of the picture in the `human_test_images` folder.

# Hosting
Here are two good & free ways to host this Flask + PyTorch project.

## Ngrok
Ngrok is a service that allows you to expose your localhost to the internet. <br>
To set it up follow these steps:
1. Sign up for Ngrok at https://ngrok.com/signup
2. Follow the download and setup instructions at https://dashboard.ngrok.com/get-started/setup/ 
3. Follow the Installation instructions (from above)
4. Run `ngrok http 5000` in a second terminal: This will give you a URL that you can use to access your server from anywhere.

## Render
Render is a service that allows you to host web services for free. <br>
To set it up follow these steps:
1. Sign up for Render at https://dashboard.render.com/register
2. Create a new Web Service (it's important to create a Web Service and NOT a Static Site)
3. Select "Public Git Repository"
4. Paste in "https://github.com/devsai9/hosting-flask"
5. Click "Connect"
6. Make sure Language is set to "Python 3"
7. Set the Start Command to `python app.py`
8. To keep it free, set the Instance Type to "Free"
9. Click "Deploy Web Service"
10. After a few minutes, your web service will be live and you can access it from the URL provided.

## Details
I used PyTorch to create this. <br>
The models are neural networks. One of them looks like this: <br>
```python
self.model = Sequential(
    Flatten(),
    Linear(28 * 28, 512),
    ReLU(),
    Linear(512, 512),
    ReLU(),
    Linear(512, 10),
)
```
The model was trained and stored in a `model1.pth` file.