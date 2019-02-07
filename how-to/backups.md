---
description: >-
  Backups are used to save and duplicate your server. Backups are limited to the
  user that created it, but not limited to a server. That means you can use
  backups to move, or duplicate a server.
---

# Backups

## Creating a backup

Create a backup of your discord. After the bot created the backup, it sends you the backup-id via direct messages.

{% hint style="warning" %}
Make sure you allow direct messages from Xenon
{% endhint %}

### Syntax

```text
x!backup create [chatlog]
```

### Arguments

{% tabs %}
{% tab title="chatlog" %}
 The count of messages to save per channel 

Only available for [pro](xenon-pro.md) users!

**`max: 25` `default: 0` `optional`**
{% endtab %}
{% endtabs %}

## Loading a backup

Load a backup. You obviously need to create backup before you can use this command.

{% hint style="danger" %}
Loading a backup replaces all channels and roles in the discord. It does **not** kick the members.
{% endhint %}

### Syntax

```text
x!backup load <backup-id> [chatlog] [load_options...]
```

### Arguments

{% tabs %}
{% tab title="backup-id" %}
The id of the backup you want to load. You get this after creating a backup

**`required`**
{% endtab %}

{% tab title="chatlog" %}
The count of messages to load per channel 

Only available for [pro](xenon-pro.md) users!

**`max: 25` `default: 25` `optional`**
{% endtab %}

{% tab title="load\_options" %}
A list of arguments, seperated by a space. Passing something to this argument will **overwrite** not update the default values. 

**Example:** `x!backup load <backup-id> roles` will only load rolles

**`optional` `default: channels roles bans members settings`**
{% endtab %}
{% endtabs %}

## Automated Backups / Interval

The bot creates a backup of your guild in a certain interval. Everytime the bot creates a backup, you will get a direct message.

### Syntax

```text
x!backup interval <interval...>
```

### Arguments

{% tabs %}
{% tab title="interval" %}
A list of arguments, seperated by a space. The time the bot should wait between two automated backups. Supported units are `weeks (w)` `days (d)` `hours (h)` `minutes (m)`

**Example:** `x!backup interval 1d 12h` will backup your discord every 36 hours

**`required`**
{% endtab %}
{% endtabs %}

## Reinvite Members

Reinvite members from a backup. Be careful with and don't spam people with this feature. You will get permanently blacklisted.

{% page-ref page="xenon-pro.md" %}

### **Syntax**

```text
x!backup reinvite <backup_id> [limit]
```

### Arguments

{% tabs %}
{% tab title="backup\_id" %}
The id of the backup you want to reinvite members from. You get this after creating a backup

`required`
{% endtab %}

{% tab title="limit" %}
The count of members to reinvite. If your discord has more members than the limit, the bot will reinvite the members with the most roles.

**`max: 100` `default: 100` `optional`**
{% endtab %}
{% endtabs %}

