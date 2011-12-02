<!SLIDE subsection>
# gogreen


<!SLIDE bullets incremental>
# gogreen

* Coroutine utilities package based on Greenlet
* Coroutine MySQL module
* Thread scheduler and others
* Includes pure Python web server corohttpd


<!SLIDE small>
# corohttpd Example

	@@@ python
	server = HttpServer(
		args = (('0.0.0.0', 7001), 'access.log'))
	file_handler = HttpFileHandler('/home/htdocs/')
	server.push_handler(file_handler)
	server.start()
	coro.event_loop()


<!SLIDE bullets incremental>
# How it works

* Everything is a coro.Thread
* HttpServer spawns HttpProtocol to handle requests
* HttpProtocol generates HttpRequest and sends to handler code
* Build higher level web framework on top



<!SLIDE bullets incremental>
# Why Coro

* Concurrency from a single thread
* Clean code


<!SLIDE bullets incremental>
# Caveats

* Custom coro based modules
* The code is the document


<!SLIDE bullets incremental>
# Get gogreen

## https://github.com/slideinc/gogreen


<!SLIDE subsection>
# Questions?

## Find me at

* github.com/dhou
* twitter.com/houyr
* weibo.com/dhouyr
* damienh.org
