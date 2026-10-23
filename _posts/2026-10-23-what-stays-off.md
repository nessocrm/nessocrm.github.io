---
layout: post
title: "What stays off"
date: 2026-10-23
lang: en
locale: en_US
permalink: /en/blog/what-stays-off/
alt: /it/blog/quello-che-resta-spento/
description: "The fourth chapter names the brakes that exist, why the trial leaves them off, and what a person sees before the first write."
image: /assets/images/blog/ch4-switches-off.webp
image_sm: /assets/images/blog/ch4-switches-off-640.webp
image_alt: "Four switches left off beside a sheet still to be read."
series: giro
series_order: 4
author: Nesso
---

This is the fourth of four readings of the same run. The first put Espo on one side and the channel on the other, and separated the connection from the integration. The second showed the key, the hash, and the cursor. The third followed the empty cell, the field owner, and the close that leaves the record in the history. This chapter turns nothing on. It tells the brakes, and the switches that exist and stay off.

Off, here, is a choice. It is not a piece that was forgotten, and it is not a hidden defect under a kinder name. The trial leaves four switches off on purpose: write-back, the retry queue, the portal filter, the seal on secrets. A run can start anyway. What does not start is the behaviour those switches would add. Whoever reads on Monday morning must be able to say, out loud, which lever is down and which lever was never raised.

If a sentence of this journal and a sentence of the manual diverge, the manual wins. The manual lives in the docs folder of the public repository, and it changes with the code. This site does not recompile it. The journal explains the why. The manual remains the text that says what the program does today.

The thread is still the customer-master file. It arrives at night. It has the external code, the name, the city, the VAT number, a note. In the story of the series, C001 is the new row, Nord Est, Trieste. C014 is the row identical to last time. One row lacks a required column, and that reject is at file level. The note, on this integration, has Espo as its owner. None of this, at the opening of the chapter, has been written yet. The chapter stops one step before the POST, and then says what, even afterwards, stays off.

## Before the first write

The person who installs has already taken the four steps, or is stopped on the third. The connection is there: an address, a kind, and a password if one is needed. The integration is there, or it is still a draft: the entity, the identity column, the mapping, the cadence. The file is in the folder, or the SELECT is saved, or the webhook has not called yet. Espo is on the other side, empty if this is the trial, or already in use if this is a real run. In both cases the morning question is the same. What would happen if the run started now, and what will not happen anyway, because the lever is down.

The answer sits on three sheets. It does not sit on a query.

The first sheet is the preview. It counts the whole run and does not write. It says what would be born, what would change, what would stay as it is, what would be rejected. A VAT number already present is seen before the POST.

The second sheet is a brake that can be pulled. Read mode, on one integration, and the global write switch, on the whole engine. A run in read mode reads, compares, and does not send the POST. The global switch stops every write toward Espo. These are not the four switches of the trial. They are the brakes to use when one wants to look at a run that, by default, would have permission to write. Read mode is born off. The global switch, if nobody has cleared it, leaves writes allowed. Pulling them is a choice. Leaving them is the other choice. Neither one is a fault.

The third sheet is the list of what the trial does not raise. Write-back stays at zero until a person turns it on, and even then it touches only the named columns. The retry queue stays off until the setting `retry_queue` is `1`. The portal filter stays off until the rule is read as enabled. The seal stays absent until the variable `NESSO_SECRET_KEY` is in the process: the trial does not set it, and the connection password stays in clear text in the local SQLite volume. Saying these four things to the person who receives the trial is part of the handover. They are not footnotes.

Undo comes after, not before. It goes back on what the run wrote. Before the first write it has no run to undo. That is worth knowing now, so nobody looks for it in place of the preview. The preview is the look. Undo is the return, and the return exists only where a write has happened.

## The file, still sitting still

It helps to keep the rows in view, because the switches are judged on a row, not on a slogan.

C001 is not yet an Account. The preview counts it among what would be born. The name Nord Est and the city Trieste are the values the file carries. The key that would be born is the one from the second chapter: the integration id, a colon, C001, on the field the entity already has. Until the POST starts, that key is not on Espo and it is not in the engine memory as a synced row. The preview does not create it in order to see the effect. It describes it.

C014 has already been seen, in the story, and the hash of the row is the one that was saved. The preview counts it among what would not change. It does not prepare an update. It does not prepare a second send. A run that later started for real would do the same, for the reason in the second chapter: same hash, status already aligned, Espo is not called. The point here is earlier. The count of "would not change" is still a count, and it is not a write.

