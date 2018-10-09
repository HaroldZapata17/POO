#include <iostream>
#include <cstdlib>
#include <random>
using namespace std;

void tablero(){
  for(int i = 0; i < 9; i ++){
    cout << endl;
    cout <<"--|---|---|---|---|---|---|---|---| "<< endl;
  }
}

void juego(){
    // --- SUDOKU DONDE NOSOTROS LLENAMOS --- //
    int sudoku[9][9]= {};
    int suma[27]={};
    int cont = 0;
    for(int i=0; i < 9; i++){
        cout <<endl;
        cout << "--+---+---+---+---+---+---+---+---+ "<< endl;
        for(int j = 0; j < 9; j++){
            cin >> sudoku[i][j];
            cout << sudoku[i][j] << " | ";
        }
    }

    for(int i =0; i < 9; i++){
      for(int j = 0; j < 9; j++){
        suma[i]+=sudoku[i][j];
      }
    }

    for (int i = 0; i <9; i++){
      for(int j = 0; j < 1; j++){
        suma[9+j]+=sudoku[i][j];
      }
    }

    for (int i = 0; i <9; i++){
      for(int j = 1; j < 2; j++){
        suma[9+j]+=sudoku[i][j];
      }
    }

    for (int i = 0; i <9; i++){
      for(int j = 2; j < 3; j++){
        suma[9+j]+=sudoku[i][j];
      }
    }

    for (int i = 0; i <9; i++){
      for(int j = 3; j < 4; j++){
        suma[9+j]+=sudoku[i][j];
      }
    }

    for (int i = 0; i <9; i++){
      for(int j = 4; j < 5; j++){
        suma[9+j]+=sudoku[i][j];
      }
    }

    for (int i = 0; i <9; i++){
      for(int j = 5; j < 6; j++){
        suma[9+j]+=sudoku[i][j];
      }
    } 

    for (int i = 0; i <9; i++){
      for(int j = 6; j < 7; j++){
        suma[9+j]+=sudoku[i][j];
      }
    } 

    for (int i = 0; i <9; i++){
      for(int j = 7; j < 8; j++){
        suma[9+j]+=sudoku[i][j];
      }
    }  

    for (int i = 0; i <9; i++){
      for(int j = 8; j < 9; j++){
        suma[9+j]+=sudoku[i][j];
      }
    }

    for(int i = 0; i < 3; i++){
      for(int j= 0; j < 3; j++){
        suma[18]+=sudoku[i][j];
      }
    }

    for(int i = 0; i < 3; i++){
      for(int j= 3; j < 6; j++){
        suma[19]+=sudoku[i][j];
      }
    }

    for(int i = 0; i < 3; i++){
      for(int j= 6; j < 9; j++){
        suma[20]+=sudoku[i][j];
      }
    }

    for(int i = 3; i < 6; i++){
      for(int j= 0; j < 3; j++){
        suma[21]+=sudoku[i][j];
      }
    }

    for(int i = 3; i < 6; i++){
      for(int j= 3; j < 6; j++){
        suma[22]+=sudoku[i][j];
      }
    }

    for(int i = 3; i < 6; i++){
      for(int j= 6; j < 9; j++){
        suma[23]+=sudoku[i][j];
      }
    }


    for(int i = 6; i < 9; i++){
      for(int j= 0; j < 3; j++){
        suma[24]+=sudoku[i][j];
      }
    }

    for(int i = 6; i < 9; i++){
      for(int j= 3; j < 6; j++){
        suma[25]+=sudoku[i][j];
      }
    }

    for(int i = 6; i < 9; i++){
      for(int j= 6; j < 9; j++){
        suma[26]+=sudoku[i][j];
      }
    }
    
    for (int i = 0; i <27; i++){
      if(suma[i]==45){
        cont +=1;
      }
    }
  
    cout << endl;
    if(cont == 27){
      cout << "Juego finalizado con éxito";
    }

    else{
      cout << "Juego incompleto, revise datos";
    }
}

