## Linux File Permissions and Ownership Lab

### Overview

This hands-on Linux lab focused on managing **file and directory permissions** and **file ownership** using Bash commands.

During the lab, I practiced:

* Checking file and directory permissions
* Understanding Linux permission notation
* Changing permissions with `chmod`
* Using numeric and symbolic permission notation
* Changing file ownership with `chown`
* Verifying permission changes with `ls`
* Working with Linux users, groups, and other users

These skills are important for **IT Support, Linux administration, and cybersecurity** because incorrect permissions can prevent users from accessing resources or allow unauthorized access.

---

### Lab Type

Hands-on Linux File Permissions and Ownership Lab

#### Operating System

Linux

#### Environment

* Qwiklabs Linux environment
* Bash shell
* Linux command line

#### Tools & Commands

* `ls`
* `ls -l`
* `ls -ld`
* `cd`
* `chmod`
* `chown`
* `sudo`

---

## Learning Objectives

The main objectives of this lab were:

1. Learn how to change permissions for files and directories.
2. Learn how to change ownership of files and directories.
3. Understand the difference between the **owner**, **group**, and **others**.
4. Practice both numeric and symbolic `chmod` syntax.
5. Verify permission and ownership changes using `ls`.

The lab specifically focused on changing permissions and ownership in a Linux environment.

---

## Checking File Permissions

To view the permissions of a file:

```bash
ls -l
```

The lab used `ls -l` to examine the permissions of files.

![2](https://i.imgur.com/PluLt9r.png)

---

## Changing File Permissions with chmod

The `chmod` command changes permissions.

Basic syntax:

```bash
chmod PERMISSIONS FILE
```

The lab changed `important_document` so that the owner received read, write, and execute permissions while the group and others received no permissions.

![4](https://i.imgur.com/vdW9OwM.png)

---

## Checking Directory Permissions

When checking the permissions of a directory itself, use:

```bash
ls -ld DIRECTORY
```

The `-d` option tells `ls` to display information about the directory itself rather than its contents. The lab specifically used `ls -ld` for this purpose.

---

## Changing Directory Permissions

The lab also demonstrated changing permissions on a directory called:

```text
secret_folder
```

The required permissions were:

1. Owner → all permissions
2. Group → write only
3. Others → no permissions

The final permission state was:

```text
drwx-w----
```

![2](https://i.imgur.com/2rxxf6V.png)

The lab also emphasized that changing the permissions of a directory does **not automatically change the permissions of the files inside it**.

---

## Changing File Ownership

Linux files have an owner.

The `chown` command is used to change ownership.

Basic syntax:

```bash
chown USER FILE
```

The lab changed the owner of the `taco` directory from `root` to the user `cook`.

![2](https://i.imgur.com/AVO4ybw.png)


---

## Practice: not_so_important_document

The lab included another practice file:

```text
not_so_important_document
```

Its original permissions were:

```text
-rw-r-----
```

The final permission state was:

```text
-rwxrw-r--
```

This demonstrates how symbolic `chmod` commands can be used to add permissions incrementally.

![2](https://i.imgur.com/tKNHTDK.png)

---

## Practice: public_document

Another file in the lab was:

```text
public_document
```

The final permissions were:

```text
-rwxrwxrwx
```

This means everyone has full permissions.

The lab demonstrated that symbolic `chmod` can add multiple permissions at once.

![2](https://i.imgur.com/GvIwQR2.png)

---

### Permission Management Workflow

A useful troubleshooting workflow is:

```text
1. Identify the file/directory
          ↓
2. Check permissions
          ↓
3. Check owner/group
          ↓
4. Determine required access
          ↓
5. Use chmod or chown
          ↓
6. Verify the result
```

---

### IT Support Relevance

Understanding Linux permissions is important for IT Support because users can experience problems such as:

* "Permission denied"
* Unable to open a file
* Unable to modify a file
* Unable to access a directory
* Application cannot access required files
* Incorrect ownership
* Incorrect group permissions

---

### Cybersecurity Relevance

Linux permissions are also an important cybersecurity concept.

Incorrect permissions can result in:

* Unauthorized file access
* Unauthorized modification
* Data exposure
* Privilege-related security issues
* Users accessing resources they do not need

For example:

```text
-rwxrwxrwx
```

allows everyone to read, write, and execute the file.

In contrast:

```text
-rwx------
```

restricts access to the owner.

This is why permission management is an important part of securing Linux systems.

---

### Troubleshooting Scenario

#### Scenario

A user tells you:

> "I can see the file, but Linux says Permission denied when I try to modify it."

#### Step 1 — Check permissions

```bash
ls -l filename
```

#### Step 2 — Check the owner and group

Look at the output:

```text
-r--r----- 1 root admins 100 file.txt
```

The file is owned by:

```text
root
```

The group is:

```text
admins
```

#### Step 3 — Determine the user's required access

If the user needs to modify the file, they need appropriate **write permission**.

#### Step 4 — Correct the permission or ownership

An administrator could use `chmod` or `chown`, depending on the situation.

#### Step 5 — Verify

```bash
ls -l filename
```

Always verify the result after making a permission change.

---

### Key Concepts Learned

| Concept              | What I Learned                        |
| -------------------- | ------------------------------------- |
| `ls -l`              | View file permissions and ownership   |
| `ls -ld`             | View directory permissions            |
| `chmod`              | Change permissions                    |
| Numeric permissions  | Use values such as `700`              |
| Symbolic permissions | Use `u`, `g`, `o`, `a`, `+`, and `-`  |
| `chown`              | Change file ownership                 |
| Owner                | User who owns the file                |
| Group                | Group associated with the file        |
| Others               | Everyone else                         |
| `r`                  | Read                                  |
| `w`                  | Write                                 |
| `x`                  | Execute                               |
| `sudo`               | Run commands with elevated privileges |

---

## Skills Demonstrated

#### Linux

* Linux command line
* Bash
* File permissions
* Directory permissions
* File ownership
* User and group permissions
* Permission troubleshooting

#### Commands

```bash
ls
ls -l
ls -ld
cd
chmod
chown
sudo
```

#### Cybersecurity Skills

* Access control
* Least privilege
* Permission auditing
* Linux security fundamentals
* Unauthorized access prevention
* Security troubleshooting

---

### Lab Results

During this lab, I successfully practiced:

* Checking file permissions
* Checking directory permissions
* Changing file permissions with numeric `chmod`
* Changing permissions with symbolic `chmod`
* Adding permissions
* Removing permissions
* Changing directory permissions
* Changing file ownership with `chown`
* Verifying changes using `ls`

The lab concludes with successful use of `chmod` on both files and directories and successful use of `chown` to change ownership.

---

## Portfolio Skills

**Linux | Bash | File Permissions | chmod | chown | User Access | Groups | Access Control | Least Privilege | Linux Security | IT Support | Troubleshooting | Cybersecurity**
