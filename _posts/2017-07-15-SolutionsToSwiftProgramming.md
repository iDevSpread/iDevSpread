# Solutions to The Swift Programming Language 
> Write a function that compares two Rank values by comparing their raw values

```Swift
//: Playground - noun: a place where people can play

import UIKit

var str = "Hello, playground"

enum Rank: Int {
	case ace = 1
	case two, three, four, five, six, seven, eight, nine, ten
	case jack, queen, king
	
	func simpleDescription() -> String {
		switch self {
		case .ace:
			return "ace"
		case .jack:
			return "jack"
		case .queen:
			return "queen"
		case .king:
			return "kind"
		default:
			return String(self.rawValue)
		}
	}
	
	
}

// if declared outside of the enumeration, you can make use of it. 
func hasSameRank(first: Rank, second: Rank) -> Bool {
	return (first.rawValue == second.rawValue)
}

let ace = Rank.ace
let aceRawValue = ace.rawValue

let first = Rank.five
let second = Rank.ten

hasSameRank(first: first, second: second)

```