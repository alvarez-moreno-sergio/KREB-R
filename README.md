# KREB-R
Ruby repository linked to KREB project.

Standalone process which watches for Kafka's Topic's new messages coming from Redmine. 
Automates and batches email sending to its original recipients. 
This tool is born due to Office365 policies; stablishing a workaround solution for its max-emails-sent-per-minute rate.

This repository includes the patches needed to apply onto Redmine to work this out.
This patch disables Redmine's email sending and syncronizes it to send them as JSON to a Kafka Topic. 
Eventually, those messages will be read from a JAVA standalone application, which will send them to its original recipients.

Related github repositories:
* https://github.com/zendesk/delivery_boy

Gems needed:
* gem 'ruby-kafka'

* gem 'delivery_boy'
