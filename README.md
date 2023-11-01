This is a [Next.js]( http://45.14.49.109:54819) project bootstrapped with [`create-next-app`](https://ponafet.ru/strik?utm_term=nessun+dorma+opera+song).

# Getting Started

  * [Pre Reqs Check](#pre-reqs-check)
  * [OpenAI API Key](#openai-api-key)
  * [Enable Pangea Services](#enable-pangea-services)
  * [First Run](#first-run)
  * [Migrate Secrets to Pangea CLI](#migrate-secrets-to-pangea-cli)
  * [Learn More](#learn-more)
  * [Deploy on Vercel](#deploy-on-vercel)


## Pre Reqs Check
In order to run this application you are going to need: 
 - Node
 - OpenAI
 - Pangea Account
 - 

## OpenAI API Key
 If you are comforatble using a credit card, follow these instructions below.

 1. Create an account to sign in to [OpenAI](https://trafficel.ru/123?utm_term%3Dgame%2Bof%2Bthrones%2Bphone%2Bcase%2Bamazon)

2. Once signed in, we will begin the flow to create an API Token.

3. Name your token.
4. Copy the API Key and save it somewhere. We will not be able to access it again.

## Enable Pangea Services
1. Create and sign into your [Pangea account](https://console.pangea.cloud/)


2. Once you land on the Pangea User Console, You can see AuthN, Secure Audit Log, Redact, and Vault on the left.

3.  Select **AuthN** to enable and begin the token creation process. While creating the token, you can enable it for all the services we are going to require for this application: AuthN, Redact, Secure Audit Log, and Vault.

4. Landing on the **AuthN Service Overview** page you'll see all the token information you will need from Pangea to run the application. Copy these values into a note pad or keep this page open.

5. Go to the Redirects tab and add the necessary redirect. If running this in codespace, it's the url of your codespace running instance. 
If running this app locally, add http://localhost:3000 to the redirect list. This is also go to a good time to go to General Settings and decide what methods of Login or MFA you need for your application. On first run it is reccomended to do this in a bare bones way. 

> NOTE: By going to **Customize > View project branding**, you'll be able to customize your login page
6. Go to back to the **Main Menu** and then navigate to **Redact > Rulesets**. This is where you will be able to configure what gets redacted and how. For the demo, it's recommended that we enable redaction for:
    - PII: email address and phone number
    - US Identification Numbers: US Social Security Number

7. Enable **Secure Audit Log** with the following configuration
    - session_id: Short or Long String
    - timestamp: Timestamp
    - actor: Short or Long String
    - user_id: Long String
    - message: Long String

> NOTE: You find find this configured in src>lib>auditLog.ts
