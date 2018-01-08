# How to create your SSH Keys {#how-to-create-your-ssh-keys}



The first thing you need to do is go to your[command line](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html)and follow the[instructions](https://docs.gitlab.com/ee/ssh/README.html)to generate your SSH key pair.

1. Once you do that, login to GitLab with your credentials.

2. On the upper right corner, click on your avatar and go to your**Profile settings**.

   [![](https://docs.gitlab.com/ee/gitlab-basics/img/profile_settings.png "Profile settings dropdown")](https://docs.gitlab.com/ee/gitlab-basics/img/profile_settings.png)

3. Navigate to the**SSH keys**tab.

   [![](https://docs.gitlab.com/ee/gitlab-basics/img/profile_settings_ssh_keys.png "SSH Keys")](https://docs.gitlab.com/ee/gitlab-basics/img/profile_settings_ssh_keys.png)

4. Paste your**public**key that you generated in the first step in the 'Key' box.

   [![](https://docs.gitlab.com/ee/gitlab-basics/img/profile_settings_ssh_keys_paste_pub.png "Paste SSH public key")](https://docs.gitlab.com/ee/gitlab-basics/img/profile_settings_ssh_keys_paste_pub.png)

5. Optionally, give it a descriptive title so that you can recognize it in the event you add multiple keys.

   [![](https://docs.gitlab.com/ee/gitlab-basics/img/profile_settings_ssh_keys_title.png "SSH key title")](https://docs.gitlab.com/ee/gitlab-basics/img/profile_settings_ssh_keys_title.png)

6. Finally, click on**Add key**to add it to GitLab. You will be able to see its fingerprint, its title and creation date.

   [![](https://docs.gitlab.com/ee/gitlab-basics/img/profile_settings_ssh_keys_single_key.png "SSH key single page")](https://docs.gitlab.com/ee/gitlab-basics/img/profile_settings_ssh_keys_single_key.png)

> **Note:**Once you add a key, you cannot edit it, only remove it. In case the paste didn't work, you will have to remove the offending key and re-add it.

---

Congratulations! You are now ready to use Git over SSH, instead of Git over HTTP!

