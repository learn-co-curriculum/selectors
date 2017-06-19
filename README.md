# Selectors

In the last section, you saw that your store is kind of like your database, and the data should be normalized similarly to how data in a database would be.  Now, imagine that we have a blogger application that is using redux, and therefore our redux store captures information about authors and blogposts. 

```javascript
let store = {
	authors: {
		1: {id: 1, name: 'Mark Twain'}
	},
	blogPosts: {
		1: {title: 'Tom and Huck', authorId: 1},
		2: {title: 'Prince and the Pauper', authorId: 1}
	}
}
```    

Now, on an author show page, we still want to show the posts related to a given author.  And you can imagine that we might want a function like this in multiple places.

That is where selectors come in handy.  Selectors allow your application to perform querying logic in a place that is isolated from your view.  So selectors decouple the querying logic from the views.

Selectors also have a second purpose, which is to decouple your store from the views.  That way, if say your store changes it's structure, you only need to change the selector in one location, and not change any of your views that depend on that data.

It's ok if this is slightly confusing, let's give some readings that will help clear this up.

* [Selectors Example](https://gist.github.com/abhiaiyer91/aaf6e325cf7fc5fd5ebc70192a1fa170) 
* [Selectors Documentation](http://redux.js.org/docs/recipes/ComputingDerivedData.html)
* [Dan Abramov on Selectors](https://egghead.io/lessons/javascript-redux-colocating-selectors-with-reducers)
<p class='util--hide'>View <a href='https://learn.co/lessons/selectors'>Selectors</a> on Learn.co and start learning to code for free.</p>
