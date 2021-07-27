# Useful bash scripts

- **Find text in file and replace it**
  ```bash
  sed -i -e 's/<text>/<replace-text>/g' <path-to-file>
  ```
  *Example*:
  ```bash
  # decrease block time
   sed -i -e 's/pub const MILLISECS_PER_BLOCK: u64 = 6000;\
    /pub const MILLISECS_PER_BLOCK: u64 = 4000;/g' \
    ./runtime/src/lib.rs
  ```
