## 

I removed a record from prod DB and... noticed that it is not quite what needed to be removed.
Next second my wife finishing her sentence with "...this what soft remove for.". And I instantly recall that we have removed_at field FOR THIS EXACT PURPOSE!!!

Anyway. I refreshed the page - the record is still there. That's odd. 
I refresh DBeaver UI - it shows that the record has been removed (no record shown). 

5-10 minutes later I noticed that the record is there again. And my ass is saved. 
I added a timestamp to 'removed_at' and the job has been done finally. 

So, I dodged the bullet this time :D It was close.

A mystery here: I unpressed a lock icon on prod DB in DBeaver UI. So I thought I'm in read-write mode now. But I didn't somehow.
Shout out to this issue from DBeaver. 
But it might be useful if DBeaver will really unlock the data when I unlock it
