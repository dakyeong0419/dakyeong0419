from PIL import Image, ImageDraw
import matplotlib.pyplot as plt

class KimDaKyung:
    def __init__(self):
        self.name = "김다경"
        self.age = 20
        self.university = "한신대학교"
        
        # 프로필 이미지 (기존 이미지 경로)
        self.profile_image = "/mnt/data/a_close_up_indoor_selfie_portrait_scene_a_young_e.png"
        
        # 컴퓨터 이미지 경로
        self.computer_image = "/mnt/data/computer.png"
        
        # 컴퓨터 이미지 자동 생성
        self.create_computer_image()
    
    def introduce(self):
        return f"안녕하세요! 저는 {self.university}에 다니는 {self.age}살 {self.name}입니다."
    
    def create_computer_image(self):
        img = Image.new('RGB', (512, 512), 'white')
        draw = ImageDraw.Draw(img)

        # 노트북 모양
        draw.rectangle([100, 150, 412, 350], outline='black', width=3)  # 화면
        draw.rectangle([80, 350, 432, 420], outline='black', width=3)   # 키보드
        
        # 화면 안쪽
        draw.rectangle([120, 170, 392, 330], outline='black', width=2)

        img.save(self.computer_image)
    
    def show_images(self):
        fig, axes = plt.subplots(1, 2)

        # 프로필 이미지
        img1 = Image.open(self.profile_image)
        axes[0].imshow(img1)
        axes[0].set_title("Me")
        axes[0].axis('off')

        # 컴퓨터 이미지
        img2 = Image.open(self.computer_image)
        axes[1].imshow(img2)
        axes[1].set_title("My Interest")
        axes[1].axis('off')

        plt.show()

# 실행
me = KimDaKyung()
print(me.introduce())
me.show_images()
