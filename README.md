# speech_to_audio_streamlit
Captures the speech and reproduces in audio

Implements:
- Streamlit in Python to user interface

Steps:

1) run a docker image

   $ docker container run -d -p 8501:8501 python:3.10 sleep infinity
   
2) pip install streamlit

3) create self-signed SSL certificate and provide passphrase

   openssl req -x509 -newkey rsa:4096 -keyout key.pem -out cert.pem -sha256 -days 365
   
   Enter PEM pass phrase:
   Verifying - Enter PEM pass phrase:
   
3) streamlit run --server.sslCertFile /root/cert.pem --server.sslKeyFile /root/key.pem streamlit.py