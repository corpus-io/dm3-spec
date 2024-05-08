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

### 2.3. Communication as a Public Good ???

#### 2.3.1. Open Source - Open Standards

#### 2.3.2. Inclusivity and Accessability

#### 2.3.3. Community

#### 2.3.4. Censorship resistance



## 3. The dm3 Protocol

The dm3 protocol provides a decentralized, end-to-end encrypted, messaging protocol, aiming to bridge interoperability gaps across platforms without compromising security, privacy, or user experience, thereby transforming the messaging ecosystem for a connected and self-sovereign communication future.

### 3.1. The Mission

Our mission sets the stage for a new era of communication in Web3 by breaking down the barriers set by centralized Web2 platforms and establishing new standards for user-centric, self-sovereign communication. The focus is not on replacing existing and established solutions or driving them out of the market, but on connecting them. At the same time, however, the dm3 protocol is intended to provide new solutions with a suitable basis for setting up modern communication in such a way that security, privacy, interoperability, and the user's self-sovereignty are at the very center of attention.

### 3.2. The Vision

We see a world where individuals communicate freely and securely, where privacy is upheld as a fundamental right, and where the power dynamics of centralized platforms are rebalanced in favor of users. Beginning with web3 messaging, dm3 protocol will establish a connected messaging ecosystem that enables the users self-sovereignly to manage their communication and messaging solutions and being interoperable with others without compromising their security, privacy, and UX.

### 3.3. The Core Protocol

#### 3.3.1. Message Relay Network

There are various approaches to implementing decentralized communication. It is important that an infrastructure is implemented that is not controlled by or dependent on one party (organization or company).
With dm3, the infrastructure is based on a decentralized **Message Relay Node Network**. These relay nodes (delivery service) are independent and have the task of temporarily storing messages (message cache) until they are picked up by the recipient. As soon as the messages have been retrieved and processed by the recipient, they are deleted.

Each recipient decides for themselves which relay nodes they want to be connected to and thus via which nodes they can be reached. They can operate their own message relay node, use the node of a specific service or use public independent nodes.
Since the relay nodes do not redistribute the messages in the network, this type of distributed network is easily scalable by adding further nodes.

The nodes can also perform other tasks, e.g. for extended privacy, or they can also act as a gateway to other protocols and services. In this case, the relay node would receive a message and then inject it into the other network or service. This makes them crucial building blocks for interoperability.

The message relay nodes are expressly not intended for the permanent storage of messages, but this is the task of the clients, which do this locally, in a cloud service, or even in a decentralized data store, depending on requirements and implementation.

#### 3.3.2. Communication Profile Registry

To enable secure encrypted and tamper-proof communication, various public keys and information about how messages can be delivered must be published. To enable a decentralized, permissionless and censorship-resistant architecture, the registry that publishes this information (communication profile) must be centrally accessible and yet decentralized. A central service provider cannot assume this function.
Web3 technology lends itself precisely to this, with a blockchain-based registry taking on this task.

Such a communication profile contains:

- **Encryption key:** public keys for end-to-end encryption
- **Signature key:** public keys for signatures
- **Delivery Information:** Information on which message relay nodes can be used to deliver the messages.

The dm3 protocol uses ENS (Ethereum Name Service) for this registry. Each ENS name (or sub-name) can hold a text record that contains the profile.

#### 3.3.3. Cross-chain, L2s, and Cloud-Services

Registries from other sources (be it other chains (cross-chain), L2s, Identity profiles, or even cloud services) can also be integrated via customized resolvers (via CCIP - Cross-Chain-Interoperability Protocol) and linked to a sub-name. In this way, the ENS-based registry can be used as a universal registry for communication profiles, regardless of where the actual information is ultimately published.

#### 3.3.4. Token-based Functions

A special capability of Web3 technology is that values can be digitally linked, locked, or transmitted. This is used by dm3 to effectively implement various functions, e.g. spam protection, extended privacy functions.

### 3.4. Interoperability

Most messengers currently in use are closed ecosystems. Communication between users of different platforms is not possible because the protocols and infrastructures are not compatible or, in the past, even interoperability was actively prevented by the service providers.
From the point of view of many users, interoperability is important and desirable. Interoperability can be divided into different levels:

