function calculateAchievement(tasks) {
  if (tasks.length === 0) return 0;

  const completed = tasks.filter(
    task => task.completed
  ).length;

  return Math.round(
    (completed / tasks.length) * 100
  );
}

const tasks = [
  { name: "المذاكرة", completed: true },
  { name: "الرياضة", completed: true },
  { name: "القراءة", completed: false }
];

console.log(calculateAchievement(tasks)); // 67
