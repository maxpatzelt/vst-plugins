# VST Plugins

Collection root for the VST and JUCE projects developed in the audio
programming workspace. The NAS remains the primary working location.

## Projects

- `RandomDriftDelay/` is a JUCE plugin project currently tracked in this collection.
- `DubWise/` is a Git submodule at `https://github.com/maxpatzelt/DubWise`.
- `SDR-VST/` is a Git submodule at `https://github.com/maxpatzelt/rtl-sdr-vst3`; JUCE is nested as a submodule inside that project.

## Checkout

Clone the collection and its nested project repositories with:

```powershell
git clone --recurse-submodules https://github.com/maxpatzelt/vst-plugins.git
```

For an existing checkout, initialize or refresh its submodules with:

```powershell
git submodule update --init --recursive
```

Build each project using its own README. The collection ignores generated
`build/` trees; do not commit compiled plugin artifacts.

## Repository Rules

- Keep each independent plugin's build instructions in that project's README.
- Exclude generated `build/` output, local credentials, and unrelated operational files.
- Add a child as a submodule only after its remote URL is reachable and its commit is available there.
- Do not force-push or overwrite a project's existing history.
