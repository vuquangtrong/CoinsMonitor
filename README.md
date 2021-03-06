CoinsMonitor
===========
__Monitor the price of your coins, popup alerts, manage your portfolio in realtime__

(September 24th, 2017)

_Currently only support [BITTREX](https://bittrex.com/)_

## Components
I'd like to write some small modules first for some purposes:
* Learning: to get firmiliar with script language, libraries
* Testing: to debug and fix issues easier

**CoinsMonitor**
This will be the main program that has all feature of **CoinGraph**, and **CoinAlert**.
It will support **TRADING** and **STOP-LIMIT** feature

Current Status:

* 29/09/2017: Stackable Layout, each coin will be display as a stack which has all necessary actions

![CoinsMonitor_Layout_1](./CoinsMonitor_Layout_1.jpg)

Fill your api key and secret into **settings.ini** file

	[Bittrex]
	key=
	secret=
	watch=

**CoinAlert**
This module is to popup an alert when the price of selected coins go up/down to a threshold value. When its code is tested, it will be integarated into **CoinsMonitor**.
Practicing in Json, ListView, Multiple Windows

![CoinAlert](./CoinAlert.jpg)

**CoinGraph**
This module is to display the price in a nice graph area. When its code is tested, it will be integarated into **CoinsMonitor**.
Practicing in GUI, Json, Graphics

![CoinGraph](./CoinGraph.jpg)


## Run
* Run **.au3** script directly, or
* Run **.exe** binary files

## Changes
**0.0.0.0**		24/09/2017		20:00
* 	Initialize file

**0.0.0.1**		25/09/2017		15:00
* 	Add Bittrex API
* 	Add Hash HMAC
* 	Add dependent files

**0.0.0.2**		25/09/2017		16:00
* 	Add CoinAlert v0.0.0.1
* 	Update Bittrex API

**0.0.0.3**		25/09/2017		17:00
* 	Add CoinGraph v0.0.0.1
* 	Add dependent files

**0.0.0.4**		29/09/2017		17:00
* 	Add CoinsMonitor v0.0.0.1
* 	Add dependent files

## Dependencies and Credits:
* **WinHttp** for handling connections, requests. By **trancexx** at [AutoIT WinHTTP](https://www.autoitscript.com/forum/topic/84133-winhttp-functions/) or [GitHub WinHTTP](https://github.com/dragana-r/autoit-winhttp)
* **Json** for handling returned value from exchanges, by **Ward** at [AutoIT JSON](http://www.autoitscript.com/forum/index.php?showtopic=148114)
* **GraphGDIPlus** for displaying nice graphs. by **andybiochem** [AutoIT GraphGDIPlus](http://www.autoitscript.com/forum/index.php?showtopic=104399)
* **Hash HMAC** using SHA512 hashing for encrypted-method of account management, by me ^^ at [GitHub HASH HMAC](./Hash_Hmac.au3)
* **Bittrex** for openning API to exchange, by me ^^ at [GitHub Bittrex](./Bittrex.au3)
* **Stack_Component** for creating stackable layout, by me ^^ at [GitHub Bittrex](./Stack_Component.au3)

currently support Bittex APIs:

	; ===========================================================================================
	; Public Functions:
	; 	time($startDate = "1970/01/01")
	; 	bittrex_openConnection()
	; 	bittrex_closeConnection()
	; 	bittrex_getMarketSummary($sMarket)
	; 	bittrex_getMarketHistory($sMarket)
	; 	bittrex_getTicker($sMarket)
	; 	bittrex_buyLimit($sMarket, $fQuantity, $fRate)
	; 	bittrex_sellLimit($sMarket, $fQuantity, $fRate)
	; 	bittrex_cancel($sUUID)
	; 	bittrex_getOpenOrders($sMarket="")
	; 	bittrex_getBalances()
	; 	bittrex_getBalance($sCurrency)
	; 	bittrex_getDepositAddress($sCurrency)
	; ===========================================================================================

## Contributing guidelines
I’d love you to help me improve this project. To help me keep this project high
quality, I request that contributions adhere to the following guidelines.

- **Provide a link to the application or project’s homepage**. Unless it’s
  extremely popular, there’s a chance the maintainers don’t know about or use
  the language, framework, editor, app, or project your change applies to.

- **Explain why you’re making a change**. Even if it seems self-evident, please
  take a sentence or two to tell me why your change or addition should happen.
  It’s especially helpful to articulate why this change applies to *everyone*
  who works with the applicable technology, rather than just you or your team.

In general, the more you can do to help me understand the change you’re making,
the more likely I’ll be to accept your contribution quickly.

## Contributing workflow
Here’s how I suggest you go about proposing a change to this project:

1. [Fork this project][fork] to your account.
2. [Create a branch][branch] for the change you intend to make.
3. Make your changes to your fork.
4. [Send a pull request][pr] from your fork’s branch to our `master` branch.

Using the web-based interface to make changes is fine too, and will help you
by automatically forking the project and prompting to send a pull request too.

[fork]: https://help.github.com/articles/fork-a-repo/
[branch]: https://help.github.com/articles/creating-and-deleting-branches-within-your-repository
[pr]: https://help.github.com/articles/using-pull-requests/

## About
* **vuquangtrong** at gmail dot com

Donations are welcome and will be accepted via below addresses:

	BTC:	13e2SdFuyEzqw8dPjRNkyp6rDuTGKaW2rY
	LTC:	LTAJo4s5eGGMtao5gVjXSCULXV7iSc9ZnL

Thank you for the shiny stuff :kiss:

## License
[Apache-2.0](./LICENSE).
