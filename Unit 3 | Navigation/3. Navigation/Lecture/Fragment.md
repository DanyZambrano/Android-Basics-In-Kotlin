## [Fragment]

A fragment is a reusable piece of UI; fragments can be reused and embedded in one or more activities. In the above screenshot, tapping on a tab doesn't trigger an intent to display the next screen. Instead, switching tabs simply swaps out the previous fragment with another fragment. All of this happens without launching another activity.

You can even show multiple fragments at once on a single screen, such as a master-detail layout for tablet devices. In the example below, both the navigation UI on the left and the content on the right can each be contained in a separate fragmen. Both fragments exist simultaneously in the same activity.

A fragment is simply a reusable piece of your app's user interface. Like activities, fragments have a lifecycle and can respond to user input. A fragment is always contained within the view hierarchy of an activity when it is shown onscreen. Due to their emphasis on reusability and modularity, it's even possible for multiple fragments to be hosted simultaneously by a single activity. Each fragment manages its own separate lifecycle.

As with activities, each fragment you add will consist of two files—an XML file for the layout and a Kotlin class to display data and handle user interactions.


<br>

![img](Lecture/1.png)

<br>


### Fragment lifecycle

Like activities, fragments can be initialized and removed from memory, and throughout their existence, appear, disappear, and reappear onscreen. Also, just like activities, fragments have a lifecycle with several states, and provide several methods you can override to respond to transitions between them. The fragment lifecycle has five states, represented by the Lifecycle.State enum.

* INITIALIZED: A new instance of the fragment has been instantiated.
* CREATED: The first fragment lifecycle methods are called. During this state, the view associated with the fragment is also created.
* STARTED: The fragment is visible onscreen but does not have "focus", meaning it can't respond to user input.
* RESUMED: The fragment is visible and has focus.
* DESTROYED: The fragment object has been de-instantiated.


<br>

![img](Lecture/2.png)
![img](Lecture/3.png)

<br>

The lifecycle states and callback methods are quite similar to those used for activities. However, keep in mind the difference with the onCreate() method. With activities, you would use this method to inflate the layout and bind views. However, in the fragment lifecycle, onCreate() is called before the view is created, so you can't inflate the layout here. Instead, you do this in onCreateView(). Then, after the view has been created, the onViewCreated() method is called, where you can then bind properties to specific views.