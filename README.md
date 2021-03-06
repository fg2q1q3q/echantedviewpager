# echantedviewpager
EchantedViewPager is a custom ViewPager that provides some custom and usefull functionalities, such as, scalling scroll, alpha scroll and swipe to dismiss option.

![sslv animation](http://i.giphy.com/xTiN0qDxERHeG51Tl6.gif)

#Usage
Inside your pager adapter you must do this whenever you instantiate a view:
```java
@Override
    public Object instantiateItem(ViewGroup container, int position) {
        (...)
        mCurrentView.setTag(EnchantedViewPager.ENCHANTED_VIEWPAGER_POSITION + position);
        container.addView(mCurrentView);

        return mCurrentView;
    }
```
```xml
<com.tiagosantos.enchantedviewpager.EnchantedViewPager
    android:layout_width="match_parent"
    android:layout_height="wrap_content"/>
```
#Scale scroll
```java
 final EnchantedViewPager mViewPager = (EnchantedViewPager) findViewById(R.id.viewpager);
 mViewPager.useScale();
```
#Alpha scroll
```java
 final EnchantedViewPager mViewPager = (EnchantedViewPager) findViewById(R.id.viewpager);
 mViewPager.useAlpha();
```
#Swipe to dismiss
```java
 final EnchantedViewPager mViewPager = (EnchantedViewPager) findViewById(R.id.viewpager);
 mViewPager.addSwipeToDismiss(new EnchantedViewPager.EnchantedViewPagerSwipeListener() {
                        @Override
                        public void onSwipeFinished(int position) {
                            //execute code to remove the swiped item
                        }
                    });
```
#Gradle
```
compile 'com.tiagosantos:enchantedviewpager:1.0.0'
```
#License
```
Copyright 2016 Tiago Santos

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```