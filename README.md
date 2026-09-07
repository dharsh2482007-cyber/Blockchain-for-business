EXNO-I 



CREATING A PRIVATE DATE: BLOCKCHAIN AIM To create a Private Blockchain and to add nodes,
create accounts, transfer Ether into it by creating and deploying Smart contract PROCEDURE
1 .GO to https //geth.ethereun.org/ and download the software for Windows. While installing
select
both geth and development tools.


2.
3.
4.
5.
6.
7.
8.  To check whether the geth is installed , run "geth" cmmand in your command prorvt.
9. TO create a Private Blockchain , we must create a genesis block.
In your cmrand prompt, create a directory go-ethereum.
mkdir go-ethereum
cd go-ethereum
10. Create two nodes inside go-ethereum.
mkdir nodel
mkdir node2
S.Open vs code using "code . "
To create account for two nodes
6.0pen terminal in vs code and change directory to nodel.
geth — -datadir account
Save the public address and password Of nodel in info.txt.
11. Repeat the same procedures for node2
cd node2
geth --datadir 'data" account new
Save the public address and password of node2 in info.txt.
To create a genesis block
8 -Create a file named "privateblock.]son" inside go-ethereum.
E Replace {Chain id } Kith your own chain id and check whether it exists or not using https
//chainlist.org/
E Replace initial signer address and firstnode address With nodel address saved in info.txt.
E And second node with node2 address saved in info. txt
E Then replace balance as "3øøøøøøeeøøeeaøøeøø» for both nodes.
To configure both nodes using genesis block
12. change directory to nodel in terminal and run this command.
geth - -datadir . /data init 'privateblock.json
1m Split terminal and cd to node2 and run the same.
13. Again split terminal and create bootnode.
mkdir bnode
cd bnode
14. TO generate key
bootnode - genkey boot. key
bootnode -nodekey boot. key verbosity 7
15. save the enode value in info.txt.
14.Run nodel and node2
- addr
"127.ø.e.1 3e3e1"
To start nodel > geth --datadir " . 'data" --port 3004 --bootnodes enode YOUR_VALUE
authrpc . port 8547 --ipcdisable —allow-insecure-unlock --http --http.corsdomain•"https
//remix.ethereum.org" --http.api --netuorkid NETWRK_ID
unlock { ADDRESS_NODEI } --password (
mine --miner.etherbase- { SIGNER_ADDRESS )
TO Start node2 > geth - -datadir . / data" - —port - -bOOtnOdes YOUR_VALUE }
authrpc.port 8546 --networkid { NETIØRK_ID } --unlock { ADDRESS_NoDE2 --password
E Replace Nodel address in {signer address} and {address nodel) and enode value with
{your value}
E {Network id} is your chain id given in privateblock.json.
Create password .txt undernodel and node2 and enter the password in it.
Replace password.txt with } .
15.60 to https //remix.ethereum.org/ and in left pane click deploy and run transactions icon.
16. Change the environment to Custm- External HTTP Provlder
17. Click on file and under create file named
18. Save the file and go to deploy tab and deploy.
19.NOdeI has deployed and added to blockchain.
#Genesis file privateblock.json
"config"
"chainld" 878787,
"homesteadBlock" e,
"eip1søB10ck" e,
"eip1s5B10ck" e,
"eip1s8B10ck" e,
"byzantiunalock" e,
"constantinopIeBIock"
"petersburgBIock"
"istanbuIBIock" a,
"berlinBIock" e,
"clique"
"period" 5,
"epoch" 3øøøe
"difficulty"
"gasLimit" "8øøeaøø",
"extradata"
" exeeeeeaøøeøøøeaøøøøøøøøøøeøøøøøøeøøøøeaøøeøøøøøøøeøøøøøøøøøøøøøøeldøgcd 3F475a65
7381 b223A9c91e29865b27 Ee27 eeeaøeaeeeeeeeaøeeøeeeaøeeeeeeeeeeeaøeaøeeeeeeaeøøøeeøø
aøeeeeeeaøeeeeeeaeeeeeeeeeeeeaøeaøeeeeeeaøeaøeeeaeeeeeeeaeeeeaøeaøeeeeeeaøe" ,
"allot" {
"Ide9cd3F47sa657381b223A9c91e29865b27Ee27" { "balance" "seeaeaøeaøeeeeeeaøø"
"ese398eFB9E4D17a48b973Bøeee1759DcF2d7879" { "balance" "yøeøøøøøøøeeøøøeaøø"
#Smart Contract New. sol
//SPDX-L1cense-1dentif1er hlT
pragma solidity •e.g. 19;
contract New(
string name;
function setNane(string memory _nme) public {
nane— name;
function getNane() public view returns (string
return name;
OUTPUT



Deploying Transaction in RemiX

<img width="1277" height="803" alt="Screenshot 2026-09-07 095919" src="https://github.com/user-attachments/assets/ae0062e0-e35c-4693-aae3-e4e826d593ee" />


<img width="1285" height="642" alt="image" src="https://github.com/user-attachments/assets/504e8bd1-137b-42f6-954f-707095409e8b" />

Releases
NO
Create a new rel ease
Packages
No packages published
P"hlish
Contributors
No contributor
