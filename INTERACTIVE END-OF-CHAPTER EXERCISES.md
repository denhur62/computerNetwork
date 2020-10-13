# INTERACTIVE END-OF-CHAPTER EXERCISES 1

### CIRCUIT SWITCHING

>Consider the circuit-switched network shown in the figure below, with circuit switches A, B, C, and D. Suppose there are 19 circuits between A and B, 13 circuits between B and C, 12 circuits between C and D, and 16 circuits between D and A.
>
>![image-20200917181015350](C:\Users\denhu\AppData\Roaming\Typora\typora-user-images\image-20200917181015350.png)
>
>Question List
>
>>1. What is the maximum number of connections that can be ongoing in the network at any one time?
>>
>>2. Suppose that these maximum number of connections are all ongoing. What happens when another call connection request arrives to the network, will it be accepted? Answer Yes or No
>>
>>3. Suppose that every connection requires 2 consecutive hops, and calls are connected clockwise. For example, a connection can go from A to C, from B to D, from C to A, and from D to B. With these constraints, what is the is the maximum number of connections that can be ongoing in the network at any one time?
>>
>>4. Suppose that 18 connections are needed from A to C, and 17 connections are needed from B to D. Can we route these calls through the four links to accommodate all 35 connections? Answer Yes or No
>>
>>1. 한 번에 네트워크에서 진행 가능한 최대 연결 수는 얼마인가?
>>
>>2. 이러한 최대 연결 수가 모두 진행 중이라고 가정합시다. 다른 통화 연결 요청이 네트워크에 도착하면 어떻게 되는가, 수락될 것인가? 예 또는 아니오로 대답
>>
>>3. 매 연결마다 2회 연속 홉이 필요하고, 통화는 시계방향으로 연결된다고 가정한다. 예를 들어, 연결은 A에서 C로, B에서 D로, C에서 A로, D에서 B로 갈 수 있다. 이러한 제약조건으로, 네트워크에서 한 번에 계속 진행 가능한 최대 연결 수는 얼마인가?
>>
>>4. A에서 C까지 18개의 연결이 필요하고, B에서 D까지 17개의 연결이 필요하다고 가정한다. 이 통화들을 4개의 링크를 통해 35개의 연결을 모두 수용할 수 있도록 할 수 있을까? 예 또는 아니오로 대답
>
>Solution
>
>>1. The maximum number of connections that can be ongoing at any one time is the sum of all circuits, which happens when 19 connections go from A to B, 13 connections go from B to C, 12 connections go from C to D, and 16 connections go from D to A. This sum is 60.
>>
>>2. No, it will be blocked because there are no free circuits.
>>
>>3. There can be a maximum of 28 connections. Consider routes A->C and C->A, sum the bottleneck links, and compare that value to the equivalent of B->D and D->B.
>>
>>4. Using our answer from question 4, the sum of our needed connections is 35, and we have 28 available connections, so it is NOT possible.
>>
>>1. 한 번에 진행 가능한 최대 연결 수는 모든 회로의 합으로, 19개의 연결부가 A에서 B로, 13개의 연결부가 B에서 C로, 12개의 연결부가 C에서 D로, 16개의 연결부가 D에서 A로 연결될 때 발생한다. 이 금액은 60이다. (60)
>>
>>2. 아니, 자유로운 회로가 없기 때문에 차단될 것이다. (No)
>>
>>3. 최대 28개의 연결이 있을 수 있다. 경로 A->C와 C->A를 고려하여 병목 링크를 합산한 후 그 값을 B->D와 D->B의 등가 값과 비교한다. (28)
>>
>>4. 질문 4.의 답변을 이용하여 필요한 연결의 합은 35이며, 28개의 연결 가능한 연결이 있으므로 불가능하다. (No)

### QUANTITATIVE COMPARISON OF PACKET SWITCHING AND CIRCUIT SWITCHING

