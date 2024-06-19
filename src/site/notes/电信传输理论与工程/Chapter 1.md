---
{"dg-publish":true,"permalink":"/电信传输理论与工程/Chapter 1/","tags":["网络拓扑","QoS","dB","增益"]}
---

# Basic concepts of telecommunication transmission
## 1.2 A communication model
![assets/Pasted image 20240601201227.png|575](/img/user/%E7%94%B5%E4%BF%A1%E4%BC%A0%E8%BE%93%E7%90%86%E8%AE%BA%E4%B8%8E%E5%B7%A5%E7%A8%8B/assets/Pasted%20image%2020240601201227.png)
- **Source**: generates the data to be transmitted. <br>产生需要传输的数据
- **Transmitter**: transforms and encodes the information in such a way as to produce electromagnetic signals that can be transmitted across some sort of transmission system. <br>将信息转化和编码为传输系统中接受的电磁信号
- **Transmission system**: connects source and destination, *this can be a single transmission line or a complex network* <br>连接 source 和 destination<br>_**注意**：“系统”的定义不是死的，可以是传输线，也可以是复杂的网络_
- **Receiver**:  accepts the signal from the transmission system and converts it into a form that can be handled by the destination device. <br>接收信号并转化成数据信息
- **Destination**: Takes the incoming data from the receiver.<br>接收数据

## 1.3 The Transmission of Information
- **Transmission**: 传输
- **Propogation**: 传播 (物理的)

### 1.3.1 Transmission and Transmission Media
常见的 Transmission Media:
- twisted pair lines 双绞线
- coaxial cable 同轴线
- optical fiber cable 光缆
- terrestrail and satellite microwave 地面微波和卫星微波 (波导)

### 1.3.2 Transmission Efficiency
在任何计算机/通信设施中，传输费用都是一项主要的花费。正因为如此，**在给定的资源上运载最大量的信息**，或者换一种做法，**用最小的传输容量来满足给定信息的通信要求**，就显得非常重要。达到上述目标有两种做法：**复用和压缩**. 这两种技术可以单独使用也可以结合起来使用。第 8 章将考察三种最常用的复用技术：频分、同步时分复用和统计时分复用，以及一些重要的压缩技术。

- 复用 multiplexing
- 压缩 compression

## 1.4 Transmission Networks
### 1.4.1 Topology
The IEEE defines topology as “the interconnection pattern of nodes on a network.”

- **mesh network**:<br>![assets/Pasted image 20240602112807.png|225](/img/user/%E7%94%B5%E4%BF%A1%E4%BC%A0%E8%BE%93%E7%90%86%E8%AE%BA%E4%B8%8E%E5%B7%A5%E7%A8%8B/assets/Pasted%20image%2020240602112807.png)
	- If every switch in a network is connected to all other switches (or nodes) in the network, we call this “pattern” a full-mesh network.
	- <u>very survivable</u> because of a plethora of possible alternative routes
- **star network**: <br>![assets/Pasted image 20240602113908.png|125](/img/user/%E7%94%B5%E4%BF%A1%E4%BC%A0%E8%BE%93%E7%90%86%E8%AE%BA%E4%B8%8E%E5%B7%A5%E7%A8%8B/assets/Pasted%20image%2020240602113908.png)
	- the <u>least survivable</u> but most *economic* nodal patterns both to install and to administer
	- **multiple star network**: <br>![assets/Pasted image 20240602113852.png|450](/img/user/%E7%94%B5%E4%BF%A1%E4%BC%A0%E8%BE%93%E7%90%86%E8%AE%BA%E4%B8%8E%E5%B7%A5%E7%A8%8B/assets/Pasted%20image%2020240602113852.png)
		- free to modify by adding direct routes
	- **hierarchical network**: 
		- a natural outgrowth of the multiple star network

"**3R**": ==TBC==

## 1.5 QoS (Quality of service)

Quality of service means *how happy* the telephone company (or other common carrier) is keeping the customer.
QoS 的关键指标有：可用性、吞吐量、时延、丢包率等

## 1.8 The decibel :BoBxsStar:

$$(\mathrm{dB}) = 10\log(\mathrm{the ~ power ~ ratio})$$
- ==dB 值的正负可以代表增益 (gain) 和衰减 (loss)==
- 两倍的增益对应的是 3dB
- 增益可以使用直接加减运算
- 电压和电流的增益计算<br>
	电压增益：$$\mathrm{dB(\mathrm{voltage})} = 20\log \frac{E_2}{E_1}$$
	电流增益：$$\mathrm{dB(\mathrm{current})} = 20\log \frac{I_2}{I_1}$$
## 1.9 Basic derived decibel units
- **dBm**
  $$\mathrm{Power(dBm)}=10\log\left(\frac{P \mathrm{(~mW)}}{1 \mathrm{~mW} }\right)$$
- **dBW**
  $$\mathrm{Power(dBW)}=10\log\left(\frac{P \mathrm{(~W)}}{1 \mathrm{~W} }\right)$$
- Relationships:
  $$1 \mathrm{~mW}=0 \mathrm{~dBm}$$
  $$1 \mathrm{~W}=0 \mathrm{~dBW}$$
  $$+30 \mathrm{~dBm}=0 \mathrm{~dBW} = 1 \mathrm{~W}$$
  $$-30 \mathrm{~dBW}=0 \mathrm{~dBm} = 1 \mathrm{~mW}$$

## 1.9 The Neper
$$N_p=\frac{1}{2}\ln(\frac{P_1}{P_2})$$
$$dNp: \frac{1}{10}N_p$$
Relationships:
$$1 \mathrm{~Np} = 8.686 \mathrm{~dB}$$
$$1 \mathrm{~dB} = 0.1151 \mathrm{~Np}$$
## 1.10 The addition of power levels in dB
![assets/Pasted image 20240602135533.png|275](/img/user/%E7%94%B5%E4%BF%A1%E4%BC%A0%E8%BE%93%E7%90%86%E8%AE%BA%E4%B8%8E%E5%B7%A5%E7%A8%8B/assets/Pasted%20image%2020240602135533.png)
在上面的例子中，需要先**去对数化后相加**。
Solusion and example: 
```blindfold
![assets/Pasted image 20240602142242.png](/img/user/%E7%94%B5%E4%BF%A1%E4%BC%A0%E8%BE%93%E7%90%86%E8%AE%BA%E4%B8%8E%E5%B7%A5%E7%A8%8B/assets/Pasted%20image%2020240602142242.png)
```