The row without a required column does not let the file through halfway. The reject is at file level. The file does not move to `elaborati`. The preview reports it as a reject, and it does not repair the file in place of the person who put it there. An empty external id is a file-level reject, and later it will be clear that the retry queue, even when on, does not take it. When off, it takes nothing.

The salesperson's note is on the record, if the record already exists, and it is empty on the file, or the file would bring another text. The owner is Espo. The third chapter said the run does not clear it. This chapter adds only the boundary of the return: off, write-back does not copy that note onto the file. They are two different protections. One keeps the field on Espo. The other does not rewrite the source. Both, in the trial and in an installation that has not decided otherwise, are the default behaviour.

None of these rows needs an off switch to be "repaired" before it can be understood. The file is read. The preview counts it. The POST waits for a person, or for the cadence, once the person has decided that the run may write.

## The preview

The preview counts the whole run without writing. The count is what a person reads before saying yes: how many rows would be born, how many would change, how many would stay as they are, how many would be rejected, and whether a close of records that disappeared would be waiting for confirmation. The dangerous rows, when there are any, carry today's value and the incoming value. They are the contrast that the third chapter puts in the queue to look at, shown before anyone writes it.

The preview does not move the CSVs. A file that is still in the inbound folder stays in the inbound folder. It does not end up in `elaborati` only because someone asked for the count. The preview does not advance the cursor. An outbound run does not consume the records only because it counted them. The cursor is the memory of the second chapter, and it moves when a send has succeeded, not when a count has been read.

The dry run is the short sibling of the same brake. It reads at most five rows and returns the mapped body, or the reject of that row. It does not write to Espo. It is there to see the shape, not the total. Whoever confuses the five rows with the whole run stops too early: a duplicated VAT number can sit on the sixth row. The preview is the count of the run. The dry run is a sample. Neither one is the POST.

A VAT number already present is seen first. If the fiscal field of the row is already on another record of the same entity, the engine says so before creating. The sentence is the one of the field: VAT number or fiscal code already present. In the preview that sentence enters the count of the rejects. The record that already exists stays as it is. The new record is not born. There is no creation POST just to try, and there is no POST that is then deleted. The look is a read. The write has not started.

This order matters on Monday, when a customer-master file repeats a VAT number that a salesperson already loaded by hand on Friday, with another key. Without the preview, the first sign would be a reject in the journal, after the run. With the preview, the sign is before. The person who checks can stop, can correct the file, can decide that the row must stay out. The run, if it then starts, meets the same check before the POST. The preview is not a softer rule. It is the same rule, without the write.

On the activation plan, the preview has a second use, a narrow one. A plan orders integrations that are already saved. The next step can be turned back on only if the previous one was confirmed after its preview, and it does not turn on by itself. Confirming does not turn on the step after. An integration outside the plan is paused and turned back on as before. The plan is not one of the four switches. It is the order in which one says yes. The sentence that blocks a premature yes is simple: the preview has to be seen first.

A webhook, until the external system calls, has no rows to read. The preview says so, and it does not invent a body. The dry run, if an example is pasted into it, interprets that body and does not write. They are still looks. The first real POST remains a separate gesture.

## Read mode and the global switch

Read mode sits on the integration. It is turned on with an explicit gesture. A run started while it is on reads, compares, and does not send the POST. The comparison is the one of the preview: what would be born, what would change, what is unchanged, which reject there would be. The difference is that the run is there, in the journal, as a read. The status is `lettura`. It is not a preview asked by hand and then forgotten. It is an execution that chose not to write.

Read mode does not go back to writing by itself. Leaving it is a second gesture, the one that turns it off. A number of hours can be written beside the integration, as a noted deadline. That deadline is not a postponed POST that starts on its own when the time is up. The brake does not release itself. Whoever pulled it releases it, or leaves it pulled. Both are visible on the card.

The global switch sits on the engine, not on one integration. When it is stopped, every write toward Espo stops. It covers the customer-master run and an outbound run, "Run now" and the scheduler. The preview and the dry run remain. One can still count. One cannot yet write. It is the brake to pull when the doubt is not about one file, but about everything the engine might send this morning.

The two brakes add up. If the global switch is stopped, an integration that is not in read mode does not write either. If the global switch allows writes, and one integration is in read mode, that integration does not write, and another integration, not in read mode, may write. The global brake is one. Read mode is per integration. Knowing which of the two is pulled avoids a morning in which one believes everything was stopped and only one card was stopped, or one believes one card was stopped and the engine was stopped.

A held run is not a failed run to be retried by the queue. It did not send the POST. It does not have an HTTP failure to put back in line. It has a count. When the brake is released, the next run is a new run, with the usual rules: hash, field owner, VAT already present, cursor. It does not complete the earlier read as if the read had left a send half done. The read does not leave a send half done. It does not start one.

