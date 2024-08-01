# Documentation for the API Server-to-Server-Communication - Products with external Order Routes

## 1. Introduction

Sovendus displays your product following some transaction process (e.g. order checkout) at its numerous partners. To be able to register your orders properly and assign them correctly to our respective advertising partners, Sovendus offers the possibility to transmit your generated orders via API call.
To achieve this, Sovendus transfers a generic token with any request of your landing page URL. This token is the base of order registration at Sovendus. It is generated dynamically and therefore changes with every request. This token has to be picked out of the URL of your landing page, buffered und returned to Sovendus via a simple API call after completion of the transaction.

> [!WARNING]
> Prerequisite for a successful cooperation is the return transfer of the token.
> Without a proper back transfer, the Sovendus algorithm is not able to handle your product as intended. As a
> result, your product won’t be displayed on our advertising partners‘ pages any more, just few days after.

## 2. Login credentials

Please keep your login credentials confidential. If you received this documentation in advance, your credentials will be sent to you by your contact at Sovendus.

> [!WARNING]
> Product-ID:
>
> API key:
>

## 3. Workflow

![Workflow-image](https://raw.githubusercontent.com/Sovendus-GmbH/Generic-Sovendus-Checkout-Products-Postback-Integration-Documentation/main/workflowimg.png)

## 4. External Product-ID
Every campaign at Sovendus receives its own fixed alphanumerical Product-ID. This Product-ID has to be added to the API call transfer. The Product-ID is permanently assigned to your product.
You receive this Product-ID from your contact at Sovendus or you can learn it from paragraph 2 of this documentation.

## 5. Token
With every click on your product teaser image an ampersand (&) and the parameter sovReqToken will be added to the URL of your landing page by default. The alphanumerical value of the sovReqToken parameter is dynamic and changes with every new click on your product. The token has to be picked out of the URL by you, buffered and transferred back to Sovendus via API call after completion of the transaction.

> [!WARNING]
> <span style="background-color: blue; color: black;">https://www.website.com/landingpage?channel=sovendus</span><span style="background-color: red; color: black;">&sovReqToken=XXXXX-XXXXX-XXX-XXXXX</span>
>
> <span style="background-color: blue; color: black;">URL of your landingpage</span> <span style="background-color: red; color: black;">Token</span>