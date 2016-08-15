#Usage
=====

These lines formats simply your input for default locale.

```xml
<faranjit.currency.edittext.CurrencyEditText
        android:id="@+id/edt_currency"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:inputType="numberDecimal"
        android:textColor="@android:color/black" />
```

You can choose any locale.
```xml
<faranjit.currency.edittext.CurrencyEditText
        android:id="@+id/edt_currency"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:inputType="numberDecimal"
        android:textColor="@android:color/black"
        app:locale="en_US" />
```

or

```java
final CurrencyEditText currencyEditText = (CurrencyEditText) findViewById(R.id.edt_currency);
currencyEditText.setLocale(new Locale("en", "US"));
```

`CurrencyEditText` shows currency symbol depends on locale but you can set to not show.
```xml
<faranjit.currency.edittext.CurrencyEditText
        android:id="@+id/edt_currency"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:inputType="numberDecimal"
        android:textColor="@android:color/black"
        app:locale="en_US"
        app:showSymbol="false" />
```
or
```java
currencyEditText.showSymbol(false);
```

If you want to you can change grouping and monetary seperators for money symbolization.
```xml
<faranjit.currency.edittext.CurrencyEditText
        android:id="@+id/edt_currency"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:inputType="numberDecimal"
        android:textColor="@android:color/black"
        app:groupDivider="."
        app:monetaryDivider=","
        app:locale="en_US"
        app:showSymbol="true" />
```
or
```java
currencyEditText.setGroupDivider('.');
currencyEditText.setMonetaryDivider(',');
```

When set text to _123450_, this gives to output _$1.234,50_ instead of _$1,234.50_.
