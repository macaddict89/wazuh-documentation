.. Copyright (C) 2020 Wazuh, Inc.

.. meta:: :description: Learn how to install the Wazuh agent on AIX

.. _wazuh_agent_package_aix:

AIX
===

You can download the `AIX installer <https://packages.wazuh.com/3.x/aix/wazuh-agent-|WAZUH_LATEST_AIX|-|WAZUH_REVISION_AIX|.aix.ppc.rpm>`_ from our :ref:`packages list <packages>`. You can choose installation or a deployment:

  a) Installation:

    .. code-block:: console

      # rpm -ivh wazuh-agent-|WAZUH_LATEST_AIX|-|WAZUH_REVISION_AIX|.aix.ppc.rpm

    With this simple installation, the next step is to register and configure it to communicate with the manager. For more information about this process, please visit the document: :ref:`user manual<register_agents>`.

  b) Deployment:

    You can automate the agent registration and configuration using variables. It is necessary to define at least the variable ``WAZUH_MANAGER``. The agent will use this value to register and this will be the assigned manager for forwarding events.

    .. code-block:: console

      # WAZUH_MANAGER="10.0.0.2" rpm -ivh wazuh-agent-|WAZUH_LATEST_AIX|-|WAZUH_REVISION_AIX|.aix.ppc.rpm

    See the following document for additional deployment options: :ref:`deployment variables <deployment_variables_aix>`.
