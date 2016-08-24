# arXiv API
A simple JavaScript API that can be used to query the arXiv HTTP API. Requires JQuery.

the function:
```
arxiv_search({all, author, title, abstrct, journal_ref}) 
```

takes one or more of the following optional string arguments. Each string will match against its respective field:
* all (match provided string against all possible fields)
* author
* title
* abstract
* journal reference

It returns a JQuery Promise that resolves to an array of JSON once "done". JSON is in the format:

```javascript
{
 'title': title,
 'link': URL,
 'summary': summary,
 'date': publication_date,
 'authors': authors             //note this is an array of strings
}
```

For more information please see the [example](example.html)