## Undo

Undo goes back on what the run wrote. The memory is the field history of that run: the previous value and the written value. For each record that was touched, the engine reads the current value again. If the current value is still the one the run wrote, it puts back the previous one. If someone changed it afterwards, that field stays as it is. The answer says how many fields went back and how many were kept.

The limit is the point. Undo is not a journey through the time of the whole of Espo. It does not delete the record. It does not close the record. It does not put back a note that a person rewrote after the run, because that note is no longer "what the run wrote": it is what the person wrote afterwards. The third chapter separated the close from the delete. Undo is a third gesture again: the return of the fields of the last run, where the record is still in the state the run left them in.

Before the first write, asking for undo has no object. There is no run to undo. The answer is that, not a preview in disguise. Whoever wants to see without writing uses the preview or read mode. Whoever has written and wants to go back uses undo, and uses it while writes are allowed. Undo is itself a write toward Espo: it puts the previous values back through the APIs, not through a query on the tables. If read mode or the global switch is holding writes, undo does not start. The brake that prevents the POST also prevents the POST of the return. To undo a run one must first allow writes to exist, and then ask for the return. The order is intended. A pulled brake must not be able to write "only to fix things".

Undo looks at the last run that left history, not at a run chosen from the week. It is not a record editor. It is not the conflict queue, where an Espo owner kept the person's value and the file's value waits for an eye. That queue is settled field by field, keeping Espo or keeping the source. Undo puts back, in a block on the fields that are still intact, the previous state of the last run. They stand next to each other, and they are not the same lever.

## Four switches, left down

The brakes above are pulled when one wants to look or when one wants to undo. The four switches in this list are another family. They exist. In the trial they are down. In an installation that has not yet decided, they are down. Raising one changes the run. Leaving it down does not take away the run's ability to read, to compare and, when writes are allowed and read mode is off, to send the POST of the rules already chosen.

The first is the seal. Without `NESSO_SECRET_KEY` the connection password stays in clear text in the SQLite file of the local volume. The trial does not set the variable.

The second is the retry queue. The setting `retry_queue` is not `1`. A run that rejects a row does not write it a second time through the queue.

The third is the portal filter. The rule is null or off. Outbound does not change the select and does not change the record list. It does not call Espo's portal or role APIs, and it does not create portal users.

The fourth is write-back. The default is zero. When on, it updates only the named columns. It does not rewrite the whole file. It is not the outbound HTTP cursor.

The rest of the chapter walks them one by one, then says what a person sees on the page, and then returns to tonight's file with the four levers still down. There is no fifth hidden switch that turns them on for the demo. The demo in the manual, Gruppo Meridia, is the proof of a run. It is not a second product and it is not a customer published on this site. It is not there to raise these levers.

## The seal, and the trial that does not set it

A connection's password lives in the `config_json` of that connection, in the SQLite of the local volume. It is the password of the external database, or the other secret that the connection kind keeps. It is not the password of an Espo user, and it is not a secret to be sent into the journal. Without the variable `NESSO_SECRET_KEY`, that value stays in clear text on the volume. Whoever can read the volume file can read the password. It should be said to the person who receives the trial, with the same calm used to say where the file folder is. It is not a surprise to discover on Tuesday.

The trial does not set the variable. Docker Compose starts the database, an empty Espo, and the engine. It does not, on its own, add the key of the secrets. The volume of this trial stays in clear text. It is not a slip of the compose file to be quietly fixed inside an image. It is the published behaviour: until the person who installs puts the variable in the process, new saves are not sealed.

With the variable present, a new save is sealed. The value in the file carries the prefix `enc1:`. The public connection page does not show the text and does not show the seal. In place of the password there is the sign that a password is there, not the password. The configuration export does not receive the secrets: no passwords, no tokens, no header values, and no seal to copy into another file in the belief that it is the password. The export is the shape of the connections and of the integrations, to be reviewed. It is not a backup of the secrets.

A row already in clear text still opens, if the variable is there. The engine knows how to read the text that does not have the prefix. Putting the variable in place is not a run that walks the old connections and seals them by itself. A new save, made while the variable is there, is born sealed. The old row, for as long as it remains that row, opens. They are two facts, and they stay distinct. Mixing them would make one believe that turning the key on has already protected the volume, while the volume still has the previous row, in clear text.

Removing the variable after a save has been sealed has the opposite effect, and it should be said before removing it. That connection does not open until the password is typed again. The seal without the key is not a password one can guess. It is a value the engine refuses to open. The page, in that case too, does not show the seal as if it were a clue. Whoever removed the variable must have the password from somewhere else, and must type it again. There is no "show the secrets" switch on the public page.

