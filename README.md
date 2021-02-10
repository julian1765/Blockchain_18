# Blockchain_18 POA 

# Step One Setting up both nodes

   ### -The First Step of Running a Proof of Authority Block Chain Is to set up both Nodes that will be used as a preapproved sealer addresses. 

   ### -You will need to navigate into your blockchain folder and use the following code in order to create two new nodes. 

### ./geth --datadir node1 account new
### ./geth --datadir node2 account new


   <p align="center">
    <ins><b>Nodes 1 & 2 Addresses:</b><br><ins>
    <img src=screen_shots_folder/Node_Info.PNG </p>

 # Creating Genesis Block

### -Navigate to your geth-alltools-windows-amd64-1.9.7-a718daa6 Folder and run the ./puppeth command in your terminal and name  your new network. Then select the option to configure a new genesis block. 

### -Click number two for Clique (proof of Authority) Consensus Mechanism. 

### -You will then have the option to paste both account node addresses in order to seal. 

### -Continue to add both node addresses again when prompted to Pre-fund Accounts.

### -The next step is to select no to prefund the complied accounts. 

### -Specify a Chain ID number for the Genesis Block. Should be 3 numbers. 

 <p align="center">
    <ins><b>Creating Genesis Block:</b><br><ins>
    <img src=screen_shots_folder/Capture_2.PNG </p>

### -Then finish the rest of the prompts  and select " Manage Existing Genesis". 

### -Export the configuration and make sure there are two files availble. 

<p align="center">
    <ins><b>Exported Genesis Files:</b><br><ins>
    <img src=screen_shots_folder/json_info.PNG </p>

# Initialize the nodes with Json Files.

### -By using these lines of code you will be able to initialize each node.

### ./geth --datadir node1 init poablockchain.json
### ./geth --datadir node2 init poablockchain.json

<p align="center">
    <ins><b>Initialized nodes:</b><br><ins>
    <img src=screen_shots_folder/initialize_node.PNG </p>

# Mining Blocks
### -Open two seperate Termimnal windows in order to start mining.

### - Navigate to the geth-alltools-windows-amd64-1.9.7-a718daa6 folder and use the following code: 

### ./geth --datadir node1 --unlock e5812bFcbd645DF727CAf0b2167Cc264542D7FDf --rpc --mine --minerthreads 1 --password password.txt --allow-insecure-unlock 

### -Keep in mind this terminal will not start minning until you have completed node 2. 

### -For your second terminal use the following code: 

### --datadir node2 --mine --unlock 34A6C759C74F202Ec1C7dA16607297724c335CFE --password password.txt --port 30304 --allow-insecure-unlock --bootnodes enode://cf8d18e244ac9828a6390ba8f477dabeccd559ed7c69a89844d01448ba05541377b786ee45830916ea22e6c752ec31cc03e7210564b363b7efbd4b915e7e4f8e@127.0.0.1:30303--ipcdisable 

### Once you have entered the following code your nodes should begin minning. 

### NOTE: Make sure to create a text file with your password in order to access nodes.

<p align="center">
    <ins><b>Node 1 Minning:</b><br><ins>
    <img src=screen_shots_folder/node_1_minning.PNG </p>

<p align="center">
    <ins><b>Node 2 Minning:</b><br><ins>
    <img src=screen_shots_folder/node_2_minning.PNG </p>

# Adding the Blockchain to MyCrypto

### Launch the MyCrypto Application and change the network by clicking "Change Network" at the bottom left. 

### Select " Add Custom Node" and plug in your Custom Network Credentials.

<p align="center">
    <ins><b>Set Up Your Custom Node:</b><br><ins>
    <img src=screen_shots_folder/custom_node_setup.PNG </p>

### -Make sure to select ETH for currency and have the correct chain id. 

### -For the URL Type in http://127.0.0.1:8545. 

### -Select "Save & Use Custom Node" when finished. 

# Acessing MyCrypto wallet and testing connection. 

### -Click on the "View & Send" option on the left hand side followed by clicking on the Keystore File.

### -Next Step is to select "Select Wallet File" and find your keystore file inside your node 1 File.

### -Once you have selected the file type in your password and then hit "Unlock".

<p align="center">
    <ins><b>Unlock your Keystore File:</b><br><ins>
    <img src=screen_shots_folder/unlock_kestore.PNG </p>

# Sending transactions from MyCrypto Wallet 

### -Once You have opened your Account Wallet you should see your ETH account balance under the "Account Balance" Section to the upper left hand side.

<p align="center">
    <ins><b>Crypto Wallet with Account Balance:</b><br><ins>
    <img src=screen_shots_folder/wallet_with_eth.PNG </p>


### -To send a transaction, type in the public address of node 2 and fill in the amount of ETH you would like to send. 

<p align="center">
    <ins><b>Sending ETH :</b><br><ins>
    <img src=screen_shots_folder/prepare_to_send.PNG </p>

### Confirm the transaction by selecting " Send Transaction and you will get a summary pop up with your transaction summary. Hit "Send" when this pop up generates. 

<p align="center">
    <ins><b>Confirm Transaction :</b><br><ins>
    <img src=screen_shots_folder/confirm_transaction.PNG </p>

### Once you hit "Send" a green message on the bottom of your screen will indicate that your transaction is being processed. 

<p align="center">
    <ins><b>Transaction Status :</b><br><ins>
    <img src=screen_shots_folder/Transaction_Sent.PNG </p>

### Next click on the "Check TX Status" to check the status. 

### Once you have followed these steps you have created a private Blockchain. 


# Dependencies 

### - MyCrypto 
### - GitBash
### - Geth & Puppeth















