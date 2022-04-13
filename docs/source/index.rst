#########
OakVar
#########

OakVar is a fork of OpenCRAVAT, further developed by the former lead architect of OpenCRAVAT, Ryangguk Kim.

OakVar is a drop-in replacement of OpenCRAVAT and does not have a breaking change. Same ``oc`` commands work. OakVar's own command ``ov`` works just like ``oc`` at this moment.

For what is not explained in this document, please refer to https://open-cravat.readthedocs.org for documentation.

************
Installation
************


Pre-requisite: Uninstalling OpenCRAVAT (if installed)
*****

* If OpenCRAVAT was installed with ``pip``, do ``pip uninstall open-cravat``.
* If OpenCRAVAT was installed with ``conda``, do ``conda remove open-cravat``.

======================================
Linux
======================================

Non-conda environment
===================

Single-user use
---------------
::

  >pip install oakvar

See the output of ``pip install`` for the location of ``oc`` executable, which should be added to PATH. A system configuration file and system folders will be created in ``~/.oakvar``.
::

  >oc module install-base

Base modules (minimum needed modules) will be installed.

Installation configuration can be examined with ``oc config system``.

System-wide use
-----------
::

  >sudo install oakvar

``oc`` executable will be installed where it can be accessed by all users. A system configuration file will be installed in the package's folder. Thus, ``oc`` commands which change system configurations (such as ``oc config md``) should be done with ``sudo``. However, other operations such as annotation with ``oc run`` and GUI with ``oc gui`` will not need ``sudo``. System folders will be installed in ``~/.oakcravat`` of the user who did the installation.
::

  >oc

  It seems that OakVar has been installed as root 
  and that you are running it for the first time. 
  To configure OakVar properly, you can do one of 
  the following:
  
  1) Stop at this point with Ctrl-C and run 
  `sudo oc` just once to create a system configration 
  file and system folders.
  
  OR
  
  2) Type Enter and continue. OakVar will need to 
  access `sudo` three times, once to create a system
  configration file, then to modify it, and then to
  change its file permission back. 
  
  Either way, afterwards, normal users will be able 
  to use `oc` commands without sudo privilege, 
  except when making changes to system settings.

  Ctrl-C to stop or Enter to continue>

Choose one of the two options to set up a system configuration file.

The default system folders (module folders, job folders, etc)  will have been made under ``~/.oakvar`` of the user who installed OakVar. If wish to move the system folders to a different location such as a shared one, do ``oc config system`` and find the location of the OakVar system configuration file at ``Configration file path``. Open the file and edit ``modules_dir``, ``conf_dir``, ``jobs_dir``, and ``log_dir`` as wished.

::

  >oc module install-base

Base modules (minimum needed modules) will be installed.

Installation configuration can be examined with ``oc config system``.

Conda/mamba environment
===================

Single-user use
---------------
::

  >pip install oakvar

``oc`` executable will be installed where the user can access. A system configuration file and system folders will be created in ``~/.oakvar``.
::

  >oc module install-base

Base modules (minimum needed modules) will be installed.

Installation configuration can be examined with ``oc config system``.