>This question requires a little bit of background in probability (but we'll try to help you though it in the solutions). Consider the two scenarios below:
>
>- A circuit-switching scenario in which *Ncs* users, each requiring a bandwidth of 10 Mbps, must share a link of capacity 100 Mbps.
>- A packet-switching scenario with *Nps* users sharing a 100 Mbps link, where each user again requires 10 Mbps when transmitting, but only needs to transmit 30 percent of the time.
>
>![image-20200917184122317](C:\Users\denhu\AppData\Roaming\Typora\typora-user-images\image-20200917184122317.png)
>
>Question
>
>>1. When circuit switching is used, what is the maximum number of users that can be supported?
>>
>>2. Suppose packet switching is used. If there are 19 packet-switching users, can this many users be supported under circuit-switching? Yes or No.
>>
>>3. Suppose packet switching is used. What is the probability that a given (specific) user is transmitting, and the remaining users are not transmitting?
>>
>>4. Suppose packet switching is used. What is the probability that one user (*any* one among the 19 users) is transmitting, and the remaining users are not transmitting?
>>
>>5. When one user is transmitting, what fraction of the link capacity will be used by this user? Write your answer as a decimal.
>>
>>6. What is the probability that any 10 users (of the total 19 users) are transmitting and the remaining users are not transmitting?
>>
>>7. What is the probability that *more* than 10 users are transmitting?
>>
>>\1. 회로 전환을 사용할 때 지원할 수 있는 최대 사용자 수는 얼마인가?
>>
>>\2. 패킷 교환이 사용된다고 가정한다. 19명의 패킷 교환 사용자가 있는 경우, 이 많은 사용자가 회로 교환 하에서 지원될 수 있는가? 예스 또는 아니오.
>>
>>\3. 패킷 교환이 사용된다고 가정한다. 주어진 (특정) 사용자가 송신하고 있고, 나머지 사용자가 송신하지 않을 확률은 얼마인가?
>>
>>\4. 패킷 교환이 사용된다고 가정한다. 사용자 한 명(19명 중 한 명)이 송신하고, 나머지 사용자가 송신하지 않을 확률은 얼마인가.
>>
>>\5. 한 명의 사용자가 송신할 때, 이 사용자가 사용하는 링크 용량의 일부분은? 답안을 십진법으로 쓰시오.
>>
>>\6. (총 19명의 사용자 중) 10명의 사용자가 송신하고 있으며, 나머지 사용자가 송신하지 않을 확률은 얼마인가?
>>
>>\7. 10명 이상의 사용자가 송신하고 있을 확률은 얼마인가?
>
>Solution
>
>>\1. When circuit switching is used, at most 10 users can be supported. This is because each circuit-switched user must be allocated its 10 Mbps bandwidth, and there is 100 Mbps of link capacity that can be allocated.
>>
>>\2. No. Under circuit switching, the 19 users would each need to be allocated 10 Mbps, for an aggregate of 190 Mbps - more than the 100 Mbps of link capacity available.
>>
>>\3. The probability that a given (specific) user is busy transmitting, which we'll denote p, is just the fraction of time it is transmitting, i.e. 0.3. The probability that one specific other user is not busy is (1-p), and so the probability that all of the other Nps-1 users are not transmitting is (1-p)Nps-1. Thus the probability that one specific user is transmitting and the remaining users are not transmitting is p*(1-p)Nps-1, which has the numerical value of 0.00049.
>>
>>\4. The probability that exactly one (any one) of the Nps users is transmitting is Nps times the probability that a given specific user is transmitting and the remaining users are not transmitting. The answer is thus Nps * p * (1-p)Nps-1, which has the numerical value of 0.0093.
>>
>>\5. This user will be transmitting at a rate of 10 Mbps over the 100 Mbps link, using a fraction 0.1 of the link's capacity when busy.
>>
>>\6. The probability that 10 specific users of the total 19 users are transmitting and the other 9 users are idle is p10(1-p)9. Thus the probability that any 4 of the 7 users are busy is choose(19, 10) * p10(1-p)9, where choose(19, 10) is the (19, 10) coefficient of the binomial distribution). The numerical value of this probability is 0.022.
>>
>>\7. The probability that more than 10 users of the total 19 users are transmitting is Σ i=11,19 choose(19, i) * pi(1-p)19 - i. The numerical value of this probability is 0.011. Note that 10 is the maximum number of users that can be supported using circuit switching. With packet switching, nearly twice as many users (19) are supported with a small probability that more than 10 of these packet-switching users are busy at the same time.
>>
>>\1. 회선 전환을 사용할 경우 최대 10명의 사용자를 지원할 수 있다. 회선 교환 사용자마다 10Mbps 대역폭을 할당해야 하고, 할당할 수 있는 링크 용량이 100Mbps에 달하기 때문이다.
>>
>>\2. 아니오. 회선 전환에서 19명의 사용자는 각각 사용 가능한 링크 용량의 100Mbps 이상인 190Mbps의 총계값으로 10Mbps를 할당받아야 한다.
>>
>>\3. 주어진 (특정) 사용자가 전송을 하고 있을 확률은, 우리가 p를 나타내게 될 것은, 그것이 전송하고 있는 시간의 일부, 즉 0.3에 지나지 않는다. 특정 다른 사용자 한 명이 바쁘지 않을 확률은 (1-p)이므로 다른 모든 Nps-1 사용자가 전송하지 않을 확률은 (1-p)Nps-1이다. 따라서 특정 사용자 한 명이 송신하고 나머지 사용자가 송신하지 않을 확률은 0.00049의 숫자 값을 갖는 p*(1-p)Nps-1이다.
>>
>>\4. Nps 사용자 중 정확히 1명(누구나)이 송신하고 있는 확률은 특정 사용자가 송신하고 나머지 사용자가 송신하지 않는 확률을 Nps로 곱한 것이다. 따라서 Nps * p * (1-p)Nps-1로, 숫자 값은 0.0093이다.
>>
>>\5. 이 사용자는 통화 중일 때 링크 용량의 0.1분의 1을 사용하여 100Mbps 링크에서 10Mbps의 속도로 전송한다.
>>
>>\6. 전체 19명의 사용자 중 10명의 특정 사용자가 송신하고 나머지 9명의 사용자가 유휴 상태일 확률은 p10(1-p)9이다. 따라서 7명의 사용자 중 4명이 사용 중일 확률은 선택(19, 10) * p10(1-p)9이며, 여기서 선택(19, 10)은 이항 분포의 (19, 10) 계수다. 이 확률의 수치는 0.022이다.
>>
>>\7. 총 19명의 사용자 중 10명 이상이 송신하고 있을 확률은 is i=11,19 select (19, i) * pi(1-p)19 - i이다. 이 확률의 수치는 0.011이다. 10은 회로 전환을 사용하여 지원할 수 있는 최대 사용자 수라는 점에 유의하십시오. 패킷 교환을 통해, 이러한 패킷 교환 사용자들 중 10명 이상이 동시에 사용 중일 가능성이 거의 두 배(19명)에 달하는 사용자들이 지원된다.

