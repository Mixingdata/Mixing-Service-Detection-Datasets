
This repository provides an example dataset for money laundering detection. Here are two CSV files:

1. bitcoinwalletall_address_features.csv: A list of features for Bitcoin addresses. The first 20 columns represent basic features of the address.
   The subsequent 18 columns represent enhanced features that provide additional insights into the address's behavior. The description of the basic features is as follows:

 +----------------------------------------+---------------------------------------------------------------------------------+
 | Feature                                | Description                                                                     |
 +----------------------------------------+---------------------------------------------------------------------------------+
 | total_transaction                      | The total number of transactions involving the address                          |
 | total_received                         | The total amount received by the address                                        |
 | total_sent                             | The total amount received by the address                                        |
 | indegree                               | The in-degree of the address                                                    |
 | outdegree                              | The out-degree of the address                                                   |
 | total_address                          | The total number of second-order neighboring addresses of the address           |
 | unique_address                         | The number of unique second-order neighboring addresses of the address          |
 | redundant_address                      | The number of duplicate second-order neighboring addresses of the address       |
 | average_address_per_tx                 | The average number of second-order neighboring addresses of the address         |
 | address_variance                       | The variance of  second-order neighboring addresses of the address              |
 | average_indegree                       | The average in-degree of first-order neighboring transactions of the address    |
 | indegree_variance                      | The variance in-degree of first-order neighboring transactions of the address   |
 | average_outdegree                      | The average out-degree of first-order neighboring transactions of the address   |
 | outdegree_variance                     | The variance out-degree of first-order neighboring transactions of the address  |
 | income_to_expense_ratio                | The ratio of income to expense                                                  |
 | total_income_expense                   | The total amount involved in all transactions of the address                    |
 | average_income_per_indegree            | The average amount received by the address                                      |
 | income_variance                        | The variance of the amount received by the address                              |
 | average_expense_per_outdegree          | The average amount sent by the address                                          |
 | expense_variance                       | The variance of the amount sent by the address                                  |
 +----------------------------------------+---------------------------------------------------------------------------------+

2. bc1qz6u899624hdhwq0k6rxzqhsc2rknplzwlvv3g9.csv: This file contains all transaction records for the address with ID bc1qz6u899624hdhwq0k6rxzqhsc2rknplzwlvv3g9.
   It provides detailed transaction-level features for this specific address, which provides raw transaction features for temporal transaction sequence learning.
   The description of the transaction features is as follows:

 +----------------------------------------+---------------------------------------------------------------------------------+
 | Feature                                | Description                                                                     |
 +----------------------------------------+---------------------------------------------------------------------------------+
 | address_in_amount                      | The amount input to the central address from this transaction                   |
 | address_out_amount                     | The amount received from the central address in the transaction                 |
 | time_diff                              | The time interval (in seconds) between this transaction and the previous one    |
 | fee                                    | The difference between the total input amount and the total output amount       |
 | in_degree                              | The in-degree of the transaction                                                |
 | out_degree                             | The out-degree of the transaction                                               |
 | degree_ratio                           | The ratio of the in-degree to the out-degree of the transaction                 |
 | all_degree                             | The sum of the in-degree and the out-degree                                     |
 | total_in                               | The total amounts input to this transaction                                     |
 | max_in                                 | The maximum of the amounts input to this transaction                            |
 | min_in                                 | The minimum of the amounts input to this transaction                            |
 | median_in                              | The median of the amounts input to this transaction                             |
 | mean_in                                | The average amounts input to this transaction                                   |
 | var_in                                 | The variance of the amounts input to this transaction                           |
 | total_out                              | The total amounts output from this transaction                                  |
 | max_out                                | The maximum of the amounts output from this transaction                         |
 | min_out                                | The minimum of the amounts output from this transaction                         |
 | median_out                             | The median of the amounts output from this transaction                          |
 | mean_out                               | The average amounts output from this transaction                                |
 | var_out                                | The variance of the amounts output from this transaction                        |
 +----------------------------------------+---------------------------------------------------------------------------------+

