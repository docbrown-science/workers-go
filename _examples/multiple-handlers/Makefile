.PHONY: dev
dev:
	wrangler dev --test-scheduled

.PHONY: build
build:
	go run ../../cmd/workers-assets-gen -mode=go
	GOOS=js GOARCH=wasm go build -o ./build/app.wasm ./...

.PHONY: deploy
deploy:
	wrangler deploy