The export stays without secrets both when the volume is in clear text and when the volume is sealed. The handover page, in turn, contains no passwords. They are three different surfaces. The volume is the place where the secret sits, in clear text or sealed. The connection page is the place where one configures, without seeing the secret. The export and the handover are the places one can pass to another person, and they do not carry the secret with them. Whoever receives the export will have to put the passwords back. It is the passage from trial to operation: secrets and addresses are removed, and nothing is saved until they are reviewed.

The seal does not choose the channel. It does not turn write-back on. It does not set the retry queue to `1`. It does not turn the portal filter on. It is a process key, for the secrets of the connections. The rest of the run, with or without it, obeys the other levers. The trial, by not setting it, asks the person who installs to know that the volume is in clear text, and to decide whether, outside the trial, the variable should be there. Deciding not to set it on a volume that others can read is not the advice of this chapter. The fact of this chapter is narrower: the trial does not set it, and a new save is sealed only when it is there.

## The retry queue, off

The setting is called `retry_queue`. Off means the value is not `1`. In that state the engine, when it rejects a row, writes the reject and does not write a second queue row. The run that rejected it does not write a second time through the queue. There is no `next_at`. There is no deferred attempt. The reject stays where rejects stay. The next run, if the cadence provides one, will read the source again, with the usual rules. Not because a queue put it back in motion. Because the run started again.

This is the default, and it is the default of the trial. An error on one row is not, by itself, an invitation to write it again in a minute. On Monday morning, if Espo refused a row, the journal has the row. The queue has not prepared another one. Whoever expected a second automatic POST and does not see it is not looking at a hole. They are looking at the switch down.

When on, the queue does one thing, and it does it narrowly. It requeues only an inbound row that has a non-empty external id. The identity is the column the second chapter uses for the key. Without that value, there is no row to retry: there is a file-level reject. The file-level reject does not enter the queue. An empty identity column does not become deferred work. The file is to be fixed, not postponed.

The retry does not happen in the same cycle. When the queue is on and the identity is there, the row is born waiting with `next_at` at least one minute ahead. `retry_wait(0)` is one minute. The run that has just rejected it does not pick it up again before closing. There is no second POST "right away, since the queue is on". The minute is the minimum. The cycle that rejects is not the cycle that writes again.

HTTP outbound does not use this queue. The outbound cursor already retries the record that did not leave: it stays on the last POST that succeeded, and the next run sends what had not left. Sending the outbound again from the queue as well would count the same failure twice, with two clocks. The queue does not do that. The detail of the cursor is in the second chapter. Here it is enough not to look for it in the retry queue, and not to turn the queue on "to make outbound start again". Outbound starts again from the cursor, with the queue off or on in the same way.

When a queue attempt fails, the attempts increase and `next_at` moves further out. The wait, in minutes, is the minimum of two to the power of the step and `24` times `60`. The step does not go past `10`. At the start the step is zero, and the wait is one minute: two to the power of zero is one, and one is under the ceiling. At the next failure the step is one and the wait is two minutes, then four, then eight, then sixteen, then thirty-two, then sixty-four, then one hundred and twenty-eight. After eight attempts the status of the queue row becomes `scarto`. It does not stay waiting forever. Eight is the end of that queue row, not a rounding. The ceiling of one day, `24` times `60` minutes, sits in the formula together with the step that stops at ten. The formula is this one, even when the eight attempts arrive before that ceiling. One does not derive from it a ninth slot "as a courtesy".

A success marks the queue row as `fatto`. It does not put it back to waiting. It does not delete it to make it look as if it had never been born. `fatto` is the sign that the retry wrote. The journal of the run stays the journal. The queue row does not replace it.

When off, none of this calendar exists. There is no `fatto` to look for, and there is no queue `scarto` after eight attempts, because the queue attempts never started. The reject of the run is there, in the reject table, as it was before the queue existed as a switch. The off default means one practical thing: the rejecting cycle does not write a second time through the queue. Whoever wants the calendar must set `retry_queue` to `1`, knowing that the first retry is at least one minute later, that an empty identity does not enter, that HTTP outbound does not enter, and that at the eighth attempt the queue row is `scarto`.

Two rows of the file, so the formula does not stay abstract. C001, if the POST fails and the identity is there, with the queue on would wait at least one minute and then try again, with the wait growing, up to eight attempts. With the queue off, that failure stays a reject of the run. C014, if it is unchanged, is not a reject and does not enter the queue either on or off: there is nothing to retry. The row without an identity does not enter the queue even when the queue is on. Tonight's file, on the trial, meets the off version.

