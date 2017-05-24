# RecyclerviewEmptyViewSupport
Developer can use Empty TextView or ImageView while data list is Zero in the RecyclerViewAdapter

1) Use below link to download  .aar file, add this library to libs folder and import to project
   link:

2) Add below layout to your xml

    <com.virendra.view.RecyclerViewEmptySupport
            android:id="@+id/recyclerview1"
            android:layout_width="match_parent"
            android:layout_height="match_parent"/>

3) Create Adapter and set Adapter to recyclerview1

4) Use setAdapter() method as per your requirement
    e.g. a)  recyclerview1.setAdapter(adapter);
         b)  recyclerview1.setAdapterWithEmptyTextView(adapter, "There are no record to show...");
         c)  recyclerview1.setAdapterWithEmptyImageView(adapter, ContextCompat.getDrawable(this, R.mipmap.ic_launcher));
         d)  recyclerview1.setAdapterWithEmptyImageView(adapter, ContextCompat.getDrawable(this, R.mipmap.ic_launcher), 100, 100); // unit is dp
         e)  recyclerview1.setAdapterWithEmptyImageView(adapter, null); //To show library default image

5) Empty Text and Image can be added in xml layout
    If your mentioned text and image in xml layout then ImageView has more priority than TextView
    a)  For empty text:  import at parent layout:  xmlns:app="http://schemas.android.com/apk/res-auto"

        <com.virendra.view.RecyclerViewEmptySupport
            android:id="@+id/recyclerview1"
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            app:empty_list_text="No data found..." />

     b) For image : import at parent layout:  xmlns:app="http://schemas.android.com/apk/res-auto"
        If height and width not mentioned then image parameters are WRAP_CONTENT

        <com.virendra.view.RecyclerViewEmptySupport
             android:id="@+id/recyclerview1"
             android:layout_width="match_parent"
             android:layout_height="match_parent"
             app:empty_image_drawable="@mipmap/ic_launcher"
             app:empty_image_height="100dp"
             app:empty_image_width="100dp" />


