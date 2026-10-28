FlexEarner - static HTML version
================================

Upload the CONTENTS of this folder to the web root of flexearner.com, or to any subfolder
for a staging preview. All links are relative, so it works in either place.

All 89 URLs are unchanged (home, contact, 20 posts, categories, tags, author pages,
paginated pages and image attachment pages). Each URL is a folder containing index.html.

Contact form
------------
Contact Form 7 needed WordPress, so the form now posts to contact/send.php (needs PHP).
IMPORTANT: open contact/send.php and set $to to the address that should receive messages.
Until then the form shows its error message instead of sending.
A hidden honeypot field provides basic spam protection.

Notes
-----
- The thumbnail image on "Living to Work or Working to Live" is already missing on the live site.
- WordPress-only links in <head> (REST API, feeds, xmlrpc) were removed.

Noindex (staging)
-----------------
Every page has <meta name="robots" content="noindex, nofollow" /> and .htaccess sends an
X-Robots-Tag: noindex, nofollow header, so search engines will not index this copy.
BEFORE GOING LIVE on the real domain: remove that meta line from each page and delete the
"BEGIN noindex ... END noindex" block from .htaccess, or the site will drop out of Google.