- **Level 1:** New messages can be transferred from one system to another. The storage of messages remains the responsibility of the system
- **Level 2:** In addition to transferring new messages, it is also possible to synchronize saved conversations.
- **Level 3:** All resources can be shared (new messages, historical conversations, configurations, ...)

Level 1 is required for an interoperable ecosystem, level 2 is useful but not essential. To support the greatest possible diversity, level 3 is not helpful, as different architectures (centralized, decentralized, different network types, ...) and a focus on different use cases would lead to disproportionate and therefore impractical overheads.

In the core protocol, the dm3 protocol focuses exclusively on the transmission of messages (level 1). Replication of historical conversations (level 2) is provided as a protocol extension.

#### 3.4.1. Gateways to other networks and serivces

The dm3 message relay network enables the decentralized transmission of messages between individual users. In addition, the message relay nodes can also serve as a gateway to other networks and services.
A message gateway consists of one or more message relay nodes via which the recipient can be addressed in the dm3 network. However, instead of storing the received messages and keeping them ready for retrieval, the messages are transferred to the connected system.

Any existing messaging service or messaging network can be made dm3 interoperable by implementing the following:

1. publishing user dm3 profiles in ENS names or subnames. This is done by connecting the data source via a CCIP resolver.
2. implementing and operating a gateway consisting of a message relay node and a node or client of the connected system.
3. integration of the dm3 encoder and decoder into the client in order to read the embedded dm3 message or to wrap a sent message in a dm3 envelope.

Gateways can be operated decentrally and non-custodially. This means in particular that gateways can (and should) be designed in such a way that there are no middlemen who have access to the content at any time or who could censor the conversations. All keys are exclusively under the control of the user (or the client).

##### 3.4.1.1. Receive messages from dm3 network

Messages that are sent via a gateway are end-to-end encrypted by dm3 and are at the gateway embedded in a message from the connected system and re-encrypted if so required. To show the message, the receiving client uses a dm3 decoder to make the message readable for the user.
This means that messages sent via a gateway are securely encrypted end-to-end at all times and the security, encryption and privacy of the connected system are not restricted or reduced in any way.

???[image send from dm3 to service]

##### 3.4.1.2. Send messages into the dm3 network

Messages can also be sent to all other dm3-compatible recipients via the gateways. To do this, the message is first encrypted by a dm3 encoder for the recipient and then packaged as a data packet in a message that is addressed to the gateway. The gateway extracts the message, which is still dm3 encrypted, and sends it to the recipient using the dm3 message transport protocol.

???[image send from service to dm3]

#### 3.4.2. Messaging Bridges

While gateways are well suited and the best way to integrate networks and services into the dm3 ecosystem, it is necessary that the various customizations in the clients are necessary to establish dm3 interoperability. But what if a messenger, messaging service or network does not want to cooperate? Then there are messaging bridges!
The aim of messaging bridges is to enable messages to be sent to other systems without having to rely on their cooperation. Changes to their clients, their protocol or infrastructure are not necessary. All that is needed is an API that can be used to inject messages into the system (or to receive messages).
A messaging bridge is also a message relay node on the dm3 side, which can receive messages via the dm3 message transport protocol. In addition, the messaging bridge provides the necessary dm3 profiles for the recipients, which also means that the dm3 keys are kept in custody.

##### 3.4.2.1. Receive messages from dm3 network

To send a message from a dm3 interoperable client, the message is first encoded according to the rules of the receiving system (which usually includes appropriate encryption). Corresponding encoders (and decoders if necessary) are available in the dm3 library and API.
This message is then sent to the bridge as an attachment to a dm3 message. Since the bridge has control over the dm3 keys, it can read the (dm3) message. The actual message, which is encrypted in the attachment, is then forwarded to the connected system via its API.
Since the bridge only processes the message encrypted according to the rules of the receiving system, the content is still securely encrypted end-to-end. The only limitation is that a bridge could possibly censor messages so that they are not forwarded to certain recipients.