### CAR - CARAVAN ANALOGY

>Consider the figure below, adapted from Figure 1.17 in the text, which draws the analogy between store-and-forward link transmission and propagation of bits in packet along a link, and cars in a caravan being serviced at a toll booth and then driving along a road to the next tollbooth.
>
>Suppose the caravan has 10 cars, and that the tollbooth services (that is, transmits) a car at a rate of one car per 5 seconds. Once receiving serving a car proceeds to the next tool both, which is 500 kilometers away at a rate of 10 kilometers per second. Also assume that whenever the first car of the caravan arrives at a tollbooth, it must wait at the entrance to the tollbooth until all of the other cars in its caravan have arrived, and lined up behind it before being serviced at the toll booth. (That is, the entire caravan must be stored at the tollbooth before the first car in the caravan can pay its toll and begin driving towards the next tollbooth).
>
>본문의 그림 1.17에서 개조한 아래 그림을 고려해 보십시오. 이 그림은 링크를 따라 패킷의 저장 및 전달 링크 전송과 캐러밴에 탄 자동차들이 요금소에서 서비스를 받은 후 다음 톨게이트로 가는 도로를 따라 주행하는 것과 유사하다.
>
>캐러밴에 10대의 차가 있고, 톨게이트가 5초당 1대의 속도로 자동차를 서비스(즉, 전송)한다고 가정하자. 서빙 차량을 받으면 초당 10km의 속도로 500km 떨어진 다음 공구로 이동한다. 또한 캐러밴의 첫 번째 차가 톨게이트에 도착할 때마다 캐러밴의 다른 차들이 모두 도착할 때까지 톨게이트 입구에서 대기하고 그 뒤에 줄을 서야 톨게이트에서 서비스를 받을 수 있다고 가정한다.(즉, 캐러밴의 첫 번째 차가 발을 딛기 전에 캐러밴 전체를 톨게이트에 보관해야 한다.통행료를 지불하고 다음 통행료 징수소를 향해 운전하기 시작한다.
>
>![image-20200917184351037](C:\Users\denhu\AppData\Roaming\Typora\typora-user-images\image-20200917184351037.png)
>
>Question
>
>>\1. Once a car enters service at the tollbooth, how long does it take until it leaves service?
>>
>>\2. How long does it take for the entire caravan to receive service at the tollbooth (that is the time from when the first car enters service until the last car leaves the tollbooth)?
>>
>>\3. Once the first car leaves the tollbooth, how long does it take until it arrives at the next tollbooth?
>>
>>\4. Once the last car leaves the tollbooth, how long does it take until it arrives at the next tollbooth?
>>
>>\5. Once the first car leaves the tollbooth, how long does it take until it enters service at the next tollbooth?
>>
>>\6. Are there ever two cars in service at the same time, one at the first toll booth and one at the second toll booth? Answer Yes or No
>>
>>\7. Are there ever zero cars in service at the same time, i.e., the caravan of cars has finished at the first toll both but not yet arrived at the second tollbooth? Answer Yes or No
>>
>>\1. 일단 톨게이트에서 운행이 시작되면, 운행이 끝날 때까지 얼마나 걸리나?
>>
>>\2. 전체 캐러밴이 톨게이트에서 서비스를 받는 데 걸리는 시간은 (첫 번째 차량이 서비스를 시작하는 시점부터 마지막 차가 톨게이트를 떠나는 시점까지) 어느 정도인가?
>>
>>\3. 첫차가 톨게이트를 떠나면 다음 톨게이트에 도착하기까지 얼마나 걸리나?
>>
>>\4. 마지막 차가 톨게이트를 떠나면 다음 톨게이트에 도착할 때까지 얼마나 걸리나?
>>
>>\5. 첫 번째 차가 톨게이트를 벗어나면 다음 톨게이트에서 운행되기까지 얼마나 걸리는가?
>>
>>\6. 1호 요금소와 2호 요금소에 각각 1대씩, 2호 요금소에 2대의 차량이 동시에 운행된 적이 있는가? 예 또는 아니오로 대답
>>
>>\7. 동시에 운행되는 차량이 제로인 적이 있는가? 즉, 카러밴이 첫 번째 통행료에서 모두 끝났지만 두 번째 통행료 징수소에 아직 도착하지 않은 적이 있는가? 예 또는 아니오로 대답
>
>Solution
>
>>\1. Service time is 5 seconds
>>
>>\2. It takes 50 seconds to service every car, (10 cars * 5 seconds per car)
>>
>>\3. It takes 50 seconds to travel to the next toll booth (500 km / 10 km/s)
>>
>>\4. Just like in the previous question, it takes 50 seconds, regardless of the car
>>
>>\5. It takes 95 seconds until the first car gets serviced at the next toll booth (10-1 cars * 5 seconds per car + 500 km / 10 km/s)
>>
>>\6. No, because cars can't get service at the next tollbooth until all cars have arrived
>>
>>\7. Yes, one notable example is when the last car in the caravan is serviced but is still travelling to the next toll booth; all other cars have to wait until it arrives, thus no cars are being serviced

### COMPUTING THE ONE-HOP TRANSMISSION DELAY

>Consider the figure below, in which a single router is transmitting packets, each of length *L* bits, over a single link with transmission rate *R* Mbps to another router at the other end of the link.
>
>![image-20200917184526250](C:\Users\denhu\AppData\Roaming\Typora\typora-user-images\image-20200917184526250.png)
>
>Suppose that the packet length is *L*= 16000 bits, and that the link transmission rate along the link to router on the right is *R* = 1 Mbps.
>
>Round your answer to two decimals after leading zeros
>
>아래 그림은 단일 라우터가 각 길이 *L* 비트의 패킷을 링크의 다른 쪽 끝에 있는 다른 라우터에 전송 속도 *R* Mbps의 단일 링크를 통해 전송하고 있는 것을 고려해 보십시오.
>패킷 길이가 *L*= 16000비트이고, 오른쪽의 라우터에 대한 링크를 따라 전송되는 링크 전송 속도가 *R* = 1Mbps라고 가정하자.
>
>0을 리딩한 후 답안을 2자리 숫자로 반올림하십시오.
>
>Question
>
>>\1. What is the transmission delay?
>>
>>\2. What is the maximum number of packets per second that can be transmitted by this link?
>>
>>\1. 변속기의 지연은?
>>
>>\2. 이 링크로 전송할 수 있는 초당 최대 패킷 수는 얼마인가?
>
>Solution
>
>>The transmission delay = L/R = 16000 bits / 1000000 bps = 0.016 seconds
>>
>>The number of packets that can be transmitted in a second into the link = R / L = 1000000 bps / 16000 bits = 62 packets
>>
>>전송 지연 = L/R = 16000비트/1000000bps = 0.016초
>>
>>1초 내에 링크로 전송할 수 있는 패킷 수 = R/L = 1000000bps / 16000비트 = 62개 패킷

### QUEUING DELAY

>Consider the queuing delay in a router buffer, where the packet experiences a delay as it waits to be transmitted onto the link. The length of the queuing delay of a specific packet will depend on the number of earlier-arriving packets that are queued and waiting for transmission onto the link. If the queue is empty and no other packet is currently being transmitted, then our packet’s queuing delay will be zero. On the other hand, if the traffic is heavy and many other packets are also waiting to be transmitted, the queuing delay will be long.
>
>![img](http://gaia.cs.umass.edu/kurose_ross/interactive/qdelay.png)
>
>Assume a constant transmission rate of R = 500000 bps, a constant packet-length L = 3200 bits, and a is the average rate of packets/second. Traffic intensity I = La/R, and the queuing delay is calculated as I(L/R)(1 - I) for I < 1.
>
>패킷이 링크로 전송되기를 기다리는 동안 패킷이 지연되는 라우터 버퍼의 대기 지연을 고려하십시오. 특정 패킷의 대기열 지연 길이는 링크에 대한 전송을 대기하고 대기 중인 이전 도착 패킷의 수에 따라 달라진다. 대기열이 비어 있고 현재 전송되고 있는 다른 패킷이 없다면, 우리의 패킷의 대기열 지연은 0이 될 것이다. 반면 트래픽이 많고 다른 많은 패킷들도 전송을 기다리고 있다면 대기열 지연은 길어질 수밖에 없다.
>
>일정한 전송 속도는 R = 500,000 bps, 일정한 패킷 길이 L = 3200 비트, 그리고 a는 패킷/초의 평균 전송 속도라고 가정한다. 트래픽 강도 I = La/R, 대기열 지연은 I < 1에 대해 I(L/R)(1 - I)로 계산된다.
>
>Question
>
>>\1. In practice, does the queuing delay tend to vary a lot? Answer with Yes or No
>>
>>\2. Assuming that a = 28, what is the queuing delay? Give your answer in milliseconds (ms)
>>
>>\3. Assuming that a = 88, what is the queuing delay? Give your answer in milliseconds (ms)
>>
>>\4. Assuming the router's buffer is infinite, the queuing delay is 1.5744 ms, and 1837 packets arrive. How many packets will be in the buffer 1 second later?
>>
>>\5. If the buffer has a maximum size of 968 packets, how many of the 1837 packets would be dropped upon arrival from the previous question?
>>
>>\1. 실제로 대기열 지연은 많이 달라지는 경향이 있는가? 예 또는 아니오로 대답
>>
>>\2. a = 28이라고 가정할 때 대기열 지연은? 밀리초(ms) 단위로 답변 제공
>>
>>\3. a = 88이라고 가정할 때, 대기열 지연은 무엇인가? 밀리초(ms) 단위로 답변 제공
>>
>>\4. 라우터의 버퍼가 무한하다고 가정하면, 대기 지연은 1.5744ms이며, 1837개의 패킷이 도착한다. 1초 후에 버퍼에 몇 개의 패킷이 있는지요?
>>
>>\5. 버퍼의 최대 크기가 968 패킷인 경우, 이전 질문에서 오는 즉시 삭제되는 패킷은 1837개 중 몇 개인가?
>
>Solution
>
>>\1. Yes, in practice, queuing delay can vary significantly. We use the above formulas as a way to give a rough estimate, but in a real-life scenario it is much more complicated.
>>
>>\2. Queuing Delay = I(L/R)(1 - I) * 1000 = 0.1792*(3200/500000)*(1-0.1792) * 1000 = 0.9414 ms.
>>
>>\3. Queuing Delay = I(L/R)(1 - I) * 1000 = 0.5632*(3200/500000)*(1-0.5632) * 1000 = 1.5744 ms.
>>
>>\4. Packets left in buffer = a - floor(1000/delay) = 1837 - floor(1000/1.5744) = 1202 packets.
>>
>>\5. Packets dropped = packets - buffer size = 1837 - 968 = 869 dropped packets.
>>
>>\1. 예, 실제로 대기열 지연은 상당히 다를 수 있다. 우리는 대략적인 견적을 내기 위한 방법으로 위의 공식들을 사용하지만, 실제 상황에서는 훨씬 더 복잡하다.
>>
>>\2. 큐 지연 = I(L/R)(1 - I) * 1000 = 0.1792*(3200/500000)*(1-0.1792) * 1000 = 0.9414ms
>>
>>\3. 큐 지연 = I(L/R)(1 - I) * 1000 = 0.5632*(3200/500000)*(1-0.56322) * 1000 = 1.5744ms
>>
>>\4. 버퍼에 남아 있는 패킷 = a - floor(1000/delay) = 1837 - floor(1000/1.5744) = 1202 패킷.
>>
>>\5. 손실된 패킷 = 패킷 - 버퍼 크기 = 1837 - 968 = 869 패킷.

### COMPUTING END-END DELAY (TRANSMISSION AND PROPAGATION DELAY)

>Consider the figure below, with three links, each with the specified transmission rate and link length.
>
>
>
>![img](data:image/png;base64,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0aJFj27cuHHG66+/fne/fv0KDx8+HPXkk09+AwAjR45cfYnXhAkTJmxauHDhI4MHD869lGMw3LR1HD5bLn25//77P4ZPFlzPcuDAgZht27YlA6CffPLJ7ZQqOVgA0D//+c+LfI8BgHbt2jWHUiUnBgA6Y8YMbyboESNG7ARA33333fuaa8OgQYMON9eGwYMHH2zr+9Nel2XLlk1au3btwLZux+9dnnzyydeb++03bdrU25Mx94033nicUiXLOAA6e/bsz3yPERAQIEVGRtZ5/keTTNCTJ09eDYC+9NJLTzU9/7p161I95/TNtAuA9u7d+3Rb35/LvaSkpJwdPXr09qNHj4a1dVuuluXOO+/80vf58HweP348YP369akA6PLlyydQSrF79+44APS55577m+8xANA+ffocp5Ti+PHjAQDo/fff780D5JGBH3300QW5p95///17musj8+bNe7ut7w1bKIj7B2ZcheTm5gqHDh0aQQiBLMscIUR2OBz6WbNmrQGUOjdjxoz53hMpsmzZskmpqak/+44aV69ePcRoNFZ7Ige+/PLLmxMTE9N9Ter/+te/7u3du/eeIUOGZDdtw08//dQzLy8vyWg01hqNRovdbtdXV1eHdOzYMXvMmDHpV/4uMNqSFStWjOE4TpYkSSCEyFar1XDfffetApRaYEOGDNmQlJRkBYDly5dP6Nq165HevXubPfuvX78+led5efz48UcA4JtvvhkTHh5+btiwYZmebT788MO7EhISTowePfqC52nlypXD1Gq102q1GkRRFDiOk61WqyEmJibX42B6rZCfn89dS1FfrUFWVpY+LS1tMNBo2RFFUbj77rvXA4qMfOCBB771bL906dIpgwcP3uR5ZgHgu+++GxUSElLs8bFatmzZpG7duh3q27ev1yfuvffeu69fv34/N+eDk5GRYfjpp5+m5uXlpXTo0CFnxIgRa3r16mVuuh2j9WEKEIPBYDAYjOuOa8IPgcFgMBgMBuO3wBQgBoPBYDAY1x1MAWIwGAwGg3HdwRQgBoPBYDAY1x1MAWIwGAwGg3HdwRQgBoPBYDAY1x1MAWIwGAwGg3HdwRQgBoPBYDAY1x1MAWIwGAwGw4dFrx6e/+bLB59q63YwrixMAWIAAL76Mvfmtm4Dg8FgtAdWrj016/v1J+9u63YwrixMAWJg377C2Lvu+Xxd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)
>
>
>
>
>
>Assume the length of a packet is 16000 bits. The speed of light propagation delay on each link is 3x10^8 m/sec
>
>Round your answer to two decimals after leading zeros
>
>각각 지정된 전송 속도 및 링크 길이를 가진 3개의 링크가 있는 아래 그림을 고려하십시오.
>패킷의 길이가 16000비트라고 가정하십시오. 각 링크의 광 전파 지연 속도는 3x10^8 m/초이다.
>
>0을 리딩한 후 답안을 2자리 숫자로 반올림하십시오.
>
>Question
>
>>\1. What is the transmission delay of link 1?
>>
>>\2. What is the propogation delay of link 1?
>>
>>\3. What is the total delay of link 1?
>>
>>\4. What is the transmission delay of link 2?
>>
>>\5. What is the propogation delay of link 2?
>>
>>\6. What is the total delay of link 2?
>>
>>\7. What is the transmission delay of link 3?
>>
>>\8. What is the propogation delay of link 3?
>>
>>\9. What is the total delay of link 3?
>>
>>\10. What is the total delay?
>>
>>\1. 링크 1의 전송 지연은?
>>
>>\2. 링크 1의 예보 지연은?
>>
>>\3. 링크 1의 총 지연 시간은?
>>
>>\4. 링크 2의 전송 지연은?
>>
>>\5. 링크 2의 예보 지연은?
>>
>>\6. 링크 2의 총 지연 시간은?
>>
>>\7. 링크 3의 전송 지연은?
>>
>>\8. 링크 3의 예보 지연은?
>>
>>\9. 링크 3의 총 지연 시간은?
>>
>>\10. 총 지연은 얼마인가?
>
>Solution
>
>>Link 1 transmission delay = L/R = 16000 bits / 100 Mbps = 0.00016 seconds
>>
>>Link 1 propagation delay = d/s = ()2 Km) * 1000 / 3*10^8 m/sec = 6.67E-6 seconds
>>
>>Link 1 total delay = d_t + d_p = 0.00016 seconds + 6.67E-6 seconds = 0.00017 seconds
>>
>>Link 2 transmission delay = L/R = 16000 bits / 100 Mbps = 0.00016 seconds
>>
>>Link 2 propagation delay = d/s = ()5000 Km) * 1000 / 3*10^8 m/sec = 0.017 seconds
>>
>>Link 2 total delay = d_t + d_p = 0.00016 seconds + 0.017 seconds = 0.017 seconds
>>
>>Link 3 transmission delay = L/R = 16000 bits / 100 Mbps = 0.00016 seconds
>>
>>Link 3 propagation delay = d/s = ()2 Km) * 1000 / 3*10^8 m/sec = 6.67E-6 seconds
>>
>>Link 3 total delay = d_t + d_p = 0.00016 seconds + 6.67E-6 seconds = 0.00017 seconds
>>
>>The total delay = d_L1 + d_L2 + d_L3 = 0.00017 seconds + 0.017 seconds + 0.00017 seconds = 0.017 seconds
>>
>>링크 1 전송 지연 = L/R = 16000비트/100Mbps = 0.00016초
>>
>>링크 1 전파 지연 = d/s = ()2Km) * 1000 / 3*10^8m/초 = 6.67E-6초
>>
>>링크 1 총 지연 = d_t + d_p = 0.00016초 + 6.67E-6초 = 0.00017초
>>
>>링크 2 전송 지연 = L/R = 16000비트/100Mbps = 0.00016초
>>
>>링크 2 전파 지연 = d/s = ()5000Km) * 1000 / 3*10^8m/초 = 0.017초
>>
>>링크 2 총 지연 = d_t + d_p = 0.00016초 + 0.017초 = 0.017초
>>
>>링크 3 전송 지연 = L/R = 16000비트 / 100Mbps = 0.00016초
>>
>>링크 3 전파 지연 = d/s = ()2Km) * 1000 / 3*10^8m/초 = 6.67E-6초
>>
>>링크 3 총 지연 = d_t + d_p = 0.00016초 + 6.67E-6초 = 0.00017초
>>
>>총 지연 = d_L1 + d_L2 + d_L3 = 0.00017초 + 0.017초 + 0.00017초 = 0.017초

