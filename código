package com.example.myapplication

import android.os.Bundle
import androidx.activity.ComponentActivity
import androidx.activity.compose.setContent
import androidx.compose.foundation.layout.*
import androidx.compose.material3.*
import androidx.compose.runtime.Composable
import androidx.compose.runtime.mutableStateOf
import androidx.compose.runtime.remember
import androidx.compose.ui.Alignment
import androidx.compose.ui.Modifier
import androidx.compose.ui.unit.dp
import androidx.compose.ui.tooling.preview.Preview
import com.example.myapplication.ui.theme.MyApplicationTheme

class MainActivity : ComponentActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContent {
            MyApplicationTheme {
                // A surface container using the 'background' color from the theme
                Surface(
                    modifier = Modifier.fillMaxSize(),
                    color = MaterialTheme.colorScheme.background
                ) {
                    MyScreen()
                }
            }
        }
    }
}

@Composable
fun MyScreen() {
    val text1 = remember { mutableStateOf("Nombre ( ͡❛‿‿ ͡❛)") }
    val text2 = remember { mutableStateOf("( ͡▀̿ ‿‿ ͡▀̿ Pasatiempo )") }
    val text3 = remember { mutableStateOf("Color favorito(っ ̿͡ ‿‿ ̿͡  )っ 3") }
    val buttonClicked = remember { mutableStateOf(false) }

    Column(
        modifier = Modifier
            .fillMaxSize()
            .padding(16.dp),
        horizontalAlignment = Alignment.CenterHorizontally,
        verticalArrangement = Arrangement.Center
    ) {
        Text(text = text1.value, modifier = Modifier.padding(bottom = 8.dp))
        Text(text = text2.value, modifier = Modifier.padding(bottom = 8.dp))
        Text(text = text3.value, modifier = Modifier.padding(bottom = 16.dp))

        Button(onClick = {
            buttonClicked.value = true
            text1.value = "Marcos Ambrocio"
            text2.value = "Videojuegos y dibujar"
            text3.value = "Morado"
        }) {
            Text("Presionar")
        }

        if (buttonClicked.value) {
            Text(text = "¡Ahora vas tú (っ ͡◣‿‿ ͡◢)っ!")
        }
    }
}

@Preview(showBackground = true)
@Composable
fun DefaultPreview() {
    MyApplicationTheme {
        MyScreen()
    }
}
