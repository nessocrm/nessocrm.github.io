---
layout: post
title: "The empty cell"
date: 2026-10-22
lang: en
locale: en_US
permalink: /en/blog/the-empty-cell/
alt: /it/blog/la-cella-vuota/
description: "At night an empty cell clears the field the source owns, and the note written on Espo stays."
image: /assets/images/blog/ch3-empty-cell.webp
image_sm: /assets/images/blog/ch3-empty-cell-640.webp
image_alt: "An empty city cell, and a note that stays on the record."
series: giro
series_order: 3
author: Nesso
---

This is the third of four readings of the same run. It does not tell a customer story. It tells what a cell does when the night file arrives, and who has the right to clear it. The first reading put Espo on one side and the channel on the other: the connection is the channel, the integration is the rule, and the passage uses the HTTP APIs. The second holds the key, the hash and the cursor, which is how a row is recognised and how an identical row is not written again. The fourth holds what stays off: write-back, the retry queue, the portal filter, the seal. Nothing of that is switched on here. Here one cell is looked at, and the reason the empty value is annoying is the same reason it is correct.

If a sentence of this journal and a sentence of the manual diverge, the manual wins. The manual lives in the docs folder of the public repository, and it changes with the code. This site does not rebuild it. The journal explains the why of one night. The manual remains the text that says what the program does today.

The journal of a run stays in the language of the run. If the run started from a page in Italian, the journal sentences stay in Italian even if the page is opened in English the next day. A badge already placed on the record is not translated afterwards. This journal exists twice, in Italian and in English, because it is an explanation and not a minute of the run. The two texts say the same facts. They do not say that the run journal will do the same.

## The file, before the rule

The file is the accounts file, the same one as the chapters beside this and the same one the home page shows in small. It arrives at night in a folder. The columns this chapter follows are five. Each already has an owner, chosen in the mapping, before the file is put down.

The external code is the identity of the row. It is how one knows which record is in question. How that identity becomes the key on the entity — the integration id, a colon, and the code — is the work of the chapter on the key. Here the code is read and kept aside. C001 is the new row. C014 is the unchanged row. A third situation, without a code invented for the occasion, is the row already known whose city arrives empty.

The name is a field of the source. The city is a field of the source. The VAT number is a field of the source. The note, in this integration, has Espo as owner. By default the owner is the source. Moving the note to Espo is an explicit decision: a salesperson writes on that field, and the night file must not take it away. The decision sits on the mapping row, next to the field, and it is read again on the handover page, where the owner of each field is listed and there are no passwords.

Then there is everything the mapping does not name. A field of the entity that does not appear in the map does not enter the run. A column of the file that nobody has linked to a field writes nowhere. Clearing, when it comes, is not a pass over the whole record. It is a pass over the fields the source owns, and only those.

Visibility is not one of these five account columns. It is a separate rule: this row belongs to the Sales team, assigned to this person. The team and the person come from a column, or the team is fixed. I come back to it when the values of the row have been read through. Mixing them in now would make a cleared city look like a reassignment of the customer. That is not what happens.

## By default the source wins

The rule is short. By default the source wins, including an empty cell. If tonight's file brings an empty city, the city on Espo becomes empty. The cell is not read as a missing fact that should leave the old value alone. It is read as a value, and the value is empty. In the file an empty cell stays an empty string. The column is there. The content is not. That string, on the field the source owns, is what gets written.

The reason is the same reason a new name replaces the old name. The source is the place from which that field takes the truth of this run. A cell that says Trieste and a cell that says nothing have the same shape: they are the content that arrived tonight. Treating the empty as a silent exception would mean the file commands only when it fills, and that when it stops filling the record keeps a memory the source has already withdrawn. On Monday that memory would look like caution. It would be a second truth, held on the record against the file. The first chapter has already said there is no third truth in the middle. This chapter is the point where that sentence can be touched: the third truth would be precisely the old city left in peace because the new cell is blank.

That is why clearing is annoying, and why it is correct. The annoyance and the rightness are the same gesture. A person opens the company and the city is gone. Yesterday it was there. Nobody pressed a delete on the field, by hand, in the interface. The file, in one cell, was blank. The annoyance is the right reaction to a visible fact that is no longer visible. The remedy is not to stop clearing on every field. It is to have chosen, before the night, which fields accept this rule. The city accepted it, because the owner is the source. The note did not accept it, because the owner is Espo.

