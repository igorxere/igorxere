import pygame
import random

# Inicjalizacja Pygame
pygame.init()

# Ustawienia okna gry
screen_width = 800
screen_height = 600
screen = pygame.display.set_mode((screen_width, screen_height))
pygame.display.set_caption('Zbieranie Punktów')

# Kolory
white = (255, 255, 255)
red = (255, 0, 0)

# Ustawienia gry
score = 0
font = pygame.font.Font(None, 36)
circle_radius = 30

def draw_circle():
    x = random.randint(circle_radius, screen_width - circle_radius)
    y = random.randint(circle_radius, screen_height - circle_radius)
    pygame.draw.circle(screen, red, (x, y), circle_radius)
    return (x, y)

# Główna pętla gry
running = True
circle_position = draw_circle()

while running:
    screen.fill(white)
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False
        elif event.type == pygame.MOUSEBUTTONDOWN:
            mouse_x, mouse_y = event.pos
            if (mouse_x - circle_position[0]) ** 2 + (mouse_y - circle_position[1]) ** 2 <= circle_radius ** 2:
                score += 1
                circle_position = draw_circle()

    # Wyświetlanie punktów
    score_text = font.render(f'Punkty: {score}', True, (0, 0, 0))
    screen.blit(score_text, (10, 10))

    pygame.display.flip()

# Zakończenie gry
pygame.quit()import pygame
import random

# Inicjalizacja Pygame
pygame.init()

# Ustawienia okna gry
screen_width = 800
screen_height = 600
screen = pygame.display.set_mode((screen_width, screen_height))
pygame.display.set_caption('Zbieranie Punktów')

# Kolory
white = (255, 255, 255)
red = (255, 0, 0)

# Ustawienia gry
score = 0
font = pygame.font.Font(None, 36)
circle_radius = 30

def draw_circle():
    x = random.randint(circle_radius, screen_width - circle_radius)
    y = random.randint(circle_radius, screen_height - circle_radius)
    pygame.draw.circle(screen, red, (x, y), circle_radius)
    return (x, y)

# Główna pętla gry
running = True
circle_position = draw_circle()

while running:
    screen.fill(white)
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False
        elif event.type == pygame.MOUSEBUTTONDOWN:
            mouse_x, mouse_y = event.pos
            if (mouse_x - circle_position[0]) ** 2 + (mouse_y - circle_position[1]) ** 2 <= circle_radius ** 2:
                score += 1
                circle_position = draw_circle()

    # Wyświetlanie punktów
    score_text = font.render(f'Punkty: {score}', True, (0, 0, 0))
    screen.blit(score_text, (10, 10))

    pygame.display.flip()

# Zakończenie gry
pygame.quit()


<!---
igorxere/igorxere is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
