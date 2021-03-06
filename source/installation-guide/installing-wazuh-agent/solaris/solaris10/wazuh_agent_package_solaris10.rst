.. Copyright (C) 2019 Wazuh, Inc.

.. _wazuh_agent_package_solaris10:

Solaris 10 from package
=======================
You can download the `Solaris10 installer (Intel architecture) <https://packages.wazuh.com/3.x/solaris/i386/10/wazuh-agent_v3.11.4-sol10-i386.pkg>`_ or `Solaris10 installer (SPARC architecture) <https://packages.wazuh.com/3.x/solaris/sparc/10/wazuh-agent_v3.11.4-sol10-sparc.pkg>`_ from our from our :ref:`packages list<packages>`. The current version has been tested on Solaris 10 version 5.10. Install the agent as follows:

  a) For Solaris 10 i386:

    .. code-block:: console

      # pkgadd -d wazuh-agent_v3.11.4-sol10-i386.pkg

  b) For Solaris 10 SPARC:

    .. code-block:: console

      # pkgadd -d wazuh-agent_v3.11.4-sol10-sparc.pkg

After creating the repository install the package:

    .. code-block:: console

        # pkg install --accept wazuh-agent

Finally, remove the publisher:

    .. code-block:: console

        # pkg unset-publisher wazuh

Now that the agent is installed, the next step is to register and configure it to communicate with the manager. For more information about this process, please visit the document: :ref:`user manual<register_agents>`.

Uninstall
---------

To uninstall the agent in Solaris 10:

    .. code-block:: console

      # pkgrm wazuh-agent
