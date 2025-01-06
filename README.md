# Zabbix Email HTML Templates with your company logo


## Description  
These HTML templates for Zabbix notifications are designed to enhance the user experience by using improved message templates.  


## Table of Contents  

<!-- TOC tocDepth:2..3 chapterDepth:2..6 -->

- [Zabbix Email HTML Templates with your company logo](#zabbix-email-html-templates-with-your-company-logo)
  - [Description](#description)
  - [Table of Contents](#table-of-contents)
  - [Requirements](#requirements)
  - [HTML Email Notification Templates](#html-email-notification-templates)
    - [Template Views](#template-views)
    - [Installation and Usage](#installation-and-usage)

<!-- /TOC -->

## Requirements  
- Zabbix >= 6.4  


## HTML Email Notification Templates

### Template Views    

<div style="width: 100%; display: flex; flex-direction: row;">
  <img src="img/problem_template.png" alt="Problem Template" style="width: 31%; margin: 5px;">
  <img src="img/resolve_template.png" alt="Resolve Template" style="width: 30%; margin: 5px;">
  <img src="img/update_template.png" alt="Update Template" style="width: 30%; margin: 5px;">
</div>


### Installation and Usage  

1. Add your company logo and name to the files in the `html_templates` folder by changing lines 16, 18, 19, and 203:  
   ```bash
    <a href="https://www.YOUR_COMPANY.com" style="text-decoration:none" # replace with your company website
    <img src="https://99designs-blog.imgix.net/blog/wp-content/uploads/2016/07/logo-2.png" # replace with your company logo
    alt="logo YOUR_COMPANY" # replace with your company name
    2024 YOUR_COMPANY Zabbix </p>
   ```

2. Insert the template texts in the Zabbix WEB-UI: *Alerts -> Media types -> Email (HTML) -> Message templates*     
   ![Update Template](img/media_type_html.png)  

3. The title format for email templates:  
       - *your_company_problem_template*: `Problem: {HOST.NAME}: {EVENT.NAME}`  
       - *your_company_resolve_template*: `Resolved in {EVENT.DURATION}: {EVENT.NAME}`   
       - *your_company_problem_update_template*: `Updated problem in {EVENT.AGE}: {EVENT.NAME}`  
     
