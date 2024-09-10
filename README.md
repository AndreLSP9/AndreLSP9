package com.example.demo.rest;
package com.example.demo.entities;

import com.example.demo.entities.Livro;
import org.springframework.http.ResponseEntity;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RestController;

import java.util.ArrayList;

@RestController
public class TesteController {
    @GetMapping("/buscarLivro")
    public ResponseEntity<Livro> buscarLivro() {
        Livro livro = new Livro(1, "Biblia", "1");

        return ResponseEntity.ok(livro);
    }
    @GetMapping("/buscarLivros")
    public ResponseEntity<ArrayList<Livro>> buscarLivros() {
        Livro livro1 = new Livro(1, "Biblia", "1");
        Livro livro2 = new Livro(2, "Imitação de Cristo", "2");

        ArrayList<Livro> livros = new ArrayList<Livro>();


public class Livro {
    private int id;
    private String nome;
    private String isbn;

    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public String getNome() {
        return nome;
    }

    public void setNome(String nome) {
        this.nome = nome;
    }

    public String getIsbn() {
        return isbn;
    }

    public void setIsbn(String isbn) {
        this.isbn = isbn;
    }

    public Livro(int id, String nome, String isbn) {
        this.id = id;
        this.nome = nome;
        this.isbn = isbn;


    }
}
