# GraphiQL Plugins

Google Summer of Code Proposal to GraphQL. This propoosal contains a brief introduction of me as well. You can jump to the project [here](#project)

## Contents

1. [About Me](#about-me)
2. [Project for GSoC](#project)
3. [Test Project](#test-project)

## About Me

I am a senior Engineering student at Pakistan Institute of Engineering and Applied Sciences. I have a deep interest in programming since I was in middle school. I have completed several software engineering projects. I have experience of full stack web development, mobile app development and embedded system programming. 

### Personal Details
- **Legal Name** : Ali Nauroze
- **Email** : alinauroze@hotmail.com
- **Github** : [alinauroz](https://github.com/alinauroz)
- **Slack, Discord** : nauroz

### Tools


- **Programming Languages**: Javascript (NodeJS), Typescript
- **Libraries**: React, Redux
- **Cloud** : AWS, Heroku, Google Cloud


_I have experience of many other programming langauges such as C++, Java, PHP. But to be concise I am only mentioining things that are related to this project._

### Projects Completed

- **Odd Jobs**: An android app that connects workers with consumers in realtime. Frontend was in Java and backend was in NodeJS.
- **Messenger**: Built a messenger using NodeJS. PostreSQL and MongoDB were used to save data. 
- **2D Mapping using LIDAR** : A lidar and microcontroller programmed in C++ was used to detect distance and the data was sent to a PC using serialport. A Webpage then draws a 2D map of that space. I wrote mapping library myself. Frontend was in Vanilla Javascript.
- **Event Websites** : Developed event websites for university. More than 2000 users have registered using these websites.

### Opensource Projects
- Math Trade with Trade Maximizer, currently implemented using Couchbase. This ensures maximum possible trades between people. Both API and a simple frontend is available on [github](https://github.com/alinauroz/crowd-trade).
- Hardware Security Module, this project's main purpose is to write encryption and hashing algorithms that can run on small microcontrollers
- [Feat: Added XML support to Graphiql](https://github.com/graphql/graphiql/pull/1430)

## Project

### Adding Support of XML, YAML, MDX, TOML, ProtoBuf to GraphiQL

This package, lets name it _GraphiQLHuc (Huc is latin word, meaning anywhere)_, will allow developers to view XML, YAML, MDX, TOML, ProtoBuf as well as JSON results in GraphiQL.

**My plan to accomplish this Task**

First, I will start with adding XML support to new GraphiQL which will have Monaco Editor. Currently, there is a fetcher query in _GraphiQl.tsx_, that fecthes data and checks whether it is a valid JSON or not. If response is XML or in some other format, it makes the response red and views it as an error. So far, I have done some changes to make it generic. Once XML support is added, it will be easy to add YAML, TOML and MDX support.

Monaco Editor does not have syntax highlighting for ProtoBuf by default. So, I have to add Syntax Highlighting for ProtoBuf to Monaco Editor. Once it is added, adding ProtoBuf support will be easy. For testing purposes, I will have to modify express-graphql and make it able to send results in different formats. 

Tab option is not available in current version of GraphiQL however this is present in upcoming GraphiQL. My goal is make this plugin work with each tab separately. For example, ResultViewer mode of TAB1 is YAML and that of TAB2 is JSON. When developer switches to TAB1, ResultViewer mode will be set to YAML and similarly when tab is switched to TAB2, the mode will be changed to JSON automatically.

**Timeline**

_Community Bonding Period:_ The best way of community bonding in an opensource organization is to read code, learn from it, fix issues and participate in discussions. I will be doing these things in community bonding period.

_Week 1:_ Modifying GraphQL to send different types of reponses  so that we can view them in GraphiQL

_Week 2-3:_ Adding support of XML to new GraphiQL

_Week 4-6:_ Adding support for MDX, YAML and TOML

_Week 7-8:_ Adding support for ProtoBuf. This includes syntax highlighting for ProtoBuf in MoncaEditor as well.

_Week 9-10:_ Making this plugin to work with each Tab seapratrly.

_Week 11-12:_ Testing and Documentation

### Why should you pick me?

I have understanding of current GraphiQL codebase and i have added a support of XML to GraphiQL. To test this, i have done some changes in express-graphql to send xml response. Below is a glimpse of my work.

![XML Mode](./xml-mode.png)

### Test Project

This project is a proof that i have knowledge of GraphQL. I have created both server and client. They are deployed on AWS. This is a basic app. API provides information of patients, hospitals and statistics. New patients and hospitals can be added using mutations. GraphQL is used to avoid under-fetching and over-fetching. Links are given here.

- [AWS : GraphQL Hospital Server](http://52.66.182.42:3003) 
- [AWS : GraphQL Hospital Client](http://52.66.182.42:3001)
- [AWS: GraphiQL](http://52.66.182.42:3003/graphiql)
- [Github: API Source](https://github.com/alinauroz/graphql-hospital)

Here is a snapshot of the client.

![GraphQL Client](./client.png)






