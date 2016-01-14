## Architecture and Design ##

The GVirtuS (General-purpose Virtualization Service), is implemented as a framework for split-driver based abstraction components.

The brightest GVirtuS feature is the independence from all involved technologies: the hypervisor, the communicator and the target of the virtualization (general purpose graphic processing units for computing acceleration, high performance network interface cards for improved message passing interface parallel applications, virtual distributed parallel file systems, instruments and data acquisition interfaces).

In GVirtuS a generic split-driver is abstracted and made available for developers thanks to the underlying idea of shared common parts among different driver applications. In this way, developing a virtualization driver means implement only application specific code leveraging on common utilities and communication enforcements.

GVirtuS abstracts the following components:

  * Stub library:
> imitates the real driver library offering its same application binary interface. The gest side virtualization is done in the stub library calling the front end component that interfaces with the backend via the communicator. From the architectural point of view, the stub library represents the front end itself.

  * Daemon:
> runs on the host operating system in the user space or super user space depending by the specific application and security policies. The daemon implements the back end dealing with the real device driver and performing the host side virtualization.

  * Communicator:
> performs the connection between the real machine on the host side and the virtual machines on the guest side. As in the commonly used split driver model, the communicator has high performance constraints and must honor high performance requirements. In GVirtuS the communicators have to be even hypervisor and virtualized technology independent.