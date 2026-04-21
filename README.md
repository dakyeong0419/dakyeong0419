# 👋 Hello, I'm 김다경!

<p align="center">
  <img src="https://raw.githubusercontent.com/github/explore/main/topics/python/python.png" width="200"/>
</p>

```python
class KimDaKyung:
    def __init__(self):
        self.name = "김다경"
        self.age = 20
        self.university = "한신대학교"
        self.major = "AI·SW"

        self.personality = ["밝음", "끈기 있음", "꾸준함"]
        self.interest = ["AI", "데이터", "코딩", "문제 해결"]
        self.goal = "꾸준히 성장하는 개발자 💻"

    def introduce(self):
        return f"""
        안녕하세요 :)
        저는 {self.university}에서 {self.major}를 전공하고 있는 {self.name}입니다.

        아직은 배우는 단계이지만,
        하나씩 직접 만들어보며 성장하는 것을 좋아합니다.
        """

me = KimDaKyung()
print(me.introduce())
