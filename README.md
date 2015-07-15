#bugur

A thing that ingests bugzilla email, and spits out another thing.

Will only supply finite history. Last 3 days; last 7 days; last 30 days; _maybe_ last quarter

bugur.co/ckprice

    activity in the last x
    last x things
    most used product/component

bugur.co/trophy/x/y

    most x in the last y

bugur.co/1234567

    bug contributors
    bug stats

##schema 1 (mail)
    
    mail_id (pk)
    mail_date
    bug_id
    user_id
    comment
    product
    component

##schema 2 (what changed)

    changed_id (pk)
    mail_id (fk)
    bug_id - not great, but could come in handy having it here
    what
    removed
    added
    
##schemd 3 (bug meta - maybe)

    bug_id
    summary
    reported
    reported_by
    product
    component

##API uses?

    get user ID [https://bugzilla.mozilla.org/rest/user?names=cprice@mozilla.com]
    get product/component ID's?
    
