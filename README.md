<h1>Project Description</h1>

<p style="font-size: 15px;">The research team at my organization needs to update the file permissions for certain files and directories within the projects directory. The permissions do not currently reflect the level of authorization that should be given. Checking and updating these permissions will help keep their system secure.</p>

<h2>Tasks Performed</h2>

<p style="font-size: 15px;">To complete this task, I performed the following tasks:</p>

<ol>
  <li><strong>Check file and directory details:</strong> I used Linux commands to determine the existing permissions set for a specific directory in the file system.</li>
</ol>

<p style="font-size: 15px;">The following code demonstrates how I accomplished this:</p>

<div align="center">
  <img src="Picture1.jpg" alt="Project Image">
</div>

</br>
<p style="font-size: 15px;">The first line of the screenshot displays the command I entered, and the other lines display the output. The code lists all contents of the projects directory. I used the `ls` command with the `-la` option to display a detailed listing of the file contents that also returned hidden files. The output of my command indicates that there is one directory named "drafts," one hidden file named ".project_x.txt," and five other project files. The 10-character string in the first column represents the permissions set on each file or directory.</p>

</br>
</br>

<ol start="2">
  <li><strong>Description of the permission strings:</strong></li>
</ol>

<p style="font-size: 15px;">The 10-character string can be deconstructed to determine who is authorized to access the file and their specific permissions. The characters and what they represent are as follows:</p>

<ul>
  <li><strong>1st character:</strong> This character is either a `d` or hyphen (`-`) and indicates the file type. If it’s a `d`, it’s a directory. If it’s a hyphen (`-`), it’s a regular file.</li>
  <li><strong>2nd-4th characters:</strong> These characters indicate the read (`r`), write (`w`), and execute (`x`) permissions for the user. When one of these characters is a hyphen (`-`) instead, it indicates that this permission is not granted to the user.</li>
  <li><strong>5th-7th characters:</strong> These characters indicate the read (`r`), write (`w`), and execute (`x`) permissions for the group. When one of these characters is a hyphen (`-`) instead, it indicates that this permission is not granted for the group.</li>
  <li><strong>8th-10th characters:</strong> These characters indicate the read (`r`), write (`w`), and execute (`x`) permissions for others. This owner type consists of all other users on the system apart from the user and the group. When one of these characters is a hyphen (`-`) instead, it indicates that this permission is not granted for others.</li>
</ul>

<p style="font-size: 15px;">For example, the file permissions for `project_t.txt` are `-rw-rw-r--`. Since the first character is a hyphen (`-`), this indicates that `project_t.txt` is a file, not a directory. The second, fifth, and eighth characters are all `r`, which indicates that the user, group, and others all have read permissions. The third and sixth characters are `w`, which indicates that only the user and group have write permissions. No one has execute permissions for `project_t.txt`.</p>

</br>
</br>
<ol start="3">
  <li><strong>Changing file permissions:</strong></li>
</ol>

The organization determined that other shouldn't have write access to any of their files. To comply with this, I referred to the file permissions that I previously returned. I determined project_k.txt must have the write access removed for other.

The following code demonstrates how I used Linux commands to do this:

<div align="center">
  <img src="Picture2.jpg" alt="Project Image">
</div>

</br>
The first two lines of the screenshot display the commands I entered, and the other lines display the output of the second command. The `chmod` command changes the permissions on files and directories. The first argument indicates what permissions should be changed, and the second argument specifies the file or directory. In this example, I removed write permissions from `other` for the `project_k.txt` file. After this, I used the following command to review the updates I made:

</br>
</br>
<ol start="4">
  <li><strong>Changing file permissions on a hidden file:</strong></li>
</ol>






