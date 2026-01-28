#!/usr/bin/env bash
set -euo pipefail

# Create a minimal Jekyll site scaffold
cat > _config.yml <<'YAML'
title: "My Site"
email: you@example.com
description: "A simple personal site"
baseurl: ""
url: "https://example.com"
theme: minima
YAML

cat > index.md <<'MD'
---
layout: home
title: "Home"
---
Welcome to my site.

- [About](/about/)
- [Writing](/writing/)
- [Speaking](/speaking/)
- [Contact](/contact/)
MD

cat > about.md <<'MD'
---
layout: page
title: "About"
permalink: /about/
---
Short bio or project description goes here.
MD

cat > writing.md <<'MD'
---
layout: page
title: "Writing"
permalink: /writing/
---
Links to posts, essays, or publications.
MD

cat > speaking.md <<'MD'
---
layout: page
title: "Speaking"
permalink: /speaking/
---
Talks, slides, and upcoming events.
MD

cat > contact.md <<'MD'
---
layout: page
title: "Contact"
permalink: /contact/
---
Email: you@example.com
Social links or contact form info.
MD

echo "Created: _config.yml index.md about.md writing.md speaking.md contact.md"