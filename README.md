# Fraud Detection

Fraudsters create fake transactions to boost sales/shop ratings. Fake transactions are defined as transactions where the buyer and seller are the same individual (in reality). To help Shopee tackle this issue, you are expected to detect these fake transactions from normal transactions. Sample data for transactions and users' details will be provided.

## Task

Find fake orders where the buyer and the seller share the same details, i.e. directly linked by any of the following links: Device, Credit Card, Bank Account.

## Basic Concepts

Each userid represents a distinct user on Shopee.
Each orderid represents a distinct transaction on Shopee.
Device, Credit Card, Bank Account data is encrypted to preserve data privacy. Each distinct value represents a unique entity.

## Example

orderid: 1955598428, buyer userid: 35545436, seller userid: 70763052.

* The buyer has this device: "/3TLpeou8xXsNxpACFFKr34Kqqwxiu5Hi1keJ6plk5E=".
* The seller also has this device: "/3TLpeou8xXsNxpACFFKr34Kqqwxiu5Hi1keJ6plk5E=". 
* Therefore, we consider that the buyer and the seller are linked by device.

This order is a fraud order by definition.

## Submit Format

Two columns required:

* orderid.
* is_fraud: assign value 1 if the order is fraud, otherwise 0

Your submission should have 620947 rows, each with 2 columns.
