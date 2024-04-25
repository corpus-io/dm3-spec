# dm3 - encrypted and decentralized web3 messaging

## 1. General

### 1.1. Motivation

Digital communication has become an integral part of our lives. In addition to e-mail, chat, and instant messaging applications are among the most widely used applications on the Internet. While e-mail has a decentralized architecture but is still largely used unencrypted today, messenger services have become established that often allow end-to-end encrypted communication but are usually operated as centralized services by well-known and powerful tech companies. The services are operated as closed systems; there is no interoperability beyond their borders or, even under current regulation, they are not very suitable for giving users real freedom in their choice of application without having to accept restrictions on communication.
Even if the content of end-to-end encrypted communication appears trustworthy (which cannot be definitively guaranteed in closed systems, as backdoors cannot be ruled out), the connection metadata in a centralized system is not secure. In addition, censorship cannot be ruled out or even prevented in such a service.
Another problem with current communication services is spam. Depending on the system, this is a profound problem (e.g. in email communication, it can be assumed that at least 50-80% of the messages sent are spam). Filters and extensive, constantly updated blacklists are used in an attempt to curb this problem, which on the one hand represents an enormous effort and, in many cases, only works inadequately.

In recent years, many interesting new messaging solutions have emerged that use web3 technology to realize new approaches with the aim of solving existing problems. While secure end-to-end encryption is state of the art, these web3 approaches also offer good solutions for decentralized and censorship-resistant communication and often also excellent privacy.
However, a problem of the web2 world threatens to repeat itself here too: most of these systems are closed ecosystems that cannot interoperate with each other. Although many of the decentralized protocols are technically excellent in terms of encryption and privacy for special applications, limited scalability makes it impossible for such protocols to serve as an interoperability layer.
The spam problem has also been insufficiently addressed in web3 messaging solutions to date but is essential for building the next generation messaging ecosystem.

### 1.2. Rethinking Digital Communication

In today's digital age, communication has evolved into an essential facet of modern life, enabling instant connections across the globe. However, the existing communication landscape presents several challenges that the dm3 protocol aims to address.

#### 1.2.1. The Limitations of Traditional Communication Methods

**Email's Decentralization and Unencrypted Communication**
Email, an early Internet innovation, initially offered decentralized communication. Yet, it struggled with issues such as a lack of adequate spam protection and widespread unencrypted transmission. While protocols emerged to address these concerns, mainstream adoption of encryption remained limited, leaving a significant portion of email communication vulnerable.
Besides the weak point of missing encryption (which even PGP could not solve due to lack of application), spam became more and more a significant problem. Today, spam accounts for the largest share of email traffic (60-90%, source: www.verbraucherzentrale.de). This has led to spam filters on the server side (at the service provider) as well as on the client side to filter out a large part of the spam or to prevent it from being transmitted in the first place.
Another consequence of this is that large email providers today only accept emails from a few other large providers, which means that it is now almost impossible to host an email service yourself, as the mails sent in this way are not accepted by the spam filters of the large providers.

**SMS and its Encryption Gap**
Short Message Service (SMS) revolutionized communication with its device-to-device text messages. However, SMS messages are transmitted without end-to-end encryption, posing security risks. This encryption gap raises concerns about data privacy in an interconnected world.

With the emergence and eventual triumph of instant messaging applications, which were much less restrictive in terms of how much data and which media could be transmitted in addition to text messages and, last but not least, were cheaper, the importance of SMS declined rapidly.
Their importance as a means of communication between people beyond the function as service messages has almost disappeared today. Therefore, the interest in introducing innovative improvements has also almost vanished.

**Web2 Messengers and Closed Silos**
In the late 1990s, instant messaging services emerged that made it possible to send direct messages from computer to computer. With the breakthrough of the iPhone and other smartphones at the end of the 2000s and messagers such as WhatsApp, WeChat, Facebook Messenger, Signal, Telegram, and many others, these largely replaced SMS, not least because it was possible to send short messages free of charge.

Even though today most messengers promise end-to-end encryption for message transmission, in some cases the encryption may be lifted, e.g. when messages are to be checked for offensive content based on a report of suspicion.
Although most messengers today have a very similar feature set, cross-platform communication is not possible because each messenger maintains its own community and keeps data in its own silos. Interoperability is currently not possible, although this would be very desirable from the user's point of view.
Legislative initiatives such as the planned "Digital Markets Act" of the EU (see https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=celex%3A32022R2065) as well as various national drafts aim to make interactions between users of the different platforms possible in the future. The challenge, however, is that the various solutions have each developed their own protocols (with a different focus on security and privacy, for example) and store user data in their individual data centers. The opening up of the gatekeepers' systems that the regulators are striving for will not really solve the interoperability problem; there is even a serious risk that it will exacerbate the pressure for monopolization.

What these solutions also have in common is that they are centralized services. Communication always takes place over the servers of the respective service, just as the data (e.g., chat histories, but also metadata such as connection data) is managed by the service providers. In some cases, users have to make far-reaching concessions regarding their sovereignty (e.g., sharing of contact information, ...).

