proc fibonacci { a b n} {
set fib {}
set fib [linsert $fib 0 $a]
set fib [linsert $fib 1 $b]

for {set i 2} {$i < $n} {incr i} {
  lappend fib [expr [lindex $fib [expr $i -1]]+[lindex $fib [expr $i -2]]]
}
 return $fib
}

puts "num1:"
gets stdin num1
puts "num2"
gets stdin num2
puts "length?"
gets stdin len
puts [fibonacci $num1 $num2 $len]