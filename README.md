# learning-go

This simple repo is created to track my Go language learning progress.



## Topics Covered

1. **govulncheck**: The provided link leads to a page discussing vulnerability checks for Go packages. However, `govulncheck` is not a default library in Go. It's a tool provided by Google to check for vulnerabilities in Go modules. It's not part of the standard Go toolchain.
    - [Go Vulnerability Checks](https://go.dev/doc/tutorial/govulncheck)
    - [Go Security Best Practices](https://go.dev/doc/security/best-practices)
    - [Go Package Documentation](https://pkg.go.dev/)

2. **Concurrency in Go**: Your explanation about Go's support for concurrency and running on multiple cores is accurate. Go's concurrency model with goroutines and channels is a significant feature that distinguishes it from some other languages.

3. **Resource Consumption**: Yes, Go is designed to be efficient in terms of resource consumption, which is often attributed to its statically compiled nature and its garbage collection mechanism.

4. **Compiled Language and Dependency Management**: Go being a compiled language is correct. When you build a Go program, it's compiled into a binary executable, making it easy to distribute and run across different platforms. Go's dependency management system (`go mod` introduced in Go 1.11) helps mitigate dependency hell.

5. **Formatting with gofmt**: Correct, `gofmt` is a tool for formatting Go code according to the official Go formatting guidelines.

6. **Package Organization**: Go heavily relies on packages for organizing and reusing code.

7. **Standard Library and Third-Party Packages**: You've listed examples of both standard library packages (`fmt`) and third-party packages (`gorilla/mux`). This is accurate. Go's standard library is extensive and well-designed, and third-party packages are generally designed to work seamlessly with it.

8. **Go Tools**: You've listed several useful Go tools. However, there's a slight error in the tool names:
    - **gofmt**: Correct.
    - **go run**: Compiles and runs Go programs.
    - **go get**: Used to download and install packages from the internet.
    - **godoc**: Generates documentation for Go code.
    - **go test**: Runs tests and benchmarks.
    - **go build**: Compiles packages and dependencies.
    - **go vet**: Analyzes Go code for potential issues.

## Go Module and Dependency Management

In Go, a module refers to a project's root directory. At the beginning of your development, you need to initialize the module using the command `go mod init <choose a name for your project>`. This will create a `.mod` file, which serves as a tracking tool for your dependencies installed via the `go get` command.

Your project will have one `.mod` file that automatically updates with the packages and their versions. Optionally, you may also have a `.sum` file that contains checksums for specific versions of dependencies used by your project.

Go also provides a module proxy, `proxy.golang.org`, which improves development workflows by caching module versions.

## Benefits of Packages in Go

- Encapsulation: Packages provide a scope for identifiers, allowing for encapsulation.
- Modularity: Promotes modular design by breaking down code into smaller, manageable units.
- Reusability: Facilitates code reuse through the importation of functionality from other packages.
- Namespace: Prevents naming conflicts by providing separate namespaces for identifiers.
- Scalability: Supports scalability of projects by providing a structured approach to code organization.
- Collaboration: Facilitates collaboration among developers by providing clear boundaries and interfaces.
- Testing: Facilitates unit testing by organizing test files alongside source code in the same package.

## Entry Point Package (main)

The main file that contains the `main` function serves as the entry point of your application. At compile time, the program starts execution from this function. The main package should only contain the `main` function, while other packages can contain any number of packages.

Example:
```go
func main() {
    fmt.Print("ezzops")
}
```
I import the fmt package to print out on the screen. I don't like that, but let's see tomorrow.

References:

Nana's GoLang course, and I extended the concepts using ChatGPT to understand.


