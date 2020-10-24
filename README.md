# Master-Minions
Master-Minions model that achieves network-attached-storage behavior using RAID 01 technique. The program consists of different modulus that all attached together according to the OOP principles.  


1. Back Ground:

The project supplies a mechanism which allows taking advantage of external storage devices.  As the IOT suggests, our system consists of interrelated computing devices, mechanical and digital machines provided with unique id and the ability to transfer data over a network without requiring human-to-human or human-to-computer interaction. The end user will see all the entire external storage devices as one external server that will be used as an external storage device. Our system operates as a NAS (Network Attached Storage) server which is a file-level computer data storage server connected to a computer network providing data access to a heterogeneous group of clients.
We use RAID 01 technique to equivalently stripe the data across multiple disks and increase reliability by creating a copy of each data block that was written within another disk. 
The Master - Minions is a model of asymmetric communication where one device (Master) controls multiple external devices (Minions).
We’re using the NBD (Network Block Device) to send requests via the kernel back to the user space. A specific folder should be chosen and be mounted to the NBD. Once that happens, and the program is running, each change within the mounted folder will be translated as a unique request and will be transferred to the external storage devices in a form of RAID01 technique as explained before. 

2. Purposes:

    • Educational purposes: 
        a. Design Patterns
            • Factory
            • Singleton
            • Dispatcher
            • Reactor
            • Subject - Observer
            • ThreadPool
             • Command
        b. Networking
        c. Serializer

    • Project purposes:
    a. Using external storage devices to store data externally by taking advantage of already existing smart devices.
    b. Creating  a default backup mechanism for the entire transferred data. 
    c. Working in parallel to improve performance. 

    3. Attributes:
            a. EventDriven
            b. Configurability:
                The architure of our system can be modified as needed. For instance, the amount of minions(external storage devices) can be changed.
            c. Fault Tolerance:
                We used a WatchDog software component to monitor each process in our system. 
            d. Plug and Play:
               Our program is extensible. New features can be added during run-time.

    4. Verification
    
           Our program will be verified by using an external Raspberry Pi as a storage device.
