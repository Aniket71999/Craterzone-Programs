#include <iostream>
#include "Quadtree_tester.h"
int main() {
	Quadtree_tester<double> tester;
	std::cout << "Starting Test Run" << std::endl;
	tester.run();
	std::cout << "Finishing Test Run" << std::endl;
	return 0;
}