# domed.github.io
<!DOCTYPE html>
<html>
<head>
<title>Tính điểm sinh viên</title>
</head>
<body>

<h1>Tính điểm sinh viên</h1>

<form>

<label for="name">Họ và tên:</label>
<input type="text" id="name" name="name"><br>

<label for="math">Điểm Toán:</label>
<input type="number" id="math" name="math" min="0" max="10"><br>

<label for="physics">Điểm Vật Lý:</label>
<input type="number" id="physics" name="physics" min="0" max="10"><br>

<label for="chemistry">Điểm Hoá Học:</label>
<input type="number" id="chemistry" name="chemistry" min="0" max="10"><br>

<input type="button" value="Tính điểm" onclick="calculateGrade()"><br>

<label for="result">Kết quả:</label>
<input type="text" id="result" name="result" readonly><br>

</form>

<script>
function calculateGrade() {
  var math = parseInt(document.getElementById("math").value);
  var physics = parseInt(document.getElementById("physics").value);
  var chemistry = parseInt(document.getElementById("chemistry").value);
  var average = (math + physics + chemistry) / 3;
  var grade;

  if (average >= 9) {
    grade = "Xuất sắc";
  } else if (average >= 8) {
    grade = "Giỏi";
  } else if (average >= 6.5) {
    grade = "Khá";
  } else if (average >= 5) {
    grade = "Trung bình";
  } else {
    grade = "Yếu";
  }

  document.getElementById("result").value = grade;
}
</script>

</body>
</html>
