# sdl-learning
help idk what to do
#include <iostream>
#include "SDL.h"

using namespace std;



auto SDL_main(int argc, char* argv)
{

	SDL_Init(SDL_INIT_EVERYTHING);
	SDL_Window* wind;

	int h, w;
	char a, b;
	char name[512];
	cout << "do you want to create a window" << endl;
	cin >> a;

	if (a == 'y') {
		cout << "enter window height and weight" << endl;
		cin >> h >> w;

		cout << "name your window" << endl;
		cin >> name;



		wind = SDL_CreateWindow(name,
			SDL_WINDOWPOS_UNDEFINED,
			SDL_WINDOWPOS_UNDEFINED,
			w,
			h,
			SDL_WINDOW_RESIZABLE);

		cout << "do you wish to destroy window" << endl;
		cin >> b;

		if (b == 'y') {
			SDL_DestroyWindow(wind);
		}


	}

	SDLK_0;
	SDL_QUIT;

	return 0;


}
