# Slider Color Picker

<img src="https://github.com/DastanIqbal/vertical-slide-color-picker/blob/master/output.gif" width=300/>

## Vertical Color Picker Example usage

layout.xml
```XML
<com.github.veritas1.verticalslidecolorpicker.VerticalSlideColorPicker
            android:id="@+id/color_picker"
            android:layout_width="30dp"
            android:layout_height="100dp"
            colorpicker:borderColor="@android:color/black"
            colorpicker:borderWidth="2dp"
            colorpicker:colors="@array/my_color_array"/>
```

Activity.java
```Java
final VerticalSlideColorPicker colorPicker = (VerticalSlideColorPicker) findViewById(R.id.color_picker);
final View selectedColorView = findViewById(R.id.selected_color);

colorPicker.setOnColorChangeListener(new VerticalSlideColorPicker.OnColorChangeListener() {
    @Override
    public void onColorChange(int selectedColor) {
        selectedColorView.setBackgroundColor(selectedColor);
    }
});
```

## Horizontal Color Picker Example usage
layout.xml
```XML
<com.github.veritas1.HorizontalSlideColorPicker
        android:id="@+id/color_hpicker"
        android:layout_width="match_parent"
        android:layout_height="50dp" />
```

Activity.java
```Java
final HorizontalSlideColorPicker colorPickerH = (HorizontalSlideColorPicker) findViewById(R.id.color_hpicker);
final View selectedColorViewH = findViewById(R.id.selected_hcolor);

colorPickerH.setOnColorChangedListener(new HorizontalSlideColorPicker.OnColorChangedListener() {
    @Override
    public void onColorChanged(String color) {
        selectedColorViewH.setBackgroundColor(Color.parseColor(color));

    }
});
```
