Android Coding Guidelines
=========================

Follow [Android coding style](http://source.android.com/source/code-style.html) except for:

* No warnings
* No switch/case statements
* Use CamelCase for instance members
* Use underscore_case for variables
* All variables must be final (except int i)
* By default, all methods private and final
* Hungarian notation:
  * btSomething is a Button
  * frSomething is a Fragment
  * ivSomething is an ImageView
  * lvSomething is a ListView
  * tvSomething is a TextView
  * vpSomething is a ViewPager
  * mSomething for the rest
  * sSomething for static members

Activities
----------

* Activity class names must end with "Activity"
* Activity classes are final by default
* onCreate must call private methods findViews(), setListeners(), fetchData() and loadData()
* findViews(): sets all view instance members (findViewById goes here)
* setListeners(): sets all listeners on views. Let the Activity implement OnClickListener, etc.
* fetchData(): retrieve data to be displayed by this activity, be it from the filesystem, database, network, etc.
* loadData(): display the data on the views (tv.setText, lv.setAdapter goes here)

Layouts
-------

* Layout file for SomethingActivity is something_layout.xml
* View ids use the same name as the activity instance member variables, i.e. tvSomething, lvSomething, etc.
* Separate layout files in folders by minimum screen width. Make scrollable on shorter screens

Resources
---------

* Resource names must contain a class prefix. A string resource used in SomethingActivity will be R.string.something_astring
* Do not use drawable/ folder, use drawable-nodpi instead. No bitmaps

