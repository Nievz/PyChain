# PyChain Ledger Application

Welcome to the PyChain Ledger Application! In this project, we have built a blockchain-based ledger system with a user-friendly web interface, which allows partner banks to conduct financial transactions and verify the integrity of the data in the ledger.

## Table of Contents

- [Background](#background)
- [What We've Created](#what-weve-created)
- [Files](#files)
- [Instructions](#instructions)
  - [Step 1: Create a Record Data Class](#step-1-create-a-record-data-class)
  - [Step 2: Modify the Existing Block Data Class](#step-2-modify-the-existing-block-data-class)
  - [Step 3: Add Relevant User Inputs to the Streamlit Interface](#step-3-add-relevant-user-inputs-to-the-streamlit-interface)
  - [Step 4: Test the PyChain Ledger by Storing Records](#step-4-test-the-pychain-ledger-by-storing-records)
- [Screenshots](#screenshots)
- [Conclusion](#conclusion)

## Background

As fintech engineers working at one of the world's largest banks, we were tasked with leading the development of a decentralized finance team. Our mission was to build a blockchain-based ledger system with a user-friendly web interface. The purpose of this system was to enable partner banks to perform secure financial transactions and ensure data integrity within the ledger.

## What We've Created

We are proud to share the successful completion of the PyChain Ledger Application. Here's what we've accomplished:

### Step 1: Create a Record Data Class

We defined a new Python data class named `Record`. This class serves as the template for financial transaction records in the ledger.

```python
@dataclass
class Record:
    sender: str
    receiver: str
    amount: str 
```
### Step 2: Modify the Existing Block Data Class

We renamed the data attribute in the Block class to record and set its data type to Record.

```python
record: Record
    creator_id: int
    prev_hash: str = "0"
    timestamp: str = datetime.datetime.utcnow().strftime("%H:%M:%S")
    nonce: int = 0
```
### Step 3: Add Relevant User Inputs to the Streamlit Interface

In our Streamlit application, we made the following updates:

    We deleted the input_data variable.
    We added input areas to collect values for sender, receiver, and amount from the user.
    We updated the new_block functionality to include a Record attribute containing sender, receiver, and amount when adding a new block.

### Step 4: Test the PyChain Ledger by Storing Records

We thoroughly tested our completed PyChain ledger and user interface by performing the following steps:

   1. We navigated to the project folder in the terminal.

   2. We ran the Streamlit application using the following command:
```python
streamlit run pychain.py
```
3. We entered values for sender, receiver, and amount, and then clicked the "Add Block" button multiple times to store several blocks in the ledger.

4. We verified the block contents and hashes in the Streamlit drop-down menu. We took a screenshot of the Streamlit application page, which displayed a blockchain consisting of multiple blocks. This screenshot is included in our README below.

5. We tested the blockchain validation process using the web interface. We took a screenshot of the Streamlit application page, which indicated the validity of the blockchain. This screenshot is also included in our README below.

## Screenshots

### Blockchain with Multiple Blocks

### Blockchain with Multiple Blocks

### Blockchain Validation

### Blockchain Validation

## Conclusion

We are thrilled to announce the successful completion of the PyChain Ledger Application. Our decentralized ledger system empowers partner banks to conduct financial transactions securely. If you have any questions or need further information, please feel free to reach out. 