void juego2(){
    int sudoku[9][9]= {};
    int suma[27] = {};
    int cont = 0;
    //---SUDOKU DONDE SE LLENA ALEATORIAMENTE---//
    for(int i=0; i < 9; i++){
        cout <<endl;
        cout << "--+---+---+---+---+---+---+---+---+ "<< endl;
        for(int j = 0; j < 9; j++){
            sudoku[i][j] = 1 + (rand()%(0-9));
            cout << sudoku[i][j] << " | ";
        }
    }
    cout << endl;
    cout << "--+---+---+---+---+---+---+---+---+ ";

    for(int i =0; i < 9; i++){
      for(int j = 0; j < 9; j++){
        suma[i]+=sudoku[i][j];
      }
    }

    for (int i = 0; i <9; i++){
      for(int j = 0; j < 1; j++){
        suma[9+j]+=sudoku[i][j];
      }
    }

    for (int i = 0; i <9; i++){
      for(int j = 1; j < 2; j++){
        suma[9+j]+=sudoku[i][j];
      }
    }

    for (int i = 0; i <9; i++){
      for(int j = 2; j < 3; j++){
        suma[9+j]+=sudoku[i][j];
      }
    }

    for (int i = 0; i <9; i++){
      for(int j = 3; j < 4; j++){
        suma[9+j]+=sudoku[i][j];
      }
    }

    for (int i = 0; i <9; i++){
      for(int j = 4; j < 5; j++){
        suma[9+j]+=sudoku[i][j];
      }
    }

    for (int i = 0; i <9; i++){
      for(int j = 5; j < 6; j++){
        suma[9+j]+=sudoku[i][j];
      }
    } 

    for (int i = 0; i <9; i++){
      for(int j = 6; j < 7; j++){
        suma[9+j]+=sudoku[i][j];
      }
    } 

    for (int i = 0; i <9; i++){
      for(int j = 7; j < 8; j++){
        suma[9+j]+=sudoku[i][j];
      }
    }  

    for (int i = 0; i <9; i++){
      for(int j = 8; j < 9; j++){
        suma[9+j]+=sudoku[i][j];
      }
    }

    for(int i = 0; i < 3; i++){
      for(int j= 0; j < 3; j++){
        suma[18]+=sudoku[i][j];
      }
    }

    for(int i = 0; i < 3; i++){
      for(int j= 3; j < 6; j++){
        suma[19]+=sudoku[i][j];
      }
    }

    for(int i = 0; i < 3; i++){
      for(int j= 6; j < 9; j++){
        suma[20]+=sudoku[i][j];
      }
    }

    for(int i = 3; i < 6; i++){
      for(int j= 0; j < 3; j++){
        suma[21]+=sudoku[i][j];
      }
    }

    for(int i = 3; i < 6; i++){
      for(int j= 3; j < 6; j++){
        suma[22]+=sudoku[i][j];
      }
    }

    for(int i = 3; i < 6; i++){
      for(int j= 6; j < 9; j++){
        suma[23]+=sudoku[i][j];
      }
    }


    for(int i = 6; i < 9; i++){
      for(int j= 0; j < 3; j++){
        suma[24]+=sudoku[i][j];
      }
    }

    for(int i = 6; i < 9; i++){
      for(int j= 3; j < 6; j++){
        suma[25]+=sudoku[i][j];
      }
    }

    for(int i = 6; i < 9; i++){
      for(int j= 6; j < 9; j++){
        suma[26]+=sudoku[i][j];
      }
    }
    
    for (int i = 0; i <27; i++){
      if(suma[i]==45){
        cont +=1;
      }
    }
  
    cout << endl;
    if(cont == 27){
      cout << "Juego finalizado con éxito";
    }

    else{
      cout << "Juego incompleto, revise datos";
    }


}
int main() {
    juego2();
    return 0;
}
