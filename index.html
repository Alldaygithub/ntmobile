<?php

// กำหนดเส้นทางโฟลเดอร์
$folderPath = 'F:/NTGAMEFILE';  // เปลี่ยน \ ให้เป็น / ที่นี่
$baseUrl = 'http://ntgame.shock-connect.com/APIGAME/PC/resource/';

// ฟังก์ชันสำหรับการคำนวณขนาดไฟล์ในรูปแบบที่มนุษย์อ่านได้
function humanFileSize($size) {
    $units = ['B', 'KB', 'MB', 'GB', 'TB'];
    $i = 0;
    while ($size >= 1024 && $i < count($units) - 1) {
        $size /= 1024;
        $i++;
    }
    return round($size, 2) . ' ' . $units[$i];
}

// สแกนหาไฟล์ทั้งหมดในโฟลเดอร์
$files = new RecursiveIteratorIterator(new RecursiveDirectoryIterator($folderPath));

// เตรียมข้อมูล JSON
$resources = [];

foreach ($files as $file) {
    if ($file->isFile()) {
        // เปลี่ยน \ ให้เป็น / สำหรับเส้นทาง URL
        $relativePath = str_replace($folderPath . '\\', '', $file->getPathname());
        $relativePath = str_replace('/', '/', $relativePath);  // เปลี่ยนเป็นรูปแบบเส้นทาง URL แบบมาตรฐาน
        
        $resources[] = [
            'name' => $file->getFilename(),
            'size' => $file->getSize(),
            'path' => $relativePath,
            'url' => $baseUrl . $relativePath,
            'ver' => '1' // เปลี่ยนจาก 'gpu' => 'all' เป็น 'ver' => '1'
        ];
    }
}

// แปลงข้อมูลเป็น JSON
$jsonData = json_encode(['resource' => $resources], JSON_PRETTY_PRINT);

// เขียนข้อมูล JSON ลงไฟล์
$filePath = 'ListGameAPI.json';
file_put_contents($filePath, $jsonData);

// ส่งค่า JSON กลับเป็นการตอบสนอง
header('Content-Type: application/json');
echo $jsonData;

?>
