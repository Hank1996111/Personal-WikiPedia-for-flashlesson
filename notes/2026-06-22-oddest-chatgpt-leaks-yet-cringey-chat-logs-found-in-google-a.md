---
title: "**Oddest ChatGPT leaks yet: Cringey chat logs found in Google analytics tool**"
date: 2026-06-22
tags: [Business, Google, Hardware, LLM, Legal]

type: note
status: read
---
**Oddest ChatGPT leaks yet: Cringey chat logs found in Google analytics tool**

For months, extremely personal and sensitive ChatGPT conversations have been leaking into an unexpected destination: Google Search Console (GSC), a tool that developers typically use to monitor search traffic, not lurk private chats.

Normally, when site managers access GSC performance reports, they see queries based on keywords or short phrases that Internet users type into Google to find relevant content. But starting this September, odd queries, sometimes more than 300 characters long, could also be found in GSC. Showing only user inputs, the chats appeared to be from unwitting people prompting a chatbot to help solve relationship or business problems, who likely expected those conversations would remain private.

Jason Packer, owner of an analytics consulting firm called Quantable, was among the first to flag the issue in a detailed [blog](https://www.quantable.com/ai/the-old-rules-are-dead/) last month.

Determined to figure out what exactly was causing the leaks, he teamed up with “Internet sleuth” and web optimization consultant Slobodan Manić. Together, they conducted testing that they believe may have surfaced “the first definitive proof that OpenAI directly scrapes Google Search with actual user prompts.” Their investigation seemed to confirm the AI giant was compromising user privacy, in some cases in order to maintain engagement by seizing search data that Google otherwise wouldn’t share.

OpenAI declined Ars’ request to confirm if Packer and Manić’s theory posed in their blog was correct or answer any of their remaining questions that could help users determine the scope of the problem.

However, an OpenAI spokesperson confirmed that the company was “aware” of the issue and has since “resolved” a glitch “that temporarily affected how a small number of search queries were routed.”

Packer told Ars that he’s “very pleased that OpenAI was able to resolve the issue quickly.” But he suggested that OpenAI’s response failed to confirm whether or not OpenAI was scraping Google, and that leaves room for doubt that the issue was completely resolved.

Google declined to comment.

**“Weirder” than prior ChatGPT leaks**

The first odd ChatGPT query to appear in GSC that Packer reviewed was a wacky stream-of-consciousness from a likely female user asking ChatGPT to assess certain behaviors to help her figure out if a boy who teases her had feelings for her. Another odd query seemed to come from an office manager sharing business information while plotting a return-to-office announcement.

These were just two of 200 odd queries—including “some pretty crazy ones,” Packer told Ars—that he reviewed on one site alone. In his blog, Packer concluded that the queries should serve as “a reminder that prompts aren’t as private as you think they are!”

Packer suspected that these queries were connected to [reporting from The Information](https://www.theinformation.com/articles/openai-challenging-google-using-search-data) in August that cited sources claiming OpenAI was scraping Google search results to power ChatGPT responses. Sources claimed that OpenAI was leaning on Google to answer prompts to ChatGPT seeking information about current events, like news or sports.

OpenAI has not confirmed that it’s scraping Google search engine results pages (SERPs). However, Packer thinks his testing of ChatGPT leaks may be evidence that OpenAI not only scrapes “SERPs in general to acquire data,” but also sends user prompts to Google Search.

Manić helped Packer solve a big part of the riddle. He found that the odd queries were turning up in one site’s GSC because it ranked highly in Google Search for “<https://openai.com/index/chatgpt/”—a> ChatGPT URL that was appended at the start of every strange query turning up in GSC.

It seemed that Google had tokenized the URL, breaking it up into a search for keywords “openai + index + chatgpt.” Sites using GSC that ranked highly for those keywords were therefore likely to encounter ChatGPT leaks, Parker and Manić proposed, including sites that covered prior ChatGPT leaks where [chats were being indexed in Google search results](https://arstechnica.com/tech-policy/2025/08/chatgpt-users-shocked-to-learn-their-chats-were-in-google-search-results/). Using their recommendations to seek out queries in GSC, Ars was able to verify similar strings.

“Don’t get confused though, this is a new and completely different ChatGPT screw-up than having Google index stuff we don’t want them to,” Packer wrote. “Weirder, if not as serious.”

It’s unclear what exactly OpenAI fixed, but Packer and Manić have a theory about one possible path for leaking chats. Visiting the URL that starts every strange query found in GSC, ChatGPT users encounter a prompt box that seemed buggy, causing “the URL of that page to be added to the prompt.” The issue, they explained, seemed to be that:

> Normally ChatGPT 5 will choose to do a web search whenever it thinks it needs to, and is more likely to do that with an esoteric or recency-requiring search. But this bugged prompt box also contains the query parameter ‘hints=search’ to cause it to basically always do a search: <https://chatgpt.com/?hints=search&openaicom_referred=true&model=gpt-5>

Clearly some of those searches relied on Google, Packer’s blog said, mistakenly sending to GSC “whatever” the user says in the prompt box, with “<https://openai.com/index/chatgpt/”> text added to the front of it.” As Packer explained, “we know it must have scraped those rather than using an API or some kind of private connection—because those other options don’t show inside GSC.”

This means “that OpenAI is sharing any prompt that requires a Google Search with both Google and whoever is doing their scraping,” Packer alleged. “And then also with whoever’s site shows up in the search results! Yikes.”

To Packer, it appeared that “ALL ChatGPT prompts” that used Google Search risked being leaked during the past two months.

OpenAI claimed only a small number of queries were leaked but declined to provide a more precise estimate. So, it remains unclear how many of the 700 million people who use ChatGPT each week had prompts routed to GSC.

**OpenAI’s response leaves users with “lingering questions”**

After ChatGPT prompts were found surfacing in Google’s search index in August, OpenAI clarified that users had clicked a box making those prompts public, which OpenAI defended as “sufficiently clear.” The AI firm later scrambled to remove the chats from Google’s SERPs after it became obvious that users felt misled into sharing private chats publicly.

Packer told Ars that a major difference between those leaks and the GSC leaks is that users harmed by the prior scandal, at least on some level, “had to actively share” their leaked chats. In the more recent case, “nobody clicked share” or had a reasonable way to prevent their chats from being exposed.

“Did OpenAI go so fast that they didn’t consider the privacy implications of this, or did they just not care?” Packer posited in his blog.

Perhaps most troubling to some users—whose identities are not linked in chats unless their prompts perhaps share identifying information—there does not seem to be any way to remove the leaked chats from GSC, unlike the prior scandal.

Packer and Manić are left with “lingering questions” about how far OpenAI’s fix will go to stop the issue.

Manić was hoping OpenAI might confirm if prompts entered on <https://chatgpt.com> that trigger Google Search were also affected. But OpenAI did not follow up on that question, or a broader question about how big the leak was. To Manić, a major concern was that OpenAI’s scraping may be “contributing to ‘crocodile mouth’ in Google Search Console,” a troubling trend SEO researchers have flagged that causes impressions to spike but clicks to dip.

OpenAI also declined to clarify Packer’s biggest question. He’s left wondering if the company’s “fix” simply ended OpenAI’s “routing of search queries, such that raw prompts are no longer being sent to Google Search, or are they no longer scraping Google Search at all for data?

“We still don’t know if it’s that one particular page that has this bug or whether this is really widespread,” Packer told Ars. “In either case, it’s serious and just sort of shows how little regard OpenAI has for moving carefully when it comes to privacy.”