## The other clock, after an error

There is a second clock, and it is not the queue. After an error the scheduler waits the full interval. `last_run` is updated on the error branch, and the next attempt of the integration is measured from there. If the cadence is one hour, the hour starts again from the error. Not from the moment the integration was tried the time before, and not from one minute. Only with `retry_failed` set to `1` does the clock stay still: the previous `last_run` does not move, the status becomes error, and the run can present itself sooner, because the interval is still counted from the old time.

The default is the full wait. `retry_failed` is not `1` unless someone has set it. The trial does not raise it to compensate for the queue being off. They are different settings. The queue, when it is there, concerns an inbound row with an identity. `retry_failed` concerns the clock of the whole integration, after an error of the run. Turning one on does not turn the other on. Turning one off does not turn the other off. On Monday, if the run fell, the question "when does it start again by itself" is answered with the cadence and with this clock, not with `retry_wait`.

Keeping the full interval is the choice against hammering. Espo not answering, a SELECT that fails, an exception in the run: the journal has the error, the clock moves, and one waits. Whoever is awake at seven reads the journal and decides whether to launch "Run now". "Run now" is a person's gesture. It is not `retry_failed`. Pause, in turn, is yet another lever: the scheduler and the webhook skip an integration that is paused, "Run now" does not. None of these levers is the retry queue.

The same integration does not start twice. If a run is already in progress, the second receives that a run is already in progress. The scheduler, in that case, skips it and does not write an error every thirty seconds. Two different integrations can run together. The detail of this constraint is in the second chapter. It enters here for one reason only: an error must not become two overlapping runs of the same rule, and the error clock is not a permission to overlap them. The brake on a double start remains, with the queue off and with the queue on, with `retry_failed` still and with `retry_failed` at `1`.

## The portal filter, off

The filter lives in `portal_json`, on the outbound integration. Null, or read and not enabled, it does not change outbound. The select is the one from before: the fields of the mapping, together with `id` and `modifiedAt`. `teamsNames` is not added for this filter. The record list is the list from before. A record of the Sales team and a record of the Purchasing team both leave, if the cursor says they must leave. The filter has not distinguished them, because the filter is not in function.

It does not call Espo's portal APIs. It does not call the role APIs. It does not create portal users. An outbound of Lead or of Account does not become, merely by existing, an invitation to the portal. The portal roles, on Espo, stay the ones an administrator put there. Nesso does not change them. This holds when off, and it holds when on: when on, the filter chooses which records leave, and it does not rewrite the roles.

When the rule parses as enabled, outbound adds `teamsNames` to the select. Then it skips the records for which `portal_visible` is false. The function is narrow. If the rule is missing or is not enabled, the record is not skipped by this filter. If the rule is enabled and the record's entity is not the entity of the rule, the record is not visible for outbound. If the rule names a team and that team is not among the record's teams, the record is not visible for outbound. A record of another team does not leave. The cursor stays on the last record that left. A team change, on Espo, updates `modifiedAt`, and the record can be read again on the next run. The filter does not keep a second memory of the teams. It reads what outbound asked for.

There is an exception the filter does not take for itself. A missing external key still stops the pull. The filter does not turn that stop into a silent skip, and it does not let the records after continue as if the key were there. The second chapter owns the detail of the cursor that stops. This chapter says only that turning the portal on does not remove that stop. The portal rule and the missing key do not trade jobs.

When off, the select and the record list are unchanged. There is no "default" team applied in secret. There is no empty portal created for the trial. Whoever expected outbound to speak the language of portal roles, and sees the records leave without that filter, is seeing the lever down. Raising it is naming the rule and having it enabled. It is not a flag inherited from the name of the integration, even if the name says "portal". The name is not the rule. The rule is `portal_json` read as enabled.

## Write-back, off

`write_back` is born at zero. Until a person sets it to one, the run does not update the source. The night file stays the file that arrived. A SELECT stays a read. The external database does not receive an UPDATE merely because Espo has a newer value, or a value the file did not have. Off, write-back does not touch the source.

When on, it touches only the named columns. The list is `write_fields`. A column that is not named does not enter the update. It does not rewrite the whole file. It is an update of the columns someone wrote in the list.

It is not the outbound HTTP cursor. The cursor remembers the last record sent out of Espo toward an outbound connection, and it advances after the POSTs that succeeded. Write-back, when one day it is on, is the other direction: from the memory of what Espo has, toward named columns of the source. An inbound integration does not become an outbound because the return was turned on. The connection stays what it is. The return is one more decision, on the same rule, and by default it is not there.

