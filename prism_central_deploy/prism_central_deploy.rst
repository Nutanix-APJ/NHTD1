.. _prism_central_dashboards_reports:

-------------------------------------
PC Deployment
-------------------------------------

Overview
++++++++

.. note::

  Estimated time to complete: **30 Minutes**

This lab will introduce Prism Central’s One-Click deploy process

Create Primary and Secondary networks
+++++++++++++++++++++++++++++++++++++

.. note::

The primary network is for PC and other VMs deployment, the secondary network is requried in X-Ray and Files lab

Open \https://*<POCxx-ABC Cluster IP>*:9440 (\https://10.42.xx.37:9440) in your browser and log in with the following credentials:

- **Username** - admin
- **Password** - tech2020!

Navigate to **Prism > Configuration** and click **Network Configuration**, then **Virtual Networks** .

Click **Create Network**. Fill out the following fields and click **Save**:

Name - Primary
VLAD ID - 0

Click **Create Network**. Using the Cluster Details spreadsheet, fill out the following fields and click **Save**:

- **Name** - Secondary
- **VLAD ID** - *<Secondary VLAN ID>* xx1 (xx is your cluster ID)

.. figure:: images/image001.png

Prism Central Deploy
+++++++++++++++++++++

Open \https://*<POCxx-ABC Cluster IP>*:9440 (\https://10.42.xx.37:9440) in your browser and log in with the following credentials:

- **Username** - admin
- **Password** - tech2020!

Navigate to **Home** page and click **Register or create new** in Prism Central widget.

.. figure:: images/1.png

Choose the first **Deploy** option.

.. figure:: images/2.png

Download the latest version and click **deploy 1-VM PC**

.. figure:: images/3.png

Fill out the following fields, leave others as default and click **Deploy**:

- **AHV Network** - Primary
- **IP Address** - 10.42.xx.39
- **Subnet Mask** - 255.255.255.128
- **Default Gateway** - 10.42.xx.1
- **DNS Address(Es)** - 10.42.196.10

.. figure:: images/4.png

.. figure:: images/5.png

.. note::

After Prism Central VM is successfully deployed, open \https://*<PC VM IP>*:9440 (\https://10.42.xx.39:9440) in your browser and log in with the following credentials:

- **Username** - admin
- **Password** - default with capital N
- change password to **techX2020!**

Test if you can login Prism Central with the new password.


Prism Central Registration
+++++++++++++++++++++

Go back to POCxx-ABC Cluster  (\https://10.42.xx.37:9440), navigate to **Home** page and click cluster name **POCxx-ABC** and provide a cluster data service ip **10.42.xx.38**

.. figure:: images/9.png

Click **Register or create new** in Prism Central widget. 

.. figure:: images/1.png

Choose the second **Connect** option. 

.. figure:: images/2.png

Click **Next**

.. figure:: images/6.png

Fill out the following fields, leave others as default and click **Connect**:

- **Prism Central IP** - 10.42.xx.39
- **Port** - 9440
- **Username** - admin
- **Password** - techX2020!

.. figure:: images/7.png

You will see an **OK** with PC's IP in Prism Central widget.

.. figure:: images/8.png

.. note::

  Prism Central's default password must be changed before cluster registering PC


