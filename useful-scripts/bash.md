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

- List files in the directory in a human readable form

```bash
du -a -h --max-depth=1 | sort -hr
```

- Kill process running at port N
```bash
lsof -i tcp:<N> # get PID from here
kill -9 <PID>
```

- Debug and trace any script

```bash
bash -x some-script.sh

# Debug yarn
bash -x /usr/local/bin/yarn start
```