### END TO END THROUGHPUT AND BOTTLENECK LINKS

>Consider the scenario shown below, with four different servers connected to four different clients over four three-hop paths. The four pairs share a common middle hop with a transmission capacity of R = 400 Mbps. The four links from the servers to the shared link have a transmission capacity of RS = 70 Mbps. Each of the four links from the shared middle link to a client has a transmission capacity of RC = 80 Mbps.
>
>![image-20200917185015988](INTERACTIVE END-OF-CHAPTER EXERCISES.assets/image-20200917185015988.png)
>
>\1. What is the maximum achievable end-end throughput (in Mbps) for each of four client-to-server pairs, assuming that the middle link is fairly shared (divides its transmission rate equally)?
>
>\2. Which link is the bottleneck link? Format as Rc, Rs, or R
>
>\3. Assuming that the servers are sending at the maximum rate possible, what are the link utilizations for the server links (RS)? Answer as a decimal
>
>\4. Assuming that the servers are sending at the maximum rate possible, what are the link utilizations for the client links (RC)? Answer as a decimal
>
>\5. Assuming that the servers are sending at the maximum rate possible, what is the link utilizations for the shared link (R)? Answer as a decimal
>
>\1. 중간 링크가 공평하게 공유된다고 가정할 때(전송 속도를 균등하게 나눈다) 네 개의 클라이언트-서버 쌍 각각에 대해 달성 가능한 최대 엔드엔드 처리량(Mbps)은 얼마인가?
>
>\2. 병목 링크는 어느 링크인가? Rc, Rs 또는 R 형식
>
>\3. 서버가 가능한 최대 속도로 전송한다고 가정할 때, 서버 링크(RS)에 대한 링크 활용도는? 십진수로 대답
>
>\4. 서버가 가능한 최대 속도로 전송한다고 가정할 때, 클라이언트 링크(RC)에 대한 링크 활용도는? 십진법으로 대답하다.
>
>\5. 서버가 가능한 최대 속도로 전송한다고 가정할 때, 공유 링크(R)의 링크 활용도는? 십진법으로 대답하다.
>
>Solution
>
>>\1. The maximum achievable end-end throughput is the capacity of the link with the minimum capacity, which is 70 Mbps
>>
>>\2. The bottleneck link is the link with the smallest capacity between RS, RC, and R/4. The bottleneck link is Rs.
>>
>>\3. The server's utilization = Rbottleneck / RS = 70 / 70 = 1
>>
>>\4. The client's utilization = Rbottleneck / RC = 70 / 80 = 0.88
>>
>>\5. The shared link's utilization = Rbottleneck / (R / 4) = 70 / (400 / 4) = 0.7
>>
>>\1. 달성 가능한 최대 엔드엔드 처리량은 최소 용량을 가진 링크의 용량으로, 70Mbps이다.
>>
>>\2. 병목 링크는 RS, RC, R/4 사이의 용량이 가장 작은 링크다. 병목 링크는 Rs이다.
>>
>>\3. 서버 활용도 = Rbottle / RS = 70 / 70 = 1
>>
>>\4. 의뢰인의 활용도 = Rottlek / RC = 70 / 80 = 0.88
>>
>>\5. 공유 링크의 이용률 = Rottlek / (R / 4) = 70 / (400 / 4) = 0.7

