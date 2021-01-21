[https://github.com/daimajia/AndroidViewAnimations](https://github.com/daimajia/AndroidViewAnimations)

[https://github.com/daimajia/AnimationEasingFunctions](https://github.com/daimajia/AnimationEasingFunctions)

```xml
implementation 'com.daimajia.androidanimations:library:2.4@aar'
implementation 'com.daimajia.easing:library:2.4@aar'
```

```kotlin
import androidx.appcompat.app.AppCompatActivity
import android.os.Bundle
import android.view.animation.BounceInterpolator
import com.daimajia.androidanimations.library.Techniques
import com.daimajia.androidanimations.library.YoYo
import kotlinx.android.synthetic.main.activity_main.*

class MainActivity : AppCompatActivity() {

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        button.setOnClickListener {
            YoYo.with(Techniques.FlipOutX)
                    .duration(200)
                    .repeat(1)
                    .interpolate(BounceInterpolator())
                    .playOn(textview)
        }

    }

}
```