On the customer-master file the difference is touched with the note. The Espo owner keeps the note on the record. Write-back, off, does not write that note into the cell of the file. If one day the return is turned on and the named column is the city, and only the city, the note still does not leave. Naming is the only list. "Everything Espo knows" is not an entry in that list.

The return does not choose the channel, does not create users, does not turn the queue on, does not turn the portal on, does not set the secrets variable. It is a lever on the integration. The trial leaves it at zero. An installation that copies the trial without reading the lever leaves it at zero, and does well until someone has decided which columns come back. Deciding the columns is the work. The switch without columns is not a return.

## What does not move, even with the levers down

Some boundaries are not switches of this chapter. They remain boundaries, and they are worth naming here because an off switch is often mistaken for one of them, or one of them is looked for among the switches.

CRM mail stays in Espo. Nesso does not become the program that reads the mailbox and does not become the program that sends the CRM's mail. A retry lever, a portal lever, or a return lever does not "include the mail" when it is raised. Espo's mail stays configured where it is. The engine, if one day it has a mail of its own, will be another thing, hooked to its own sending, and today it is not the customer-master run.

The Advanced Pack is not rewritten. It is not in the repository. If someone has it locally, it stays local. The engine does not publish it and does not copy it together with the data. Turning the portal off is not a way of keeping the Advanced Pack out: the Advanced Pack is already out. Turning the portal on does not bring it in.

No SQL on Espo's tables. The brakes of this chapter stop POSTs, or they avoid UPDATEs on the external source. They do not open a side path on Espo's database "to read faster" or "to fix by hand". Reading an entity is a call. Writing an entity is a call. When the write call does not start, it does not start. It is not replaced by a query.

Production dumps do not enter the trial. The Espo that Compose starts is empty. A backup is not mounted, the attachments are not copied, a company's real history is not used as development data. The off switches are not a substitute for this rule. Even with the four levers raised, a production dump is not a step of the trial. The trial is empty before any lever.

Espo users are not created from a master. A file of people is not a file of logins. The portal filter, even when on, does not create portal users. The seal does not create users. The contacts recipe prepares a mapping toward Contact, to be reviewed, and it does not create the users those contacts might one day become. Creating a user is an administration gesture, with a password and a role. No lever of this chapter does it in place of that gesture.

## The mapping proposal, and the columns still empty

Before the POST there is the mapping, and the mapping has its own brakes. They are not the four switches. They are the reason a mapping is not born by itself while one looks at a column.

Propose the mapping reads the column names, in the language of the page. The synonyms are a list, per language. A column whose name looks like a VAT number can propose the fiscal field, if the entity has it. A column that is not recognised stays empty, to be filled by hand. The proposal does not go out on the network. It does not save the integration. The person reviews, changes what does not fit, and then saves. The save is the yes. The proposal is the sheet before the yes.

Fill empty columns calls a model only if an address is set. Without an address no call starts, and the synonym proposal remains. With the address, the call fills only the columns that are still empty, among the fields the entity already knows. It does not touch a column that is already mapped. It does not save the integration. It does not send the connection password. It sends the column names, at most three short cells, and the field name. The model address does not enter the configuration export. Whoever passes the export to another person does not pass them, along with it, the model address.

The model does not choose the channel. It does not create the entities. It does not turn write-back on. It does not set `retry_queue` to `1`. It does not turn the portal filter on. It does not set `NESSO_SECRET_KEY`. A column proposed well is not a raised lever. It is a mapping row, still to be saved, still to be passed through the preview.

The language of the proposal is the language of the page. The page can be in Italian or in English. The synonyms of one language do not cancel the other: an Italian column name and an English column name can propose the same field, each from its own list. The journal, by contrast, stays in the language of the run. If the run started in Italian, the journal sentences stay in Italian even if in the afternoon the page is opened in English. They are not translated afterwards. The journal is the record of the run. The proposal is a help before the save. They are not exchanged.

## The recipes, to be reviewed

Accounts, contacts, sites, and price list are four starting points. Each prepares a mapping. None is a certified connector. The name of the system on the other side is not written in the program, and it is not written in the recipe. The recipe says: this entity, these columns, this identity. The person reads and can change the rows before saving. The recipe does not save the integration by itself.

Accounts prepares Account, with the identity on the code column and with the fields a customer export already has, including the VAT number if the field is there. Contacts prepares Contact: code, first name, last name, email, phone, and the company looked up by name on Account. Sites prepares the shipping address on Account, one site per company, only if the field is already there. None of these recipes creates the entity. If the field is not there, the mapping row does not invent the field to make the recipe come out even.