Often a certain messenger has become established as a quasi-standard in a certain region or user group (e.g. WhatsApp in Europe, WeChat in China, Facebook Messenger in U.S., ...). This then leads to the fact that one must also be registered with this service in order to communicate with friends and acquaintances, since they often use the most common messenger and rarely select the messenger based on its technical performance but rather on the network effect in their circle of acquaintances.

```[PIC DATA-SILOS]```

User administration is carried out as usual with username and password (sometimes including 2FA), whereby the telephone number is often used as user identification. However, this also means that the user profiles are under the control of the service providers. This means that censorship cannot be completely ruled out, connection data can be tricked even if the content is encrypted, and users are dependent on the service provider.

Even if it is not as severe as with email communication, spam is also an issue here. It is partly contained by the fact that the operators of the platforms also have user management under their control and respond to spam attacks by blocking or sanctioning these users. The more open these networks are (e.g., through interoperability), the more serious the spam problem becomes. If users are no longer exclusively controlled by one company or organization, the only protection against spam is usually to use suitable filters and blacklists to identify and intercept supposed spam.

#### 1.2.2. What is needed?

In order to build a secure messaging ecosystem that is secure, protects the privacy of communications, and is also interoperable, it is necessary to focuss on the following basic features:

**Secure End-to-End Encryption**
Secure end-to-end encryption is state-of-the-art and must be the foundation of all communication protocols, platforms and services.

**Decentralization**
Centralized systems have the general problem that censorship cannot be prevented and/or that there are single points of failure whose failure or malfunction can lead to the failure of the entire system. With a decentralized architecture that is not controlled by a single entity (be it a company, organization or government), censorship-resistant, fail-safe systems can be built. Consequently, this is also important for the messaging ecosystem of the future.

**Privacy**
Privacy is not just a nice-to-have, but a fundamental right. Even if there are different requirements for the degree of privacy in our communication (an in-app chat function in a game may have fewer requirements than, for example, the communication of a whistleblower to an investigative journalist). Modern communication systems must meet the requirement of enabling private communication without adding ideological complexity. Sound messengers and messaging protocols must meet this requirement.

**Interoperability**
For the end user, it does not matter which service or system their communication partner uses as long as the messages can be exchanged. Just as interoperability and compatibility are completely normal in many areas of application, interoperability must also be the standard for messaging. Diversity is good. Solutions that are tailored to specific ecosystems or applications often offer better UX, but can only be used by a larger user group if they can interoperate with others.
Although interoperability can be achieved by all using the same core protocol and possibly also the same infrastructure, this is not expedient in the current situation, as different systems with different core systems are active and widly accepted. What is needed is an interoperability protocol that can serve as a core protocol (layer 1) for new solutions, but which can also be used to connect existing protocols and services (layer 0) without compromising the security, privacy, and UX of existing solutions. Such a protocol must be lean and fundamentally scalable.

**Spam-Protection**
The omnipresent problem of spam must be solved sensibly, as otherwise interoperability in particular will lead to more strain.
It is essential that better methods than the existing filters and blacklists are used. Web3 in particular provides us with suitable tools to solve the spam problem once and for all.

#### 1.2.3. What is essential?

It is particularly important to focus on the really essential functions when setting up a protocol that is intended to establish interoperability between various existing and new protocols, services and applications. These are

1. a scalable, decentralized, scalable and permissionless network for the transmission of messages.
2. a decentralized, permissionless registry for the communication profiles (public keys for encryption and signatures and information on how and where messages can be delivered)
3. a lean and modular protocol that supports the above features and can be used both as a layer 1 and as a layer 1 protocol and that does not introduce any restrictions compared to existing systems.

### 1.3. Introducing the dm3 Protocol

???

## 2. Market ???

### 2.1. Market size (potential users)

In the ever-evolving realm of communication, messaging has emerged as a cornerstone of digital interactions. With the proliferation of modern messaging platforms, the number of active users has surged, illustrating the integral role these tools play in our interconnected world.

**2.1.1 The Current Landscape**
As we peer into the present, it's evident that messaging platforms have etched themselves into the lives of over a quarter of the global population. Around 26% of individuals ([source](https://www.similarweb.com/blog/research/market-research/worldwide-messaging-apps/)) are engaged with one or more messaging platforms, ranging from household names like WhatsApp, Facebook Messenger, Telegram, Viber, Line, to Snapchat. Leading this pack is WhatsApp, boasting 2.7 billion monthly active users ([source](https://www.bankmycell.com/blog/number-of-whatsapp-users/)), closely followed by Facebook Messenger with 931 million ([source](https://www.bankmycell.com/blog/number-of-facebook-messenger-users/)), and Telegram with 700 million monthly active users ([source](https://www.bankmycell.com/blog/number-of-telegram-users/)).

