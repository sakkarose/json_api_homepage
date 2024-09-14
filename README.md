## lastfm-api_homepage

Showcase your Last.fm listening habits directly on your [homepage](https://github.com/gethomepage/homepage).

### Features

* Last Scrobbled Track:
* Top Weekly Albums:
* Top Weekly Artists:
* Top Weekly Tracks:

### Preview

![image](https://github.com/user-attachments/assets/8562edf5-ec63-4f7f-9b34-09883c01b3d9)

### Installation

1. **Get an API Key:** Create a Last.fm API account at [https://www.last.fm/api/account/create](https://www.last.fm/api/account/create).
2. **Configure `services.yaml`:** 
   * Add the provided `services.yaml` content to your existing `services.yaml` file.
   * Replace `<apikey>` with your actual Last.fm API key.
   * Replace `<username>` with your Last.fm username.

3. **Customize (Optional):**
   * **Increase List Entries:** 
     * In the `url` section of each widget, change `...&limit=1` to your desired number of entries.
   * **Add More Rankings:**
     * Copy the entire `mappings` section for the relevant widget.
     * In the copied section:
       * Change the `0` to the desired ranking number minus one (e.g., for #3, use `2`).
       * Change the `label` to the actual ranking number (e.g., `#3`).

### Example `mappings` Customization

```yaml
mappings:
  - field: 
      weeklyalbumchart:
        album:
          0:
            artist: "#text"
    label: "#1"
    color: white
    additionalField:
      field:
        weeklyalbumchart:
          album:
            0: name
      color: theme
```

**Remember:** Indentation is crucial in YAML. Make sure your changes maintain the correct structure.

