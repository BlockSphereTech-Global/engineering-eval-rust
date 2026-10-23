# 15min - timed skill test for Rust developer

Create your branch from the project root before you change any code:

```bash
git checkout -b John-david-1998-03-01
```

Run the current API from the project root and leave that terminal open:

```bash
cd backend
npm install
npm run dev
```

The API listens on http://localhost:4000.

## Task

The catalog is a list of property listings. Finish `select_listings` in `src/main.rs` so the program prints the residential listings a buyer would see when they ask for a modeled yield of at least 6.

Keep listings whose type is Residential and whose `yieldPercent` is at least 6. Sort by `yieldPercent`, highest first. When two yields are equal, the lower `id` comes first.

Each object must include `modeledIncomeNote` set to `"{yieldPercent}% modeled annual yield"`.

Array order matters. Field order does not.

Leave the existing API unchanged, and do not call it from your program.

Run your result from the project root:

```bash
cd rust
cargo run
```

Read the API result in another terminal, from the project root:

```bash
curl.exe "http://localhost:4000/api/properties?type=Residential&minYield=6&sort=yieldPercent&order=desc"
```

Pass if the parsed JSON is the same array, in the same order, as http://localhost:4000/api/properties?type=Residential&minYield=6&sort=yieldPercent&order=desc.