**2.1.2.Transitioning to Protected and Confidential Communication**
In a world where the metaverse increasingly hosts our interactions, this user base is poised to grow even further. This shift isn't just about expanding numbers; it's about users seeking alternatives that offer the promise of genuine privacy and security. They yearn for communication where they retain true ownership of their conversations, away from the prying eyes of centralized entities.

While the messaging landscape is currently dominated by centralized giants, the emergence of web3 players is signaling a new wave of possibilities. These players, rooted in blockchain technology, are pioneering the path to decentralized, secure, and private communication.

**2.1.3. The Potential of Blockchain**
When delving into potential users who are already adopting chat and email services built upon blockchain technology, we uncover intriguing insights. More than 80 million crypto wallet users had been created by 2022 ([source](https://www.statista.com/statistics/647374/worldwide-blockchain-wallet-users/)), underscoring the growing interest in blockchain-based solutions. Within this cohort, a noteworthy 449,918 wallets were actively engaged on the Ethereum blockchain as of June 2023 ([source](https://www.demandsage.com/blockchain-statistics/)), highlighting the Ethereum network's prominence.

As a protocol deeply integrated with the Ethereum Name Service (ENS), dm3 protocol's reach aligns with the Ethereum ecosystem. ENS, reporting over 50 thousand monthly active users in September 2022 ([source](https://messari.io/report/state-of-ens-q3-2022)), solidifies the Ethereum blockchain as a stronghold for potential dm3 users.

### 2.2. Advantages of the dm3 Protocol in the Web3 Messaging Landscape 

In the rapidly evolving messaging landscape, the dm3 protocol distinguishes itself by introducing several key advantages that change the way we communicate in the web3 era. These advantages usher in a new era of privacy, security, and interoperability:

- **Interoperable Standard with Privacy Focus**
At the heart of the dm3 protocol lies a mission to connect disparate messaging systems through a standardized, interoperable protocol. It emphasizes self-sovereign communication while preserving privacy and security. This focus on interoperability ensures that dm3 can seamlessly integrate with various messaging platforms, creating a unified messaging experience that spans across services.

- **Chain-Agnostic Approach**
dm3 takes a chain-agnostic approach. This flexibility allows the protocol to adapt and function across different blockchain networks, ensuring widespread adoption without constraints.

- **Comprehensive Scalability and Performance**
dm3 can handle a large number of users and messages without compromising on responsiveness. This scalability is vital as it accommodates the rapid growth of the web3 community while maintaining a seamless user experience.

- **Modular Design and Extensions**
The dm3 protocol embraces a modular design, allowing for the incorporation of various extensions and optional features. This adaptability tailors its functionalities to diverse messaging needs, from private peer-to-peer conversations to group communication.

### 2.3. Communication as a Public Good

2.3.1. Censorship resistant
2.3.2. Open Source - Open Standards
2.3.3. Inclusivity and Accessability
2.3.4. Community

## 3. The dm3 Protocol

The dm3 protocol provides a decentralized, end-to-end encrypted messaging protocol for Web3, aiming to bridge interoperability gaps across platforms without compromising security, privacy, or user experience, thereby transforming the messaging ecosystem for a connected and self-sovereign communication future

### 3.1. The Mission

Our mission sets the stage for a new era of communication in Web3 by breaking down the barriers set by centralized Web2 platforms and establishing new standards for user-centric, self-sovereign communication.

### 3.2. The Vision

We see a world where individuals communicate freely and securely, where privacy is upheld as a fundamental right, and where the power dynamics of centralized platforms are rebalanced in favor of users.

### 3.3. The Core Protocol

#### 3.3.1. Message Relay Network

#### 3.3.2. Communication Profile Registry

#### 3.3.3. Address- and Token-based Function

#### 3.3.4. Cross-chain



### 3.4. Interoperability

#### 3.4.1. Gateways to other networks

#### 3.4.2. Messaging Bridges



### 3.5. Spam Protection

#### 3.5.1. Black- and Whitelists

#### 3.5.2. Proof-of-Activity

#### 3.5.3. Proof-of-Ownership

#### 3.5.4. Token Stake and Burn



### 3.6. Architecture

#### 3.6.1. Blockchain layer

#### 3.6.2. Protocol layer

#### 3.6.3. Application layer



### 3.7. Protocol Extensions

#### 3.7.1. Group chat

#### 3.7.2. Billboard chat

#### 3.7.3. Public Messages

#### 3.7.4. Privacy Routing

#### 3.7.5. Linked Profiles

#### 3.7.6. Cross-Chain

#### 3.7.7. Token gated access

#### 3.7.8. Embedded Services

#### 3.7.9. Storage, Notification,...


### 3.8. Messenger UI

#### 3.8.1. Embedded Widgets

#### 3.8.2. Messenger



## 4. DM3 Token and Tokenomics

### 4.1 Token Standard

### 4.2. Token Utility

#### 4.2.1. Network Application (Utilities)

##### 4.2.1.1. Spam Protection

##### 4.2.1.2. Privacy

#### 4.2.2. Governance

#### 4.2.3. Standard Incentive

### 4.5. Token Distribution



## 5. Roadmap

## 6. References
