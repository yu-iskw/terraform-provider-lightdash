# Copyright 2023 Ubie, inc.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#      https://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.


default: testacc

# Run acceptance tests
.PHONY: testacc
testacc:
	TF_ACC=1 go test ./... -v $(TESTARGS) -timeout 120m

build:
	go build -v ./

format:
	go fmt ./internal/...

install:
	go build -v ./ && go install .

test:
	cd "internal/" && TF_ACC=1 go test -count=1 -v ./...

gen-docs:
	go generate ./...

tidy:
	go mod tidy

setup-dev: setup-pre-commit

setup-pre-commit:
	pre-commit install

run-pre-commit:
	pre-commit run --all-files