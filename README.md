# ModalBottomSheetDialogFragment

Modal bottom sheet dialog based on the [Material Guidelines](https://material.io/guidelines/components/bottom-sheets.html#bottom-sheets-modal-bottom-sheets)

[![Build Status](https://travis-ci.org/Commit451/ModalBottomSheetDialogFragment.svg?branch=master)](https://travis-ci.org/Commit451/ModalBottomSheetDialogFragment) [![](https://jitpack.io/v/Commit451/ModalBottomSheetDialogFragment.svg)](https://jitpack.io/#Commit451/ModalBottomSheetDialogFragment)

## Usage
`ModalBottomSheetDialogFragment`s are controlled via a menu item resource. The menu item resource defined what the title, icon, and ID is of each option. The menu item resource might looks something like this:
```xml
<?xml version="1.0" encoding="utf-8"?>
<menu xmlns:android="http://schemas.android.com/apk/res/android">

    <item
        android:id="@+id/action_favorite"
        android:icon="@drawable/ic_favorite_black_24dp"
        android:title="Favorite" />

    <item
        android:id="@+id/action_share"
        android:icon="@drawable/ic_share_black_24dp"
        android:title="Share" />

    <item
        android:id="@+id/action_edit"
        android:icon="@drawable/ic_edit_black_24dp"
        android:title="Edit" />

</menu>
```
Then, use the builder to create and show the bottom sheet dialog:
```kotlin
ModalBottomSheetDialogFragment.Builder(R.menu.options)
    .show(supportFragmentManager, "options", {
        Snackbar.make(root, "Selected option $it", Snackbar.LENGTH_SHORT)
                .show()
    })
```

License
--------

    Copyright 2018 Commit 451

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.