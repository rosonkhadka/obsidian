***

**Grade

```
if ($percentage >= 90) {
	return "A+";
} elseif ($percentage >= 80) {
	return "A";
} elseif ($percentage >= 70) {
	return "B+";
} elseif ($percentage >= 60) {
	return "B";
} elseif ($percentage >= 50) {
	return "C+";
} elseif ($percentage >= 40) {
	return "C";
} elseif ($percentage >= 35) {
	return "D";
} elseif ($percentage < 35) {
	return "NG";
}
return 'NG';
```

**Gradepoint

```
if ($percentage >= 90) {
	return 4;
} elseif ($percentage >= 80) {
	return 3.6;
} elseif ($percentage >= 70) {
	return 3.2;
} elseif ($percentage >= 60) {
	return 2.8;
} elseif ($percentage >= 50) {
	return 2.4;
} elseif ($percentage >= 40) {
	return 2.0;
} elseif ($percentage >= 35) {
	return 1.6;
} elseif ($percentage < 35) {
	return '-';
}
return '-';
```
