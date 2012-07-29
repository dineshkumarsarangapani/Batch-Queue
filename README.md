Batch-Queue
===========

A batch queue module for drupal developers.

A batch queue module for drupal developers. Recently in my project we need to run Drupal queue in Drush using sh scripts. I was also in the search for running queue faster and contiously as we would get huge amount of queue data. 

I came across some use full post and module related to queue which i will share.

1 .Drush Queue Module 
    This module provides a Drush command to run the queue using Drush. So we can also run the Queue in sh script in some definite intervals.
2. Queue UI Module
    This module provides a UI for avalable queue in the system which has items available. It also provides additional functionality to run Queue in batch process and cron process.
    The dis-advantage is that this module needs aditional hook "hook_queue_info" where developers use it to define the batch process and implement the operations.
    So with the help of above modules i decided to write a batch queue module which will run batch queue in  Drush as a background process. 

You can grab the code from 

https://github.com/dinesh-kumar-11/Batch-Queue#batch-queue

Features:

Hooks up all queue defined in the system using "hook_cron_queue_info" with Queue ui module.
Batch process for all the queue in the Queue ui interface.
Drush command to run batch queue in back ground
Example: Drush batch-queue-run queue-name

(Replace "queue-name" with the queue name from your system ).



