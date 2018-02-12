# About

Code to download the images by using the image URLs provided in the NYC data from
http://insideairbnb.com/get-the-data.html and save those images into local folders.

# Setup and Run

Python 3

- create virtual environment: `$virtualenv -p python3 venv`
- activate virtual env: `$source venv/bin/activate`
- install required packages: `pip3 install -r requirements.txt`

To run (NOTE: for the NYC dataset, it took about 4.5 hours to download the ~ 45,000 images):

1. copy the real listing csv file to /data/ and comment out the `# listings = pd.read_csv('data/listings.csv')`
2. `python3 get-images.py` will download the save the images to /data/images/ folder


