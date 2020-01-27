# TextWriter
⚡️ Animate your text like never before ⚡️

## Add dependency

Add this in your root build.gradle at the end of repositories:

```bash
allprojects {
	repositories {
		...
		maven { url 'https://jitpack.io' }
	}
}		
```
Add this in your app level gradle:

```bash
implementation 'com.github.sarnavakonar:TextWriter:v1.0'
```

## Initialization

Add TextWriter in your xml file:

```bash
<com.sarnava.textwriter.TextWriter
        android:id="@+id/textWriter"
        android:layout_width="match_parent"
        android:layout_height="match_parent" />
```

Initialize in the Activity file:

```bash
TextWriter textWriter;

textWriter = findViewById(R.id.textWriter);
```

## Customization

Customize according to your need (**as of now it only support uppercase letters and whitespace** :broken_heart:):

```bash
textWriter
         .setWidth(12)
         .setDelay(30)
         .setColor(Color.RED)
         .setConfig(TextWriter.Configuration.INTERMEDIATE)
         .setSizeFactor(30f)
         .setLetterSpacing(25f)
         .setText("LIVERPOOL FC")
         .setListener(new TextWriter.Listener() {
          	@Override
          	public void WritingFinished() {

			//do stuff after animation is finished
                }
          })
         .startAnimation();
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
[MIT](https://choosealicense.com/licenses/mit/)
