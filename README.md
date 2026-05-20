# hx-pr-assets

Asset host repo for HX PR images.

Upload via:
```bash
B64=$(base64 -i path/to/image.png)
gh api -X PUT "/repos/duymaib13/hx-pr-assets/contents/<unique-name>.png" \
  -f message="add <CU-id> <description>" \
  -f content="$B64" --jq .content.download_url
```

Embed in PR:
```
![alt](https://raw.githubusercontent.com/duymaib13/hx-pr-assets/main/<filename>.png)
```
