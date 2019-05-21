# Concurrency-First Development in Golang

Traditional Concurrency Primitives
Go concurrency primitives
Getting into trouble
Getting out of trouble

Traditional concurrency programming is difficult because it forces the developer to think from the perspective of data at rest. Concurrent programming should create applications that are capable of doing many things at once, but also provide clarity when synchronicity is needed. Go is a language developed by Google that turns the old model on its head. This talk focuses on the concurrency primitives and how to use them effectively, so that a dev new to the language can know how to get their feet wet.

It puts them on the defensive; it has mutexes and semaphores to protect values from race conditions.

How do we flip the script and give power to the thread, rather than the address? By creating actors that receive signal and own their own state, we can decentralize and build evolved applications. Many languages approach concurrency in a structured way, and some employ the actor model, but golang is one of the very few that does it in the base library. This talk explores the freedom of concurrent programming in Go, and should set you up for success the next time you use it.

Concurrent programming is hard, mainly because the traditional tools contradict a more natural way of thinking. Mutexes and semaphores are value-centric tools for protecting integrity, but humans think in trains of thought and sequences of events. Golang, and the actor model of programming flow, work together extremely well. In this talk we’ll go over examples of advancing complexity, and by the end you should feel confident enough to Go on your own.

Channel Lifecycle
Collections, FanIn, Fanout
Natural Selection (select, making tough decisions more natural)

Ball Hockey
Players passing to each other, ease of state corruption
Ability to add/remove players dynamically
Can we show that tighter waits produce higher likeliness of state corruption?

Divergence

Golang Nuances
architecture-targeted compilation (x64, x86, arm, arm64, ppc64, ppc64le, mips64, mips64le
no generics (retaining type safety might require some extra boilerplate)
no versioning (use git or other addon)
robust concurrency primitives
memory management
runtime, but no vm

go 1.9
minor release every 8 or so months
type aliases
math/bits for doing low level math with special CPU functions
sync.Map for concurrent safe maps (best used as add-only)
testing helpers
time improvements to track leap seconds
compiler now compiles functions concurrently!

Go is right for 
High-concurrency or high-contention requirements
high performance
low resource (works best in multi-proc systems, but excels single-proc low memory low disk as well)
getting really close to the system without being hampered by archaic syntax

Simple syntax
no semicolons
:= declare/assign operator
multiple returns
& reference and * dereference
export with uppercase, private with lowercase

Error handling
return errors rather than try catch