##### 3.4.2.2. Send messages into the dm3 network

To send messages from a service to the dm3 network, the Messaging Bridge creates a virtual user to whom the message is then sent. However, the message received by the messaging bridge is not decrypted by the bridge, but in turn embedded in a dm3 message and sent to the recipient. Received in a dm3 sub-operable client, it is then decoded accordingly.

### 3.5. Spam Protection

Spam is a major challenge in current communication systems. Depending on the survey, between 50% and well over 90% of all emails sent are classified as spam. But spam and the fight against it is also an important issue in the larger messenger services.
Centralized systems generally find it somewhat easier to take action against spam, as they can censor more easily via their central infrastructure than in decentralized infrastructures (such as email).
All widely used approaches to curbing spam are based on blocking messages suspected of being spam. With web3-based methods, however, it is possible to go further and make the sending of spam so unattractive for the sender that the motivation to send spam is no longer there.
The dm3 protocol uses a web3-based multi-level spam defense system, which in combination makes spam unprofitable for the sender while not significantly hindering the desired communications.

#### 3.5.1. Black- and Whitelists

**Blacklists** are a common method of filtering messages from proven malicious senders. In terms of web3-based communication, this means that addresses that have become conspicuous are included in such lists and can then be filtered out. 
This makes it possible to use public lists of known scammers and spammers for pre-filtering. As all messages in dm3 are signed by the sender, it is not possible for spammers to use the identity of others to send messages.
This method should be used in combination, as it cannot provide reliable protection against spam. However, blacklists in web3 are only effective to a limited extent, as a spammer can easily keep generating new addresses that are not yet on the blacklist. Blacklists are mainly used to evaluate public lists (e.g. on which sanctioned users are noted).

**Whitelists** are suitable for giving preferential treatment to addresses that the user trusts. This makes it easy to exclude addresses on such a list from the check of further criteria, which are described in the following paragraphs.

These methods can already be executed by the message relay node so that potential spam is not even accepted.

#### 3.5.2. Proof-of-Activity

The sender's address is regarded as **proof of activity** if it has a nonce greater than 1 (or a number > 1 specified by the recipient). This ensures that this address has already been active and transactions have been executed. This is usually not a problem for a "normal" wallet address of an active wallet.

However, if spammers try to send spam from newly generated addresses, they would first have to carry out transactions before they could use these addresses to send spam. This costs both money (transaction fees) and time (until the transaction is added to the blockchain). It also massively limits the number of possible new addresses. While a spammer could create an unlimited number of new addresses, the number of "used" addresses depends on the capacity of the blockchain, as at least one transaction would have to originate from each address.

This method is well suited to preventing spam attacks in which spammers constantly generate new addresses in order to circumvent block lists. This method can already be executed by the message relay node so that potential spam is not even accepted.

#### 3.5.3. Proof-of-Ownership

Another way to make sending spam unattractive is to require the sender to hold a certain number of tokens or an NFT from a certain collection on their wallet. This also prevents newly generated addresses from being used to send spam, as the spammer would then have to equip all these addresses with these tokens.

This is not a relevant challenge for regularly used wallets. To send a message to a recipient who requires this condition, the required tokens must be transferred to the wallet. However, the possession of exotic tokens or very high amounts should not be required, as this may represent an obstacle to use.

However, this also results in high costs and expenses for the potential spammer if he first has to equip each new address with tokens before it can be used for sending. This method can already be executed by the message relay node so that potential spam is not even accepted.

#### 3.5.4. Token Stake and Burn

While the methods already listed serve to limit mass spam in particular, a next level of spam protection is being introduced.

Each recipient defines how many dm3 tokens a sender has to deposit as security to guarantee that the message is not spam or scam.
For a sender to be able to submit a message to the recipient's message relay, it must have deposited at least the required amount. Only then will the message relay accept the message.
If the recipient declares the message as spam, part of the deposit is burned and the sender of the spam is penalized. In this way, the sender of spam can be penalized at any cost, so that sending spam is no longer profitable at all.
If the message is accepted, the deposit is not affected. This means that nothing happens in regular conversations and the sender does not have to fear any loss.
The message relay can also check whether the sender has deposited a sufficiently high deposit. The execution of the punishment for spam requires interaction with the receiving client.

