```mermaid
classDiagram
    class CUERPO TECNICO {
        +String titulo
        +String autores
        +String isbn
        +boolean isAvailable()
    }

    class PLANTEL {
        +String name
        +String memberId
        +borrowBook(Book book)
        +returnBook(Book book)
    }

    class UTILEROS {
        +String name
        +String employeeId
        +addBook(Book book)
        +removeBook(Book book)
    }

    class LOS DUEÑOS DE ROSARIO {
        +String name
        +List<Book> books
        +List<Member> members
        +List<Librarian> librarians
        +addMember(Member member)
        +removeMember(Member member)
    }

    Libro --> Library : contiene
    Member --> Library : registra
    Librarian --> Library : administra
