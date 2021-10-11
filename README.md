# pulpissimo-assets

This repository contains assets for the pulp-pulpissimo platform (see [Pulpissimo](https://github.com/pulp-platform/pulpissimo)).

The following bitstreams were generated with version v7.0.0 of Pulpissimo and contain only the default IPs of Pulpissimo. Check out the documentation of Pulpissimo on how to configure your FPGA with these bitstreams.
* ``bitstrams/pulpissimo-zcu104.bit``, ``bitstreams/pulpissimo-zcu104.bin``
* ``bitstramspulpissimo-ultrazed7ev.bit``, ``bitstreams/pulpissimo-ultrazed7ev.bin``

The following bitstreams were generated with version v7.0.0 of Pulpissimo with the example AXI-attached IP Core *wide_alu*.
* ``bitstrams/pulpissimo_zcu104_pulpissimoV7_wide_alu.bit``, ``bitstreams/pulpissimo_zcu104_pulpissimoV7_wide_alu.bin``
* ``bitstrams/pulpissimo_ultrazed_7ev_cc_pulpissimoV7_wide_alu.bit``, ``bitstreams/pulpissimo_ultrazed_7ev_cc_pulpissimoV7_wide_alu.bin``


The directory ``openocd-cfg`` holds config files that are used to communicate with the jtag controller of pulpissimo. Check out the pulpissimo documentation on how to use the config files and how to debug pulpissimo running on an FPGA target
* ``openocd-cfg/openocd-zcu104-digilent-jtag-hs3.cfg``
* ``openocd-cfg/openocd-ultrazed7ev-digilent-jtag-hs3.cfg``

The following directory holds FPGA target specifics for Pulpissimo on UltraZed7EV Platform. In order synthesize the design for UltraZed7EV move this directory into the ``fpga`` subdirectory of pulpissimo. Further replace the ``Makefile`` in the ``fpga`` directory of pulpissimo with the customized Makefile ``Makefile_move_to_parent_dir``. Check out the documentation of pulpissimo on how to synthesize pulpissimo for a specific FPGA target.
* ``pulpissimo-ultrazed7ev``

The directory ``elf-files`` holds precompiled elf files for pulpissimo, i.e., applications that can be loaded and run on a FPGA target that was configured with Pulpissimo. Check out the Pulpissimo documentation about how to load and debug an application.
* ``elf-files/zcu104-default-design-test`` - can be used on a unmodified version of Pulpissimo v7.0.0; prints ``Hello !`` to UART
* ``elf-files/zcu104-pulpissimoV7_wide_alu_test`` - example application for the ``wide_alu`` design; prints  ``result[0]: 7`` via UART; use this application in combination with ``bitstrams/pulpissimo_zcu104_pulpissimoV7_wide_alu.bit``
* ``elf-files/ultrazed7ev-pulpissimoV7_wide_alu_test``- example application for the ``wide_alu`` design; prints  ``result[0]: 7`` via UART; use this application in combination with ``bitstrams/pulpissimo_ultrazed7ev_pulpissimoV7_wide_alu.bit``