### THE IP STACK AND PROTOCOL LAYERING

>In the scenario below, imagine that you're sending an http request to another machine somewhere on the network.
>
>![img](http://gaia.cs.umass.edu/kurose_ross/interactive/layers.png)
>
>아래 시나리오에서 네트워크상의 다른 컴퓨터에 http 요청을 보내고 있다고 가정해 보십시오.
>
>Question
>
>>\1. What layer in the IP stack best corresponds to the phrase: 'handles the delivery of segments from the application layer, may be reliable or unreliable'
>>
>>\2. What layer in the IP stack best corresponds to the phrase: 'passes frames from one node to another across some medium'
>>
>>\3. What layer in the IP stack best corresponds to the phrase: 'bits live on the wire'
>>
>>\4. What layer in the IP stack best corresponds to the phrase: 'moves datagrams from the source host to the destination host'
>>
>>\5. What layer in the IP stack best corresponds to the phrase: 'handles messages from a variety of network applications'
>>
>>\6. What layer corresponds to box 1?
>>
>>\7. What layer corresponds to box 2?
>>
>>\8. What layer corresponds to box 3?
>>
>>\9. What layer corresponds to box 4?
>>
>>\10. What layer corresponds to box 5?
>>
>>\11. What layer corresponds to box 6?
>>
>>\12. What layer corresponds to box 7?
>>
>>\13. What layer corresponds to box 8?
>>
>>\14. What layer corresponds to box 9?
>>
>>\15. What layer corresponds to box 10?
>>
>>\16. What layer corresponds to box 11?
>>
>>\17. What layer corresponds to box 12?
>>
>>\18. What layer corresponds to box 13?
>>
>>\19. What layer corresponds to box 14?
>>
>>\20. What layer corresponds to box 15?
>>
>>\1. IP 스택의 어떤 계층이 '애플리케이션 계층으로부터 세그먼트의 전달을 처리하며, 신뢰할 수 없거나 신뢰할 수 없는 것일 수 있다'라는 구문에 가장 부합하는가?
>>
>>\2. IP 스택의 어떤 계층이 '어떤 매체를 통해 한 노드에서 다른 노드로 프레임을 전달한다'는 구문에 가장 부합한다.
>>
>>\3. IP 스택의 어떤 계층이 가장 잘 대응되는가: '비트는 와이어에 산다'
>>
>>\4. IP 스택의 어떤 계층이 '소스 호스트에서 대상 호스트로 데이터그램 이동'이라는 구문에 가장 부합하는가?
>>
>>\5. IP 스택의 어떤 계층이 '다양한 네트워크 애플리케이션에서 메시지를 처리하다'라는 구문에 가장 부합하는가?
>>
>>\6. 상자 1에 해당하는 레이어는?
>>
>>\7. 상자 2에 해당하는 층은?
>>
>>\8. 상자 3에 해당하는 층은?
>>
>>\9. 상자 4에 해당하는 층은?
>>
>>\10. 상자 5에 해당하는 층은?
>>
>>\11. 상자 6에 해당하는 층은?
>>
>>\12. 상자 7에 해당하는 층은?
>>
>>\13. 상자 8에 해당하는 층은?
>>
>>\14. 상자 9에 해당하는 층은?
>>
>>\15. 상자 10에 해당하는 층은?
>>
>>\16. 상자 11에 해당하는 층은?
>>
>>\17. 상자 12에 해당하는 층은?
>>
>>\18. 상자 13에 해당하는 층은?
>>
>>\19. 상자 14에 해당하는 층은?
>>
>>\20. 상자 15에 해당하는 층은?
>
>Solution
>
>>\1. The given phrase corresponds to the Transport Layer.
>>
>>\2. The given phrase corresponds to the Link Layer.
>>
>>\3. The given phrase corresponds to the Physical Layer.
>>
>>\4. The given phrase corresponds to the Network Layer.
>>
>>\5. The given phrase corresponds to the Application Layer.
>>
>>\6. Box 1 is the Application Layer.
>>
>>\7. Box 2 is the Transport Layer.
>>
>>\8. Box 3 is the Network Layer.
>>
>>\9. Box 4 is the Link Layer.
>>
>>\10. Box 5 is the Physical Layer.
>>
>>\11. Box 6 is the Physical Layer.
>>
>>\12. Box 7 is the Link Layer.
>>
>>\13. Box 8 is the Physical Layer.
>>
>>\14. Box 9 is the Link Layer.
>>
>>\15. Box 10 is the Network Layer.
>>
>>\16. Box 11 is the Physical Layer.
>>
>>\17. Box 12 is the Link Layer.
>>
>>\18. Box 13 is the Network Layer.
>>
>>\19. Box 14 is the Transport Layer.
>>
>>\20. Box 15 is the Application Layer.
>>
>>\1. 주어진 구절은 Transport Layer에 해당한다.
>>
>>\2. 주어진 구절은 링크 레이어에 해당된다.
>>
>>\3. 주어진 구절은 물리적 계층에 해당된다.
>>
>>\4. 주어진 구절은 네트워크 계층에 해당된다.
>>
>>\5. 주어진 구절은 애플리케이션 계층에 해당된다.
>>
>>\6. 상자 1은 애플리케이션 계층이다.
>>
>>\7. 상자 2는 전송 계층이다.
>>
>>\8. 상자 3은 네트워크 계층이다.
>>
>>\9. 상자 4는 링크 레이어다.
>>
>>\10. 상자 5는 물리적인 층이다.
>>
>>\11. 상자 6은 물리적인 층이다.
>>
>>\12. 상자 7은 링크 레이어다.
>>
>>\13. 상자 8은 물리적인 층이다.
>>
>>\14. 상자 9는 링크 레이어다.
>>
>>\15. 상자 10은 네트워크 계층이다.
>>
>>\16. 상자 11은 물리적인 층이다.
>>
>>\17. 상자 12는 링크 레이어다.
>>
>>\18. 상자 13은 네트워크 계층이다.
>>
>>\19. 상자 14는 트랜스포트 레이어다.
>>
>>\20. 박스 15는 애플리케이션 계층이다.



