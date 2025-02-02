# Hub Admin Privileges

```{note}
Curious about admin privileges in Datahub? If yes, read below!

```

**What does admin privilege in the hub mean?**

Admin privilege provides the necessary features required to troubleshoot students notebook interface in the hub. If you are an admin user, you can do the following,

1. You can start and stop the students' server in your dedicated hub
2. You can access the student server to debug issues in their notebook

```{warning}
Admin privileges are hub-wide. If you have a GSI teaching your course using a particular hub but are also a student in another course using the same hub, this can result in a conflict of interest. Please report such issues to the infrastructure admin team so that we can take the necessary corrective action.
```

Check this image to know your privileges for the admin option

```{figure} ../images/admin.png
:width: 500px
:align: center
:name: Datahub Admin

Here is how the admin dashboard looks like!
```

**How do I get access to the admin option?**

We generally recommend the teaching team alone have admin access in the hubs they use for the instructional purposes. If you are part of the teaching team and require admin access, please create a request using this [template](https://github.com/berkeley-dsep-infra/datahub/issues/new?assignees=&labels=support&template=admin_request.yml). The infrastructure admins will assist with the process of assigning admin privileges to the instructors.

```{note}
This process has undergone a major change. You no longer need to provide the list of usernames for the staff who require admin access. You just need to provide the bcourses ID for all the courses for which you require admin access.
```

To assign admin privileges to a set of people other than all course staff, for example a subset of them, please do the following:
- In order to assign people to a group, they must have the role of "student". By default, course staff are either "teacher" or "ta", but they can be assigned more than one role. Visit the `People` section and click `+ People`. Specify the users' email addresses and make sure the Role is set to `Student`.
- Create a [bcourses group](https://community.canvaslms.com/t5/Instructor-Guide/How-do-I-manually-create-groups-in-a-group-set/ta-p/700). The first step will be to create a groupset and then create a group inside it. For example, you can title the groupset "Staff Groups" and the group "Hub Admins".
- [Add people to the created group](https://community.canvaslms.com/t5/Instructor-Guide/How-do-I-manually-assign-students-to-groups/ta-p/663).
- Share the bcourses ID in the Github template. The admins will make changes to the Datahub configuration to enable this feature. If you are assigning privileges to a group of people other than course staff, specify this in the Github issue.
- Once admin privileges are assigned to jupyterhub groups based on the [Datahub documentation](https://docs.datahub.berkeley.edu/en/latest/admins/howto/course-config.html#assigning-scopes-to-roles), the people being granted those privileges will need to logout of the hub and then log in again for the config changes to persist. This is not the same thing as stopping and starting the server -- users need to click "Logout".
- You will be able to access the admin interface in the UI by navigating to "<Hub URL>/hub/admin" and check for the admin status of varied users. You will also be able to use the "Manage groups" option in the admin interface to check the bcourses id of courses with admin privileges.

```{note}
If you need any help in this process of creating bcourses groups, please reach out to bcourseshelp@berkeley.edu
```

**How do I navigate the admin portal?**

Please follow the steps below to navigate admin interface,

- Login to your hub instance
- Click the admin option from the top bar

```{figure} ../images/adminaccess.PNG
:width: 500px
:align: center
:name: Datahub Admin snapshot

Here is where you can find admin option!
```
- Once  you click, you have access to instances of users and admins in that specific hub

```{note}
If you are using the R hub, then you may need to follow the below steps,

- You can replace https://r-staging.datahub.berkeley.edu/user/your-calnet-id/rstudio/ with https://r-staging.datahub.berkeley.edu/hub/admin to access the admin interface.
- You can use https://r-staging.datahub.berkeley.edu/hub/home to restart your server.
```

**How do I start a student server?**

- Click on the control panel

```{figure} ../images/controlpanel.PNG
:width: 500px
:align: center
:name: Control Panel

Here is how the control panel option looks like!
```
- Click admin option

```{figure} ../images/adminaccess.PNG
:width: 500px
:align: center
:name: Datahub Admin snapshot

Here is where you can find admin option!
```
- Find the user whose server you want to restart.

```{figure} ../images/user.PNG
:width: 500px
:align: center
:name: User List

Here is how to search for an user!
```
- Click restart server option

**How do I stop a student server?**

- Click the control panel option
- Click admin option
- Find the user whose server you want to stop.
- Click stop server option

**How can I access the instance of a student server?**

- Click the control panel option
- Click admin option
- Search the calnet id of the student's instance you want to access
- Click access server option to access student's instance


```{figure} ../images/accessserver.PNG
:width: 500px
:align: center
:name: Access Server

Here is how to access a server's instance!
```
