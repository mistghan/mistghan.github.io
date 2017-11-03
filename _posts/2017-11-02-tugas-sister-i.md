---
layout: default
title: "SisTer"
tags: tag1 tag2
---

## Tugas I Sistem Terdistribusi

coding VB oleh asisten lab.


form_login.vb

```Visual Basic
 Public Class form_login

    Private Sub Button1_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button1.Click
        form_utama.Label15.Text = TextBox2.Text
        form_utama.Label16.Text = TextBox3.Text

        If TextBox1.Text = "admin" Then
            form_utama.ShowDialog()
        End If
    End Sub

    Private Sub Button2_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button2.Click
       Close()

    End Sub
 End Class
```


form_utama.vb

```Visual Basic
 Public Class form_utama

    Private Sub ComboBox1_SelectedIndexChanged(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles ComboBox1.SelectedIndexChanged 
        If ComboBox1.Text = "Mie Goreng" Then
            Label9.Text = 15000
        ElseIf ComboBox1.Text = "Mie Kuah" Then
            Label9.Text = 12000
        ElseIf ComboBox1.Text = "Nasi Goreng" Then
            Label9.Text = 20000
        End If
        TextBox1.Text = 0
    End Sub

    Private Sub TextBox1_TextChanged(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles TextBox1.TextChanged
        Label10.Text = TextBox1.Text * Label9.Text
        Label14.Text = Val(Label10.Text) + Val(Label12.Text)
    End Sub

    Private Sub ComboBox2_SelectedIndexChanged(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles ComboBox2.SelectedIndexChanged
        If ComboBox2.Text = "Air Putih" Then
            Label11.Text = 1000
        ElseIf ComboBox2.Text = "Es Teh" Then
            Label11.Text = 2000
        ElseIf ComboBox2.Text = "Es Jeruk" Then
            Label11.Text = 5000
        End If
        TextBox2.Text = 0
    End Sub

    Private Sub TextBox2_TextChanged(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles TextBox2.TextChanged
        Label12.Text = TextBox2.Text * Label11.Text
        Label14.Text = Val(Label10.Text) + Val(Label12.Text)
    End Sub
 End Class
```
