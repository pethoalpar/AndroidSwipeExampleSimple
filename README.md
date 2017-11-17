# Android Swipe Example Simple

```java
public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate( Bundle savedInstanceState ) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }

    @Override
    public boolean onTouchEvent( MotionEvent event ) {
        int action = MotionEventCompat.getActionMasked(event);

        switch (action){
            case (MotionEvent.ACTION_DOWN) :
                Toast.makeText(this,"Down",Toast.LENGTH_SHORT).show();
                return true;
            case (MotionEvent.ACTION_MOVE) :
                Toast.makeText(this,"Move",Toast.LENGTH_SHORT).show();
                return true;
            case (MotionEvent.ACTION_UP) :
                Toast.makeText(this,"UP",Toast.LENGTH_SHORT).show();
                return true;
            case (MotionEvent.ACTION_CANCEL) :
                Toast.makeText(this,"Cancel",Toast.LENGTH_SHORT).show();
                return true;
            case (MotionEvent.ACTION_OUTSIDE) :
                Toast.makeText(this,"Outside",Toast.LENGTH_SHORT).show();
                return true;
            default:
                return super.onTouchEvent(event);
        }

    }
}
```
