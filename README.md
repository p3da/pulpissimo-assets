# pulpissimo-assets

This repository contains assets for the pulp-pulpissimo platform (see [Pulpissimo](https://github.com/pulp-platform/pulpissimo)).

The following bitstreams were generated with version v7.0.0 of Pulpissimo and contains only the default IPs of Pulpissimo. Check out the documentation of Pulpissimo on how to configure your FPGA with these bitstreams.
* bitstrams/pulpissimo-zcu104.bit, bitstreams/pulpissimo-zcu104.bin
* bitstramspulpissimo-ultrazed7ev.bit, bitstreams/pulpissimo-ultrazed7ev.bin

The directory ``openocd-cfg`` holds config files that are used to communicate with the jtag controller of pulpissimo. Check out the pulpissimo documentation on how to use the config files and how to debug pulpissimo running on an FPGA target
* openocd-cfg/openocd-zcu104-digilent-jtag-hs3.cfg

The following directory holds FPGA target specifics for Pulpissimo on UltraZed7EV Platform. In order synthesize the design for UltraZed7EV move this directory into the ``fpga`` subdirectory of pulpissimo. Further replace the ``Makefile`` in the ``fpga`` directory of pulpissimo with the customized Makefile ``Makefile_move_to_parent_dir``. Check out the documentation of pulpissimo on how to synthesize pulpissimo for a specific FPGA target. 