Clearing does not walk the entity at random. It applies only where the owner is the source. A field whose owner is Espo is not cleared because the cell is blank. An unmapped field is not cleared, because the file has nothing to say about it: neither a full value nor an empty one. The sentence "the file updated the accounts" is true for the mapped fields of the source. It becomes false if it is read as "the file rewrote the entity". The entity has fields the night does not know. Those fields, in the morning, are the fields of the evening before.

There is a neighbouring case, and it must not be confused with the blank city. If the mapping marks a field as required and the cell arrives empty, the row is rejected and the field is named, before the call to Espo. The record is not half-cleared, and the empty is not written onto a field the rule has declared necessary. The first chapter already separates two different errors: a required column is missing, and then the file does not move; a cell is missing and the column is there, and then that row is rejected. The empty cell of this chapter is the third situation. The column is there, the cell is blank, the field is not held as required, the owner is the source, and the field on Espo becomes empty. The city of the example is this third situation. If someone, in the mapping, had marked the city as required, the row would not reach the clear: it would be rejected with the name of the field. The example does not make that choice. The example lets the empty win, because that is how the default rule is seen.

## A row already known, cell by cell

It helps to follow a row that already exists on Espo and that is still in the file tonight, with the city blank. I do not give it a code the story does not have. It is the row on which the city arrives empty. The other cells of the same row do not share a single fate. They are read one by one.

The code is there. Without a code one would not know which record to update, and the error of a missing identity belongs to the chapter on the key, not here. With the code, the run knows which Account this is. The code is not a field that "gets cleared" in the sense of the city: it is the way of finding the record. An empty code cell is not tonight's example.

The name, if the name cell brings a value, is written, because the name belongs to the source. If the name cell were blank, and the name were not required, the name on Espo would become empty, by the same rule as the city. In the file this chapter tells, the cell that arrives empty is the city. The name remains a field the source can update when it brings a text. No new name is invented here for that row, and no cleared name is invented. The only point is that the rule which clears the city is the rule of the name, on the day the name cell is blank.

The city is blank, and the column is there. The owner is the source, so the city on the record becomes empty. It is the gesture at the centre of the chapter. The write toward Espo is an HTTP call, on the same record, of the city field. It is not a query on the table. It is not a command that wipes the row. The other fields of this call are the ones the mapping sends along, not the whole entity. The city goes out empty. The note, if Espo owns it, does not go out in that call as an empty that deletes.

The VAT number, if the cell brings a number, remains a field of the source and follows the cell. If that number is already present on another record, it is seen before the write. The preview shows it, and the run sees it before the POST. The duplicate is not discovered only after a second Account has been created with the same number. An empty VAT number, if the cell is present and empty, the field belongs to the source, and it is not required, would clear the field. It is the same rule as the city. The extra treatment, the one the VAT number has and the city does not have in this telling, is only this: a number already present is seen first.

The note does not follow the city. The owner is Espo, and the record already exists. If a person has written a note, the note stays. If the note cell arrives empty, the field is not cleared, and the empty does not even go to the queue: there is no different text to look at, there is an absence, and the absence has no right to replace the sentence. If the cell brings a text different from the one already on the record, that text goes to a queue to look at. The field on Espo does not change. The queue holds the value that arrived next to the one that is already there, so that someone can look at it. Looking is not writing.

An unmapped field stays still for the whole row. It may be a telephone a person filled in on the entity, if the telephone is not in the map. It may be a column of the file, present tonight, that nobody linked. In the first case the run has no field name to write. In the second case it has a column and no destination. In both cases the morning finds that fact as it was, or does not find it on Espo because it was never a field of the run. The mapping is the list of fields on which the night has a right to speak. Outside that list the night is silent, even while the city, which is on the list, becomes empty.

On the same row the two gestures can live together. The city is cleared, because it belongs to the source and the cell is empty. The note stays, because it belongs to Espo. If in addition the file brings a different note, the city is cleared and, together with that, the different text enters the queue. They are not two modes of the run to choose between. They are two owners on the same row, applied on the same night. Whoever in the morning says that either everything is updated or nothing is touched is describing a script, not this mapping.

