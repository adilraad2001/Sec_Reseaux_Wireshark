# TP2_Sec_Reseaux
![LOGO](https://user-images.githubusercontent.com/99618982/225015198-317d743a-74b9-44ad-a13b-7e698620b346.jpeg)
Realisé Par : Adil Erraad

# Sommaire:

 1. **Introduction:**
 
    1. *Objectifs de ce TP :*
    
    >
    > - To set up a network topology using three virtual machines: one router and two clients.
    
    > - Connect the clients to the router using their respective interfaces.

    > - Configure the router to allow for ping communication between the clients.

    > - Use Wireshark to capture network traffic between the clients when pinging each other.

    > - Analyze the captured traffic and gain an understanding of how the network operates.
           
    >
    
    2. *Outils logiciels :*
    
    >
    > - Wireshark.
    
    > - virtualbox: 3 Machine.
    
    >
      
 2. **Network Topology:**
 
 ![Topology](https://user-images.githubusercontent.com/99618982/226592631-a67a5393-3de2-44a5-b258-d57e92b541d3.jpg)
 
   2.1. Device preparation:
 
 First, we must prepare the devices used so that we will install an operating system in each device using the virtualBox, and then clarify the device that will work as a client and the device that will work as a server or router .
 
   Clients:
    
  >
  > -  Client1(Ubuntu):Ubuntus Client1.
    
  > -  Client2(Ubuntu):Ubuntus Client1 .
    
  >
    
   Server:
    
> -  adilraad(Ubuntu):Ubuntus
 
 Secondly, each client device must be placed on a different network, and we do this by making each device connected to a different interface and making the server connected to all interfaces in order to work as a router.
 
  >
  > -  Client1: intnet.
    
  > -  Client2: intnet2.
  
  > -  Server: intnet + intnet2.
    
  >
 
Clients:

![2023-03-28 15_02_48-ubuntus Client1 - Settings](https://user-images.githubusercontent.com/99618982/228282098-2c902f13-caa6-41c7-a269-303e0a6cb1b5.jpg)


Server:

![2023-03-28 15_05_50-ubuntus - Settings](https://user-images.githubusercontent.com/99618982/228282595-f5fed2b3-5da6-4655-ae8b-a10e930b5be4.jpg)

   2.2. Device Configuration:
   
   At this part, we will give the server and clients fixed IP addresses, and check whether the server works as a router or not by confirming the existence of a connection between two connected clients in a different network.
   
   Server:
   
   * **intnet(192.168.1.1)** 
   
   * **intnet2(192.167.1.1)**
   
   ![4](https://user-images.githubusercontent.com/99618982/228285913-e9813403-11cb-4679-9d8a-a2bfb91fa9c2.jpg)
   
   And check is the interface work well by pinging
   
   ![3](https://user-images.githubusercontent.com/99618982/228286071-0afa6c5b-743d-4dcf-9c50-aaeadf88f5ba.jpg)
   
   ![5](https://user-images.githubusercontent.com/99618982/228287002-5fb8c9b2-c32c-4412-9beb-9ae231bf8b71.jpg)


   So Everything work Now let's go to clients

   Clients:
   
   There are several ways to give the device a fixed IP address, such as using commands, but I will depend on the settings of the device:
   
   * **client1(192.168.1.2)** 
   
   ![7](https://user-images.githubusercontent.com/99618982/228288452-f11cf15b-42df-46f2-8b08-f2d613efbf38.jpg)
   
   Now Check the addresse and check connection with the server:
   
   ![8](https://user-images.githubusercontent.com/99618982/228288651-1f0612bd-c00b-419e-8f0f-4425cd900afc.jpg)
   
   ![9](https://user-images.githubusercontent.com/99618982/228288790-0c83b170-79f4-4103-9c30-736240be316f.jpg)
   
   So we have connection with successful and as we see the client added to arp table of server with the id of interface from where connected

   * **client2(192.167.1.2)**
   
   ![11](https://user-images.githubusercontent.com/99618982/228289668-0bd237bb-9ebc-4f37-b86b-a2b8456ec354.jpg)
   
   ![12](https://user-images.githubusercontent.com/99618982/228289748-7495e50c-54c4-4fcf-8172-1f2fcf41efd4.jpg)

   ![13](https://user-images.githubusercontent.com/99618982/228289779-14533ffd-8c20-45fa-8b43-1f1b085b0bd8.jpg)
   
   *So, as you can see, every time a new device is connected to the server, it is added to the server ARP table in order to associate each IP address with its MAC address.*
   
   *So each new Connection equal new arp traffic*
   
   **Now Let's check the connection between the two client**
   
   ![14](https://user-images.githubusercontent.com/99618982/228291351-2af3f874-5c03-46d0-952e-0522f69094fb.jpg)
   
   So the connection failed --> So we need to allow the routing in the server Device
   
   ![15](https://user-images.githubusercontent.com/99618982/228291640-1772adab-f0ce-4a3d-be1d-0547297f2935.jpg)

  Let'x check:

   ![16-1](https://user-images.githubusercontent.com/99618982/228291768-63a6cd97-39c0-497a-9ece-de5fb38eca1b.jpg)
    
  Now the connection with successful between two device in different networks
    
  **So we to make device work as router we need to connect the device with the different networks of clients and allow Routing by using the command or do it manualy by the  routing table**
    
  _*Now let's cupt the traffic between the two client*_


   

 3. **Capture des traffic:**
 
 
    
 
 4. **Conclusion:**
