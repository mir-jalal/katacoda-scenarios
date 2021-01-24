Now we should create service to run the script in the background.

Create a new service file and paste following code in it.

`sudo nano /lib/systemd/system/devops_service.service`{{execute}}

<pre>
[Unit]
Description=DevOps Service

[Service]
Type=simple
ExecStart=/bin/bash /usr/bin/devops_script.sh

[Install]
WantedBy=multi-user.target
</pre>

After saving and closing the script, start service.

`sudo systemctl start devops_service`{{execute}}
