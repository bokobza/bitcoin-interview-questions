

# Bitcoin interview Questions

Here is a list of Bitcoin-specific questions for interviewers and interviewees. It can help you prepare for an interview, regardless of which side of the table you sit.

Some of the questions are pretty open-ended and only require the interviewee to show how much they know about a certain subject, even if they don't know all of its intricate details.



### No answers?

Nope. Not yet, anyway. 

However, the answers can be found in the list of resources provided at the end. It's the job of the interviewee to go and do their own research, learn about what they don't know, dig deeper and make up their own answer. This list only provides a starting point of things to go and explore.



### Contributing

You're welcome to contribute to this guide (please do), just keep a couple of things in mind.

- I've left all the trivia questions out of this guide.
  Questions like `how many bitcoin will there ever be?` or `who created bitcoin?` are of very little value.

- Please don't submit PRs reformatting the whole thing. 

  
## Table of contents

- [Questions](#questions)
    - [General](#general)
    - [Wallets](#wallets)
    - [Mining](#mining)
    - [Privacy and Security](#privacy-and-security)
    - [P2P](#p2p)
    - [Cryptography](#cryptography)
    - [Blocks](#blocks)
    - [Transactions and scripts](#transactions-and-scripts)
    - [Other](#other)
- [Exercises](#exercises)
    - [Exercise 1](#exercise-1)
    - [Exercise 2](#exercise-2)
    - [Exercise 3](#exercise-3)
- [Helpful learning resources](#helpful-learning-resources)
- [Credits for some of the questions and exercises:](#credits-for-some-of-the-questions-and-exercises)
- [License](#license)




## Questions



### General

- What is a soft fork vs a hard fork?
- What is the difference between a full node client and an SPV client?
- What consensus rules do you know?
- What are your favorite bitcoin improvement proposals (BIPs)?
- What is Segregated Witness, how does it work and what problems does it solve?
- In a nutshell, how does lightning network work?



### Wallets

- What does the HD in HD wallet mean? How does it work?
- What's the difference between mnemonics, passphrases and passwords in the context of HD wallets?



### Mining

- How does Proof-of-work work?
- Why is it almost impossible for miners to mine competing blocks having the same hash?
- What are the difficulty and the target? How are they calculated?
- How does a miner go about constructing a block?



### Privacy and Security

- Why do we advise users to only use addresses once?
- Do you know any mixing protocols? How do they work?
- What types of attacks on Bitcoin do you know?
- What is Byzantine Fault Tolerance?
- How does Bitcoin achieve Byzantine Fault Tolerance?



### P2P

- What P2P message types do you know? What do they do?
- How are peers discovered on the network?



### Cryptography

- What are blind signatures?
- what is a hash function vs cryptographic hash function?
- What is ECDSA used for in Bitcoin? How does it work?
- How do digital signatures work?
- What types of cryptography are used in Bitcoin?
- What is a cryptographic commitment?



### Blocks

- What does IBD mean?
- What is headers-first?



### Transactions and scripts

- What is the particularity of OP codes ending in *VERIFY?
- What are inputs and outputs in transactions?
- What is meant by a dust output?
- What is the purpose of the different signature hash types?
- What does the sequence in a transaction input mean?
- What is a transaction lock time?
- What is transaction malleability?
- What are Merkle trees, Merkle roots and why is it useful in Bitcoin?
- How is a P2PKH bitcoin address constructed?
- What's P2SH and how does it work?
- What are bech32 addresses? 
- In what cases can we have orphaned transactions?



### Other

- What are little endian and big endian?





## Exercises



### Exercise 1

How can this be spent?
```
IF
  <Bob PubKey> CHECKSIG
ELSE
  <Alice PubKey> CHECKSIG
ENDIF
```


### Exercise 2

How can this be spent?
```
IF
  <Bob PubKey> CHECKSIGVERIFY 
  HASH160 <Bob Hash> EQUAL
ELSE
  <Alice PubKey> CHECKSIG
ENDIF
```



### Exercise 3

What does this do?

```
IF
  IF
    2
  ELSE
    <30 days> CHECKSEQUENCEVERIFY DROP
    <A PubKey> CHECKSIGVERIFY
	1 
  ENDIF
  <B PubKey> <C PubKey> <D PubKey> 3 CHECKMULTISIG
ELSE
  <90 days> CHECKSEQUENCEVERIFY DROP
  <A PubKey> CHECKSIG
ENDIF
```



## Helpful learning resources

[Bitcoin source code](https://github.com/bitcoin)

[Bitcoin Developer Documentation](https://bitcoin.org/en/developer-documentation)

[Bitcoin Wiki](https://en.bitcoin.it/wiki)

[Bitcoin Stack Exchange](https://bitcoin.stackexchange.com)

[Mastering Bitcoin](https://github.com/bitcoinbook/bitcoinbook)

[Programming Bitcoin](https://github.com/jimmysong/programmingbitcoin)

[Learn me a Bitcoin](https://learnmeabitcoin.com/)

[SF Bitcoin Developers YouTube Channel](https://www.youtube.com/channel/UCREs0ConyCR2sEFf-DrLRMw)

[Bitcoin Peer-to-Peer Network Programming](https://www.youtube.com/playlist?list=PLQ56Yiu6lEayrOrjxefwkxKakZgMNIzL0)

[Blockchain tutorial videos](https://www.youtube.com/playlist?list=PLmL13yqb6OxdEgSoua2WuqHKBuIqvll0x)



## Credits for some of the questions and exercises:

@aprogiena
@aantonopoulos



## License

![CC0 1.0 Universal](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg "CC0 1.0 Universal (CC0 1.0)")