The price list points at the Product entity. The rows are description, code, price, and currency, only if the field is already on the entity. It does not create Product. In the trial, if Product is not there, the price-list fields stay empty. It is a visible empty. It is not a phantom catalogue created to fill the preview. Whoever wants the price list has the entity on Espo first, then the recipe, then the review, then the preview. Skipping to the POST is not a step of the recipe.

A recipe does not raise the four switches. It does not put write-back on the columns it named. Naming a field in the mapping toward Espo is not naming it in `write_fields`. It does not turn the queue on. It does not turn the portal on. It does not seal the volume. After the recipe, the trial is still the trial from before: four levers down, and a mapping to read.

## The trial, the clone, the handover

The trial is taken by cloning the public repository, `https://github.com/nessocrm/nessocrm`. There is no installer to download separately. There is no form that asks for an email address. There is no waitlist. The contact is the repository. Docker Compose starts the database, an empty Espo, and the engine. The first time the work is that: build, wait until Espo is up, open the page. Production dumps are not a step of that work.

The handover page lists the addresses, the integrations, the cadence, the owner of each field, and how writes are stopped. It contains no passwords. It contains no tokens. It does not contain webhook or inbox addresses as secrets to paste into a message. The person who hands over passes that page, and passes by voice, or by a channel that is not the export, the passwords the export removed. The handover page is not the export, and the export is not the volume. Three objects, already said about the seal, and repeated here because the handover is the moment one discovers whether someone expected to find the password written at the bottom.

The journal stays in the language of the run. The page can be in Italian or in English, and the choice belongs to the page. A run launched from a page in Italian leaves sentences in Italian. Opening it later in English does not rewrite them. The scheduler speaks the language in which it was set. Whoever reads an error at seven must read the sentence the engine wrote. This journal, unlike the run journal, exists twice, in Italian and in English, because it is an explanation. The two texts say the same facts. They do not promise that the run journal will do the same.

On the trial, before the first POST, a person can do this, and this alone is already the run of this chapter. Save a connection, knowing that the password stays in clear text on the volume. Ask for a recipe, or propose the mapping by synonyms, and do not treat as saved what has not been confirmed. Look at the preview. If one wants an execution that does not write, turn read mode on, or stop the global switch. Read the count. Leave write-back, the queue, the portal, and the seal down, until there is a reason to raise one of them, and the reason is not "let us see what happens".

## Gruppo Meridia, and the two runs

In the manual, Gruppo Meridia is the proof of a run. It is there to see the shape of a load, with entities and teams, inside a trial Espo. It is not a second product, beside Nesso, to be installed under another name. It is not a customer published on this site. Naming it in the journal is a way to take it off the list of things this chapter would have turned on. It did not turn the four levers on. It does not turn them on for whoever clones the repository today. Whoever looks on the site for a commercial case under that name does not find it, because that is not the use of the name. The use is in the manual, as a proof.

The same integration does not start twice. Two different integrations can run together. The second chapter keeps the detail: the second start of the same one receives that a run is already in progress, and the scheduler does not fill the journal with that error every thirty seconds. In this chapter the sentence is there so the brakes can be read without mixing them. Read mode is per integration: one can read while the other, if writes are allowed, writes. The global switch is not like that: stopped, it writes neither of the two. The retry queue is a setting of the engine, one for all the runs. The seal is a variable of the process, one for the saves of the connections. Write-back and the portal filter sit on the integration, and they can differ between the customer masters and an outbound. Two runs together do not fuse these levers into one lever.

## Monday, with the levers still down

At seven the file is there. Whoever watches the number on the home does not yet have a success of today to show, if the run has not started. The preview does not manufacture one. A count without a POST does not move the last success and does not turn off an expected-file edge. The number stays a check. It does not turn green because someone looked.

Whoever has the note opens the record, if the record was already there, and the note is still there. The run has not started, or it started in read mode and did not send the POST. In both cases write-back, off, has not copied the note onto the file. The Espo owner and the off return have worked in the same direction, for different reasons. The badge, if the run did not write, has no new origin to show. The third chapter says what the badge means when the run writes. Here the badge is not called on to cover a preview.

Whoever checks opens the preview and reads the counts. C001 among the births. C014 among the unchanged. The file-level reject, if the column is missing, in view, without the file having been moved. The VAT already present, if it is there, in the count of the rejects, before any POST. If the counts hold and writes are allowed and read mode is off, "Run now" is the first POST. If the counts do not hold, the POST is not the next step. The next step is the file, or the mapping, or the decision to leave the brake pulled.

