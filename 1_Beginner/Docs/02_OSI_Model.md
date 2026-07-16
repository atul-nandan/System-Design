### 🔷🔶🔷 Chapter 2: OSI Model

---

### 🔷🔶🔷 What is a Computer Network?

    🔹 In its most basic form, a computer network is defined as two or more
       connected devices that can communicate with each other and share resources.

    🔹 The medium of connection can be:
        🔸 Copper wires
        🔸 Optical fibers
        🔸 Wireless connection

    🔹 The Internet is a network of such similar networks — linking multiple
       computers together for communication and data sharing.

---

### 🔷🔶🔷 Why Do We Need the OSI Model?

**🟠 The Problem — Different Devices, Different Configurations**

    🔹 Imagine you open your browser and search on google.com.

    🔹 Your search request travels through the internet and reaches
       Google's servers.

    🔹 Google's server processes your request and sends back the result
       to your browser.

    🔹 But here is the question:
        🔸 What if your device runs Windows and Google's server runs Linux?
        🔸 What if the protocols on your device differ from Google's server?
        🔸 How can two devices with completely different configurations
           communicate successfully?

**🟠 The Solution — OSI Model**

    🔹 The answer is the OSI Model.

    🔹 OSI Model is a reference framework that explains the process of
       transmitting data between computers of different configurations.

---

### 🔷🔶🔷 What is the OSI Model?

    🔹 OSI stands for Open Systems Interconnection.

    🔹 Developed by ISO (International Organization for Standardization)
       in the year 1984.

    🔹 It is a 7-layer architecture — each layer has its own protocols
       and specific functions to perform.

    🔹 Data travels through each of these layers sequentially —
       one after the other.

    🔹 Note: OSI model is only a reference framework used in research.
       It is not in practical implementation as of today.

**🟠 The 7 Layers of the OSI Model (Top to Bottom)**

    🔸 Layer 7  ->  Application Layer
    🔸 Layer 6  ->  Presentation Layer
    🔸 Layer 5  ->  Session Layer
    🔸 Layer 4  ->  Transport Layer
    🔸 Layer 3  ->  Network Layer
    🔸 Layer 2  ->  Data Link Layer
    🔸 Layer 1  ->  Physical Layer

---

### 🔷🔶🔷 The 7 Layers — Explained in Detail

---

**🔘 Layer 7 — Application Layer**

    🔹 This is the layer where data is presented in a visual form
       that the user can understand.

    🔹 It provides the interface between the user and the application.

    🔹 Examples of network applications at this layer:
        🔸 Chrome, Edge (web browsing)
        🔸 FileZilla (file transfer)
        🔸 Outlook, Teams (email and communication)

    🔹 Functions of the Application Layer:
        🔸 Remote logging
        🔸 File transfer
        🔸 Mail services
        🔸 Resource sharing

    🔹 Protocols provided by the Application Layer:
        🔸 FTP   ->  File Transfer Protocol (for sharing files)
        🔸 HTTP / HTTPS  ->  For browsing the web
        🔸 SMTP  ->  For sending and receiving emails

    🔹 After data is prepared here, it is sent down to the
       Presentation Layer.

---

**🔘 Layer 6 — Presentation Layer**

    🔹 Also known as the Translation Layer.

    🔹 It extracts the data from the application layer and converts
       it from one format to another.
        🔸 Example: Converts data from ASCII to Binary

    🔹 Functions of the Presentation Layer:

        🔸 Translation  ->  Converting data format (e.g., ASCII to Binary)

        🔸 Compression  ->  Reducing the size of data
            Two types of compression:
                Lossy Compression:
                    - Size is reduced but some data is lost
                    - Example: Images/videos shared on WhatsApp
                      are received in reduced quality

                Lossless Compression:
                    - Size is reduced with no loss of data
                    - Example: SMS texts and emails — no data is lost
                      at the receiver's end

        🔸 Encryption   ->  Securing the data during transmission
                    - A key is used to convert data into cipher text
                    - The same key is used at the receiver's end
                      to decrypt and retrieve the original data

    🔹 After translation, compression, and encryption — the data is
       sent to the Session Layer.

---

**🔘 Layer 5 — Session Layer**

    🔹 The session layer is responsible for opening and closing the
       communication channel between sender and receiver.

    🔹 The time period for which the connection stays open is called a Session.

    🔹 Sessions can be of two types:
        🔸 Half Duplex  ->  Only one device can send data at a time
        🔸 Full Duplex  ->  Both sender and receiver can send data simultaneously

    🔹 Functions of the Session Layer:
        🔸 Establishing and managing the communication session
        🔸 Opening and closing the session
        🔸 Adding Authentication headers
            - Authentication: Verifying the identity of the user
        🔸 Adding Authorization headers
            - Authorization: Verifying if the user has permission
              to access a resource

    🔹 After session setup, data is passed to the Transport Layer.

---

