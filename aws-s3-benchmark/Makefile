all:  build-images-with-1m-data build-images-with-10m-data build-images-with-100m-data build-images-with-500m-data

build-images-with-1m-data:
	cp data/01_raw/train-1MB.csv data/01_raw/train.csv
	docker build -t aws-s3-benchmark-with-1m-data:latest -f Dockerfile .

build-images-with-10m-data:
	cp data/01_raw/train-10MB.csv data/01_raw/train.csv
	docker build -t aws-s3-benchmark-with-10m-data:latest -f Dockerfile .

build-images-with-100m-data:
	cp data/01_raw/train-100MB.csv data/01_raw/train.csv
	docker build -t aws-s3-benchmark-with-100m-data:latest -f Dockerfile .

build-images-with-500m-data:
	cat data/01_raw/train-500MB-seg-* > data/01_raw/train-500MB.csv
	rm -f data/01_raw/train-500MB-seg-*
	cp data/01_raw/train-500MB.csv data/01_raw/train.csv
	docker build -t aws-s3-benchmark-with-500m-data:latest -f Dockerfile .

