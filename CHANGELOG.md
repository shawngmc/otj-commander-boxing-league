## TODO:
- Set Stats
  - Convert Std Set Stats query to use Imported Scryfall
- Card View
  - Use [animate.css](https://animate.style/) to add a card flip animation
  - Handle Adventure cards properly (dual face, only one image)
- Deck Analysis
  - Add Color Identity Check Button to Draft/W2/W1 decks
- Preprocessor
  - Cleanup old CSVs and cached json automatically
  - Add oracle text and keyword tagging
- Git Repo
  - Backup Spreadsheet Content in repo
  - Backup Decklists in repo
- Miscellaneous
  - Find a way to automate dual-commander strategy summaries
  - Find a way to integrate scryfall 'tagger' data?

## 2024-05-22
- Pool Management
  - Actually adds or updates rows
  - Rebuilds the Pool sheet filter
  - Better behavior on the set dropdown 

## 2024-05-21
- Preprocessor
  - Added GH Action to generate card DB as a release
- Pool Management
  - Added Set Selector

## 2024-05-20
- Pool Management
  - Started New View
  - Allows Card Lookup via Autocomplete
  - Shows Count
  - Passes card back to be added

## 2024-05-17
- Card View
  - Interject MTG symbols in Oracle Text
  - UI Cleanup - center error, remove reload button

## 2024-05-16
- Card View
  - Added Click or 'R' to reload while sidebar focused
  - Added loading indicator and preload logic
  - Now loads all cards at start, but card selection turnaround is MUCH faster
  - Fixed padding

## 2024-05-08
- Card View
  - Switched to Roboto Font
  - Flip is now a separate button
  - Flip now changes type/ability text
  - Refresh button is cleaner/more convenient
  - Some rearranging to keep visual position consistency
  - Fixed bug where selected card of 'name' was treated as a card
  - Added Mana Cost using symbols from Scryfall API: https://scryfall.com/docs/api/card-symbols/all
  - Moved links to the bottom, changed to icons


## 2024-05-07
- Decks: Added Color Identity Check (need Button added in Draft/W2/W1 decks)
- Created OTJ Boxing League GitHub repo
- Preprocessor: Now uses Scryfall bulk_data API endpoint from the docs (https://scryfall.com/docs/api/bulk-data), with caching of actual downloaded file
- Preprocessor: Preserves double-faced card data
- Card View: Click to flip image 
- Git Repo: Added Apps Script
- Apps Script: Initial lint/cleanup pass

## 2024-05-06
- Sidebar: Added external links
- Sidebar: Added reload button
- Pool and Deck Sheets: Force CMC to be numbers with VALUE() to make math work
- Decks: Added Commander Field w/ Color Identity Calculation
- Pool/Decks: Replaced Score column with Color Identity to enable Color Checks, etc.
- Commanders Removed from Draw Pool

## 2024-04-29
- Added a card view sidebar
- Card view sidebar loads images
- Card view sidebar only redraws if card has changed
- Card view sidebar only does one server request at a time
- Card view selected card lookup starts on selection, not sidebar polling, to reduce wait
- Sidebar event chain is much faster by using TextFinder instead of a manual search
- Fixed issues where non-name values would match and cross-sheet refs

## 2024-04-28
- Pool: Calculate the 'Category' Column based on type and color_identity
- Added Commander sets since they can be in set boosters
- Fixed Battle Icons

## 2024-04-26
- Changed SetStats queries to write the data to the cells as direct trigger, not recalculate
- Add Neptyne to try Python out
- Updated import to add emoji
- Cleaned out old function implementations
- Changed draw cards to write the data to the cells as direct trigger, not recalculate