**🔘 Layer 4 — Transport Layer**

    🔹 The transport layer manages the network traffic between hosts
       and end systems.

    🔹 It ensures that data packets are delivered accurately and reliably.

    🔹 Functions of the Transport Layer:

        🔸 Segmentation:
            - Data is broken down into smaller units called Segments
            - Each segment gets a Sequence Number
                (used to rearrange data correctly at the receiver's end)
            - Each segment gets a Port Number
                (used to verify that data reached the correct application)

        🔸 Flow Control:
            - Manages the rate of data transfer between sender and receiver
            - Example: Sender sends at 100 Mbps but receiver can only
              handle 50 Mbps — flow control adjusts the sender's rate
              so no data is lost

        🔸 Error Control:
            - Ensures that data received is not corrupted
            - A Checksum is added to each segment
            - At the receiver's end, the checksum is used to verify
              the integrity of data
            - If data is corrupted, it is retransmitted

    🔹 After segmentation, data segments are sent to the Network Layer.

---

**🔘 Layer 3 — Network Layer**

    🔹 The network layer is responsible for transmission of data between
       devices present in different networks.

    🔹 Functions of the Network Layer:

        🔸 Logical Addressing:
            - Receives data segments from the Transport Layer
            - Converts segments into Data Packets
            - Adds Source IP Address and Destination IP Address
              to each data packet

        🔸 Routing:
            - Determines the most suitable path for the data to travel
              from the source to the destination

    🔹 After creating data packets and determining the route,
       data is passed to the Data Link Layer.

---

**🔘 Layer 2 — Data Link Layer**

    🔹 The data link layer is responsible for reliable transmission of
       data across a physical network.

    🔹 Functions of the Data Link Layer:

        🔸 Physical Addressing:
            - Receives data packets from the Network Layer
            - Creates Data Frames by adding:
                Source MAC Address
                Destination MAC Address
            - MAC Address is a unique 12-digit hexadecimal number
              that identifies a device on a network
            - It is assigned by the manufacturer during production
              of the Network Interface Card (NIC)

        🔸 Sub-layers of the Data Link Layer:
            - LLC (Logical Link Control)
                -> Handles error detection and sequencing of data frames
            - MAC (Media Access Control)
                -> Creates the data frame from the data packet
                   using the MAC address from the NIC

        🔸 Collision Detection and Avoidance:
            - If two devices try to send data at the same time,
              there is a risk of collision
            - The data link layer detects and avoids such collisions
              and controls the flow of data in the network

    🔹 After creating data frames, they are passed to the Physical Layer.

---

**🔘 Layer 1 — Physical Layer**

    🔹 The physical layer is the last and final layer of the OSI model.

    🔹 It includes the actual physical equipment involved in data transfer:
        🔸 Cables, switches, network interface cards

    🔹 It specifies how bits are represented on the medium.

    🔹 The data frames received from the Data Link Layer are in binary format.
       The physical layer converts this binary data into signals based on
       the transmission medium:

        🔸 Copper wires     ->  Electrical signals
        🔸 Optical fibers   ->  Light pulses
        🔸 Wireless         ->  Radio waves

    🔹 At the receiver's end, the Physical Layer converts these signals
       back into binary data and passes it up through the layers.

---

### 🔷🔶🔷 Data Flow Through OSI Layers — Sender to Receiver

**🟠 At the Sender's End (Top to Bottom)**

    🔹 Layer 7 — Application Layer:
        🔸 Data is prepared and presented for transmission

    🔹 Layer 6 — Presentation Layer:
        🔸 Data is translated, compressed, and encrypted

    🔹 Layer 5 — Session Layer:
        🔸 Authentication and authorization headers are added
        🔸 Communication session is established

    🔹 Layer 4 — Transport Layer:
        🔸 Data is segmented
        🔸 Sequence numbers, port numbers, and checksum are added

    🔹 Layer 3 — Network Layer:
        🔸 Segments become Data Packets
        🔸 Source and destination IP addresses are added
        🔸 Best route is determined

    🔹 Layer 2 — Data Link Layer:
        🔸 Data Packets become Data Frames
        🔸 Source and destination MAC addresses are added

    🔹 Layer 1 — Physical Layer:
        🔸 Data Frames (binary) are converted into
           electrical / light / radio signals and transmitted

**🟠 At the Receiver's End (Bottom to Top)**

    🔹 The same process happens in reverse — signals are converted back
       to binary and each layer strips off its header/information
       until the original data reaches the application at Layer 7.

---

### 🔷🔶🔷 Summary — OSI Model at a Glance

    🔸 Layer 7 — Application    ->  User interface, protocols (HTTP, FTP, SMTP)
    🔸 Layer 6 — Presentation   ->  Translation, Compression, Encryption
    🔸 Layer 5 — Session        ->  Session management, Authentication, Authorization
    🔸 Layer 4 — Transport      ->  Segmentation, Flow Control, Error Control
    🔸 Layer 3 — Network        ->  Logical Addressing (IP), Routing
    🔸 Layer 2 — Data Link      ->  Physical Addressing (MAC), Framing, Collision Control
    🔸 Layer 1 — Physical       ->  Converts binary to signals (electrical/light/radio)

    🔹 OSI Model is a reference framework — not used in practical
       implementation today, but essential for understanding how
       network communication works.

---