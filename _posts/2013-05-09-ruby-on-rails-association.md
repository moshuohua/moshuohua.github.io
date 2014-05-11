---
layout: post
title: Ruby on Rails 表关联使用小总结
category: code
---

#{{ page.title }}

<p class="meta">15 May 2013</p>

最近一直在写信息系统设计的作业，我们小组做了一个关于团队任务管理的应用，这是一个用于小型团队的在线任务管理程序，逻辑非常简单，就是基于项目为核心。由于刚刚学习 `rails` 没多久，很喜欢，于是决定用这个来开发。我们的逻辑是每个项目有一个发起者，其他人可以加入项目，也可以退出项目，同时自己也可以发起项目，简单说项目和用户这两个 `model` 之间是多对多关系，那么就需要用到 `association` 了，将两个表之间建立一定的联系

对于各种模式，我这里就不熬述了，官方文档说的很清楚，其他教程也很多，例如这里，重点说一下 `many to many`

##Many-To-Many

这里事先有两个 `model` 一个叫做 `project`，另一个叫做 `user`，当然这里是用的 `devise` 的 `User`，我们再建立一个 `model` 名字叫做 `duty` ， 这个模型用来搭建前两个模型的联系

```ruby
rails g model duty project_id:integer user_id:integer
```

其中后两者定义了两个 `Foreign Keys` ，`project_id` 会与 `Project` 表的 `id` 建立一一对应， `user_id` 对应 `User` 的 `id` ，这样一来便搭建了一个 `Join Table`，一个只包含外键的模型

三个模型在关系上的代码如下:

```ruby
class User < ActiveRecord::Base
    has_many :duties
    has_many :projects, :through => :duties
 end

class Duty < ActiveRecord::Base
    belongs_to :user
    belongs_to :project
end

class Project < ActiveRecord::Base
    has_many :duties
    has_many :users, :through => :duties
end
```

那么无论是在 `view` 或者 `controller` 中，按照以下代码便可创建一个新的关联（具体变量视情况而定）：

创建指定 `project` 与 `user` 之间的联系

```ruby
Duty.create!(:project_id => @project.id, :user_id => @user.id)
```

删除指定的一个关联

```ruby
Duty.find_by_project_id_and_user_id(@project.id,@user.id).destroy
```

删除与指定 `project` 相关的所有关联

```ruby
Duty.find_by_project_id(@project.id).destroy
```

删除与指定 `user` 相关的所有关联

```ruby
Duty.find_by_user_id(@user.id).destroy
```

类似关注用户，参加一个小组等等的功能，都可以这样来设计一下，不同的联系用不同的中间模型来处理关联，不仅方便业务逻辑处理，也非常方便一些关于 `feed` 或者 `动态列表` 的功能的实现

例如以上例子中，如果想要动态显示项目与用户之间的关系，就可以调用 `Duty` 的数据操作来显示变化

##参数介绍

无论是 `belongs_to`，`has_one`，还是 `has_many` ，都可以添加一些参数，以下列举几个

**class_name**

可以将关联的类别名称换成你想要的名称，示例代码如下:

```ruby
class Doc < ActiveRecord::Base
    belongs_to :Project, :class_name => "Task"
 end
```

需要注意的是在这里 `Task` 是 `Doc` 的父级，也就是 `Project`，只不过在这个关联中重新命名而已

**foreign_key**

```ruby
class Doc < ActiveRecord::Base
    belongs_to :Project, :class_name => "Task", :foreign_key => "project_id"
 end
```

**order**

`has_many` 可以通过 `:order` 来指定顺序

```ruby
class User < ActiveRecord::Base
    has_many :project, :order => "id desc"
    #...
 end
```

**dependent**

例如需要删除一个项目，然后项目下的文档便全部失效，同时删除等等，就需要用到 `dependent`

```ruby
class Project < ActiveRecord::Base
    has_many :docs, :dependent => :destroy 
    #...
 end
```

这样在项目删除的时候，相应的其关联的文档也会全部删除，如果参数改为 `delete`，则不会全部删除

好了，这次先写这么多，以后还会陆续写一些经验，并且及时修改更正

Enjoy！