## Why the annoyance is the sign that the rule works

It is worth staying on the city, because this is the point where a reasonable person asks to switch the rule off for every field.

The scene is this. On the record the city was there. I do not give the previous city a name: the story does not fix one, and none is needed. What matters is that there was a value, and that tonight the column is there and the cell is not. In the morning the city on the record is empty. The person who holds the commercial side says the run deleted a good fact. Sometimes they are right about the fact. The empty cell can be a bad export, a shifted column, a file that kept the rows and lost the values. Being annoyed is how one notices the export. It is not how one draws the owner of every field.

If the engine, faced with the empty, left the previous city, the bad export would pass in silence. The old city would remain. The new file would say something else. The two would live together, and the following Monday nobody would know which of the two is the source. One would be back to choosing by feel, which is the fault of the second archive described in the first chapter. The product chose the other way of living together: the annoyance is visible, the empty city is visible, and one can go back on what the run wrote. Undo does that. It is not a net spread in front of the empty to stop it passing. It is the way to undo a night, after having seen it.

There is a second annoyance, the mirror of the first, and it is the one the exception avoids. The person wrote a note. The night file brings the note empty, or brings a different note, produced by a system that does not know the salesperson's sentence. If the note followed the city, on Monday the sentence would be gone. The annoyance would be right and the rule would be wrong, because that field had not been given to the source. The note stays. The empty of the city passes. They are two decisions, saved beforehand, visible on the mapping, carried out together.

The person who configures does not have to remember it by heart the morning after. They read it again on the mapping: for each field, the source or Espo. The source wins even if the cell is empty. Espo protects the value a person has already written. The mapping sheet, the one that is downloaded and uploaded again, carries column, field, transform, owner, and whether the field is required. The handover page lists the same owners, without secrets. Those are the places where the empty cell can be foreseen by day, calmly, before the file arrives.

## The queue, when the two texts do not match

On the note, the case that asks for a look is not the empty cell. It is the cell full of another text.

The record has the person's note. The file brings a different sentence. The owner is Espo. The record already exists, so this is not creation. The field is not touched. The incoming value ends in a queue to look at. Whoever opens the queue sees what is there today and what has arrived. They can decide calmly, by day. The night stopped at not writing. It did not apply the file's text "just in case", and it did not clear the field "to be safe" while waiting for that decision.

The queue is not a second CRM. It does not hold the true accounts in a parallel place, from which one then chases Espo. It holds a conflict, on one field, for one key. The Account stays on Espo. The note a person reads when opening the Account is still theirs. The conflict is a reminder. It is not a copy that wins in secret if nobody looks within an hour. It does not expire into an automatic write. It stays there to be looked at.

An empty cell on the note does not feed that queue. Nobody, in the morning, has to confirm the empty in order to save the sentence. The sentence was not in play. This avoids a false job: the queue would fill with absences, and the real work — a different text, worth reading — would be lost among them. The empty has already been decided by the owner. The different text has not: the owner says not to write it, and the queue says not to forget it.

On create, the queue, for the note, has no text already written to compare with. That is the case of C001, and it stays separate. There the note from the file can enter the record, because there is not yet a person's note. From the next run the comparison exists, and from then on a different text takes the path of the queue.

If on the same row the city is to be written empty and the note is to go to the queue, the run does both when it writes. The call toward Espo carries the empty city and does not carry the new note. The queue receives the new note. The badge, if the run wrote, will say that the last pass on the fields it touched is the ERP. The note, not having been touched, remains the person's text. The three signs — empty city, note intact, row in the queue — tell the same night without contradicting one another.

## C001, which is born

C001 is not on Espo yet. In the story the name is Nord Est and the city is Trieste. The run prepares it as a new Account. The key that will be born, on the entities Espo already has, sits in the field cExternalKey: the integration id, a colon, and C001. The format belongs to the chapter on the key. What matters here is that the row is new, because on a new row the owner of the note behaves in a way that does not repeat from the next run on.

