Once you've uploaded content and installed the skills you want, you're ready to start working with it in Claude.  The patterns are usually the same:

# Transform the content to Markdown

Markdown is the lingua franca of Claude skills.  If your content isn't already in Markdown format, you'll need to transform it.  Many skills include a `transform` command that can do this for you.  While the specifics may vary, you can often get a good result by simply asking Claude to convert your uploaded document for you, making sure to reference any skills you think will help.  For example:

`Use document skills to convert the test.docx file to markdown.  Preserve headings, lists, and code blocks.`

# Chunk it

Once you've got markdown, you might want to work with individual pieces or sections.  It's often best to let Claude examine to structure first to decide an approach, so just state a goal.  For example:

`Break  test.md into individual markdown files based on the higest level heading.  Give each file a meaningful name based on a slug of the section name`

Often its approach will be to look at a few samples, write a small Python program that parses the doc, and then runs the program it just created.  Let it do its thing.

# Transform it

Once you have the chunks, you're ready to transform.  One of the main uses cases we're exploring is converting "North Start" documents into skills, so you can ask Claude to do that.  The "example skills" hs a skill for making skills (very meta!) so you can use that.  For example:

`Use the create skills skill to convert each of the markdown files into a skill that can answer questions about the content.  Make sure to include any relevant context from the document in the skill's description.`

This is where you'll spend most of your time, iterating on the prompts and the approach until you get the results you want.

# Zip it and dowload

The simplest way to retrieve your transformed content from the lab is to zip it up and download it.  In general, you can just ask claude to do this for you.  For example:

`Zip up all the skill files into a single zip file called transformed-skills.zip`

Then drag and drop it from the VSCode file explorer to your desktop.
