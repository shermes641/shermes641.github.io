layout: post
title:  "Create New User"
date:   2016-08-30 11:09:34 -0600
categories: jekyll update
---
- Goto http://data.powerhive.com/ph_admin/register/user
- Fill in form
- Click Register
- Goto http://data.powerhive.com/admin/auth/user/         ###SMH can create a user
- Click on the user previously created                    ###SMH nothing to click on and can not log in
- Fill in first name, last name, email, and phone number
- Select user type
- Save
- Goto permissions on django admin http://data.powerhive.com/admin/ph_model/permission/
- Click Add permission
- Select user and enter the PK of the grid to which you are granting permission
- Leave the Role and ItemType in default values
- Save
- Repeat adding permissions as necessary
