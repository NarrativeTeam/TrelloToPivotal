Trello to Pivotal Tracker converter
===================================

This converts an trello board api response json to csv files that can be imported to Pivotal Tracker.
It is based on the ruby script at http://github.com/sourcery/trello_to_tracker/ with some things modified.

* It allows for more flexible conversion of a Trello list to a Pivotal state, like started or completed.
* It converts checklist items into task items. If the name of the checklist is not "Checklist",
  the name is used as a prefix for the task item. (since there are not grouping of tasks in Pivotal)
* Labels are included in the conversion.
* Features are explicitely ordered according to order in Trello
* It is written i Python, well, just beacuse I'm more fluent in Python than Ruby, nothing noteworthy.

USAGE
-----
* Modify `ALIASES` dict to fit your board.
* Modify `ESTIMATES` dict as you wish.
* Download json data file from 
	https://trello.com/1/boards/YOUR_BOARD_ID?cards=visible&card_checklists=all&lists=all&members=all
* Then run `python trello_to_pivotal.py saved_export.json`
* Upload files in the created trello folder, in opposite order to keep the order of items.
* Inspect result, modify script, rerun until satisfied.

Author: Sebastian Jansson
