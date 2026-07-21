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

Append `&` to send the process to the background:

```
./target/release/chimera-mapper run --vid 0x248a --pid 0x8266 --usage-page 0x0001 --usage 0x0002 --side-action "command+]" --extra-action "command+[" &
```

List background/suspended jobs in the current shell:

```
jobs
```

Bring the most recent background job to the foreground:

```
fg
```

Or target a specific job number (from `jobs`):

```
fg %1
```

## Killing the process

If it's running in the foreground, press `Ctrl+C`.

If it's in the background, kill it by job number:

```
kill %1
```

Or find it by process name and kill by PID:

```
pgrep -fl chimera-mapper
kill <pid>
```