On create the record does not exist. There is no note of a person to protect. That is why, on create, the field whose owner is Espo is written too. If the file brings a note for C001, that note may be written together with the name and the city. It is not an oversight. It is the reason for the protection: the protection applies to a note someone has already written. Tonight nobody has written it yet, because the Account is not there. "May" means this: if the note cell brings a text, that text enters the creation. If the note cell is empty, there is no text to put down, and the empty is not used to prepare a blank field to protect. From the next run, the protection protects what a person will have written, not an empty the file left on the first night.

From the next run the owner counts. If a person, after Nord Est is born, writes their note, the file of the night after does not clear it. If that file brings a different text, the text goes to the queue and the field stays the person's. C001, on the first night, is the case in which the file's note still has a place. The second night is the case in which that place, if a person has taken it, belongs to Espo.

It helps to read C001 cell by cell as well, because it is the same file and not the same situation as the blank city.

The code C001 does not yet exist as a record. It becomes part of the key. It is not an update of a same-named Account found by a resemblance of name. The first chapter has already said that two accounts with different keys remain two records, and that a similar name is not a merge. Here only the consequence is used: Nord Est is born because C001 is not there, not because the name is new in the world.

The name Nord Est is written because it belongs to the source and the cell brings it. The city Trieste is written for the same reason. On those fields there is no protection to switch on after the first time. If on a future night the city of C001 arrived empty, Trieste would become empty, and it would be correct for the same reason it is correct on the already known row of tonight. The first night is not that case: on the first night Trieste is there.

The VAT number, if the cell brings it, is written like the other fields of the source. If that number is already present on a different record, it is seen first. C001, in that case, is not born as a second Account with the same number. The preview shows it before the write. It is the same check as on the already known row, applied to a birth instead of an update. The number already present stops the row and names the field. It does not silently choose which of the two Accounts "is the right one".

The note, if it is in the file, may be written in this creation, as said. An unmapped field is not filled for the occasion. Nord Est does not receive a telephone, a category, or any other fact the mapping does not name, even if a person, later, will fill them in by hand. Those fields, when someone fills them, will be protected by not being in the run, not by the Espo owner. The Espo owner is a choice on a field the file knows. The unmapped field is a field the file has no right to name.

Visibility, if the rule is there, applies to the birth as well. Nord Est can be born in the team indicated, assigned to the person indicated. The team comes from a column or is a fixed team, for example Sales. The person is a person who already exists in Espo. C001 does not create a user because the file contains a salesperson's name. I come back to this in the part on visibility: here it is enough to see that the birth of the record and the birth of a login are two gestures, and only the first belongs to this night.

The badge, after creation, says who wrote last. At this moment the run wrote. The sentence, in the language of the run, says that the update comes from the ERP, with the date and the time. It is not a legal history of Nord Est. It is the sign on the Account just born. When, in the following days, a person saves the note, the sign can become their name. Until that save, the last to write is the file.

## C014, only as contrast

C014 is identical to the last time. The hash of the row is already the one that was saved. The chapter on the key and the hash explains why, in that case, Espo is not called. This chapter does not open it. It is not the row of the empty city and it is not the new row.

It serves as contrast. An unchanged row does not meet the empty-cell rule, because there is no new cell to apply. C014 cannot be used to show that the empty is harmless. The empty, on C014, did not arrive. If on the same account the city were blank, the hash would be another, the run would call Espo, and the city would be cleared, because the city belongs to the source. C014 of this night is not that case. It is the row the run leaves alone. The rest of the chapter talks about the rows on which there is something to decide: a birth, an empty, a note not to touch, a row that is missing.

C014 is not the example of closing either. It is in the file. Closing concerns whoever is not in the file. Keeping them near each other in the story is how one avoids giving a still row the gestures of the rows that move. In the morning, whoever looks up what happened to C014 finds a short answer: nothing, it was unchanged. The long answer about the empty cell belongs to the other row.

## The badge is not a history

On the record there is a badge. It says who wrote last. In the product it is the Nesso origin field. It does not come from a column of the file. The run puts it there when it writes.

