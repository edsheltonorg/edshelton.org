---
foam_template:
  filepath: "docs/blog/${FOAM_DATE_YEAR}${FOAM_DATE_MONTH}${FOAM_DATE_DATE}-$FOAM_TITLE.md"
  name: Template - Blog
  description: Blog Post.
---
---
# draft: true
title: $FOAM_TITLE # Proper Title, Auto Slugged
description: About $FOAM_TITLE
authors:
  - ed
date:
  created: $CURRENT_YEAR-$CURRENT_MONTH-$CURRENT_DATE
  # updated:
# readtime: 15
---
$0
<!--------------------------------------------------------------->

Issue being talked about / call to action.

![[Screenshot]]{width=700}

<!-- more -->

<!-- --------------------------------------------------------- -->

<!-- OPTIONAL: ???+ info "Article Changes"
    Technical and business changes:

    | Date       | What                                          |
    | ---------- | --------------------------------------------- |
    |            |                                               | -->

<!-- --------------------------------------------------------- -->

{CONTENT}

<!-- --------------------------------------------------------- -->

<!-- OPTIONAL: ???+ bug "Issues And Questions Still Faced"

    | Error / Issue               | Article / Bug Track          |
    | --------------------------- | ---------------------------- |
    |                             | [[Answer#Section]]           | -->

<!-- --------------------------------------------------------- -->

<!-- OPTIONAL: ???+ example "Related Topics"

    | Topic & Link                | Why                          |
    | --------------------------- | ---------------------------- |
    | [[PARENT]]                  | Logical Concept              | -->

<!--------------------------------------------------------------->

<!-- TO-DO List -->
