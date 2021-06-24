# Jogo-descobra-o-numero-
Jogo  desenvolvido para android ainda em fase se criação




Jogo descubra o número   Android 

1-activity_main.xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">



    <androidx.appcompat.widget.AppCompatImageView
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:scaleType="centerCrop"
        android:src="@drawable/numero"
        />
    <View
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:background="@drawable/transparentepretocinza"
        />



    <EditText
        android:id="@+id/edtValorOculto"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_margin="10dp"
        android:background="@drawable/editgradienteverdepretoverdeicone"
        android:enabled="false"
        android:text="?"
        android:textAlignment="center"
        android:textColor="@android:color/white"
        app:layout_constraintBottom_toTopOf="@id/edtValor"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.498"
        app:layout_constraintStart_toStartOf="parent" />

    <EditText
        android:id="@+id/edtValor"
        android:layout_width="match_parent"
        android:layout_height="50dp"
        android:layout_margin="10dp"
        android:background="@drawable/editgradienteverdepretoverde"
        android:hint="Digite o valor!"
        android:inputType="number"
        android:textAlignment="center"
        android:textColor="@android:color/white"
        android:textColorHint="@android:color/white"
        app:layout_constraintBottom_toTopOf="@id/btnEnviar"
        />

    <!--
   Deve-se usar "androidx.appcompat.widget.AppCompatButton"
   em vez de "Button" para que o fundo mude de cor
  -->
    <androidx.appcompat.widget.AppCompatButton
        android:id="@+id/btnEnviar"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        app:layout_constraintBottom_toTopOf="@+id/btnNovo"
        android:text="Enviar"
        android:background="@drawable/botaoverdecomasbordasoval"
        android:textColor="@android:color/white"
        android:layout_margin="10dp"
        android:textAllCaps="false"
        />
    <androidx.appcompat.widget.AppCompatButton
        android:id="@+id/btnNovo"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        app:layout_constraintBottom_toTopOf="@+id/txtDica"
        android:text="Novo"
        android:background="@drawable/botaoverdecomasbordasoval"
        android:textColor="@android:color/white"
        android:layout_margin="10dp"
        android:textAllCaps="false"
        />

    <TextView
        android:id="@+id/txtDica"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="10dp"
        android:text="Valor de 1 até 10"
        android:textAlignment="center"
        android:textColor="@color/white"
        android:textSize="18dp"
        app:layout_constraintBottom_toBottomOf="parent"
        tools:layout_editor_absoluteX="10dp" />

</androidx.constraintlayout.widget.ConstraintLayout>


2-transparentepretocinza.xml
<?xml version="1.0" encoding="utf-8"?>
<shape xmlns:android="http://schemas.android.com/apk/res/android">

    <gradient
        android:endColor="@android:color/transparent"
        android:startColor="#FF000000"
        android:angle="90"
        android:centerColor="#AA000000"
        />
</shape>

3-edigradienteverdepretoverde.xml
<?xml version="1.0" encoding="utf-8"?>
<shape xmlns:android="http://schemas.android.com/apk/res/android">


    android:shape="rectangle">
    <gradient
        android:angle="0"
        android:startColor="@color/purple_700"
        android:centerColor="@color/black"
        android:endColor="@color/purple_500"
        />
    <corners
        android:radius="50dp"
        />


</shape>

4-editgradienteverdeepretoverdeicone.xml
<?xml version="1.0" encoding="utf-8"?>
<shape xmlns:android="http://schemas.android.com/apk/res/android">
    <corners
        android:bottomRightRadius="10dp"
    android:topLeftRadius="10dp"
    android:radius="40dp"
    />
    <gradient
        android:angle="0"
        android:startColor="@color/purple_700"
        android:centerColor="@color/black"
        android:endColor="@color/purple_500"
        android:type="linear" />
    <size
        android:width="82dp"
        android:height="82dp"
        />
    <stroke
        android:width="3dp"
        android:color="#000000"
        />





</shape>


5-botaoverdecomasbordasoval.xml
<?xml version="1.0" encoding="utf-8"?>
<shape xmlns:android="http://schemas.android.com/apk/res/android">
    android:shape="rectangle">
    <gradient
        android:angle="0"
        android:startColor="@color/purple_200"
        android:endColor="@color/black"
        />
    <corners
        android:radius="50dp"
      />
</shape>

6-MainActivity.java
package com.example.jogodescubranumero;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }
}


Values
7-themes.xml
<resources xmlns:tools="http://schemas.android.com/tools">
    <!-- Base application theme. -->
    <style name="Theme.JogoDescubraNumero" parent="Theme.MaterialComponents.DayNight.NoActionBar">
        <!-- Primary brand color. -->
        <item name="colorPrimary">@color/purple_500</item>
        <item name="colorPrimaryVariant">@color/purple_700</item>
        <item name="colorOnPrimary">@color/white</item>
        <!-- Secondary brand color. -->
        <item name="colorSecondary">@color/teal_200</item>
        <item name="colorSecondaryVariant">@color/teal_700</item>
        <item name="colorOnSecondary">@color/black</item>
        <!-- Status bar color. -->
        <item name="android:statusBarColor" tools:targetApi="l">?attr/colorPrimaryVariant</item>
        <!-- Customize your theme here. -->
    </style>
</resources>

As duas versões se alteraram quando mexi em uma e foi automático na 2. 




8-colors.xml
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <color name="purple_200">#FFBB86FC</color>
    <color name="purple_500">#FF6200EE</color>
    <color name="purple_700">#FF3700B3</color>
    <color name="teal_200">#FF03DAC5</color>
    <color name="teal_700">#FF018786</color>
    <color name="black">#FF000000</color>
    <color name="white">#FFFFFFFF</color>
</resources>

9-strings.xml

<resources>
    <string name="app_name">JogoDescubraNumero</string>
</resources>