If the last pass is the file, the badge says that the update comes from the ERP, with the date and the time, in the language of the run. If after that pass a person saves the record, the badge says that the last edit is by that person, with their name, the date and the time. A save made by the user with which Nesso talks to Espo does not count as a person's edit. That user is the technical channel. The badge does not mistake them for the salesperson who wrote the note. Without this distinction, every night write would look like a human edit, and the sign "who wrote last" would become the name of the connection, always, and would no longer be of any use.

The language of the badge is the language of the run. A run started in Italian leaves the Italian sentence. A run started in English leaves the English sentence. Changing the language of the page, the next day, does not rewrite the badge already placed, and does not rewrite the journal already written. The scheduler, which has no person in front of it, has its own language of the run. This journal is not that minute. If one looks in the run journal for the prose of this chapter, one does not find it. One finds the outcome: what was born, what changed, what stayed in the queue, what was closed, what was rejected.

The badge does not keep the series of notes. It does not prove who wrote the city last month. It is not a register to exhibit as a legal history of the changes. It says the last sign: either the ERP, or a person. For the cleared city, if the run cleared it and nobody saved afterwards, the last sign is the ERP. For the note, if a person saved it after the run, the last sign is that person, even if the file had brought another text that ended in the queue. The two facts stand together. The badge does not replace the queue. The queue does not replace the badge. Neither replaces the mapping, which is the place where the owner is read.

Whoever on Monday asks who touched the record has a short answer, and must know that it is short. To undo the values of the last run there is undo, which goes back on what that run wrote. For the protected note there is the owner. For the text the file wanted and could not write there is the queue. For the birth of Nord Est there is the record itself. The badge, on all of these, says only the last author of the save that the product recognises as the ERP or as a person.

## The row that is no longer there

So far the row was in the file. There is the other case. Tonight's file may not show it, and the rule must have it anyway: a row that was there yesterday and is not there tonight.

The record on Espo is closed and stays in the history. Closing is not deleting. The record can still be found. The note, the links, the city that was there, the name, remain to be read on that Account. Closing is not the right to be forgotten. Forgetting is another gesture, and it is not this close. This close does not forget a person and does not empty the record in order to make the data disappear. It marks that the source no longer lists that key, and it leaves the record where it is, in the history.

The close passes through the HTTP APIs, like the city and like the creation of Nord Est. It is a write of the status the entity already has, not an instruction on the Espo tables. The entity must already have a status on which to close. If the status is not there, the run does not invent a field for the occasion. Without a status, the close does not start. It is a limit that was wanted: better not to close than to close on an invented field, or on an entity that has no way of its own to say closed.

The first time a run would close records, it asks for confirmation. The reason is a truncated file. An interrupted export can contain part of the list and present itself as a whole file: the columns are there, the rows are there, only there are too few of them. If the run treated that file as the complete list, the absent records would be closed without anyone having seen the cut. Confirmation puts a person in the middle, the first time. A short file does not close the list on its own, unseen.

The confirmation concerns the keys that in that run turn out to have disappeared. After that yes, the close can be carried out. It is not a switch of chapter four. Those switches — writes held, read mode, the retry queue, the portal filter, the seal — remain another chapter, and they stay off until someone chooses them. Confirmation of the first close is the question that belongs to this gesture. It is asked when the run is about to close records for the first time, precisely because a shorter list can be an accident and not a truth.

A run that has not seen the whole source does not treat absence as a disappearance. That is the case of the cursor, and it belongs to the second chapter: if one walks only over what changed, one does not know who is missing. The confirmation spoken of here protects the other accident, the file that looks complete and is short. They are two different cautions. This chapter keeps the second. The first is pointed at and not rewritten.

A closed record can be reopened if the row comes back. It had not been deleted. There is still an Account, with its key and its history. The return of the row has a record to settle on. There is no second archive in which the closed row would live in the meantime, waiting. It lives on Espo, closed, in the history. The return is not a creation that forgets the previous close. It is the same entity, which can be open again because it is still there.

C014 does not illustrate the close: it is in the file. C001 does not illustrate the close: it arrives, and it is born. The row of the empty city does not illustrate the close: it is in the file, and it is updated. The close concerns only whoever is missing. Keeping them as four distinct cases is how one avoids closing Nord Est because Trieste is a city, and avoids clearing a city because a different row is absent.

## Who the row is for

