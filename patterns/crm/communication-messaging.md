# Communication / Messaging

**Used in:** Dialog panel messaging, email compose, note creation.

**Structure (Message thread):**
```
[Thread container]
  ├── [Message list (scrollable)]
  │     └── [Message item]
  │           ├── Avatar
  │           ├── Sender name + timestamp
  │           ├── Message content (rich text supported)
  │           └── Attachment chips
  └── [Reply composer]
        ├── Rich text input
        ├── Attachment button
        ├── Formatting toolbar
        └── Send button
```

**Key CRM-specific behaviors:**
- Messages are linked to entity records
- Email messages show full header (To, CC, BCC, Subject)
- Activities auto-logged on send
- `Icon=send` for send action

---
