Before installing Caldera, ensure you are installing Caldera on a Windows WSL or Linux operating system. You will also need to have Python 3.6.1+ (with Pip3), a Google Chrome browser, and the hardware recommended that you have available is 8GB+ RAM and 2+ CPUs. Caldera also recommends installing GoLang 1.13+ and NodeJS 16+.

Start by cloning the Github repository for Caldera, passing the desired version/release in x.x.x format. I will be using the newest version available, 5.0.0.

```git clone https://github.com/mitre/caldera.git --recursive --branch 5.0.0 ```

Next, install the PIP requirements:

```sudo pip3 install -r requirements.txt```

Finally, start the server:

```python3 server.py --insecure```

Once started, you should log into the UI using http://localhost:8888 using the credentials red/admin. Then go into Plugins -> Training and complete the capture-the-flag style training course to learn how to use the framework.