The values and the close do not say who, inside Espo, sees the record. Visibility is a rule, and it is a rule of Espo: this row belongs to the Sales team, assigned to this person. Nesso does not invent a permission outside Espo. It does not keep a second list of who may open Nord Est.

The team and the person come from a column of the file, or the team is fixed. A fixed Sales team means the rows of this integration belong to that team, without the file having to repeat the name on every row. A team column means the cell names the team of that row. A person column names the assignee. They are data of the visibility rule. They are not a user master to import.

Espo users are not created from a master. A column of people does not become a list of logins. Creating a user is an administration gesture: a password, a role, an entry. The customer file does not have that gesture inside it. If the column names a person, it names someone who already exists as a user, and that person can be assigned. If the name does not match a user, the file does not manufacture one to make the column come out right. A column full of salesperson names is not a list of access. It is, when the rule says so, the way to indicate the assignee among people who already exist.

Visibility does not clear the note and does not fill the city. It sits beside them, on another row of the mapping. Nord Est, when it is born, can be born in the team indicated, assigned to the person indicated, if the rule has been configured. The empty city of a record that already exists is not, by itself, a change of team. If the visibility rule belongs to the source and the team cell brings a team, the team follows that cell, as a field of the source. If the team is fixed, there is no cell and the fixed team stays. In none of these passages is a login born. Confusing the team with the city produces the suspicion that every clear reassigns the customers. The suspicion dissolves by reading the mapping again: the city is a field, the team is the visibility rule.

Here too a fact that was not decided is not invented. If the rule does not name a person, the run does not pick a salesperson at random for C001 or for the row of the empty city. If it does not name a team, it does not create one to make the sentence "every row has a home" come out even. The product's sentence is narrower. When visibility is configured, this row belongs to the team that was named, assigned to the person that was named. The team and the person come from a column or from a fixed team. The users remain the ones the administrator has already created.

## The preview, the VAT number, undo

Before the write one can open the preview. It does not write. It shows what would be born and what would change. It does not move the file and it does not by itself put the rows in the queue: it counts the run, and it stops.

For the night of this chapter, C001 would be born: name Nord Est, city Trieste, and the note from the file if the file brings it, because the record does not exist and the Espo-owned field, on create, is written. The city of the row whose cell is empty would change: one would see the passage from today's value to the empty. C014 would appear among what does not change, because it is unchanged. A VAT number already present is seen first, not after a POST. If the number of C001, or the number of the already known row, is already on another record, the preview meets it before a duplicate is born.

The preview also shows the conflict on the note, when the file brings a text different from the person's: the value of today and the value arriving, without applying the second. It is the same content that, if the run then writes, will end in the queue while the empty city is written. Whoever looks at the preview can therefore see, on the same row, a real change and a change that will not happen. The first is the city. The second is the note. Seeing them together is why the preview is worth opening, on this file, more than a bare count of rows.

The switches that stop every write, read mode, the retry queue, the portal filter and the seal live in chapter four. Here the preview enters only as the way to see the empty cell and the birth of C001 without having written them yet. It is not the chapter of those switches. It does not turn them on. It does not describe how a secret is sealed or how a rejected row is retried. It says that, before the gesture, one can look.

Undo goes back on what the run wrote. If the run cleared the city, undo puts back the value that was there before that write. That is the step back on the field the run touched. If after the run a person changed the field, and the value is no longer the one the run wrote, undo does not cover that later change. It goes back on what the run wrote, not on what a person wrote afterwards. The person's note, if the run did not write it, does not enter that step. There was no value of the run to restore on a field the night left alone.

Undo is not the right to be forgotten. It does not delete Nord Est from the world, and it is not the reopening of a closed record told as the reverse of a deletion. It is the return of the values of the last run, on the fields that run really wrote and that nobody has replaced in the meantime. It is used on the morning when the empty city was a bad export. The preview, if it was opened before, had already shown that empty. Undo is the later gesture, when the empty has been written and one wants to undo it.

## What stays off

