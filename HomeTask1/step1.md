Firstly I created script to run in the background.
Create a new file with `nano` and copy following script in it.

`sudo nano /devops_script.sh`{{execute}}

<pre>
echo "devops.service: ## Starting ##" | systemd-cat -p info
while :
do
TIMESTAMP=$(date '+%Y-%m-%d %H:%M:%S')
echo "devops.service: timestamp ${TIMESTAMP}" | systemd-cat -p info
sleep 60
done
</pre>

After saving and closing the script, make it executable.

`sudo chmod +x /devops_script.sh`{{execute}}
