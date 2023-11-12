**Mininet Network Emulation and TCP Congestion Control Evaluation**
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Authors:
**Ashutosh Choudhary - 20110028
Chaitanya Rao - 20110163**
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
**Overview**

This project showcases the deployment of personalized network structures using Mininet and assesses the effectiveness of TCP congestion control strategies across diverse scenarios. The trials encompass alterations to network pathways, packet capture and analysis using Wireshark, and the execution of TCP client-server applications to gauge data transfer rates. The findings offer valuable insights into how congestion control schemes influence overall network performance.
_____________________________________________________________________________________________________________________________________________________________________________
**Prerequisites**

Ensure that you have Mininet and OpenVSwitch installed on your system before running the codes.

**Mininet Installation**

Follow the steps to install mininet:

**Run the following commands after opening the terminal:**

<pre><code>
sudo apt-get update
sudo apt-get install mininet
This will install Mininet and its dependencies on your system.
</code></pre>

**Verify the installation by running:**
<pre><code>
sudo mn --version
You should see the Mininet version information.
</code></pre>
OpenVSwitch Controller Setup
For the provided scripts to work, you also need to set up the OpenVSwitch controller. Here are the steps:

**Install OpenVSwitch:**
<pre><code>
sudo apt-get install openvswitch-switch
</code></pre>
Start the OpenVSwitch service:
<pre><code>
sudo service openvswitch-switch start
</code></pre>
Verify the installation:
<pre><code>
sudo ovs-vsctl show
</code></pre>
You should see information about the OpenVSwitch bridges.

**Running the Scripts**
Now that Mininet and OpenVSwitch are set up, you can proceed to run the provided scripts:
_____________________________________________________________________________________________________________________________________________________________________________
**Part 1: Custom Topology with Mininet
Implementation**
Code: The Mininet topology is defined in the Python script q1a.py & q1c.py.
Usage: 
Execute the following script:
<pre><code>
1. open the terminal in the directory where the file is saved
2. chmod +x pythonfilename.py (make the file executable)
3. sudo ./pythonfilename.py
</code></pre>

_____________________________________________________________________________________________________________________________________________________________________________
**Part 2: TCP Client-Server Program and Throughput Analysis
Implementation**
Code: The Mininet topology, TCP client-server program are implemented in the Pythonscript pythonscript_q2.py.
Usage: Run the script using 
<pre><code>
sudo python file_name.py --config a/b/c/d --congestion cubic/bbr/reno/vegas --loss 3/1.
</code></pre>

**How to Use
Clone the repository: **
<pre><code>
git clone https://github.com/Chaitanya2708/CN_Mininet.git
</code></pre>
**Navigate to the project directory: **
<pre><code>
cd Mininet_computer_networks
</code></pre>

________________________________________________________________________________________________________________________________________________________________________________________________________________
**Throughput Analysis**
Throughput, denoted in bits per second (bps), signifies the volume of data that can be transmitted across a network within a specified time period. Tools like Wireshark and iPerf are instrumental in quantifying throughput.

**Key Experiment Observations**

1. **Impact of Congestion Control Schemes:**
   - BBR consistently outperforms other congestion control schemes, consistently achieving higher throughput.
   - Reno, in contrast, consistently exhibits the lowest throughput.

2. **Influence of Link Loss:**
   - The introduction of link loss significantly diminishes throughput, with a more pronounced effect at higher link loss rates.

3. **Effects of Multiple Clients:**
   - With multiple clients, throughput decreases compared to a single-client scenario, attributed to heightened network congestion.

**Conclusive Findings**

The throughput of a network is significantly influenced by the chosen congestion control scheme and the presence of link loss. BBR emerges as the most effective congestion control scheme, while Reno consistently displays the lowest throughput. Even at low rates, link loss can substantially degrade overall network performance.

**Potential Enhancements**

1. **Evaluation of Additional Congestion Control Schemes:**
   - Investigating the performance of alternative congestion control schemes could yield further insights into their efficacy.

2. **Analysis of Different Network Topologies:**
   - Examining the impact of congestion control schemes and link loss on diverse network topologies would broaden our understanding.

3. **Implementation of Traffic Shaping:**
   - The integration of traffic shaping techniques has the potential to optimize network performance and enhance resource utilization.
     References

[Mininet GitHub Repository](https://github.com/mininet/mininet)

[Iperf - The TCP, UDP, and SCTP Network Bandwidth Measurement Tool](https://iperf.fr/)

Feel free to explore the code and results in the provided GitHub repository for detailed insights into the implementation and experimental outcomes.
