# GitHub Upload Guide — PNC NORCET IBQ

Ye 25 .docx files GitHub par daalni hain taaki CMS ka runner inhe seedha fetch kar sake.
File picker ka jhanjhat khatam, aur galat file upload hone ka risk zero.

---

## Kya upload karna hai

Sirf ye folder: `H:\NORCET IBQs\DOCX_Output\Categorized_MCQs\_APPX_UPLOAD`

- 25 `.docx` files
- `manifest.json` aur `MASTER_PLAN.csv` bhi daal dein (record ke liye)
- `_superseded` folder **mat** daalein — wo purani do files hain jo merge ho gayi

Total size ~66 MB. GitHub ki free limit se bahut kam hai.

---

## Step 1 — Repository banao

1. github.com par login karein
2. Right top `+` → **New repository**
3. Repository name: `pnc-norcet-ibq`
4. **Public** chunein (Private rakha to raw URL kaam nahi karega)
5. "Add a README file" tick kar dein
6. **Create repository**

---

## Step 2 — Files upload karo

1. Repo khulne par **Add file** → **Upload files**
2. `_APPX_UPLOAD` folder ke **saare 25 .docx** select karke drag kar dein
3. Neeche commit box mein likhein: `Add 25 IBQ test files`
4. **Commit changes**

> 25 files ek saath mein thodi der lagegi (66 MB). Browser band mat karein.
> Agar 25 ek saath fail ho jaayein to 10-10 karke 3 baar mein daal dein.

Upload ke baad repo mein `ibq/` naam ka folder banana zaroori nahi — files root mein
rahengi to bhi chalega, bas neeche wala URL uske hisaab se badal dena.

**Agar aap `ibq/` folder chahte hain:** upload karte waqt commit box ke upar file name
ke aage `ibq/` type kar dein, ya folder ko hi drag kar dein.

---

## Step 3 — Raw URL check karo (ye step chhodna mat)

Repo mein `cardiac-ecg-rhythms-01.docx` par click karein → **Raw** button → jo URL
address bar mein aayega wahi pattern hai.

Aisa dikhna chahiye:

```
https://raw.githubusercontent.com/<AAPKA-USERNAME>/pnc-norcet-ibq/main/ibq/cardiac-ecg-rhythms-01.docx
```

Ab wo URL naye tab mein kholein — file **download honi chahiye**.
Agar 404 aaye to:

- repo Private hai (Public karein), ya
- branch ka naam `main` nahi `master` hai (URL mein badal dein), ya
- folder path galat hai

**Ek URL confirm hone ke baad mujhe apna GitHub username bhej dein** — main
`MASTER_PLAN.csv` ke saare 25 raw URLs bhar kar runner bana dunga.

---

## Naming rules (aage ke liye yaad rakhein)

- sirf lowercase, hyphen — space, `&`, bracket kabhi nahi (URL toot jata hai)
- ek file = ek test, kabhi bhi ek badi file per category nahi
- file ka naam badalna ho to pehle batayein — runner usi naam se fetch karta hai
