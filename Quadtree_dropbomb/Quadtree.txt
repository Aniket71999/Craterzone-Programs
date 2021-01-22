#ifndef QUADTREE_H
#define QUADTREE_H

#ifndef nullptr
#define nullptr 0
#endif

#include "ece250.h"
#include "Quadtree_node.h"
#include "Exception.h"
#include <iostream>

template <typename Type>
class Quadtree {
	private:
		Quadtree_node<Type> *tree_root;
		int count;

	public:
		Quadtree();
		~Quadtree();
		int size() const;
		bool empty() const;
		Type min_x() const;
		Type min_y() const;
		Type max_x() const;
		Type max_y() const;
		Type sum_x() const;
		Type sum_y() const;
		Quadtree_node<Type> *root() const;
		bool member( Type const &, Type const & ) const;
		void insert( Type const &, Type const & );
		void clear();
	template <typename T>
	friend std::ostream &operator<<( std::ostream &, Quadtree<T> const & );
};
template <typename Type>
Quadtree<Type>::Quadtree():
tree_root( 0 ),
count( 0 ) {
}
template <typename Type>
Quadtree<Type>::~Quadtree() {
}
template <typename Type>
int Quadtree<Type>::size() const {
	return 0; }
template <typename Type>
bool Quadtree<Type>::empty() const {
	return true; }
template <typename Type>
Type Quadtree<Type>::min_x() const {
	return Type(); }
template <typename Type>
Type Quadtree<Type>::min_y() const {
	return Type();}
template <typename Type>
Type Quadtree<Type>::max_x() const {
	return Type(); }
template <typename Type>
Type Quadtree<Type>::max_y() const {
	return Type(); }
template <typename Type>
Type Quadtree<Type>::sum_x() const {
	return Type(); }
template <typename Type>
Type Quadtree<Type>::sum_y() const {
	return Type(); }
template <typename Type>
Quadtree_node<Type> *Quadtree<Type>::root() const {
	return 0; }
template <typename Type>
bool Quadtree<Type>::member( Type const &x, Type const &y ) const {
	return false; }
template <typename Type>
void Quadtree<Type>::insert( Type const &x, Type const &y ) { }
template <typename Type>
void Quadtree<Type>::clear() { }
template <typename T>
std::ostream &operator<<( std::ostream &out, Quadtree<T> const &qt ) {
	return out; }
#endif