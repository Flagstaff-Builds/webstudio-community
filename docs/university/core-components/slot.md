---
description: >-
  Slots are containers for anything that you want to re-use across your site,
  like a nav menu.
---

# 🔲 Slot

{% embed url="https://vimeo.com/842097297" %}

Slots enable you to create reusable sections on your site. Changes made to one instance of the Slot will automatically change all other instances.

{% hint style="info" %}
Slots and their children will appear purple in the navigator and canvas to indicate they are Slots, and any changes made to them will affect all other instances of the Slot.
{% endhint %}

Slots are most commonly used to create reusable navigations and footers, though they are helpful for any sections you want to reuse throughout your site.

{% hint style="info" %}
Data Variables defined on the Global Root are accessible within Slots, while those defined on other instances outside the Slot are not.
{% endhint %}

***

### How to use Slot Component

Here is the process for creating and reusing Slot instances:

#### Creating a Slot instance

&#x20;![create a slot in Webstudio](../../.gitbook/assets/university/Slots_Image.avif)

1. You can find the Slots component in the “Components Panel.”
2. Drag “Slot” from the Components Panel onto your canvas to create a Slot instance. Alternatively, you can add it to the currently selected instance with a click.
3. Add other instances from the Components Panel into the Slot instance to populate it.

#### Reusing a Slot instance

Once you have a Slot on the canvas you can re-use it by simply copying and pasting it anywhere in your project.

1. Select your Slot instance and press Ctrl + C (for Windows) or CMD + C (for Mac).
2. Now, select the position where you want to insert the Slot instance and press Ctrl + V (for Windows) or CMD + V (for Mac)

And that’s it! Now updates that you make to any Slot will update all other instances of that Slot.

If you need a new unique Slot instance, simply add a new Slot from the Add panel and it will not interfere with your existing Slots.

***

### Conclusion

With Slots you can re-use content across your site and sync the changes you make to them.
