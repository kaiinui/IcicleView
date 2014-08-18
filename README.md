IcicleView
==========

Work nice with Icipick and ButterKnife!

```java
class ExampleActivity extends Activity {
  @Icicle String username;
  @IcicleView @InjectView(R.id.edit_text) EditText editText;

  @Override public void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    ButterKnife.inject(this)
    Icepick.restoreInstanceState(this, savedInstanceState);
    IcicleView.restoreInstanceState(this, savedInstanceState);
  }

  @Override public void onSaveInstanceState(Bundle outState) {
    super.onSaveInstanceState(outState);
    Icepick.saveInstanceState(this, outState);
    IcicleView.saveInstanceState(this, outState);
  }
}
```
