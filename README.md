# weather.timer
Linux lab11 systemd service and timer practice

# How to use weather.timer
**Step 1**
Clone reposity containing the files into your machine
`git clone https://github.com/98-percent-Milk/weather.timer.git`

**Step 2**
Open weather.service in vim and set paths for ExecStart and WorkingDirectory to 
directory where you cloned the repository.
For example if you've cloned repository is in "/home/week11" change the paths into

`vim weather.service`
ExecStart=/home/week11/weather.timer/weather
WorkingDirectory=/home/week11/weather.timer

**Step 3**
Move weather.service and weather.timer to "/etc/systemd/system"
`mv weather.service weather.timer /etc/systemd/system`

**Step 4** 
Check if the status of weather.service and weather.timer are active.
If the status is inactive then
`sudo systemctl start weather.service`
`sudo systemctl start weather.timer`
If the both status are active then **do nothing**

