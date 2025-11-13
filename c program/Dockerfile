# this part has the compiler and build tools
FROM gcc:bookworm AS builder
# RUN apt-get update && apt-get install -y build-essential
WORKDIR /app
COPY . /app

# makefile's "make" command runs here, so .o files, executable file are created inside /app folder
RUN make    

# this part has only the runtime environment
FROM debian:bookworm-slim
WORKDIR /app
COPY --from=builder /app/UserInterface /app/UserInterface
CMD ["./UserInterface"]
