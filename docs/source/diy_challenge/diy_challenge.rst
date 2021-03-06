05 - DIY IoT Challenge!
========================

Now it's time to test your IoT skills, and see if you can build a working end-to-end IoT solution that will measure **temperature, humidity, and light levels**, and send that data from your Rackspace IoT board to AWS using MQTT.

**Tip:** If you need to re-import a module to run the code again, check out "Re-importing module code" in section :doc:`../hints/hints`

Here are some hints to help you get started:

- Use the ``hello_world.py`` you used in section :doc:`../iot_hello_world/iot_hello_world` as a base for your script, as it already has a working MQTT client that sends data to the cloud.  You just need to change what data it sends!

- You will need to replace the hello world data in that script with temp, humidity and light data.  Use what you learned in section :doc:`../sensors/sensors` to figure out how to do this.

- Pay attention, the ``hello_world.py`` script is missing a library you need to read one of your sensors! Inspect what you previously did to read the sensors successfully, and add any missing libraries to the ``import`` section at the top of your script.

- Leave the ``topic`` values unchanged in your script.  That is, similar to::

    iotsample/company_name/team_name/data

- You have completed the challenge successfully when your device is sending json data like that shown below, to the same AWS IoT endpoint as before.  Note that the **time** and **thingId** fields are required, and are already correctly populated in the commented out example in ``hello_world.py``::

    >> import my_script
    published to topic iotsample/company_name/team_name/data: {"thingId": thingId,"time": 600,"temperature": '21',"humidity": '51',"light": '4095'}
    published to topic iotsample/company_name/team_name/data: {"thingId": thingId,"time": 605,"temperature": '21',"humidity": '51',"light": '4095'}
    ...
    ...

Did you get the desired data to send?  If so, great work!!
