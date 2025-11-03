CPU usage controll


50 percent	docker run --cpu-quota=50000 --cpu-period=100000 image
25 percent	docker run --cpu-quota=25000 --cpu-period=100000 image
200 percent (2 cores)	docker run --cpu-quota=200000 --cpu-period=100000 image

