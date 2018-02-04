---
# 久々に普通のRailsAppを書いた
## @haito_linux

---
## やったこと
- たまには普通のRailsAppを書いてみたくなった
- 当初はなんか複合仕訳をいい感じにやろうとおもったが、本番サーバーの上でやらないと美味しくないのでやめた

---
## 普通のCommand
- rails app

```rb
module UserCommand
  module Follow
    refine User do
      def follow!(another_user)
        relationship.create!(user: self, following: another_user)
      end
    end
  end
end
```

---
## 普通のController
```rb
class FolloweesController < ApplicationController
  using UserCommands::Follow

  def create
    following_user = User.find(params[:id])
    current_user.follow!(following_user)
  end
end
```

---
## 普通じゃない
- DCIっぽいことをしたかった
- Rubyは「Moduleを外せない」ので無理。万策尽きた
- せめてContextを絞りたい
- `using Module { ... }` ができたらな〜〜

---
## ref
- https://gist.github.com/HaiTo/90037fbf2a7333b47bf164b0ba4dd1d2
- https://github.com/HaiTo/slightter
