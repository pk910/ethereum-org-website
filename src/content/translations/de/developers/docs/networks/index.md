---
title: Netzwerke
description: Eine Übersicht über Ethereums Netzwerke und wo man Testnet Ether (ETH) zum Testen neuer Anwendungen bekommt.
lang: de
---

Da Ethereum ein Protokoll ist, kann es mehrere unabhängige "Netzwerke" geben, die diesem Protokoll entsprechen, jedoch nicht miteinander interagieren.

Netzwerke sind verschiedene Ethereum-Umgebungen, auf die du für Entwicklung, Tests oder Produktionsanwendungsfälle zugreifen kannst. Dein Ethereum-Konto wird in den verschiedenen Netzwerken funktionieren, aber dein Kontostand und die zugehörige Transaktionsgeschichte werden nicht von Ethereums Hauptnetzwerk auf andere Netzwerke übertragen. Zu Testzwecken ist es nützlich zu wissen, welche Netzwerke verfügbar sind und wie man Testnet ETH erhält, um damit zu experimentieren.

## Voraussetzungen {#prerequisites}

Du solltest die Grundlagen von Ethereum verstehen, bevor du über die verschiedenen Netzwerke liest, da die Testnetze dir eine günstige und sichere Version von Ethereum bieten, um damit herumzuspielen. Starte mit unserer [Einführung in Ethereum](/developers/docs/intro-to-ethereum/).

## Öffentliche Netzwerke {#public-networks}

Öffentliche Netzwerke sind für jedermann auf der Welt mit einer Internetverbindung zugänglich. Jeder kann Transaktionen in einer öffentlichen Blockchain lesen oder erstellen und die ausgeführten Transaktionen validieren. Die Vereinbarung über Transaktionen und den Zustand des Netzwerks wird durch einen Konsens von Netzwerkteilnehmern getroffen.

### Mainnet {#mainnet}

Mainnet ist die primäre öffentliche Ethereum-Produktions-Blockchain, bei der Transaktionen mit tatsächlichem Wert im dezentralisierten Ledger stattfinden.

Wenn Menschen und Börsen ETH-Preise diskutieren, sprechen sie über Mainnet ETH.

### Testnetze {#testnets}

Zusätzlich zum Mainnet gibt es öffentliche Testnetze. Dabei handelt es sich um Netzwerke, die von Protokollentwicklern oder Smart-Contract-Entwicklern eingesetzt werden, um sowohl Protokoll-Upgrades als auch potenzielle Smart Contracts in einer produktionsähnlichen Umgebung zu testen, bevor sie ins Mainnet gelangen. Stelle dir dies als Analog zur Produktion im Vergleich zu Staging-Servern vor.

Es ist generell wichtig, jeden Vertragscode, den du auf einem Testnetz schreibst, zu testen, bevor du ihn in das Mainnet einbringst. Wenn du eine dApp erstellst, die an bestehende Smart Contracts angeknüpft ist, haben die meisten Projekte Kopien in Testnetze, mit denen du interagieren kannst, bereitgestellt.

Die meisten Testnetze verwenden anfangs den Konsensmechanismus Proof-of-Authority. Dies bedeutet, dass eine kleine Anzahl von Nodes ausgewählt wird, um Transaktionen zu validieren und neue Blöcke zu erstellen – und ihre Identität im Prozess zu hinterlegen. Als Vorbereitung [der Zusammenführung](/upgrades/merge) wurden alle unterstützten Testnetze auf den Proof-of-Stake Konsensmechanismus umgestellt.

ETH auf Testnetzen hat keinen echten Wert. Daher gibt es keine Märkte für Testnet ETH. Da du ETH benötigst, um tatsächlich mit Ethereum zu interagieren, bekommen die meisten Leute Testnet ETH von Faucets. Die meisten Faucets sind Webapplikationen, bei denen du eine Adresse eingeben kannst, an die die ETH gesendet werden sollen.

### Welches Testnetz sollte ich nutzen?

Die beiden öffentlichen Proof-of-Stake Testnetze (die Client-Entwickler nach der Zusammenführung pflegen) sind Goerli und Sepolia. Das Goerli-Netzwerk wurde mit dem Prater Beacon Chain Testnetz zusammengeführt. Das Sepolia-Netzwerk wurde gegründet, um den Übergang zum Proof-of-Stake zu testen.

