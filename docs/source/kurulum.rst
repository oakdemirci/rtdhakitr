Kurulum
=====

 _kurulum:


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

#. `Linux kurulum`_ dosyasını indirin.

#. Aşağıdaki komutları çalıştırın.

.. code-block:: console

   bash Miniforge3-Linux-x86_64.sh
   eval "$(/home/murat/miniforge3/bin/conda shell.bash hook)"
   conda init
   conda config --set auto_activate_base false
.. _linux kurulum: https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-Linux-x86_64.sh


OsX
^^^^^^^^

#. `OsX kurulum`_ dosyasını indirin.

#. Aşağıdaki komutları çalıştırın.

.. code-block:: console

   bash Miniforge3-MacOSX-x86_64.sh

.. _osx kurulum: https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-MacOSX-x86_64.sh

UHTE Sanal Ortamı Oluşturma
------------

.. note::

   Windowsta; miniforge kurulumu sonrasında, "Windows" tuşuna basın, "miniforge" aratın, ve "Miniforge Prompt" uygulamasını çalıştırın.
 
UHTE sanal ortamını aşağıdaki komutu çalıştırarak oluşturun.


.. code-block:: console

   conda create -vv -n UHTE python=3.9 jupyter


JupyterLab
------------

“Miniforge Prompt” penceresinde;

#. UHTE sanal ortamını etkinleştirin.
#. JupyterLab kurun.

.. code-block:: console

   conda activate UHTE
   conda install jupyterlab


GNU Radio
------------

“Miniforge Prompt” penceresinde;

#. GNU Radio kurun.

.. code-block:: console

   conda config --append channels conda-forge
   conda install gnuradio python=3.9


Python Kütüphaneleri
------------

“Miniforge Prompt” penceresinde; 

#. Aşağıdaki Python kütüphanelerini kurun.

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

#.  `Osmocom`_ indirin.
#. Sıkıştırılmış dosyası sanal ortam kurulu dizinine çıkartın, örneğin C:\\Users\\murat\\miniforge3\\envs\\UHTE

.. _osmocom: https://downloads.osmocom.org/binaries/windows/rtl-sdr/rtl-sdr-64bit-20221120.zip

RTL-SDR Sürücüleri
------------

.. note::
   
   Sürücüler donanım takılı iken kurulabildikleri için, kurulum ders sırasında tamamlanacaktır. Bu adım için dosya indirilmesi yeterlidir.
   
#. `Rtl`_ ve `Sdr`_ dosyalarını indirin.
   
.. _rtl: https://github.com/pbatard/libwdi/releases/download/b730/zadig-2.5.exe
.. _sdr: https://airspy.com/?ddownload=3130


Kurulumun Test edilmesi
------------

#. Yeni bir “Miniforge Prompt” açın.
#. Sanal ortamı etkinleştirin.
#. Jupyter Lab'ı açın ve yeni bir not defteri açın.

.. code-block:: console

   conda activate UHTE
   jupyter-lab
