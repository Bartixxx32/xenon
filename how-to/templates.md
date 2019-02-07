---
description: >-
  Xenon gives you access to hundreds of free templates. In contrast to backups,
  templates are public and can be used by everyone.
---

# Templates

## List of templates

You can find a list of templates in the \#template\_list and the \#featured\_templates channel on the [Magic Bots discord](https://discord.club/discord).

## Loading a template

Load a template

{% hint style="danger" %}
Loading a template replaces all channels and roles in the discord. It does **not** kick the members.
{% endhint %}

### Syntax

```text
x!template load <template_name>
```

### Arguments

{% tabs %}
{% tab title="template\_name" %}
The name of the template you want to load

**`required`**
{% endtab %}
{% endtabs %}

## Creating a template

Turn a backup into a template. The backup will remain available.

{% hint style="danger" %}
All templates are public! Do not share share private information in templates.
{% endhint %}

### Syntax

```text
x!template create <backup_id> <name> <description>
```

### Arguments

{% tabs %}
{% tab title="backup\_id" %}
The id of the backup you want to turn into a template

**`required`**
{% endtab %}

{% tab title="name" %}
A name for the template. This should be unique and not contain "template"

**`required`**
{% endtab %}

{% tab title="description" %}
A short, but meaningful description

**`required`**
{% endtab %}
{% endtabs %}