Whoever installs, the same morning, can say four noes. No, the password is not sealed, because the trial does not have `NESSO_SECRET_KEY`, and it is in clear text on the volume, and it is not on the handover page. No, the rejected row will not be written again in a minute by the queue, because `retry_queue` is not `1`. No, outbound is not filtering the teams, because the portal rule is not enabled, and the portal roles on Espo have not been touched. No, the file has not been updated in return, because `write_back` is zero, and it would not be an update of the whole file even if someone named some columns. Four noes are the handover. They are not four excuses.

If the run then starts and falls, the clock waits the full interval, unless someone has set `retry_failed` to `1`, which the trial does not do on its own behalf. The full wait and the off queue add up. They do not cancel each other. The journal has the error, in the language of the run. The person reads that sentence. Not a translation made afterwards, and not a second POST started by the queue that is not there.

If the run then starts and writes, and the write is wrong, undo goes back on what that run wrote, on the fields nobody changed afterwards. It does not turn on the return toward the file. It does not seal the volume. It does not queue the rows. It does not filter the portal. Undoing a POST does not raise the levers the POST did not use.

## The same run, in the order of the page

It helps to read the facts again in the order a person meets them, because the order is part of the brake. One meets first what does not write, and afterwards what might write, and for the whole time the four levers stay where they are.

The connection is created. If it is a database, a SELECT, an address, a user, a password. The save that lists the columns has already run the read. The password, on the trial, ends up in clear text in the volume. The connection page, straight after, does not show it. The export, if it is taken now, does not contain it. None of this has written to Espo.

The entity is chosen. Account, for the customer-master file. The recipe is asked for, or the mapping is proposed. The recognised columns receive a field. The others stay empty. If one asks to fill the empty ones and the model address is not there, no call starts. If the address is there, only the empty ones are filled, without saving and without sending the password. The person confirms. Only then is the mapping saved. Write-back is still zero. The queue is still off. The portal is still off. The seal is there only if the variable was there at the save of the connection, and on the trial it was not.

The preview is looked at. The count of C001, of C014, of the reject, of the VAT if it is already present. The CSVs do not move. The cursor does not advance. If the activation plan has this integration as a step, the step can be confirmed only after this look, and the next step does not turn on by itself.

The brake is decided. Read mode, if one wants a run that compares and does not send the POST. The global switch, if one wants every write toward Espo held. Or neither, if the count holds and the POST is wanted. The POST, when it starts, is the POST of the rules already written in the earlier chapters: key, hash, owner, empty cell, close only with the confirmations the third chapter described. It is not a POST widened by the levers of this chapter, because those levers are down.

If an inbound row with an identity is rejected, the reject stays a reject. The queue does not pick it up a minute later. If the identity is empty, the reject is at file level and would not enter the queue even with the queue on. If the error is of the whole run, one waits the interval, because `retry_failed` is not `1`. If outbound is another integration, its record list is the whole list the cursor allows, without `teamsNames` added for a filter that is not there, and a missing key still stops the pull. If someone looks in the night file for the salesperson's note, they do not find it written back.

If, after a POST, one wants to go back, undo uses the history of that run. Then the levers are still down. The chapter ends in the same state in which it began, with one difference only, and it is intended: the person saw the count before writing, and can say what did not start.

## What this chapter did not turn on

It did not put `NESSO_SECRET_KEY` in the trial, and it did not rewrite the rows already in clear text. It did not set `retry_queue` to `1`, and it did not make the rejecting cycle write twice. It did not turn `portal_json` on, and it did not call Espo's portal. It did not set `write_back` to one, and it did not rewrite the file. It did not set `retry_failed` to `1`, and it did not shorten the wait after an error. It did not start a POST from the preview. It did not save the mapping proposal. It did not let the model choose the channel. It did not certify the recipes. It did not create Product because the price list had empty fields. It did not import a dump. It did not create users from a master. It did not move the mail out of Espo. It did not publish the Advanced Pack. It did not make Gruppo Meridia a customer of this site.

Tonight's file, at the end of this chapter, can still be a file. It can also have been written already, if the person saw the preview and said yes: in that case C001 is an Account, C014 was not rewritten, Espo's note is still Espo's, and the four levers are down all the same. The yes of the POST is not the yes of those levers. They are different yeses. The product keeps them separate so that on Monday morning one can say which of the two was said, and which was not.

An off switch can be read. It is read on the card, in the setting, in the absence of the variable, in the preview count that moved nothing. It is not inferred from a success. A run that went well with the levers down is the run of the earlier rules, plus the brakes that were not pulled and plus the switches that were not raised. It is the run the trial hands over. Whoever receives it also receives the duty to know that the password is in clear text, that a reject does not write itself again, that outbound does not filter the portal, and that the source is not updated in return. Knowing this is the chapter. Raising a lever, when it is needed, will be another morning, and it will still be a choice.
