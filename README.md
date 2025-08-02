import datetime

habits = {
    "Meditation": False,
    "UPSC Reading": False,
    "Sleep Before 11PM": False
}

today = datetime.date.today()
print(f"🧘 Habit Tracker for {today}")

for habit in habits:
    response = input(f"Did you complete '{habit}' today? (y/n): ")
    habits[habit] = True if response.lower() == 'y' else False

print("\n🌟 Summary:")
for habit, status in habits.items():
    print(f"{habit}: {'✅' if status else '❌'}")
