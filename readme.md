remind-recurring-todo: define recurring todo's with remind(1)

    [pdurbin@tabby remind-recurring-todo]$ ./recurring | head
    No reminders.
    No reminders.
    Reminders for Wednesday, 2nd May, 2012:

    place grocery order

    Reminders for Thursday, 3rd May, 2012:

    pay housekeeper

    [pdurbin@tabby remind-recurring-todo]$ ./recurring | ./filtertasks | head

    ===== Wednesday, 2nd May, 2012 =====
    - place grocery order

    ===== Thursday, 3rd May, 2012 =====
    - pay housekeeper

    ===== Friday, 4th May, 2012 =====
    - receive grocery order

    [pdurbin@tabby remind-recurring-todo]$ ./recurring | ./filtertasks | ./pdfcreate 
    [stdin (plain): 20 pages on 10 sheets]
    [Total: 20 pages on 10 sheets] sent to the standard output
    Saved to checklist.2012-04-30.pdf
    [pdurbin@tabby remind-recurring-todo]$ 
    [pdurbin@tabby remind-recurring-todo]$ ./recurring > recurring.`date -I`.txt
    [pdurbin@tabby remind-recurring-todo]$ wc -l recurring.2012-04-30.txt
    2285 recurring.2012-04-30.txt

