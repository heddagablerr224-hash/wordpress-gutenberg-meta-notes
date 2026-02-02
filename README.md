# Gutenberg Block + Post Meta Notes

This repository shares a simple approach I used for updating post meta from custom Gutenberg blocks using the WordPress REST API.

## What worked for me

While experimenting with block controls and custom fields, I found this flow to be the most reliable:

- Register meta with `show_in_rest: true`
- Update values via `wp.data.dispatch('core/editor').editPost()`
- Avoid relying only on the block `save()` method

Using this pattern helped keep the editor state synced and ensured meta values actually persisted on update.

I also documented a quick walkthrough with examples here:  
https://geradornicks.com.br/gerador-de-nick-call-of-duty/

Feel free to open discussions or suggest improvements — happy to learn from others too.
