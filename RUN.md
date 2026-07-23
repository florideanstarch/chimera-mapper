Building the code using:

```
cargo build --release
```

Then run the following command:

```
./target/release/chimera-mapper run --vid 0x248a --pid 0x8266 --usage-page 0x0001 --usage 0x0002 --side-action "command+]" --extra-action "command+["
```

When using in wired mode:

```
./target/release/chimera-mapper run --vid 0x248a --pid 0x5b49 --usage-page 0x0001 --usage 0x0002 --side-action "command+]" --extra-action "command+["
```

Check the pid with:

```
./target/release/chimera-mapper list
```

## Running in the background

Discard output so it doesn't spam the terminal:

```
./target/release/chimera-mapper run --vid 0x248a --pid 0x8266 --usage-page 0x0001 --usage 0x0002 --side-action "command+]" --extra-action "command+[" > /dev/null 2>&1 & disown
```

Bring it to the foreground:

```
fg
```

## Killing the process

```
pgrep -fl chimera-mapper
kill <pid>
```
