# Introduction

## git and vs code
- installing git
- using 'git clone repository.git' to hard copy github repository
- remove .git folder (hidden in the repository)
- git config --global user.name 'name'
- git config --global user.email 'email'
- git init
- git add .
- git commit -m 'message'

# github and git
- create new repository in github
- git remote add origin yours.git
- git branch -M main
- git push -u origin main
- check status of the new github repository



def delete_student():
    student_id = entry_id.get()
    cursor.execute('SELECT * from DB_student where db_student_id = ?',(student_id,))
    delete = cursor.fetchall()
    cursor.execute('DELETE from DB_student where db_student_id = ?',(student_id,))
    print ('Following row is delete: ', delete)
    conn.commit()

botton_remove = tk.Button(root, text='Remove', command=delete_student)
botton_remove.pack(pady=25)