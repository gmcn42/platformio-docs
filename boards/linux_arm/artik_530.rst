..  Copyright (c) 2014-present PlatformIO <contact@platformio.org>
    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at
       http://www.apache.org/licenses/LICENSE-2.0
    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

.. _board_linux_arm_artik_530:

Samsung ARTIK 530
=================

.. contents::

Hardware
--------

Platform :ref:`platform_linux_arm`: Linux ARM is a Unix-like and mostly POSIX-compliant computer operating system (OS) assembled under the model of free and open-source software development and distribution. Using host OS (Mac OS X, Linux ARM) you can build native application for Linux ARM platform.

.. list-table::

  * - **Microcontroller**
    - S5P4418
  * - **Frequency**
    - 1200MHz
  * - **Flash**
    - 4GB
  * - **RAM**
    - 512MB
  * - **Vendor**
    - `Samsung <https://www.artik.io?utm_source=platformio&utm_medium=docs>`__


Configuration
-------------

Please use ``artik_530`` ID for :ref:`projectconf_env_board` option in :ref:`projectconf`:

.. code-block:: ini

  [env:artik_530]
  platform = linux_arm
  board = artik_530

You can override default Samsung ARTIK 530 settings per build environment using
``board_***`` option, where ``***`` is a JSON object path from
board manifest `artik_530.json <https://github.com/platformio/platform-linux_arm/blob/master/boards/artik_530.json>`_. For example,
``board_build.mcu``, ``board_build.f_cpu``, etc.

.. code-block:: ini

  [env:artik_530]
  platform = linux_arm
  board = artik_530

  ; change microcontroller
  board_build.mcu = s5p4418

  ; change MCU frequency
  board_build.f_cpu = 1200000000L

Debugging
---------
:ref:`piodebug` currently does not support Samsung ARTIK 530 board.

Frameworks
----------
.. list-table::
    :header-rows:  1

    * - Name
      - Description

    * - :ref:`framework_artik-sdk`
      - ARTIK SDK is a C/C++ SDK targeting Samsung ARTIK platforms. It exposes a set of APIs to ease up development of applications. These APIs cover hardware buses such as GPIO, SPI, I2C, UART, connectivity links like Wi-Fi, Bluetooth, Zigbee, and network protocols such as HTTP, Websockets, MQTT, and others.