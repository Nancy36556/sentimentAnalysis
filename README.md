# sentimentAnalysis
1-create virtual environment
2-create folder named 'downloadedModel' and file named 'model_state_dict.bin'
3-Download the pre-trained model:

bin/download_model
4-run classify.py file then modelCode.py file 
5-finally run this command 'uvicorn app:app --reload'

Here's a sample request to the API:

http POST http://127.0.0.1:8000/predict text="Good basic lists, i would like to create more lists, but the annual fee for unlimited lists is too out there"

The response you'll get looks something like this:

{
    "confidence": 0.9999083280563354,
    "probabilities": {
        "negative": 3.563107020454481e-05,
        "neutral": 0.9999083280563354,
        "positive": 5.596495248028077e-05
    },
    "sentiment": "neutral"
}


Start the HTTP server:

bin/start_server
Send a test request:

bin/test_request