Write-back stays off. It is not on during this night, and this chapter does not describe it as if it were. Turning it on is a later, explicit choice. Chapter four holds it, together with the retry queue, the portal filter and the seal. The empty cell is not written back onto the file by Nesso. The person's note is not deposited into the night file by this run. The file comes in. The fields of the source follow the file, empties included. The fields of Espo stay on Espo. The return, if one day someone wants it, will be another decision, taken apart, not a consequence of the empty cell and not a way to "put the city back" into the file without having named the columns.

The passage, in every direction of this chapter, is by HTTP API only. Clearing the city is a call. Creating Nord Est is a call. Reading the note already present, to know whether the incoming text is different, is a call. Closing a record that disappeared is a call, on the status the entity already has. Undo, when it puts the previous value back, is a call. The Espo tables are not a channel. They are not a channel for fixing the empty cell by hand with a query, and they are not a channel for reading the note's value "faster". Whoever has the query in mind is thinking of the gesture the first chapter put outside the boundary.

## What this run is not

Nesso is not a second CRM. The truth of the city is the cell, because the city belongs to the source. The truth of the note is the record, because the note belongs to Espo. There is no third city kept in the engine in case the file goes too far. The engine remembers the run: hash, cursor, queue, journal, keys seen. They are memories of the passage, and the chapter on the key separates them from the records. They are not the accounts. Opening those memories does not show a customer parallel to Nord Est. It shows whether the row had already been seen, whether a conflict is waiting, whether a run can be undone.

This file is not a certified connector. The mapping was read by a person. The name of the system that put the file in the folder is not in the program. The accounts recipe, if it was used as a starting point, remains a starting point: it proposes fields, it does not certify an ERP, and it does not save itself. The person reviews the owners and then saves. The empty cell is correct because that save left the city to the source, not because a certificate says that the city column of a certain product is to be treated this way.

It is not a customer story. Nord Est and Trieste are the name and the city of the example, the same ones as the first reading. There is no company to recognise behind the code C001. There is no reference, and there is no case to cite as a commercial proof. The file is there so the rule can be seen on small rows: one is born, one does not move, one loses the city, one note stays.

Mail does not enter this run. CRM mail stays in Espo. The accounts file does not send and does not read a mailbox. The note is a field of the record. It is not a message. Treating it as mail, because it is a text a person wrote, would mix the owner of the field with another job, and with another secret. The secret of a mailbox is not the secret of an accounts file. Here there is neither to tell: there is a cell, and there is a field.

## Monday, the same night

It helps to tell the same night again, in the order a person meets it on Monday, without adding facts.

They open the preview, if they want to see before writing. They see C001 that would be born: name Nord Est, city Trieste, and the note from the file if it is there, because the record does not exist and the note whose owner is Espo, on create, may be written. They see the already known row whose city would arrive empty: the change is the city. The note of that row, if a person wrote it, is not among the changes. If the file brings a different text, the preview shows today's value and the one arriving, and that field would not be written. They see C014 among what would not change. They see, before the write, a VAT number already present, if there is one, and the row that carries it does not become a second Account in silence. If the list is shorter than yesterday and the run has seen the whole source, they see that a close would ask for confirmation the first time, and that without that yes the records would not be closed unseen.

Then, if the run really starts, the writes are the ones the preview had counted. C001 becomes an Account, over HTTP. The city of the row with the empty becomes empty, over HTTP, because that field belongs to the source. The person's note stays on the record. The different text, if it was there, is in a queue to look at, and the field has not changed. Unmapped fields are as before. The team and the person are those of the visibility rule, from a column or from a fixed team, and no login was born from the file. The badge, on the records the run wrote, says that the last to write is the ERP, in the language of the run, until a person saves. A save by the technical user does not move that sign onto a person's name. The journal of that run stays in the language in which the run started. It tells the outcome, not this chapter.

If the empty city was an error in the file, undo goes back on what the run wrote. The city can return to the previous value, if in the meantime nobody has written another value on that field. The note the run did not touch does not need undo in order to exist: it had not gone. Undo does not empty the queue in place of a person who still has to look at the different text, and it does not turn the queue into a write.

If a row is missing and someone confirms the first close, the record is closed and stays in the history. It is not deleted. It is not the gesture by which a person is forgotten. If later the row comes back, the closed record can be reopened, because it is still there. The history read on the record has not been replaced by a hole.

