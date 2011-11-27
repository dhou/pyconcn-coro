<!SLIDE subsection>
# Coroutine and Greenlet


<!SLIDE bullets incremental>
# Coroutine

* Micro-thread
* Suspend and resume execution
* Lightweight, runs on single OS thread


<!SLIDE bullets incremental>
# Greenlet

* Spin-off of Stackless
* C extension module on the default Python intepreter
* A greenlet is a coroutine
* No scheduler



<!SLIDE small>
# Greenlet Example
	@@@ python
	from greenlet import greenlet

	def test1():
		print 12
		gr2.switch()
		print 34

	def test2():
		print 56
		gr1.switch()
		print 78

	gr1 = greenlet(test1)
	gr2 = greenlet(test2)
	gr1.switch()
	

