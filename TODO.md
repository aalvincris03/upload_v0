# TODO

## Goal
1. Gawing real-time at base sa aktwal na file size ang upload progress animation sa `templates/index.html`.
2. Alisin ang bounce animation sa pag-upload.
3. Pabilisin ang pagsisimula ng pag-upload.

## Steps (Upload Progress)
- [x] Mag-compute ng kabuuang laki ng lahat ng selected files
- [x] Palitan ang `fetch()` upload ng `XMLHttpRequest` (XHR) para sa real-time upload progress
- [x] I-update ang progress bar width batay sa `e.loaded / e.total`
- [x] Magpakita ng status text na may live na percentage at nag-a-upload na bytes
- [x] Panatilihin ang auto-refresh pagkatapos ng upload
- [x] Alisin ang fake/fixed na pag-usad ng progress bar
- [x] I-update ang CSS transition sa `0.15s` para smooth pero area-time

## Steps (Alisin ang Bounce Animation)
- [x] Alisin ang `@keyframes fileBounce`
- [x] Alisin ang `.uploading-file` CSS class
- [x] Alisin ang JavaScript na nagdadagdag ng `uploading-file` class sa mga selected file items

## Steps (Pabilisin ang Pagsisimula ng Upload)
- [x] Magpakita agad ng `Preparing upload of X...` na may 3% progress fill para hindi mukhang frozen
- [x] Alisin ang `setTimeout` delays (50ms) para agad mag-refresh at mag-reset ang button

## Steps (Consistent Display sa Reload)
- [x] Alisin ang server-side rendering ng files sa `index.html`
- [x] Palitan ng loading state container (`#filesLoading`)
- [x] I-update ang `renderFiles()` para rin alisin ang loading container
- [x] Tawagin ang `refreshFiles()` sa `DOMContentLoaded` para sa pare-parehong display ng files
- [x] Panatilihin ang sorting, delete, at iba pang features

## Steps (Professional Dark Modern Design)
- [x] Lakihan ang body container (`container-fluid` + `col-12`)
- [x] Dark modern theme (dark navy/slate background na may indigo/cyan accent)
- [x] Professional sticky header na may brand icon at subtitle
- [x] Modern upload zone na may gradient button at drop icon
- [x] Upgrade ang file cards (rounded corners, hover lift, file-type color accents)
- [x] Mas maraming columns sa grid (`col-xl-3 col-lg-4 col-md-6`)
- [x] Dark-adapted modal, dropdown, context menu, at scrollbar

## Steps (Compact Professional Upload Zone)
- [x] Liitan ang upload zone (mula full-bleed pataas gawing compact horizontal bar)
- [x] Horizontal layout: icon + title + file input + upload button sa isang row
- [x] Mas maayos na button/label hierarchy at spacing
- [x] Pinaganda ang professional look sa buong page

## Steps (Ilipat ang Toolbar Buttons sa Upload Zone)
- [x] Ilipat ang Create File, Refresh, Sync, Delete All buttons sa kanang bahagi ng upload zone
- [x] Alisin ang duplicate na buttons sa "Available Files" section (iiwan lang ang sort dropdown)

## Steps (Action Card sa Tabi ng Upload Zone)
- [x] Paghiwalayin ang upload card (kaliwa) at action card (kanan)
- [x] Gumawa ng bagong "Manage Files" action card na may Create File, Refresh, Sync, at Delete All
- [x] Panatilihin ang compact upload form sa kaliwang bahagi

## Testing
- [ ] (Manu-mano) I-test ang pag-reload ng page at i-verify na pare-pareho ang display ng files
- [ ] (Manu-mano) I-verify na gumagana pa rin ang sorting, delete, at iba pang features
- [ ] (Manu-mano) I-verify na nasa kanang bahagi ng upload zone ang toolbar buttons
