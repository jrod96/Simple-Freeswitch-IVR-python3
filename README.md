# Simple-Freeswitch-IVR-python3
Simple Freeswitch IVR app written in python3 

**Options:**<br>
Press 1 for demo ivr (ext 5000)<br>
Press 2 for reach Juan (ext 1000)<br>
Press 3 to reach Jesus (ext 1001)<br>
Press 0 to exit (hung up)<br>

**Freeswitch modules used:**<br>
mod_python3<br>
mod_flite<br>

Python script is located at: /usr/share/freeswitch/scripts/ <br>

### Freeswitch Dialplan

>\<extension name="python_demo"\><br>
>&nbsp; &nbsp; &nbsp; \<condition field="destination_number" expression=**"^2407$"**\><br>
>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; \<action application="system" data="export PYTHONPATH=$PYTHONPATH:**/usr/share/freeswitch/scripts/**"\><br>
>&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; \<action application="python" data="**ivr**"\/><br>
> &nbsp; &nbsp; &nbsp;     \</condition\><br>
>\</extension\><br>