### 3.6. Architecture

The dm3 protocol consists of different layers. It has a strictly modular structure so that the required parts of the protocol and therefore also the libraries and APIs can be tailored precisely to the use case.

It consists of 3 layers:

1. **Blockhain Layer:** Besides ENS (Ethereum Name Service), which is based on Ethereum, all interfaces APIs to other data sources (other chains, layer-2, cloud services, ...) are defined in this layer.
2. **Protocol layer:** In addition to the core protocol (message transport protocol), there are many optional extensions.
3. **Application Layer:** The APIs for integration into other protocols, services and apps and the existing UI components for direct integration into other applications form the Applications layer.

??? image module

### 3.7. Protocol Extensions

The following protocol extensions are only outlined to show the modular expandability of the dm3 protocol and its applications.

#### 3.7.1. Group chat

In the dm3 core protocol, the peer-to-peer messaging is defined. However, a group chat function is also required for many applications. Group messaging must fulfill the same security and privacy criteria as peer-to-peer messaging.

Two different types are implemented, one for small groups, based on the peer-to-peer protocol, and one for large groups, based on shared group chat keys.

#### 3.7.2. Billboard chat

The Billboard chat extension provides a public chat that dm3 users can join to participate in the public conversation. The chat history is public, every added statement is published.
Billboard chats can be used e.g. as a conference chat or to create public discussion groups.

#### 3.7.3. Public Messages

Public messages are public statements that a user publishes. They can be clearly associated with the user (tamper-proof), but are publicly readable.
These public messages can be integrated as posts in social media platforms or used as status information.

#### 3.7.4. Privacy Routing

Even if the content of dm3 messages is end-to-end encrypted and therefore private, and even if the decentralized message relay node network does not make general tracking of communications possible, monitoring individual nodes would possibly reveal transmission paths.
For communications with increased privacy requirements, it is possible to handle the communication between clients and message relay nodes via a privacy network. The dm3 message relay node network itself can also be used to keep the transmission information secret.
For this purpose, the message is not sent directly from the client to the receiving message relay node, but is first redirected via several (at least 3) nodes. As these nodes only know from whom they receive the packaged message and to whom they should forward it, the connection between the original sender and the recipient is broken after 3 independent forwardings.

Message relay nodes can offer this privacy service as an option. These services can be remunerated via a decoupled incentive system without restricting privacy.

#### 3.7.5. Linked Profiles

Messaging is used in a wide variety of applications. In addition to the main messenger, which represents a user's inbox and is their central communication platform, messaging components can be integrated into other applications (e.g. wallet to wallet or dapp to dapp messaging, support messenger, ...). Usually these embedded messaging functions are independent and often neither decentralized nor well secured.
With dm3 embedded components and linked profiles (limited scope profiles), local or application-related profiles can be created that are controlled with the same wallet or identity. If required, these can simply be linked to the user's main inbox so that they can track these communications there as.

This makes it possible both to create and maintain anonymous subprofiles for these applications and to link them to the main profile in order to manage important communications in one place.

#### 3.7.6. Token gated access

For various applications, it makes sense that only a limited user group is allowed to participate in a communication. Whereas in centralized applications, access restriction is implemented by the central user management. In a decentralized application, access control can be controlled via the possession of tokens or NFTs.
With this extension, it is also possible to build closed communities that are fully interoperable with other messengers.

#### 3.7.7. Embedded Services

A particular strength of web3 is its ability to digitize not only information but also values and make them transferable. With the embedded services extension, it is possible to integrate additional functions into the conversations. This can be the direct transfer of tokens in a message, but also any interaction with other dApps.

#### 3.7.8. Storage, Notification, Search,...

In order to implement a messenger service, in addition to the transmission of messages (core protocol) and protocol extensions for extended messaging functionalities, functions such as the effective storage of communications, the forwarding of notifications for incoming messages, search functions, etc. must also be realized. Even if this is primarily the task of the clients, the dm3 protocol provides corresponding specifications, libraries and APIs.

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