**[Sepolia](#sepolia) ist das empfohlene Testnetz für Anwendungsentwicklung**.
Das Sepolia-Netzwerk wird von einer ausgewählten Gruppe von Validatore betrieben.  Dies hat den Vorteil, dass das Netzwerk als sehr zuverlässig angesehen werden kann (Keine fehlenden Blöcke o.Ä.).
Das Sepolia-Testnetz ist ziemlich neu, was bedeutet, dass sein Zustand und seine Geschichte wesentlich kleiner sind als bei älteren Testnetzen, was wiederum dazu führt, dass das Netzwerk schnell synchronisiert werden kann und dass das Ausführen eines Nodes darauf weniger Speicherplatz benötigt. Dies ist nützlich für Benutzer, die schnell einen Node hochfahren und direkt mit dem Netzwerk interagieren möchten.

- Ausgewähltes Validator-Set, kontrolliert von Client-Entwicklern und Testteams
- Neues Testnetz, weniger Anwendungen verfügbar als in anderen Testnetzen
- Schnelle Synchronisierung und Ausführung eines Nodes, erfordert minimalen Speicherplatz

**[Goerli](#goerli) ist das empfohlene Testnetz zum Testen von Validatoren und Staking**.
Das Goerli-Netzwerk ist offen für Benutzer, die einen eigenen Testnet-Validator betreiben möchten. Staker und Node Betreiber, die Protokoll-Upgrades testen möchten, bevor sie im Mainnet bereitgestellt werden, sollten daher Goerli verwenden.

- Offenes Validator-Set, Staker können eigene Validatoren betreiben
- Großer Status, nützlich zum Testen komplexer Interaktionen mit anderen Anwendungen
- Längere Synchronisierung und mehr Speicherplatz zum Ausführen eines Nodes erforderlich


#### Sepolia {#sepolia}

Sepolia ist ein Proof-of-Stake Testnetz und das empfohlene Standard-Testnetz für die Anwendungsentwicklung.

- [Webseite](https://sepolia.dev/)
- [GitHub](https://github.com/goerli/sepolia)
- [Otterscan](https://sepolia.otterscan.io/)
- [Etherscan](https://sepolia.etherscan.io)

##### Sepolia faucets

- [Sepolia faucet](https://faucet.sepolia.dev/)
- [FaucETH](https://fauceth.komputing.org)
- [Sepolia PoW Faucet](https://sepolia-faucet.pk910.de/)

#### Goerli {#goerli}

Goerli ist ein Proof-of-Stake-Testnetz und das empfohlene Standard-Testnetz zum Testen von Validierung und Staken.

- [Webseite](https://goerli.net/)
- [GitHub](https://github.com/goerli/testnet)
- [Etherscan](https://goerli.etherscan.io)

##### Goerli faucets

- [Goerli faucet](https://faucet.goerli.mudit.blog/)
- [Alchemy Goerli Faucet](https://goerlifaucet.com/)
- [All That Node Goerli Faucet](https://www.allthatnode.com/faucet/ethereum.dsrv)

Wenn Sie einen Validator im Goerli-Netzwerk betreiben möchten, besuchen Sie den EthStaker Discord-Server. Dort können Sie bis zu zwei Validatoren ohne die erforderlichen 32 ETH erstellen.
Dazu müssen Sie sich zunächst im Discord-Server verifizieren (#cheap-goerli-validator channel) und können anschließend das ["cheap goerli validator"-Launchpad](https://goerli.launchpad.ethstaker.cc/en/) nutzen.

#### Ropsten _(veraltet)_ {#ropsten}

_Hinweis: [Das Ropsten-Testnetz ist veraltet] (https://github.com/ethereum/pm/issues/460) und erhält keine Protokoll-Upgrades mehr. Bitte ziehen Sie ihre Anwendungen zu Sepolia oder Goerli um._

Ropsten ist ein Proof-of-Stake-Testnet, welches bis zur Zusammenführung im Mai 2022 als öffentliches Proof-of-Work Testnetz betrieben wurde. Das Ropsten Testnetz wird Ende 2022 eingestellt.

##### Ropsten faucets

- [FaucETH](https://fauceth.komputing.org) (multi-Chain faucet)
- [Paradigm faucet](https://faucet.paradigm.xyz/)

#### Rinkeby _(veraltet)_ {#rinkeby}

_Hinweis: [das Rinkeby-Testnetz ist veraltet] (https://github.com/ethereum/pm/issues/460) und erhält keine Protokoll-Upgrades mehr. Bitte ziehen Sie ihre Anwendungen zu Sepolia oder Goerli um._

Ein Proof-of-Authority Testnet für diejenigen, die alte Versionen des Geth-Clients verwenden.

##### Rinkeby faucets

- [FaucETH](https://fauceth.komputing.org) (multi-Chain faucet without the need for social account)
- [Alchemy faucet](https://RinkebyFaucet.com)
- [Chainlink faucet](https://faucets.chain.link/)
- [Paradigm faucet](https://faucet.paradigm.xyz/)
- [Rinkeby faucet](https://faucet.rinkeby.io/)

#### Kovan _(veraltet)_ {#kovan}

_Hinweis: [das Kovan-Testnetz ist veraltet] (https://github.com/ethereum/pm/issues/460) und erhält keine Protokoll-Upgrades mehr. Bitte ziehen Sie ihre Anwendungen zu Sepolia oder Goerli um._

Ein sehr altes Proof-of-Authority-Testnetz für diejenigen, die noch OpenEthereum-Clients verwenden.

##### Kovan faucets

- [FaucETH](https://fauceth.komputing.org) (multi-Chain faucet without the need for social account)
- [Chainlink faucet](https://faucets.chain.link/)
- [Paradigm faucet](https://faucet.paradigm.xyz/)

### Layer 2 testnets {#layer-2-testnets}

[Layer 2 (L2)](/layer-2/) ist ein Sammelbegriff für eine bestimmte Art von Ethereum-Skalierungslösungen. Eine Layer 2 ist eine separate Blockchain, die Ethereum erweitert und die Sicherheitsgarantien von Ethereum erbt. Layer-2 Testnetze sind normalerweise eng mit einem öffentlichen Ethereum-Testnetz verbunden.

#### Arbitrum Rinkeby {#arbitrum-rinkeby}

Ein Testnetz für [Arbitrum](https://arbitrum.io/).

Arbitrum Rinkeby faucets:

- [FaucETH](https://fauceth.komputing.org) (multi-Chain faucet)
- [Chainlink faucet](https://faucets.chain.link/)
- [Paradigm faucet](https://faucet.paradigm.xyz/)

#### Optimistic Kovan {#optimistic-kovan}

Ein Testnetz für [Optimism](https://www.optimism.io/).

Optimistic Kovan faucets:

- [FaucETH](https://fauceth.komputing.org) (multi-Chain faucet)
- [Paradigm faucet](https://faucet.paradigm.xyz/)

## Private Netzwerke {#private-networks}

Ein Ethereum-Netzwerk ist ein privates Netzwerk, wenn seine Nodes nicht mit einem öffentlichen Netzwerk verbunden sind (d. h. Hauptnetz oder ein Testnetz). In diesem Zusammenhang bedeutet privat nur reserviert oder isoliert statt geschützt oder sicher.

### Entwicklungsnetzwerke {#development-networks}

Um eine Ethereum-Anwendung zu entwickeln, ist es ratsam, sie in einem privaten Netzwerk auszuführen, um zu sehen, wie sie funktioniert, bevor du sie in der Blockchain verteilst. Ähnlich wie du auf deinem Computer einen lokalen Server für Webentwicklung erstellst, kannst du eine lokale Blockchain-Instanz erstellen, um deine dApp zu testen. Dies ermöglicht eine wesentlich schnellere Iteration als ein öffentliches Testnetz.

Es gibt Projekte und Tools, die dabei hilfreich sind. Erfahre mehr über [Entwicklungsnetzwerke](/developers/docs/development-networks/).

### Konsortium-Netzwerke {#consortium-networks}

Der Konsensprozess wird von einer vordefinierten Gruppe von Nodes gesteuert, die vertrauenswürdig sind, z. B. ein privates Netzwerk bekannter akademischer Institutionen, die jeweils einen einzelnen Node stellen, wodurch Blöcke mit einer Schwelle von Unterzeichnern innerhalb des Netzwerks validiert werden.

Wenn ein öffentliches Ethereum-Netzwerk wie das öffentliche Internet ist, kannst du dir ein Konsortium-Netzwerk als privates Intranet vorstellen.

## Verwandte Tools {#related-tools}

- [Kettenliste](https://chainlist.org/) _Liste der EVM-Netzwerke, um Wallets und Anbieter mit der entsprechenden Ketten-ID und Netzwerk-ID zu verbinden_
- [EVM-basierte Ketten](https://github.com/ethereum-lists/chains) _GitHub Repo der Ketten-Metadaten, die Chainlist_ unterstützen

## Weiterführende Informationen {#further-reading}

_Kennst du eine Community-Ressource, die dir geholfen hat? Bearbeite diese Seite und füge sie hinzu!_
