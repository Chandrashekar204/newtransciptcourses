# 35.10 — Understanding the Custom Element Lifecycle

> Section 35: Bonus: Web Components

So I mentioned that there is a specific web component lifecycle which the browser follows when instantiating our own custom element objects in the DOM so to say. The first thing that gets executed is the constructor because this always gets executed when an object gets created based on your class and then the class's constructor gets executed, so this is essentially called when the element is created. Now it's important to highlight here that the moment where the element is created is not the moment where the element is then also attached into the real DOM by the browser, instead it's created in memory first and it's not part of the DOM at the beginning.

So the constructor is great for some basic initializations, some basic values for the different properties and variables you might be using in your class, in your component but it's the wrong place for accessing the DOM because your custom element has not been added to the DOM yet. For this, there is another method you can add in your class which will be executed by the browser once this element, once this custom component has been mounted onto the browser's DOM and that is the connected callback method. This is called when your element has been attached to the DOM and therefore this is the place for DOM initializations, so where you can now start adding content or where you can start accessing the DOM.

There also is a disconnected callback method which will also be executed automatically for you and this method will be called by the browser whenever your element, so your custom element, your web component, whenever that is detached from the DOM, so when you destroy that node which you can do through Javascript for example and therefore this is then a great method for some cleanup work, like for example if you were sending a HttpRequest, this would be where you could cancel it.

There is another method, the attribute changed callback and that will be important for listening to changes to attributes to your own element. It is something we haven't covered yet and therefore I will come back to this, this will later become important for updating the data and the DOM of your web component when some attributes which can be passed to your component changed but we haven't covered attributes on your own elements yet, so let's ignore that and let's focus on the connected callback.

----------------------------------------
