Day 8 - ����ǰ��


���ڸ��ӵ�HTMLǰ��ҳ����˵��������Ҫһ�׻�����CSS��������ҳ�沼�ֺͻ�����ʽ�����⣬jQuery��Ϊ����DOM��JavaScript��Ҳ�ز����١�

���㿪ʼдCSS����ֱ�Ӵ�һ�����еĹ������Ƶ�CSS��ܿ�ʼ���кܶ�CSS��ܿɹ�ѡ���������ѡ��uikit���ǿ���CSS��ܡ����߱����Ƶ���Ӧʽ���֣�Ư����UI���Լ��ḻ��HTML�������������������Ƴ����۶�����ҳ�档

���Դ�uikit��ҳ���ش������Դ�ļ���

���еľ�̬��Դ�ļ�����ͳһ�ŵ�www/staticĿ¼�£������������ࣺ

static/
+- css/
|  +- addons/
|  |  +- uikit.addons.min.css
|  |  +- uikit.almost-flat.addons.min.css
|  |  +- uikit.gradient.addons.min.css
|  +- awesome.css
|  +- uikit.almost-flat.addons.min.css
|  +- uikit.gradient.addons.min.css
|  +- uikit.min.css
+- fonts/
|  +- fontawesome-webfont.eot
|  +- fontawesome-webfont.ttf
|  +- fontawesome-webfont.woff
|  +- FontAwesome.otf
+- js/
   +- awesome.js
   +- html5.js
   +- jquery.min.js
   +- uikit.min.js
   

����ǰ��ҳ��϶���ֹ��ҳһ��ҳ�棬ÿ��ҳ�涼����ͬ��ҳü��ҳ�š�
���ÿ��ҳ�涼�Ƕ�����HTMLģ�壬��ô�������޸�ҳü��ҳ�ŵ�ʱ�򣬾���Ҫ��ÿ��ģ�嶼��һ�飬����Ȼ��û��Ч�ʵġ�

������ģ�������Ѿ����ǵ���ҳ�����ظ���HTML���ֵĸ������⡣

�е�ģ��ͨ��include��ҳ���������֣�
<html>
    <% include file="inc_header.html" %>
    <% include file="index_body.html" %>
    <% include file="inc_footer.html" %>
</html>

��������ͬ�Ĳ���inc_header.html��inc_footer.html�Ϳ��Թ���

����include����������ҳ������ṹ��ά����


jinjia2��ģ�廹����һ�֡��̳С���ʽ��ʵ��ģ��ĸ��ø��򵥡�

���̳С�ģ��ķ�ʽ��ͨ����дһ������ģ�塱���ڸ�ģ���ж���һЩ���滻��block���飩��
Ȼ�󣬱�д�������ģ�塱��ÿ����ģ�嶼����ֻ�滻��ģ�嶨���block��

���磬����һ����򵥵ĸ�ģ�壺
<!-- base.html -->
<html>
    <head>
        <title>{% block title%} ���ﶨ����һ����Ϊtitle��block {% endblock %}</title>
    </head>
    <body>
        {% block content %} ���ﶨ����һ����Ϊcontent��block {% endblock %}
    </body>
</html>







������ģ��a.html��ֻ��Ҫ�Ѹ�ģ���title��content�滻����

{% extends 'base.html' %}

{% block title %} A {% endblock %}

{% block content %}
    <h1>Chapter A</h1>
    <p>blablabla...</p>
{% endblock %}



������ģ��b.html���編���ƣ�

{% extends 'base.html' %}

{% block title %} B {% endblock %}

{% block content %}
    <h1>Chapter B</h1>
    <ul>
       <li>list 1</li>
       <li>list 2</li>
    </ul>
{% endblock %}
������һ������ø�ģ������岼�ֺ�CSS��ʽ����д��ģ��ͻ�ǳ����ס