Through all of this, write-back stayed off. No switch of chapter four was turned on to make the empty cell work. The empty cell works with the owner rule. The file comes in. Espo receives, over HTTP, the fields of the source, empties included. The fields of Espo, after creation, stay with whoever wrote them on the record.

## Two desks, the same facts

The same night can be read again from the two people the first chapter already put in front of the file, without redrawing their portrait. What matters here is what each of them sees of this rule, and that neither sees a fact the other could not check.

The person who wrote the note opens the Account. The sentence is still there, if it was there before the run and the record was not being created. The city may be empty. The badge may say that the last pass of the ERP is from tonight, or, if this person saves after checking, that the last edit is theirs. In the queue, if the file had another text, that text is there, to look at, and it was not written in place of the sentence. This person does not need to know how the key is made. They need to know that the owner of the note is Espo, and that the owner of the city is the source. The two sentences explain the morning in full.

The person who confirms the closes, or the person whose task is to say yes the first time, looks at another list: the keys that are no longer in the file. They do not look at the city of whoever is still there. A truncated file is recognised there, from the size of the list one would close, not from the fact that a city is blank. Saying yes closes and leaves the history. Not saying yes leaves the records open, still listed by the previous source, waiting for a file that really is the list. Neither answer deletes, and neither is forgetting.

The person who configured the mapping, on Monday, does not discover the rule. They read it again. The city is the source. The note is Espo. The team is the visibility rule. Users are not born from the file. The preview, if they opened it, had already separated C001, the empty city, C014 and the conflict on the note. The journal confirms the outcome in the language of the run. If something in the journal and in this diary does not agree, one opens the manual. The diary may have been read in English or in Italian. The journal was not: it remained the one of the night.

## The next run, on Nord Est

The day after, or the night after, the owner that on create had made an exception returns to the ordinary rule. It is worth telling it on Nord Est alone, because it is the same record and it is no longer the same situation.

Nord Est exists. Trieste, if the file brings it again, stays or is written the same: it belongs to the source. If the file of that second night brings the city empty, Trieste goes, and it is the same correct annoyance as on the already known row. There is no grace period for records born from Nesso. Having been born yesterday does not make the city the property of the person.

The note, if on create the file had brought it and nobody has changed it yet, is the text put down on the first night. If a person in the meantime has replaced it with theirs, the Espo owner protects theirs. The file does not clear it. A different text from the file goes to the queue. The field stays. The badge, if the person has saved, names the person. If nobody has saved after the run, and the run has anyway written other fields of the source, the badge names the ERP, and the person's note is still there: the badge says the last, it does not say that every field of the record was rewritten by that last one.

C014, if it stays identical, continues not to be the subject. A row that is absent, if the file loses it and the first close has already been confirmed in a previous run, is closed and remains in the history. If it comes back, it can be reopened. None of these steps turns write-back on. None creates a user. None speaks to the tables.

## What this chapter did not do

It did not redo the boundary. Espo is still on one side, the channel on the other, and the first chapter remains the place of that sentence. It did not explain how the hash of C014 is calculated, nor how the cursor remembers the last record sent: that is the second chapter, and here C014 enters only to say that an unchanged row is not an empty cell. It did not turn write-back on, it did not describe the retry queue, it did not open the portal filter and it did not set the seal. Chapter four holds those things, and they stay off even after the city has been cleared.

It followed a file, at night, field by field. The source wins, and it wins even when the cell is empty, on the fields it owns that were not marked required. The city is cleared because it is the source's. The note is not cleared because it is Espo's, except on create, when there is not yet a note to protect and C001, Nord Est, Trieste, may receive the note from the file. From the next run, on that record, the owner counts. A different text waits in the queue and does not replace the sentence. The badge says the last author, not the legal history. The row that disappeared is closed, not deleted, not forgotten, and the first time it asks for a yes, so that a truncated file does not close the list unseen. If the row comes back, the record can be reopened. Visibility assigns the Sales team and the person, from a column or from a fixed team, and a column of people does not become a list of logins. The preview shows what would be born and what would change, and a VAT number already present is seen first. Undo goes back on what the run wrote. The manual, if this diary and the manual do not say the same thing, is what remains.
