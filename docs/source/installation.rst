Kurulum
=====

.. _installation:

Miniforge
------------

Windows
^^^^^^^^


.. note::

   Kurulum sırasında mevcut sistem ayarlarını değiştirmemek amacıyla yeni bir sanal ortam oluşturulmalıdır.

#. `miniforge`_ dosyasını indirin ve kurulumu tamamlayın. Mevcut kullanıcı için kurulum yapılması durumunda hedef dizin c:\\Users dizini olacaktır, örneğin başarılı bir kurulum sonrasında uygulamalar c:\\Users\\murat\\miniforge3 dizininde çalışacaktır.

.. _miniforge: https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-Windows-x86_64.exe

Linux
^^^^^^^^

#. Download `Linux installation`_ file.

#. Run following command(s)

.. code-block:: console

   bash Miniforge3-Linux-x86_64.sh
   eval "$(/home/murat/miniforge3/bin/conda shell.bash hook)"
   conda init
   conda config --set auto_activate_base false
.. _linux installation: https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-Linux-x86_64.sh


OsX
^^^^^^^^

#. Download `OsX installation`_ file.

#. Run following command(s)

.. code-block:: console

   bash Miniforge3-MacOSX-x86_64.sh

.. _osx installation: https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-MacOSX-x86_64.sh

UHTE Virtual Environment Creation
------------

.. note::

   On Windows; after miniforge installation, press "Windows key", search for "miniforge" and run "Miniforge Prompt".
 
Create virtual env UHTE with the following command.


.. code-block:: console

   conda create -vv -n UHTE python=3.9 jupyter


JupyterLab
------------

On “Miniforge Prompt” window;

#. activate UHTE venv
#. install JupyterLab.

.. code-block:: console

   conda activate UHTE
   conda install jupyterlab


GNU Radio
------------

On “Miniforge Prompt” window; 

#. install GNU Radio.

.. code-block:: console

   conda config --append channels conda-forge
   conda install gnuradio python=3.9


Python Libraries
------------

On “Miniforge Prompt” window; 

#. install the following Python libraries.

.. code-block:: console

   conda install numpy
   conda install scipy
   conda install matplotlib
   conda install -c conda-forge ipympl
   conda install -c conda-forge python-sounddevice
   pip install playsound==1.2.2
   conda install soapysdr-module-rtlsdr
   conda install pymodes


osmocom
------------

#. Download `Osmocom`_
#. Extract zip to virtual environment path, for example C:\\Users\\murat\\miniforge3\\envs\\UHTE

.. _osmocom: https://downloads.osmocom.org/binaries/windows/rtl-sdr/rtl-sdr-64bit-20221120.zip

RTL-SDR Drivers
------------

.. note::
   
   Drivers need physical hardware and setup will be completed during lessons. File download is sufficient for this step.
   
#. Download `Rtl`_ ve `Sdr`_ files.
   
.. _rtl: https://github.com/pbatard/libwdi/releases/download/b730/zadig-2.5.exe
.. _sdr: https://airspy.com/?ddownload=3130


Test Installation
------------

#. Open a new "Miniforge Prompt".
#. Activate virtual environment.
#. Open Jupyter Lab and open a new notebook.

.. code-block:: console

   conda activate UHTE
   jupyter-lab
