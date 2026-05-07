# Problem Statement: How might we help frontline staff capture important information quickly and reliably in the moment, without disrupting the interaction?

## Query regarding initial referral information: 
Location and appearance could initiate unique id in db. Referrals can come from the police or general public.

## Information gathering on meeting the potential client: 
### Questions to answer on meeting the client:
* Establishing identity without scaring the client off in terms of formality and reliability of self identification. Possible the police may already have passed on a name if the person is known to them.
* Reliability of internet connection for cloud syncing data, local storage on device also?
* ensure quick accurate note taking ability while maintaining interaction with client 
* What is the most fundamental data they are aiming to capture in the first contact?

## Possible solutions:
Focused on capturing information on the frontline.
* Discussed recording the client interview and generating notes via ai and audio recognition.
    * Pro's: Minimally invasive, captures interview entirely.
    * Con's: Potential for client to be paranoid about it, ai generation mistakes and if discussion 'disjointed' potential to also capture useless information.
* Written notes via special 'pen' to pad contact driven or hand written then added to system via OCR and potential to photograph any medication client to carrying to hopefully a) identify medication and b) maybe the client and dr's surgery. Possible involvement for EPS (prescription tracker still being built), but long onboarding and would need to onboard to pds so questionable if we'd have a good enough case. May not be needed if the original medication sticker still carries the clients name.
    * Pro's: maintains the current 'low key' informal approach, but means that info added goes through the filter of an experienced volunteer
    * Con's: More onus on the volunteer to multi-task between talking to client and write down useful information, so no different to current - but good opportunity to at least reduce duplication.
* Using barcodes on medication: identifies medication, but not universal yet.
* Photographs/videos of client: could be useful, but might make the client jumpy. Would need to go with judgement of volunteers on that and probably go through the other methods outline to get their 'feel' of what would work best.
* Using 'what3words' for location tracking, which tracks down to a meter. Could be good, other potential solutions include PostGIS - postgresql implementation of geospatial data. The aim for either technology would be to map any pattern client has and build up picture of a series of locations of where they are most likely to be on a given day/time.
