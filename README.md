# Transportation-managment-System
<!DOCTYPE html>
<html lang="prs" dir="rtl" id="mainHtml">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>د وسایطو مدیریت سیستم - لاګن سره</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #3498db;
            --success-color: #27ae60;
            --warning-color: #f39c12;
            --danger-color: #e74c3c;
            --info-color: #17a2b8;
            --light-color: #ecf0f1;
            --dark-color: #1a1a2e;
            --bg-primary: #0f3460;
            --bg-secondary: #16213e;
            --text-color: #e0e0e0;
            --card-bg: rgba(255, 255, 255, 0.1);
            --input-bg: white;
            --input-color: #333;
        }
        
        /* Light mode variables */
        body.light-mode {
            --primary-color: #1a5276;
            --secondary-color: #2980b9;
            --success-color: #229954;
            --warning-color: #d68910;
            --danger-color: #c0392b;
            --info-color: #117a65;
            --light-color: #f8f9fa;
            --dark-color: #2c3e50;
            --bg-primary: #3498db;
            --bg-secondary: #2980b9;
            --text-color: #2c3e50;
            --card-bg: rgba(255, 255, 255, 0.95);
            --input-bg: #f8f9fa;
            --input-color: #2c3e50;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            color: var(--text-color);
            line-height: 1.6;
            min-height: 100vh;
            position: relative;
            overflow-x: hidden;
            background-color: var(--bg-secondary);
            transition: all 0.3s ease;
        }
        
        /* Digital Background Patterns */
        /* Dark Mode Patterns */
        .bg-dark-digital {
            background-color: var(--bg-secondary);
            background-image: 
                linear-gradient(0deg, transparent 24%, rgba(255, 255, 255, 0.05) 25%, rgba(255, 255, 255, 0.05) 26%, transparent 27%, transparent 74%, rgba(255, 255, 255, 0.05) 75%, rgba(255, 255, 255, 0.05) 76%, transparent 77%, transparent),
                linear-gradient(90deg, transparent 24%, rgba(255, 255, 255, 0.05) 25%, rgba(255, 255, 255, 0.05) 26%, transparent 27%, transparent 74%, rgba(255, 255, 255, 0.05) 75%, rgba(255, 255, 255, 0.05) 76%, transparent 77%, transparent);
            background-size: 50px 50px;
        }
        
        .bg-blue-digital {
            background-color: #1a237e;
            background-image: 
                linear-gradient(0deg, transparent 24%, rgba(255, 255, 255, 0.1) 25%, rgba(255, 255, 255, 0.1) 26%, transparent 27%, transparent 74%, rgba(255, 255, 255, 0.1) 75%, rgba(255, 255, 255, 0.1) 76%, transparent 77%, transparent),
                linear-gradient(90deg, transparent 24%, rgba(255, 255, 255, 0.1) 25%, rgba(255, 255, 255, 0.1) 26%, transparent 27%, transparent 74%, rgba(255, 255, 255, 0.1) 75%, rgba(255, 255, 255, 0.1) 76%, transparent 77%, transparent);
            background-size: 50px 50px;
        }
        
        .bg-green-digital {
            background-color: #1b5e20;
            background-image: 
                linear-gradient(0deg, transparent 24%, rgba(255, 255, 255, 0.1) 25%, rgba(255, 255, 255, 0.1) 26%, transparent 27%, transparent 74%, rgba(255, 255, 255, 0.1) 75%, rgba(255, 255, 255, 0.1) 76%, transparent 77%, transparent),
                linear-gradient(90deg, transparent 24%, rgba(255, 255, 255, 0.1) 25%, rgba(255, 255, 255, 0.1) 26%, transparent 27%, transparent 74%, rgba(255, 255, 255, 0.1) 75%, rgba(255, 255, 255, 0.1) 76%, transparent 77%, transparent);
            background-size: 50px 50px;
        }
        
        .bg-purple-digital {
            background-color: #4a148c;
            background-image: 
                linear-gradient(0deg, transparent 24%, rgba(255, 255, 255, 0.1) 25%, rgba(255, 255, 255, 0.1) 26%, transparent 27%, transparent 74%, rgba(255, 255, 255, 0.1) 75%, rgba(255, 255, 255, 0.1) 76%, transparent 77%, transparent),
                linear-gradient(90deg, transparent 24%, rgba(255, 255, 255, 0.1) 25%, rgba(255, 255, 255, 0.1) 26%, transparent 27%, transparent 74%, rgba(255, 255, 255, 0.1) 75%, rgba(255, 255, 255, 0.1) 76%, transparent 77%, transparent);
            background-size: 50px 50px;
        }
        
        .bg-red-digital {
            background-color: #b71c1c;
            background-image: 
                linear-gradient(0deg, transparent 24%, rgba(255, 255, 255, 0.1) 25%, rgba(255, 255, 255, 0.1) 26%, transparent 27%, transparent 74%, rgba(255, 255, 255, 0.1) 75%, rgba(255, 255, 255, 0.1) 76%, transparent 77%, transparent),
                linear-gradient(90deg, transparent 24%, rgba(255, 255, 255, 0.1) 25%, rgba(255, 255, 255, 0.1) 26%, transparent 27%, transparent 74%, rgba(255, 255, 255, 0.1) 75%, rgba(255, 255, 255, 0.1) 76%, transparent 77%, transparent);
            background-size: 50px 50px;
        }
        
        /* Light Mode Patterns */
        body.light-mode .bg-dark-digital {
            background-color: #e3f2fd;
            background-image: 
                linear-gradient(0deg, transparent 24%, rgba(0, 0, 0, 0.05) 25%, rgba(0, 0, 0, 0.05) 26%, transparent 27%, transparent 74%, rgba(0, 0, 0, 0.05) 75%, rgba(0, 0, 0, 0.05) 76%, transparent 77%, transparent),
                linear-gradient(90deg, transparent 24%, rgba(0, 0, 0, 0.05) 25%, rgba(0, 0, 0, 0.05) 26%, transparent 27%, transparent 74%, rgba(0, 0, 0, 0.05) 75%, rgba(0, 0, 0, 0.05) 76%, transparent 77%, transparent);
        }
        
        body.light-mode .bg-blue-digital {
            background-color: #bbdefb;
            background-image: 
                linear-gradient(0deg, transparent 24%, rgba(0, 0, 0, 0.05) 25%, rgba(0, 0, 0, 0.05) 26%, transparent 27%, transparent 74%, rgba(0, 0, 0, 0.05) 75%, rgba(0, 0, 0, 0.05) 76%, transparent 77%, transparent),
                linear-gradient(90deg, transparent 24%, rgba(0, 0, 0, 0.05) 25%, rgba(0, 0, 0, 0.05) 26%, transparent 27%, transparent 74%, rgba(0, 0, 0, 0.05) 75%, rgba(0, 0, 0, 0.05) 76%, transparent 77%, transparent);
        }
        
        body.light-mode .bg-green-digital {
            background-color: #c8e6c9;
            background-image: 
                linear-gradient(0deg, transparent 24%, rgba(0, 0, 0, 0.05) 25%, rgba(0, 0, 0, 0.05) 26%, transparent 27%, transparent 74%, rgba(0, 0, 0, 0.05) 75%, rgba(0, 0, 0, 0.05) 76%, transparent 77%, transparent),
                linear-gradient(90deg, transparent 24%, rgba(0, 0, 0, 0.05) 25%, rgba(0, 0, 0, 0.05) 26%, transparent 27%, transparent 74%, rgba(0, 0, 0, 0.05) 75%, rgba(0, 0, 0, 0.05) 76%, transparent 77%, transparent);
        }
        
        body.light-mode .bg-purple-digital {
            background-color: #e1bee7;
            background-image: 
                linear-gradient(0deg, transparent 24%, rgba(0, 0, 0, 0.05) 25%, rgba(0, 0, 0, 0.05) 26%, transparent 27%, transparent 74%, rgba(0, 0, 0, 0.05) 75%, rgba(0, 0, 0, 0.05) 76%, transparent 77%, transparent),
                linear-gradient(90deg, transparent 24%, rgba(0, 0, 0, 0.05) 25%, rgba(0, 0, 0, 0.05) 26%, transparent 27%, transparent 74%, rgba(0, 0, 0, 0.05) 75%, rgba(0, 0, 0, 0.05) 76%, transparent 77%, transparent);
        }
        
        body.light-mode .bg-red-digital {
            background-color: #ffcdd2;
            background-image: 
                linear-gradient(0deg, transparent 24%, rgba(0, 0, 0, 0.05) 25%, rgba(0, 0, 0, 0.05) 26%, transparent 27%, transparent 74%, rgba(0, 0, 0, 0.05) 75%, rgba(0, 0, 0, 0.05) 76%, transparent 77%, transparent),
                linear-gradient(90deg, transparent 24%, rgba(0, 0, 0, 0.05) 25%, rgba(0, 0, 0, 0.05) 26%, transparent 27%, transparent 74%, rgba(0, 0, 0, 0.05) 75%, rgba(0, 0, 0, 0.05) 76%, transparent 77%, transparent);
        }
        
        /* New Digital Pattern Backgrounds */
        .bg-circuit-board {
            background-color: var(--bg-secondary);
            background-image: 
                radial-gradient(circle at 25px 25px, rgba(52, 152, 219, 0.2) 2%, transparent 2%),
                radial-gradient(circle at 75px 75px, rgba(52, 152, 219, 0.2) 2%, transparent 2%);
            background-size: 100px 100px;
        }
        
        body.light-mode .bg-circuit-board {
            background-color: #e3f2fd;
            background-image: 
                radial-gradient(circle at 25px 25px, rgba(30, 136, 229, 0.1) 2%, transparent 2%),
                radial-gradient(circle at 75px 75px, rgba(30, 136, 229, 0.1) 2%, transparent 2%);
        }
        
        .bg-binary-code {
            background-color: var(--bg-secondary);
            background: 
                linear-gradient(90deg, transparent 50%, rgba(46, 204, 113, 0.1) 50%),
                linear-gradient(0deg, transparent 50%, rgba(46, 204, 113, 0.1) 50%);
            background-size: 20px 20px;
        }
        
        body.light-mode .bg-binary-code {
            background-color: #f1f8e9;
            background: 
                linear-gradient(90deg, transparent 50%, rgba(76, 175, 80, 0.1) 50%),
                linear-gradient(0deg, transparent 50%, rgba(76, 175, 80, 0.1) 50%);
        }
        
        .bg-data-flow {
            background-color: var(--bg-secondary);
            background-image: 
                linear-gradient(45deg, transparent 49%, rgba(155, 89, 182, 0.2) 50%, transparent 51%),
                linear-gradient(-45deg, transparent 49%, rgba(155, 89, 182, 0.2) 50%, transparent 51%);
            background-size: 60px 60px;
        }
        
        body.light-mode .bg-data-flow {
            background-color: #f3e5f5;
            background-image: 
                linear-gradient(45deg, transparent 49%, rgba(156, 39, 176, 0.1) 50%, transparent 51%),
                linear-gradient(-45deg, transparent 49%, rgba(156, 39, 176, 0.1) 50%, transparent 51%);
        }
        
        .bg-network-grid {
            background-color: var(--bg-secondary);
            background-image: 
                linear-gradient(rgba(231, 76, 60, 0.1) 1px, transparent 1px),
                linear-gradient(90deg, rgba(231, 76, 60, 0.1) 1px, transparent 1px);
            background-size: 30px 30px;
        }
        
        body.light-mode .bg-network-grid {
            background-color: #ffebee;
            background-image: 
                linear-gradient(rgba(244, 67, 54, 0.1) 1px, transparent 1px),
                linear-gradient(90deg, rgba(244, 67, 54, 0.1) 1px, transparent 1px);
        }
        
        .bg-pixel-grid {
            background-color: var(--bg-secondary);
            background-image: 
                linear-gradient(rgba(255, 255, 255, 0.1) 1px, transparent 1px),
                linear-gradient(90deg, rgba(255, 255, 255, 0.1) 1px, transparent 1px);
            background-size: 40px 40px;
        }
        
        body.light-mode .bg-pixel-grid {
            background-color: #f5f5f5;
            background-image: 
                linear-gradient(rgba(0, 0, 0, 0.05) 1px, transparent 1px),
                linear-gradient(90deg, rgba(0, 0, 0, 0.05) 1px, transparent 1px);
        }
        
        .bg-hexagon {
            background-color: var(--bg-secondary);
            background-image: 
                linear-gradient(115deg, transparent 75%, rgba(52, 152, 219, 0.1) 75%),
                linear-gradient(245deg, transparent 75%, rgba(52, 152, 219, 0.1) 75%),
                linear-gradient(115deg, transparent 75%, rgba(52, 152, 219, 0.1) 75%),
                linear-gradient(245deg, transparent 75%, rgba(52, 152, 219, 0.1) 75%);
            background-size: 70px 120px;
            background-position: 0 0, 0 0, 35px 60px, 35px 60px;
        }
        
        body.light-mode .bg-hexagon {
            background-color: #e8f4fd;
            background-image: 
                linear-gradient(115deg, transparent 75%, rgba(30, 136, 229, 0.1) 75%),
                linear-gradient(245deg, transparent 75%, rgba(30, 136, 229, 0.1) 75%),
                linear-gradient(115deg, transparent 75%, rgba(30, 136, 229, 0.1) 75%),
                linear-gradient(245deg, transparent 75%, rgba(30, 136, 229, 0.1) 75%);
        }
        
        .bg-digital-waves {
            background-color: var(--bg-secondary);
            background: 
                radial-gradient(circle at 50% 0%, rgba(46, 204, 113, 0.1), transparent 50%),
                radial-gradient(circle at 6.7% 75%, rgba(52, 152, 219, 0.1), transparent 50%),
                radial-gradient(circle at 93.3% 75%, rgba(155, 89, 182, 0.1), transparent 50%);
            background-size: 200% 200%;
            animation: waveAnimation 15s ease infinite;
        }
        
        @keyframes waveAnimation {
            0% { background-position: 0% 0%; }
            50% { background-position: 100% 100%; }
            100% { background-position: 0% 0%; }
        }
        
        body.light-mode .bg-digital-waves {
            background-color: #f0f9ff;
            background: 
                radial-gradient(circle at 50% 0%, rgba(76, 175, 80, 0.1), transparent 50%),
                radial-gradient(circle at 6.7% 75%, rgba(30, 136, 229, 0.1), transparent 50%),
                radial-gradient(circle at 93.3% 75%, rgba(156, 39, 176, 0.1), transparent 50%);
        }
        
        .bg-matrix {
            background-color: #001a00;
            background-image: 
                linear-gradient(rgba(0, 255, 0, 0.1) 1px, transparent 1px),
                linear-gradient(90deg, rgba(0, 255, 0, 0.1) 1px, transparent 1px);
            background-size: 40px 40px;
            animation: matrixFlow 20s linear infinite;
        }
        
        @keyframes matrixFlow {
            0% { background-position: 0 0; }
            100% { background-position: 40px 40px; }
        }
        
        .header {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
            padding: 1.2rem 0;
            border-bottom: 5px solid var(--warning-color);
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
        }
        
        .logo {
            font-weight: bold;
            font-size: 1.6rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .logo i {
            color: var(--warning-color);
        }
        
        .user-info {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .user-avatar {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: var(--warning-color);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
        }
        
        /* Settings Button */
        .settings-btn {
            position: fixed;
            bottom: 20px;
            right: 20px;
            z-index: 1000;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--secondary-color), var(--primary-color));
            color: white;
            border: none;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            transition: all 0.3s;
        }
        
        .settings-btn:hover {
            transform: rotate(30deg) scale(1.1);
        }
        
        .settings-panel {
            position: fixed;
            top: 0;
            right: -350px;
            width: 320px;
            height: 100vh;
            background: rgba(26, 26, 46, 0.95);
            backdrop-filter: blur(10px);
            z-index: 9999;
            padding: 20px;
            box-shadow: -5px 0 15px rgba(0, 0, 0, 0.5);
            transition: right 0.4s ease;
            overflow-y: auto;
        }
        
        body.light-mode .settings-panel {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
        }
        
        .settings-panel.show {
            right: 0;
        }
        
        .settings-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 25px;
            padding-bottom: 15px;
            border-bottom: 2px solid var(--warning-color);
        }
        
        .login-container {
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
            background: linear-gradient(135deg, rgba(44, 62, 80, 0.95), rgba(52, 152, 219, 0.95));
            position: relative;
        }
        
        .login-container::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" preserveAspectRatio="none"><path d="M0,0 L100,0 L100,100 Z" fill="rgba(255,255,255,0.1)"/></svg>');
            background-size: cover;
        }
        
        .login-card {
            background: rgba(255, 255, 255, 0.95);
            border-radius: 15px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
            width: 100%;
            max-width: 450px;
            position: relative;
            overflow: hidden;
            animation: fadeInUp 0.8s ease-out;
        }
        
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .login-header {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
            padding: 30px;
            text-align: center;
            position: relative;
        }
        
        .login-header::after {
            content: "";
            position: absolute;
            bottom: -20px;
            left: 50%;
            transform: translateX(-50%);
            width: 40px;
            height: 40px;
            background: white;
            transform: rotate(45deg);
        }
        
        .login-body {
            padding: 40px 30px;
        }
        
        .form-control {
            border-radius: 8px;
            padding: 12px 15px;
            border: 2px solid #e0e0e0;
            transition: all 0.3s;
            background-color: var(--input-bg);
            color: var(--input-color);
        }
        
        .form-control:focus {
            border-color: var(--secondary-color);
            box-shadow: 0 0 0 0.25rem rgba(52, 152, 219, 0.25);
        }
        
        .btn-login {
            background: linear-gradient(135deg, var(--secondary-color), var(--primary-color));
            color: white;
            border: none;
            padding: 12px;
            border-radius: 8px;
            font-weight: 600;
            width: 100%;
            transition: all 0.3s;
        }
        
        .btn-login:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(52, 152, 219, 0.4);
        }
        
        .login-footer {
            text-align: center;
            padding: 20px;
            background: #f8f9fa;
            border-top: 1px solid #e0e0e0;
            color: #333;
        }
        
        .nav-tabs .nav-link {
            color: var(--light-color);
            font-weight: 600;
            border: none;
            border-bottom: 3px solid transparent;
            margin: 0 5px;
            background: rgba(255, 255, 255, 0.1);
        }
        
        body.light-mode .nav-tabs .nav-link {
            color: var(--dark-color);
            background: rgba(0, 0, 0, 0.05);
        }
        
        .nav-tabs .nav-link.active {
            color: var(--warning-color);
            background-color: rgba(255, 255, 255, 0.15);
            border-bottom: 3px solid var(--warning-color);
        }
        
        body.light-mode .nav-tabs .nav-link.active {
            background-color: rgba(0, 0, 0, 0.1);
        }
        
        .section-title {
            color: var(--light-color);
            border-bottom: 2px solid var(--warning-color);
            padding-bottom: 10px;
            margin-bottom: 25px;
            font-weight: 700;
        }
        
        body.light-mode .section-title {
            color: var(--dark-color);
        }
        
        .card {
            border-radius: 15px;
            border: none;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            margin-bottom: 20px;
            overflow: hidden;
            background: var(--card-bg);
            backdrop-filter: blur(10px);
            color: var(--text-color);
        }
        
        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.3);
        }
        
        .card-header {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
            border-radius: 15px 15px 0 0 !important;
            font-weight: 600;
            padding: 20px;
            position: relative;
            overflow: hidden;
        }
        
        .card-header::before {
            content: "";
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(45deg, transparent, rgba(255, 255, 255, 0.1), transparent);
            transform: rotate(45deg);
            animation: shine 3s infinite;
        }
        
        @keyframes shine {
            0% { transform: translateX(-100%) rotate(45deg); }
            100% { transform: translateX(100%) rotate(45deg); }
        }
        
        .btn-primary {
            background: linear-gradient(135deg, var(--secondary-color), var(--primary-color));
            border: none;
            padding: 10px 25px;
            border-radius: 8px;
            transition: all 0.3s;
        }
        
        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(52, 152, 219, 0.4);
        }
        
        .btn-success {
            background: linear-gradient(135deg, var(--success-color), #2ecc71);
            border: none;
        }
        
        .btn-warning {
            background: linear-gradient(135deg, var(--warning-color), #e67e22);
            border: none;
        }
        
        .btn-info {
            background: linear-gradient(135deg, var(--info-color), #2c3e50);
            border: none;
        }
        
        .btn-danger {
            background: linear-gradient(135deg, var(--danger-color), #c0392b);
            border: none;
        }
        
        .status-badge {
            padding: 8px 20px;
            border-radius: 25px;
            font-weight: 600;
            font-size: 0.85rem;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.2);
        }
        
        .status-registered {
            background: linear-gradient(135deg, #d5f4e6, #c8efdb);
            color: var(--success-color);
        }
        
        .status-entered {
            background: linear-gradient(135deg, #e8f4fc, #dbeaf9);
            color: var(--secondary-color);
        }
        
        .status-loaded {
            background: linear-gradient(135deg, #d1ecf1, #c4e5ea);
            color: var(--info-color);
        }
        
        .status-exited {
            background: linear-gradient(135deg, #fef5e7, #f7e9d2);
            color: var(--warning-color);
        }
        
        .zone-badge {
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
            margin: 3px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
        }
        
        .stat-card {
            text-align: center;
            padding: 25px 15px;
            border-radius: 15px;
            color: white;
            margin-bottom: 20px;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        .stat-card:hover {
            transform: translateY(-5px);
        }
        
        .stat-card::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, transparent, rgba(255, 255, 255, 0.1), transparent);
            transform: translateX(-100%);
        }
        
        .stat-card:hover::before {
            animation: shine 1.5s;
        }
        
        .stat-card i {
            font-size: 2.8rem;
            margin-bottom: 15px;
            filter: drop-shadow(0 3px 5px rgba(0, 0, 0, 0.3));
        }
        
        .stat-card-1 {
            background: linear-gradient(135deg, #3498db, #2c3e50);
        }
        
        .stat-card-2 {
            background: linear-gradient(135deg, #27ae60, #2ecc71);
        }
        
        .stat-card-3 {
            background: linear-gradient(135deg, #f39c12, #e67e22);
        }
        
        .stat-card-4 {
            background: linear-gradient(135deg, #9b59b6, #8e44ad);
        }
        
        .stat-card-5 {
            background: linear-gradient(135deg, #17a2b8, #2c3e50);
        }
        
        .table {
            color: var(--text-color);
        }
        
        body.light-mode .table {
            color: var(--dark-color);
        }
        
        .table th {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
            border: none;
            padding: 15px;
        }
        
        .table-hover tbody tr:hover {
            background-color: rgba(52, 152, 219, 0.2);
            transform: scale(1.01);
            transition: all 0.2s;
        }
        
        body.light-mode .table-hover tbody tr:hover {
            background-color: rgba(52, 152, 219, 0.1);
        }
        
        .required::after {
            content: " *";
            color: var(--danger-color);
        }
        
        footer {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: white;
            padding: 30px 0;
            margin-top: 50px;
            border-top: 5px solid var(--warning-color);
            position: relative;
            overflow: hidden;
        }
        
        footer::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" preserveAspectRatio="none"><path d="M0,100 L100,0 L100,100 Z" fill="rgba(255,255,255,0.05)"/></svg>');
            background-size: cover;
        }
        
        .fade-in {
            animation: fadeIn 0.5s ease-in;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .alert-custom {
            border-radius: 10px;
            border: none;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            padding: 15px 20px;
        }
        
        .load-type-badge {
            padding: 8px 15px;
            border-radius: 12px;
            font-size: 0.8rem;
            font-weight: 600;
            margin: 3px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
        }
        
        .load-food {
            background: linear-gradient(135deg, #d4edda, #c3e6cb);
            color: #155724;
        }
        
        .load-construction {
            background: linear-gradient(135deg, #fff3cd, #ffeaa7);
            color: #856404;
        }
        
        .load-furniture {
            background: linear-gradient(135deg, #d1ecf1, #bee5eb);
            color: #0c5460;
        }
        
        .load-agriculture {
            background: linear-gradient(135deg, #d6d8db, #c6c8ca);
            color: #383d41;
        }
        
        .load-other {
            background: linear-gradient(135deg, #f8d7da, #f5c6cb);
            color: #721c24;
        }
        
        .main-content {
            display: none;
            animation: fadeIn 0.8s ease-out;
        }
        
        .user-management-card {
            background: linear-gradient(135deg, rgba(248, 249, 250, 0.1), rgba(233, 236, 239, 0.1));
            border-radius: 15px;
            padding: 20px;
            margin-bottom: 20px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .user-role-badge {
            padding: 5px 12px;
            border-radius: 20px;
            font-size: 0.75rem;
            font-weight: 600;
        }
        
        .role-admin {
            background: linear-gradient(135deg, #3498db, #2980b9);
            color: white;
        }
        
        .role-user {
            background: linear-gradient(135deg, #27ae60, #219653);
            color: white;
        }
        
        .role-operator {
            background: linear-gradient(135deg, #f39c12, #e67e22);
            color: white;
        }
        
        /* Language Switcher */
        .language-switcher {
            position: relative;
            display: inline-block;
        }
        
        .lang-btn {
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            color: white;
            padding: 8px 15px;
            border-radius: 20px;
            display: flex;
            align-items: center;
            gap: 8px;
            transition: all 0.3s;
        }
        
        body.light-mode .lang-btn {
            background: rgba(0, 0, 0, 0.1);
            border: 1px solid rgba(0, 0, 0, 0.2);
            color: var(--dark-color);
        }
        
        .lang-btn:hover {
            background: rgba(255, 255, 255, 0.2);
        }
        
        body.light-mode .lang-btn:hover {
            background: rgba(0, 0, 0, 0.2);
        }
        
        .lang-dropdown {
            position: absolute;
            top: 100%;
            left: 0;
            background: rgba(26, 26, 46, 0.95);
            backdrop-filter: blur(10px);
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            min-width: 150px;
            display: none;
            z-index: 1000;
            overflow: hidden;
        }
        
        body.light-mode .lang-dropdown {
            background: rgba(255, 255, 255, 0.95);
        }
        
        .lang-dropdown.show {
            display: block;
        }
        
        .lang-option {
            padding: 10px 15px;
            display: flex;
            align-items: center;
            gap: 10px;
            cursor: pointer;
            transition: all 0.3s;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        body.light-mode .lang-option {
            border-bottom: 1px solid rgba(0, 0, 0, 0.1);
        }
        
        .lang-option:last-child {
            border-bottom: none;
        }
        
        .lang-option:hover {
            background: rgba(255, 255, 255, 0.1);
        }
        
        body.light-mode .lang-option:hover {
            background: rgba(0, 0, 0, 0.1);
        }
        
        .lang-option.active {
            background: rgba(52, 152, 219, 0.3);
        }
        
        /* Theme Mode Toggle */
        .theme-switch {
            position: relative;
            display: inline-block;
            width: 60px;
            height: 30px;
        }
        
        .theme-switch input {
            opacity: 0;
            width: 0;
            height: 0;
        }
        
        .theme-slider {
            position: absolute;
            cursor: pointer;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: #ccc;
            transition: .4s;
            border-radius: 34px;
        }
        
        .theme-slider:before {
            position: absolute;
            content: "";
            height: 22px;
            width: 22px;
            left: 4px;
            bottom: 4px;
            background-color: white;
            transition: .4s;
            border-radius: 50%;
        }
        
        input:checked + .theme-slider {
            background-color: #3498db;
        }
        
        input:checked + .theme-slider:before {
            transform: translateX(30px);
        }
        
        .theme-slider .theme-icon {
            position: absolute;
            top: 5px;
            font-size: 14px;
        }
        
        .theme-slider .sun {
            left: 8px;
            color: #f39c12;
        }
        
        .theme-slider .moon {
            right: 8px;
            color: #f1c40f;
        }
        
        /* Background Selection */
        .bg-options {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 10px;
        }
        
        .bg-option {
            width: 60px;
            height: 60px;
            border-radius: 10px;
            cursor: pointer;
            border: 3px solid transparent;
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
        }
        
        .bg-option:hover {
            transform: scale(1.05);
        }
        
        .bg-option.active {
            border-color: var(--warning-color);
            box-shadow: 0 0 10px var(--warning-color);
        }
        
        .bg-option .bg-name {
            position: absolute;
            bottom: 2px;
            right: 2px;
            background: rgba(0, 0, 0, 0.7);
            color: white;
            font-size: 8px;
            padding: 1px 3px;
            border-radius: 3px;
        }
        
        /* Mobile Responsiveness */
        @media (max-width: 768px) {
            .card {
                margin-bottom: 15px;
            }
            
            .section-title {
                font-size: 1.5rem;
            }
            
            .logo {
                font-size: 1.4rem;
            }
            
            .nav-tabs .nav-link {
                font-size: 0.85rem;
                padding: 8px 12px;
            }
            
            .stat-card {
                padding: 20px 10px;
            }
            
            .stat-card i {
                font-size: 2.2rem;
            }
            
            .settings-panel {
                width: 280px;
                right: -280px;
            }
            
            .bg-option {
                width: 50px;
                height: 50px;
            }
        }
        
        @media (max-width: 576px) {
            .login-card {
                margin: 10px;
            }
            
            .login-body {
                padding: 30px 20px;
            }
            
            .settings-panel {
                width: 100%;
                right: -100%;
            }
        }
        
        /* Guide Items */
        .guide-item {
            padding: 10px;
            margin-bottom: 10px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 8px;
            border-right: 4px solid var(--warning-color);
        }
        
        body.light-mode .guide-item {
            background: rgba(0, 0, 0, 0.05);
        }
        
        /* Admin User Form */
        .admin-user-form {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 10px;
            padding: 20px;
            margin-bottom: 20px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        body.light-mode .admin-user-form {
            background: rgba(0, 0, 0, 0.05);
            border: 1px solid rgba(0, 0, 0, 0.1);
        }
        
        /* Radio Button Styling */
        .form-check-input:checked {
            background-color: var(--secondary-color);
            border-color: var(--secondary-color);
        }
        
        /* Text Direction */
        .text-ltr {
            direction: ltr;
            text-align: left;
        }
        
        .text-rtl {
            direction: rtl;
            text-align: right;
        }
        
        /* Dark/Light Mode Transition */
        body, .card, .form-control, .table, .nav-tabs .nav-link, .section-title {
            transition: background-color 0.3s ease, color 0.3s ease, border-color 0.3s ease;
        }
    </style>
</head>
<body class="bg-dark-digital">
    <!-- Settings Button -->
    <button class="settings-btn" id="settingsBtn">
        <i class="fas fa-cog"></i>
    </button>
    
    <!-- Settings Panel -->
    <div class="settings-panel" id="settingsPanel">
        <div class="settings-header">
            <h4 class="mb-0" data-i18n="settings.title">تنظیمات</h4>
            <button class="btn btn-sm btn-danger" id="closeSettings">
                <i class="fas fa-times"></i>
            </button>
        </div>
        
        <!-- Theme Mode Toggle -->
        <div class="mb-4">
            <h5 data-i18n="settings.themeMode">مود (تاریک/روښانه)</h5>
            <div class="d-flex align-items-center gap-3">
                <label class="theme-switch">
                    <input type="checkbox" id="themeToggle">
                    <span class="theme-slider">
                        <i class="fas fa-sun theme-icon sun"></i>
                        <i class="fas fa-moon theme-icon moon"></i>
                    </span>
                </label>
                <span id="themeStatus" data-i18n="settings.darkMode">تاریک مود</span>
            </div>
        </div>
        
        <div class="mb-4">
            <h5 data-i18n="settings.language">ژبه</h5>
            <div class="language-switcher">
                <button class="lang-btn" id="currentLangBtn">
                    <i class="fas fa-language"></i>
                    <span id="currentLangText">پښتو</span>
                    <i class="fas fa-chevron-down"></i>
                </button>
                <div class="lang-dropdown" id="langDropdown">
                    <div class="lang-option active" data-lang="ps">
                        <i class="fas fa-flag"></i>
                        <span>پښتو</span>
                    </div>
                    <div class="lang-option" data-lang="en">
                        <i class="fas fa-flag-usa"></i>
                        <span>English</span>
                    </div>
                    <div class="lang-option" data-lang="fa">
                        <i class="fas fa-flag"></i>
                        <span>دری</span>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="mb-4">
            <h5 data-i18n="settings.background">بیکګرونډ</h5>
            <div class="bg-options">
                <div class="bg-option bg-dark-digital active" data-bg="dark-digital">
                    <span class="bg-name">تاریک</span>
                </div>
                <div class="bg-option bg-blue-digital" data-bg="blue-digital">
                    <span class="bg-name">آبی</span>
                </div>
                <div class="bg-option bg-green-digital" data-bg="green-digital">
                    <span class="bg-name">سبز</span>
                </div>
                <div class="bg-option bg-purple-digital" data-bg="purple-digital">
                    <span class="bg-name">بنفش</span>
                </div>
                <div class="bg-option bg-red-digital" data-bg="red-digital">
                    <span class="bg-name">سور</span>
                </div>
                <div class="bg-option bg-circuit-board" data-bg="circuit-board">
                    <span class="bg-name">سرکیټ</span>
                </div>
                <div class="bg-option bg-binary-code" data-bg="binary-code">
                    <span class="bg-name">باینری</span>
                </div>
                <div class="bg-option bg-data-flow" data-bg="data-flow">
                    <span class="bg-name">ډیټا</span>
                </div>
                <div class="bg-option bg-network-grid" data-bg="network-grid">
                    <span class="bg-name">نیټورک</span>
                </div>
                <div class="bg-option bg-pixel-grid" data-bg="pixel-grid">
                    <span class="bg-name">پیکسل</span>
                </div>
                <div class="bg-option bg-hexagon" data-bg="hexagon">
                    <span class="bg-name">هېکزاګون</span>
                </div>
                <div class="bg-option bg-digital-waves" data-bg="digital-waves">
                    <span class="bg-name">اونۍ</span>
                </div>
                <div class="bg-option bg-matrix" data-bg="matrix">
                    <span class="bg-name">مېټرېکس</span>
                </div>
            </div>
        </div>
        
        <div class="mb-4">
            <h5 data-i18n="settings.systemInfo">د سیستم معلومات</h5>
            <div class="card bg-dark p-3">
                <p class="mb-1"><small data-i18n="settings.version">نسخه:</small> <strong>۲.۲</strong></p>
                <p class="mb-1"><small data-i18n="settings.users">کارونکي:</small> <strong id="settingsUserCount">۰</strong></p>
                <p class="mb-1"><small data-i18n="settings.vehicles">وسایط:</small> <strong id="settingsVehicleCount">۰</strong></p>
                <p class="mb-0"><small data-i18n="settings.lastLogin">وروستی لاګن:</small> <strong id="settingsLastLogin">-</strong></p>
            </div>
        </div>
        
        <div class="mb-3">
            <h5 data-i18n="settings.exportData">ډیټا صادرول</h5>
            <div class="d-grid gap-2">
                <button class="btn btn-sm btn-outline-info" id="exportAllData">
                    <i class="fas fa-download me-2"></i>
                    <span data-i18n="settings.exportAll">ټول ډیټا صادرول</span>
                </button>
            </div>
        </div>
        
        <div class="mt-4 pt-3 border-top">
            <div class="d-grid gap-2">
                <button class="btn btn-sm btn-warning" id="resetSettings">
                    <i class="fas fa-redo me-2"></i>
                    <span data-i18n="settings.reset">تنظیمات ریسیټ کړئ</span>
                </button>
            </div>
        </div>
    </div>
    
    <!-- Login Section -->
    <div id="loginContainer" class="login-container">
        <div class="login-card">
            <div class="login-header">
                <div class="logo">
                    <i class="fas fa-truck-loading"></i>
                    <span data-i18n="login.title">د وسایطو مدیریت سیستم</span>
                </div>
                <p class="mb-0 mt-2" data-i18n="login.subtitle">د افغانستان داخلي سفرونه</p>
            </div>
            
            <div class="login-body">
                <div id="loginForm">
                    <h4 class="text-center mb-4" style="color: var(--primary-color);" data-i18n="login.formTitle">د سیستم داخلیدل</h4>
                    
                    <div class="mb-3">
                        <label for="loginUsername" class="form-label" data-i18n="login.username">د کارن نوم</label>
                        <div class="input-group">
                            <span class="input-group-text bg-light"><i class="fas fa-user"></i></span>
                            <input type="text" class="form-control" id="loginUsername" data-i18n-placeholder="login.usernamePlaceholder" placeholder="خپل کارن نوم دننه کړئ">
                        </div>
                    </div>
                    
                    <div class="mb-3">
                        <label for="loginPassword" class="form-label" data-i18n="login.password">پاسورډ</label>
                        <div class="input-group">
                            <span class="input-group-text bg-light"><i class="fas fa-lock"></i></span>
                            <input type="password" class="form-control" id="loginPassword" data-i18n-placeholder="login.passwordPlaceholder" placeholder="خپل پاسورډ دننه کړئ">
                            <button class="btn btn-outline-secondary" type="button" id="togglePassword">
                                <i class="fas fa-eye"></i>
                            </button>
                        </div>
                    </div>
                    
                    <div class="mb-3 form-check">
                        <input type="checkbox" class="form-check-input" id="rememberMe">
                        <label class="form-check-label" for="rememberMe" data-i18n="login.remember">ما په یاد ساتل</label>
                    </div>
                    
                    <div class="d-grid gap-2 mb-3">
                        <button class="btn btn-login" id="loginButton">
                            <i class="fas fa-sign-in-alt me-2"></i>
                            <span data-i18n="login.loginButton">د سیستم داخلیدل</span>
                        </button>
                    </div>
                    
                    <div class="text-center">
                        <p class="mb-0">
                            <span data-i18n="login.newUser">څوک یاست؟</span>
                            <a href="#" class="text-decoration-none ms-1" id="showRegisterForm" data-i18n="login.registerLink">نوی حساب جوړول</a>
                        </p>
                        <p class="mt-2">
                            <a href="#" class="text-decoration-none" id="showForgotPassword" data-i18n="login.forgotPassword">پاسورډ هیر دی؟</a>
                        </p>
                    </div>
                </div>
                
                <!-- Registration Form -->
                <div id="registerForm" style="display: none;">
                    <h4 class="text-center mb-4" style="color: var(--primary-color);" data-i18n="register.title">نوی حساب جوړول</h4>
                    
                    <div class="mb-3">
                        <label for="regFullName" class="form-label" data-i18n="register.fullName">بشپړ نوم</label>
                        <div class="input-group">
                            <span class="input-group-text bg-light"><i class="fas fa-user"></i></span>
                            <input type="text" class="form-control" id="regFullName" data-i18n-placeholder="register.fullNamePlaceholder" placeholder="لکه: محمد یاسین تسل">
                        </div>
                    </div>
                    
                    <div class="mb-3">
                        <label for="regUsername" class="form-label" data-i18n="register.username">د کارن نوم</label>
                        <div class="input-group">
                            <span class="input-group-text bg-light"><i class="fas fa-at"></i></span>
                            <input type="text" class="form-control" id="regUsername" data-i18n-placeholder="register.usernamePlaceholder" placeholder="لکه: myaseen">
                        </div>
                    </div>
                    
                    <div class="mb-3">
                        <label for="regEmail" class="form-label" data-i18n="register.email">ایمیل ادرس</label>
                        <div class="input-group">
                            <span class="input-group-text bg-light"><i class="fas fa-envelope"></i></span>
                            <input type="email" class="form-control" id="regEmail" data-i18n-placeholder="register.emailPlaceholder" placeholder="لکه: myaseen@example.com">
                        </div>
                    </div>
                    
                    <div class="mb-3">
                        <label for="regPassword" class="form-label" data-i18n="register.password">پاسورډ</label>
                        <div class="input-group">
                            <span class="input-group-text bg-light"><i class="fas fa-lock"></i></span>
                            <input type="password" class="form-control" id="regPassword" data-i18n-placeholder="register.passwordPlaceholder" placeholder="لږ تر لږه 6 حروف">
                        </div>
                    </div>
                    
                    <div class="mb-3">
                        <label for="regConfirmPassword" class="form-label" data-i18n="register.confirmPassword">د پاسورډ تایید</label>
                        <div class="input-group">
                            <span class="input-group-text bg-light"><i class="fas fa-lock"></i></span>
                            <input type="password" class="form-control" id="regConfirmPassword" data-i18n-placeholder="register.confirmPasswordPlaceholder" placeholder="پاسورډ بیا تکرار کړئ">
                        </div>
                    </div>
                    
                    <div class="mb-3">
                        <label for="regRole" class="form-label" data-i18n="register.role">دنده</label>
                        <select class="form-select" id="regRole">
                            <option value="user" data-i18n="register.roleUser">کاروونکی</option>
                            <option value="operator" data-i18n="register.roleOperator">اپریټر</option>
                            <option value="admin" data-i18n="register.roleAdmin">اډمین</option>
                        </select>
                    </div>
                    
                    <div class="d-grid gap-2 mb-3">
                        <button class="btn btn-success" id="registerButton">
                            <i class="fas fa-user-plus me-2"></i>
                            <span data-i18n="register.registerButton">حساب جوړول</span>
                        </button>
                    </div>
                    
                    <div class="text-center">
                        <p class="mb-0">
                            <span data-i18n="register.haveAccount">لا دمخه حساب لرئ؟</span>
                            <a href="#" class="text-decoration-none ms-1" id="showLoginForm" data-i18n="register.loginLink">داخلیدل</a>
                        </p>
                    </div>
                </div>
                
                <!-- Forgot Password Form -->
                <div id="forgotPasswordForm" style="display: none;">
                    <h4 class="text-center mb-4" style="color: var(--primary-color);" data-i18n="forgotPassword.title">پاسورډ هیر دی؟</h4>
                    
                    <div class="alert alert-info alert-custom mb-4">
                        <i class="fas fa-info-circle me-2"></i>
                        <span data-i18n="forgotPassword.instructions">خپل ایمیل ادرس دننه کړئ، موږ به تاسو ته د پاسورډ بیارغونې لینک واستوو.</span>
                    </div>
                    
                    <div class="mb-3">
                        <label for="forgotEmail" class="form-label" data-i18n="forgotPassword.email">ایمیل ادرس</label>
                        <div class="input-group">
                            <span class="input-group-text bg-light"><i class="fas fa-envelope"></i></span>
                            <input type="email" class="form-control" id="forgotEmail" data-i18n-placeholder="forgotPassword.emailPlaceholder" placeholder="خپل ایمیل ادرس دننه کړئ">
                        </div>
                    </div>
                    
                    <div class="d-grid gap-2 mb-3">
                        <button class="btn btn-warning" id="resetPasswordButton">
                            <i class="fas fa-paper-plane me-2"></i>
                            <span data-i18n="forgotPassword.resetButton">پاسورډ بیارغول</span>
                        </button>
                    </div>
                    
                    <div class="text-center">
                        <p class="mb-0">
                            <a href="#" class="text-decoration-none" id="showLoginFormFromForgot" data-i18n="forgotPassword.backToLogin">بیرته داخیلیدو ته</a>
                        </p>
                    </div>
                </div>
            </div>
            
            <div class="login-footer">
                <p class="mb-0 text-muted">© ۲۰۲۶ <span data-i18n="footer.copyright">د وسایطو مدیریت سیستم</span></p>
                <p class="mb-0 text-muted" data-i18n="footer.description">د افغانستان د داخلي سفرونو مدیریت</p>
            </div>
        </div>
    </div>

    <!-- Main System -->
    <div id="mainContent" class="main-content">
        <!-- Header -->
        <header class="header">
            <div class="container">
                <div class="d-flex justify-content-between align-items-center">
                    <div class="logo">
                        <i class="fas fa-truck-loading"></i>
                        <span data-i18n="header.title">د وسایطو مدیریت سیستم</span>
                    </div>
                    <div class="text-end d-none d-md-block">
                        <div id="current-date-time" class="text-light"></div>
                        <div class="text-warning" data-i18n="header.subtitle">د افغانستان داخلي سفرونه</div>
                    </div>
                    <div class="user-info">
                        <!-- Language Switcher -->
                        <div class="language-switcher me-3">
                            <button class="lang-btn" id="headerLangBtn">
                                <i class="fas fa-language"></i>
                                <span id="headerLangText">پښتو</span>
                            </button>
                            <div class="lang-dropdown" id="headerLangDropdown">
                                <div class="lang-option active" data-lang="ps">
                                    <i class="fas fa-flag"></i>
                                    <span>پښتو</span>
                                </div>
                                <div class="lang-option" data-lang="en">
                                    <i class="fas fa-flag-usa"></i>
                                    <span>English</span>
                                </div>
                                <div class="lang-option" data-lang="fa">
                                    <i class="fas fa-flag"></i>
                                    <span>دری</span>
                                </div>
                            </div>
                        </div>
                        
                        <!-- Theme Toggle in Header -->
                        <div class="me-3">
                            <label class="theme-switch" title="تاریک/روښانه مود">
                                <input type="checkbox" id="headerThemeToggle">
                                <span class="theme-slider">
                                    <i class="fas fa-sun theme-icon sun"></i>
                                    <i class="fas fa-moon theme-icon moon"></i>
                                </span>
                            </label>
                        </div>
                        
                        <div class="user-avatar" id="userAvatar">
                            <!-- User's first letter will be shown here -->
                        </div>
                        <div>
                            <div class="text-light fw-bold" id="userFullName"></div>
                            <div class="text-light small" id="userRole"></div>
                        </div>
                        <button class="btn btn-sm btn-warning ms-3" id="logoutButton">
                            <i class="fas fa-sign-out-alt"></i>
                        </button>
                    </div>
                </div>
            </div>
        </header>

        <!-- Main Section -->
        <main class="container my-4">
            <!-- Statistics Cards -->
            <div class="row mb-4">
                <div class="col-md-2 col-sm-6 col-6">
                    <div class="stat-card stat-card-1">
                        <i class="fas fa-registered"></i>
                        <h5 id="total-vehicles">0</h5>
                        <small data-i18n="stats.totalRegistered">ټول ثبت شوي</small>
                    </div>
                </div>
                <div class="col-md-2 col-sm-6 col-6">
                    <div class="stat-card stat-card-2">
                        <i class="fas fa-sign-in-alt"></i>
                        <h5 id="entered-vehicles">0</h5>
                        <small data-i18n="stats.enteredToday">نن ورود شوي</small>
                    </div>
                </div>
                <div class="col-md-2 col-sm-6 col-6">
                    <div class="stat-card stat-card-5">
                        <i class="fas fa-box-open"></i>
                        <h5 id="loaded-vehicles">0</h5>
                        <small data-i18n="stats.loaded">بار شوي</small>
                    </div>
                </div>
                <div class="col-md-2 col-sm-6 col-6">
                    <div class="stat-card stat-card-3">
                        <i class="fas fa-sign-out-alt"></i>
                        <h5 id="exited-vehicles">0</h5>
                        <small data-i18n="stats.exitedToday">نن خروج شوي</small>
                    </div>
                </div>
                <div class="col-md-2 col-sm-6 col-6">
                    <div class="stat-card stat-card-4">
                        <i class="fas fa-truck"></i>
                        <h5 id="inside-vehicles">0</h5>
                        <small data-i18n="stats.insideSystem">په سیستم کې</small>
                    </div>
                </div>
                <div class="col-md-2 col-sm-6 col-6">
                    <div class="stat-card" style="background: linear-gradient(135deg, #e74c3c, #c0392b);">
                        <i class="fas fa-clock"></i>
                        <h5 id="waiting-vehicles">0</h5>
                        <small data-i18n="stats.waitingForLoad">د بار انتظار</small>
                    </div>
                </div>
            </div>

            <!-- Tabs Section -->
            <ul class="nav nav-tabs mb-4" id="systemTabs" role="tablist">
                <li class="nav-item" role="presentation">
                    <button class="nav-link active" id="register-tab" data-bs-toggle="tab" data-bs-target="#register" type="button" role="tab" data-i18n="tabs.register">ثبت وسایط</button>
                </li>
                <li class="nav-item" role="presentation">
                    <button class="nav-link" id="entry-tab" data-bs-toggle="tab" data-bs-target="#entry" type="button" role="tab" data-i18n="tabs.entry">ورودی دروازه</button>
                </li>
                <li class="nav-item" role="presentation">
                    <button class="nav-link" id="load-tab" data-bs-toggle="tab" data-bs-target="#load" type="button" role="tab" data-i18n="tabs.load">بارګیری</button>
                </li>
                <li class="nav-item" role="presentation">
                    <button class="nav-link" id="exit-tab" data-bs-toggle="tab" data-bs-target="#exit" type="button" role="tab" data-i18n="tabs.exit">خروجی دروازه</button>
                </li>
                <li class="nav-item" role="presentation">
                    <button class="nav-link" id="users-tab" data-bs-toggle="tab" data-bs-target="#users" type="button" role="tab" data-i18n="tabs.users">د کارونکي مدیریت</button>
                </li>
                <li class="nav-item" role="presentation">
                    <button class="nav-link" id="list-tab" data-bs-toggle="tab" data-bs-target="#list" type="button" role="tab" data-i18n="tabs.list">د ثبت شویو لیدل</button>
                </li>
            </ul>

            <!-- Tabs Content -->
            <div class="tab-content" id="systemTabsContent">
                <!-- Vehicle Registration Section -->
                <div class="tab-pane fade show active" id="register" role="tabpanel">
                    <div class="row fade-in">
                        <div class="col-lg-8">
                            <div class="card">
                                <div class="card-header">
                                    <i class="fas fa-truck-loading me-2"></i>
                                    <span data-i18n="registerVehicle.title">د وسایطو نوی ثبت</span>
                                </div>
                                <div class="card-body">
                                    <form id="vehicleRegistrationForm">
                                        <div class="row">
                                            <div class="col-md-6 mb-3">
                                                <label for="vehicleType" class="form-label required" data-i18n="registerVehicle.vehicleType">د موټر نوعیت</label>
                                                <select class="form-select" id="vehicleType" required>
                                                    <option value="" selected disabled data-i18n="registerVehicle.selectOption">ټاکل...</option>
                                                    <option value="خاور">خاور</option>
                                                    <option value="ده چرخ">ده چرخ</option>
                                                    <option value="هشت چرخ">هشت چرخ</option>
                                                    <option value="ده چرڅ">ده چرڅ</option>
                                                    <option value="ټیله دار">ټیله دار</option>
                                                    <option value="ټیلر بغلی">ټیلر بغلی</option>
                                                    <option value="ټیلر ترپالی">ټیلر ترپالی</option>
                                                    <option value="سواری کش">سواری کش</option>
                                                    <option value="کانتینری">کانتینری</option>
                                                    <option value="بس">بس</option>
                                                    <option value="مینی بس">مینی بس</option>
                                                    <option value="موټر">موټر</option>
                                                    <option value="وانت">وانت</option>
                                                    <option value="موټرسایکل">موټرسایکل</option>
                                                </select>
                                            </div>
                                            <div class="col-md-6 mb-3">
                                                <label for="plateNumber" class="form-label required" data-i18n="registerVehicle.plateNumber">د موټر پلیټ نمبر</label>
                                                <input type="text" class="form-control" id="plateNumber" data-i18n-placeholder="registerVehicle.plateNumberPlaceholder" placeholder="لکه: کابل ۱۲۳۴۵" required>
                                            </div>
                                        </div>
                                        
                                        <div class="row">
                                            <div class="col-md-6 mb-3">
                                                <label for="chassisNumber" class="form-label required" data-i18n="registerVehicle.chassisNumber">شاسی نمبر</label>
                                                <input type="text" class="form-control" id="chassisNumber" required>
                                            </div>
                                            <div class="col-md-6 mb-3">
                                                <label for="engineNumber" class="form-label required" data-i18n="registerVehicle.engineNumber">انجن نمبر</label>
                                                <input type="text" class="form-control" id="engineNumber" required>
                                            </div>
                                        </div>
                                        
                                        <div class="row">
                                            <div class="col-md-6 mb-3">
                                                <label for="companyName" class="form-label required" data-i18n="registerVehicle.companyName">د شرکت نوم</label>
                                                <select class="form-select" id="companyName" required>
                                                    <option value="" selected disabled data-i18n="registerVehicle.selectOption">ټاکل...</option>
                                                    <option value="ارزگان شرکت">ارزگان شرکت</option>
                                                    <option value="سپین ګړی شرکت">سپین ګړی شرکت</option>
                                                    <option value="کندهاري شرکت">کندهاري شرکت</option>
                                                    <option value="نورستان شرکت">نورستان شرکت</option>
                                                    <option value="پامیر شرکت">پامیر شرکت</option>
                                                    <option value="خراسان شرکت">خراسان شرکت</option>
                                                    <option value="بلخ شرکت">بلخ شرکت</option>
                                                    <option value="نور شرکت">نور شرکت</option>
                                                </select>
                                            </div>
                                            <div class="col-md-6 mb-3">
                                                <label for="driverName" class="form-label required" data-i18n="registerVehicle.driverName">د ډریور نوم</label>
                                                <input type="text" class="form-control" id="driverName" data-i18n-placeholder="registerVehicle.driverNamePlaceholder" placeholder="لکه:  تسل امینی" required>
                                            </div>
                                        </div>
                                        
                                        <div class="row">
                                            <div class="col-md-6 mb-3">
                                                <label for="driverPhone" class="form-label required" data-i18n="registerVehicle.driverPhone">د ډریور د اړیکې شمیره</label>
                                                <input type="text" class="form-control" id="driverPhone" data-i18n-placeholder="registerVehicle.driverPhonePlaceholder" placeholder="لکه: ۰۷۰۰۱۲۳۴۵۶" required>
                                            </div>
                                            <div class="col-md-6 mb-3">
                                                <label for="driverId" class="form-label" data-i18n="registerVehicle.driverId">د ډریور د تذکرې نمبر</label>
                                                <input type="text" class="form-control" id="driverId" data-i18n-placeholder="registerVehicle.driverIdPlaceholder" placeholder="لکه: ۱۲۳۴۵۶۷۸۹">
                                            </div>
                                        </div>
                                        
                                        <div class="d-grid gap-2 d-md-flex justify-content-md-end">
                                            <button type="reset" class="btn btn-secondary me-md-2">
                                                <i class="fas fa-redo me-2"></i>
                                                <span data-i18n="buttons.reset">پاکول</span>
                                            </button>
                                            <button type="submit" class="btn btn-primary">
                                                <i class="fas fa-save me-2"></i>
                                                <span data-i18n="buttons.register">ثبتول</span>
                                            </button>
                                        </div>
                                    </form>
                                </div>
                            </div>
                        </div>
                        
                        <div class="col-lg-4">
                            <div class="card">
                                <div class="card-header">
                                    <i class="fas fa-info-circle me-2"></i>
                                    <span data-i18n="guide.title">لارښود</span>
                                </div>
                                <div class="card-body">
                                    <h6 data-i18n="guide.registrationInstructions">د ثبت کولو لارښوونې:</h6>
                                    <div class="guide-item" data-i18n="guide.instruction1">1. د موټر ټولې مالومات په سمه توګه ډک کړئ</div>
                                    <div class="guide-item" data-i18n="guide.instruction2">2. ستاسو د ثبت شوي موټر پلیټ باید یوازې وي</div>
                                    <div class="guide-item" data-i18n="guide.instruction3">3. د ثبتولو وروسته، موټر کولی شي د ورودی دروازې څخه داخل شي</div>
                                    <div class="guide-item" data-i18n="guide.instruction4">4. وروسته له ورود، موټر باید بار ته معرفي شي</div>
                                    <div class="guide-item" data-i18n="guide.instruction5">5. هر موټر باید د خروجي دروازې څخه تیریږي تر څو سیستم څخه پاک شي</div>
                                    
                                    <div class="mt-4">
                                        <h6 data-i18n="guide.categoriesList">د کټګوریو لړلیک:</h6>
                                        <div class="d-flex flex-wrap">
                                            <span class="zone-badge bg-primary text-white m-1">خاور</span>
                                            <span class="zone-badge bg-success text-white m-1">ده چرخ</span>
                                            <span class="zone-badge bg-warning text-dark m-1">هشت چرخ</span>
                                            <span class="zone-badge bg-info text-white m-1">ده چرڅ</span>
                                            <span class="zone-badge bg-danger text-white m-1">ټیله دار</span>
                                            <span class="zone-badge bg-secondary text-white m-1">ټیلر بغلی</span>
                                            <span class="zone-badge bg-dark text-white m-1">ټیلر ترپالی</span>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Entry Gate Section -->
                <div class="tab-pane fade" id="entry" role="tabpanel">
                    <div class="row fade-in">
                        <div class="col-lg-8">
                            <div class="card">
                                <div class="card-header">
                                    <i class="fas fa-sign-in-alt me-2"></i>
                                    <span data-i18n="entryGate.title">د ورودی دروازې مالومات</span>
                                </div>
                                <div class="card-body">
                                    <form id="entryGateForm">
                                        <div class="row">
                                            <div class="col-md-6 mb-3">
                                                <label for="entryZone" class="form-label required" data-i18n="entryGate.zone">زون انتخاب</label>
                                                <select class="form-select" id="entryZone" required>
                                                    <option value="" selected disabled data-i18n="entryGate.selectOption">ټاکل...</option>
                                                    <option value="هرات">هرات زون</option>
                                                    <option value="قندهار">لوی قندهار زون</option>
                                                    <option value="ننګرهار">لوی ننګرهار زون</option>
                                                    <option value="پکتیا">لویه پکتیا زون</option>
                                                    <option value="مرکزی">مرکزی زون</option>
                                                </select>
                                            </div>
                                            <div class="col-md-6 mb-3">
                                                <label for="entryGateNumber" class="form-label required" data-i18n="entryGate.gateNumber">د دروازې نمبر</label>
                                                <select class="form-select" id="entryGateNumber" required>
                                                    <option value="" selected disabled data-i18n="entryGate.selectOption">ټاکل...</option>
                                                    <option value="دروازه ۱">دروازه ۱</option>
                                                    <option value="دروازه ۲">دروازه ۲</option>
                                                    <option value="دروازه ۳">دروازه ۳</option>
                                                    <option value="دروازه ۴">دروازه ۴</option>
                                                </select>
                                            </div>
                                        </div>
                                        
                                        <div class="row">
                                            <div class="col-md-6 mb-3">
                                                <label for="entryVehicleCategory" class="form-label required" data-i18n="entryGate.vehicleCategory">د وسیلې کټګوري</label>
                                                <select class="form-select" id="entryVehicleCategory" required>
                                                    <option value="" selected disabled data-i18n="entryGate.selectOption">ټاکل...</option>
                                                    <option value="خاور">خاور</option>
                                                    <option value="ده چرخ">ده چرخ</option>
                                                    <option value="هشت چرخ">هشت چرخ</option>
                                                    <option value="ده چرڅ">ده چرڅ</option>
                                                    <option value="ټیله دار">ټیله دار</option>
                                                    <option value="ټیلر بغلی">ټیلر بغلی</option>
                                                    <option value="ټیلر ترپالی">ټیلر ترپالی</option>
                                                    <option value="سواری کش">سواری کش</option>
                                                    <option value="کانتینری">کانتینری</option>
                                                    <option value="بس">بس</option>
                                                    <option value="مینی بس">مینی بس</option>
                                                    <option value="موټر">موټر</option>
                                                    <option value="وانت">وانت</option>
                                                    <option value="موټرسایکل">موټرسایکل</option>
                                                </select>
                                            </div>
                                            <div class="col-md-6 mb-3">
                                                <label for="entryPlateNumber" class="form-label required" data-i18n="entryGate.plateNumber">د موټر پلیټ نمبر</label>
                                                <input type="text" class="form-control" id="entryPlateNumber" data-i18n-placeholder="entryGate.plateNumberPlaceholder" placeholder="ثبت شوي پلیټ دننه کړئ" required>
                                                <div class="form-text" id="plateCheckResult"></div>
                                            </div>
                                        </div>
                                        
                                        <div class="row">
                                            <div class="col-md-12 mb-3">
                                                <label for="entryRemarks" class="form-label" data-i18n="entryGate.remarks">اضافي یادښتونه</label>
                                                <textarea class="form-control" id="entryRemarks" rows="2" data-i18n-placeholder="entryGate.remarksPlaceholder" placeholder="د ورود په اړه اضافي معلومات..."></textarea>
                                            </div>
                                        </div>
                                        
                                        <div class="d-grid gap-2 d-md-flex justify-content-md-end">
                                            <button type="reset" class="btn btn-secondary me-md-2">
                                                <i class="fas fa-redo me-2"></i>
                                                <span data-i18n="buttons.reset">پاکول</span>
                                            </button>
                                            <button type="submit" class="btn btn-success">
                                                <i class="fas fa-sign-in-alt me-2"></i>
                                                <span data-i18n="buttons.registerEntry">ورود ثبتول</span>
                                            </button>
                                        </div>
                                    </form>
                                </div>
                            </div>
                        </div>
                        
                        <div class="col-lg-4">
                            <div class="card">
                                <div class="card-header">
                                    <i class="fas fa-map-marked-alt me-2"></i>
                                    <span data-i18n="zonesInfo.title">د زونونو مالومات</span>
                                </div>
                                <div class="card-body">
                                    <div class="mb-3">
                                        <h6 data-i18n="zonesInfo.zonesAndProvinces">زونونه او ولایتونه:</h6>
                                        <div class="accordion" id="zonesAccordion">
                                            <div class="accordion-item">
                                                <h2 class="accordion-header">
                                                    <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#zone1">
                                                        هرات زون
                                                    </button>
                                                </h2>
                                                <div id="zone1" class="accordion-collapse collapse show" data-bs-parent="#zonesAccordion">
                                                    <div class="accordion-body">
                                                        <span class="badge bg-secondary m-1">هرات</span>
                                                        <span class="badge bg-secondary m-1">نیمروز</span>
                                                        <span class="badge bg-secondary m-1">فراه</span>
                                                    </div>
                                                </div>
                                            </div>
                                            <div class="accordion-item">
                                                <h2 class="accordion-header">
                                                    <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#zone2">
                                                        لوی قندهار زون
                                                    </button>
                                                </h2>
                                                <div id="zone2" class="accordion-collapse collapse" data-bs-parent="#zonesAccordion">
                                                    <div class="accordion-body">
                                                        <span class="badge bg-secondary m-1">قندهار</span>
                                                        <span class="badge bg-secondary m-1">هلمند</span>
                                                        <span class="badge bg-secondary m-1">زابل</span>
                                                        <span class="badge bg-secondary m-1">اروزګان</span>
                                                    </div>
                                                </div>
                                            </div>
                                            <div class="accordion-item">
                                                <h2 class="accordion-header">
                                                    <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#zone3">
                                                        لوی ننګرهار زون
                                                    </button>
                                                </h2>
                                                <div id="zone3" class="accordion-collapse collapse" data-bs-parent="#zonesAccordion">
                                                    <div class="accordion-body">
                                                        <span class="badge bg-secondary m-1">ننګرهار</span>
                                                        <span class="badge bg-secondary m-1">کنر</span>
                                                        <span class="badge bg-secondary m-1">لغمان</span>
                                                        <span class="badge bg-secondary m-1">نورستان</span>
                                                    </div>
                                                </div>
                                            </div>
                                            <div class="accordion-item">
                                                <h2 class="accordion-header">
                                                    <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#zone4">
                                                        لویه پکتیا زون
                                                    </button>
                                                </h2>
                                                <div id="zone4" class="accordion-collapse collapse" data-bs-parent="#zonesAccordion">
                                                    <div class="accordion-body">
                                                        <span class="badge bg-secondary m-1">پکتیا</span>
                                                        <span class="badge bg-secondary m-1">مزارشریف</span>
                                                        <span class="badge bg-secondary m-1">بدخشان</span>
                                                        <span class="badge bg-secondary m-1">فاریاب</span>
                                                    </div>
                                                </div>
                                            </div>
                                            <div class="accordion-item">
                                                <h2 class="accordion-header">
                                                    <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#zone5">
                                                        مرکزی زون
                                                    </button>
                                                </h2>
                                                <div id="zone5" class="accordion-collapse collapse" data-bs-parent="#zonesAccordion">
                                                    <div class="accordion-body">
                                                        <span class="badge bg-secondary m-1">کابل</span>
                                                        <span class="badge bg-secondary m-1">پروان</span>
                                                        <span class="badge bg-secondary m-1">کاپیسا</span>
                                                        <span class="badge bg-secondary m-1">پنجشیر</span>
                                                        <span class="badge bg-secondary m-1">وردګ</span>
                                                        <span class="badge bg-secondary m-1">لوګر</span>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    
                                    <div class="alert alert-info alert-custom mt-3">
                                        <i class="fas fa-exclamation-circle me-2"></i>
                                        <strong data-i18n="zonesInfo.noteTitle">یادونه:</strong>
                                        <span data-i18n="zonesInfo.noteText">په ورودی دروازه کې یوازې زون انتخاب کېږي. د ولایت انتخاب د بارګیری په وخت کې کېږي.</span>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Loading Section -->
                <div class="tab-pane fade" id="load" role="tabpanel">
                    <div class="row fade-in">
                        <div class="col-lg-8">
                            <div class="card">
                                <div class="card-header">
                                    <i class="fas fa-box-open me-2"></i>
                                    <span data-i18n="loadAssignment.title">د وسایطو بارګیری</span>
                                </div>
                                <div class="card-body">
                                    <form id="loadAssignmentForm">
                                        <div class="row">
                                            <div class="col-md-6 mb-3">
                                                <label for="loadPlateNumber" class="form-label required" data-i18n="loadAssignment.plateNumber">د موټر پلیټ نمبر</label>
                                                <input type="text" class="form-control" id="loadPlateNumber" data-i18n-placeholder="loadAssignment.plateNumberPlaceholder" placeholder="د بار کیدونکي موټر پلیټ" required>
                                                <div class="form-text" id="loadPlateCheckResult"></div>
                                            </div>
                                            <div class="col-md-6 mb-3">
                                                <label for="loadProvince" class="form-label required" data-i18n="loadAssignment.province">ولایت انتخاب</label>
                                                <select class="form-select" id="loadProvince" required disabled>
                                                    <option value="" selected disabled data-i18n="loadAssignment.selectProvinceOption">لومړی پلیټ دننه کړئ...</option>
                                                </select>
                                            </div>
                                        </div>
                                        
                                        <div class="row">
                                            <div class="col-md-6 mb-3">
                                                <label for="loadType" class="form-label required" data-i18n="loadAssignment.loadType">د بار ډول</label>
                                                <select class="form-select" id="loadType" required>
                                                    <option value="" selected disabled data-i18n="loadAssignment.selectOption">ټاکل...</option>
                                                    <option value="خوراکي مواد">خوراکي مواد</option>
                                                    <option value="ساختماني مواد">ساختماني مواد</option>
                                                    <option value="فرنیچر">فرنیچر</option>
                                                    <option value="کرنيز توليدات">کرنيز توليدات</option>
                                                    <option value="حیوانات">حیوانات</option>
                                                    <option value="طبي توکي">طبي توکي</option>
                                                    <option value="برېښنايي توکي">برېښنايي توکي</option>
                                                    <option value="کیمیاوي مواد">کیمیاوي مواد</option>
                                                    <option value="د سپورتو توکي">د سپورتو توکي</option>
                                                    <option value="نور">نور</option>
                                                </select>
                                            </div>
                                            <div class="col-md-6 mb-3">
                                                <label for="loadWeight" class="form-label required" data-i18n="loadAssignment.loadWeight">د بار وزن (ټنه)</label>
                                                <input type="number" class="form-control" id="loadWeight" min="0.1" step="0.1" data-i18n-placeholder="loadAssignment.loadWeightPlaceholder" placeholder="لکه: ۵.۵" required>
                                            </div>
                                        </div>
                                        
                                        <div class="row">
                                            <div class="col-md-6 mb-3">
                                                <label for="loadDestination" class="form-label required" data-i18n="loadAssignment.destination">د بار مقصد</label>
                                                <input type="text" class="form-control" id="loadDestination" data-i18n-placeholder="loadAssignment.destinationPlaceholder" placeholder="لکه: کابل ښار" required>
                                            </div>
                                            <div class="col-md-6 mb-3">
                                                <label for="loadReceiver" class="form-label" data-i18n="loadAssignment.receiver">د بار اخيستونکی نوم</label>
                                                <input type="text" class="form-control" id="loadReceiver" data-i18n-placeholder="loadAssignment.receiverPlaceholder" placeholder="لکه: محمد یاسین تسل">
                                            </div>
                                        </div>
                                        
                                        <div class="row">
                                            <div class="col-md-12 mb-3">
                                                <label for="loadDescription" class="form-label" data-i18n="loadAssignment.description">د بار تفصیل</label>
                                                <textarea class="form-control" id="loadDescription" rows="3" data-i18n-placeholder="loadAssignment.descriptionPlaceholder" placeholder="د بار نور تفصیلات..."></textarea>
                                            </div>
                                        </div>
                                        
                                        <div class="row mb-4">
                                            <div class="col-md-12">
                                                <div class="card bg-light text-dark">
                                                    <div class="card-body p-3">
                                                        <h6 id="loadVehicleInfoTitle" data-i18n="loadAssignment.vehicleInfo">د وسیلې مالومات:</h6>
                                                        <div id="loadVehicleInfoDetails" class="text-muted">
                                                            <span data-i18n="loadAssignment.vehicleInfoPlaceholder">دلته به د وسیلې مالومات وښودل شي کله چې پلیټ نمبر داخل کړئ</span>
                                                        </div>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                        
                                        <div class="d-grid gap-2 d-md-flex justify-content-md-end">
                                            <button type="reset" class="btn btn-secondary me-md-2">
                                                <i class="fas fa-redo me-2"></i>
                                                <span data-i18n="buttons.reset">پاکول</span>
                                            </button>
                                            <button type="submit" class="btn btn-info">
                                                <i class="fas fa-box-open me-2"></i>
                                                <span data-i18n="buttons.registerLoad">بار ثبتول</span>
                                            </button>
                                        </div>
                                    </form>
                                </div>
                            </div>
                        </div>
                        
                        <div class="col-lg-4">
                            <div class="card">
                                <div class="card-header">
                                    <i class="fas fa-list-ol me-2"></i>
                                    <span data-i18n="waitingVehicles.title">د بار انتظار وسایط</span>
                                </div>
                                <div class="card-body">
                                    <div id="waitingVehiclesList">
                                        <p class="text-muted" data-i18n="waitingVehicles.empty">تر اوسه هیڅ وسیله د بار انتظار نه دی</p>
                                    </div>
                                </div>
                            </div>
                            
                            <div class="card mt-4">
                                <div class="card-header">
                                    <i class="fas fa-history me-2"></i>
                                    <span data-i18n="recentLoads.title">وروستي بارګیرۍ</span>
                                </div>
                                <div class="card-body">
                                    <div id="recentLoadsList">
                                        <p class="text-muted" data-i18n="recentLoads.empty">تر اوسه هیڅ بار ثبت نه دی شوی</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Exit Gate Section -->
                <div class="tab-pane fade" id="exit" role="tabpanel">
                    <div class="row fade-in">
                        <div class="col-lg-8">
                            <div class="card">
                                <div class="card-header">
                                    <i class="fas fa-sign-out-alt me-2"></i>
                                    <span data-i18n="exitGate.title">د خروجي دروازې مالومات</span>
                                </div>
                                <div class="card-body">
                                    <form id="exitGateForm">
                                        <div class="row">
                                            <div class="col-md-12 mb-4">
                                                <div class="alert alert-warning alert-custom">
                                                    <i class="fas fa-info-circle me-2"></i>
                                                    <strong data-i18n="exitGate.infoTitle">معلومات:</strong>
                                                    <span data-i18n="exitGate.infoText">د خروجي دروازې څخه تیریدو لپاره، موټر باید په سیستم کې ثبت، ورود او بار شوی وي.</span>
                                                </div>
                                            </div>
                                        </div>
                                        
                                        <div class="row">
                                            <div class="col-md-8 mb-3">
                                                <label for="exitPlateNumber" class="form-label required" data-i18n="exitGate.plateNumber">د موټر پلیټ نمبر</label>
                                                <input type="text" class="form-control" id="exitPlateNumber" data-i18n-placeholder="exitGate.plateNumberPlaceholder" placeholder="د خروجي موټر پلیټ دننه کړئ" required>
                                                <div class="form-text" id="exitPlateCheckResult"></div>
                                            </div>
                                            <div class="col-md-4 mb-3">
                                                <label for="exitTime" class="form-label required" data-i18n="exitGate.exitTime">د خروج وخت</label>
                                                <input type="text" class="form-control" id="exitTime" value="" readonly>
                                            </div>
                                        </div>
                                        
                                        <div class="row">
                                            <div class="col-md-6 mb-3">
                                                <label for="exitGateNumber" class="form-label required" data-i18n="exitGate.gateNumber">د خروجي دروازې نمبر</label>
                                                <select class="form-select" id="exitGateNumber" required>
                                                    <option value="" selected disabled data-i18n="exitGate.selectOption">ټاکل...</option>
                                                    <option value="دروازه ۱">دروازه ۱</option>
                                                    <option value="دروازه ۲">دروازه ۲</option>
                                                    <option value="دروازه ۳">دروازه ۳</option>
                                                    <option value="دروازه ۴">دروازه ۴</option>
                                                </select>
                                            </div>
                                            <div class="col-md-6 mb-3">
                                                <label for="exitRemarks" class="form-label" data-i18n="exitGate.remarks">اضافي یادښتونه</label>
                                                <textarea class="form-control" id="exitRemarks" rows="2" data-i18n-placeholder="exitGate.remarksPlaceholder" placeholder="د خروج په اړه اضافي معلومات..."></textarea>
                                            </div>
                                        </div>
                                        
                                        <div class="row mb-4">
                                            <div class="col-md-12">
                                                <div class="card bg-light text-dark">
                                                    <div class="card-body p-3">
                                                        <h6 id="exitVehicleInfoTitle" data-i18n="exitGate.vehicleInfo">د وسیلې مالومات:</h6>
                                                        <div id="exitVehicleInfoDetails" class="text-muted">
                                                            <span data-i18n="exitGate.vehicleInfoPlaceholder">دلته به د وسیلې مالومات وښودل شي کله چې پلیټ نمبر داخل کړئ</span>
                                                        </div>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                        
                                        <div class="d-grid gap-2 d-md-flex justify-content-md-end">
                                            <button type="reset" class="btn btn-secondary me-md-2">
                                                <i class="fas fa-redo me-2"></i>
                                                <span data-i18n="buttons.reset">پاکول</span>
                                            </button>
                                            <button type="submit" class="btn btn-warning">
                                                <i class="fas fa-sign-out-alt me-2"></i>
                                                <span data-i18n="buttons.registerExit">خروج ثبتول</span>
                                            </button>
                                        </div>
                                    </form>
                                </div>
                            </div>
                        </div>
                        
                        <div class="col-lg-4">
                            <div class="card">
                                <div class="card-header">
                                    <i class="fas fa-history me-2"></i>
                                    <span data-i18n="recentExits.title">نني خروجونه</span>
                                </div>
                                <div class="card-body">
                                    <div id="recentExitsList">
                                        <p class="text-muted" data-i18n="recentExits.empty">تر اوسه هیڅ خروج ثبت نه دی شوی</p>
                                    </div>
                                </div>
                            </div>
                            
                            <div class="card mt-4">
                                <div class="card-header">
                                    <i class="fas fa-clipboard-check me-2"></i>
                                    <span data-i18n="exitGuide.title">د خروجي پروسې لارښود</span>
                                </div>
                                <div class="card-body">
                                    <ol class="list-group list-group-flush list-group-numbered">
                                        <li class="list-group-item" data-i18n="exitGuide.step1">د خروجي موټر پلیټ نمبر دننه کړئ</li>
                                        <li class="list-group-item" data-i18n="exitGuide.step2">د وسیلې مالومات وګورئ</li>
                                        <li class="list-group-item" data-i18n="exitGuide.step3">د خروجي دروازې نمبر وټاکئ</li>
                                        <li class="list-group-item" data-i18n="exitGuide.step4">د خروج د ثبتولو تڼۍ ته فشار ورکړئ</li>
                                    </ol>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- User Management Section -->
                <div class="tab-pane fade" id="users" role="tabpanel">
                    <div class="row fade-in">
                        <div class="col-md-12">
                            <div class="card">
                                <div class="card-header d-flex justify-content-between align-items-center">
                                    <div>
                                        <i class="fas fa-users-cog me-2"></i>
                                        <span data-i18n="userManagement.title">د کارونکي مدیریت</span>
                                    </div>
                                    <div>
                                        <button class="btn btn-sm btn-primary" id="addUserBtn">
                                            <i class="fas fa-user-plus me-1"></i>
                                            <span data-i18n="userManagement.addUser">نوی کارن</span>
                                        </button>
                                    </div>
                                </div>
                                <div class="card-body">
                                    <!-- Admin User Creation Form -->
                                    <div id="adminUserFormContainer" style="display: none;">
                                        <div class="admin-user-form">
                                            <h5 class="mb-3" data-i18n="userManagement.createUser">نوی کارن جوړول</h5>
                                            <form id="adminUserForm">
                                                <div class="row">
                                                    <div class="col-md-4 mb-3">
                                                        <label for="adminFullName" class="form-label required" data-i18n="userManagement.fullName">بشپړ نوم</label>
                                                        <input type="text" class="form-control" id="adminFullName" required>
                                                    </div>
                                                    <div class="col-md-4 mb-3">
                                                        <label for="adminUsername" class="form-label required" data-i18n="userManagement.username">د کارن نوم</label>
                                                        <input type="text" class="form-control" id="adminUsername" required>
                                                    </div>
                                                    <div class="col-md-4 mb-3">
                                                        <label for="adminEmail" class="form-label required" data-i18n="userManagement.email">ایمیل</label>
                                                        <input type="email" class="form-control" id="adminEmail" required>
                                                    </div>
                                                </div>
                                                
                                                <div class="row">
                                                    <div class="col-md-4 mb-3">
                                                        <label for="adminPassword" class="form-label required" data-i18n="userManagement.password">پاسورډ</label>
                                                        <input type="password" class="form-control" id="adminPassword" required>
                                                    </div>
                                                    <div class="col-md-4 mb-3">
                                                        <label for="adminRole" class="form-label required" data-i18n="userManagement.role">دنده</label>
                                                        <select class="form-select" id="adminRole" required>
                                                            <option value="user" data-i18n="userManagement.roleUser">کاروونکی</option>
                                                            <option value="operator" data-i18n="userManagement.roleOperator">اپریټر</option>
                                                            <option value="admin" data-i18n="userManagement.roleAdmin">اډمین</option>
                                                        </select>
                                                    </div>
                                                    <div class="col-md-4 mb-3">
                                                        <label for="adminStatus" class="form-label required" data-i18n="userManagement.status">حالت</label>
                                                        <select class="form-select" id="adminStatus" required>
                                                            <option value="active" data-i18n="userManagement.active">فعال</option>
                                                            <option value="inactive" data-i18n="userManagement.inactive">غیرفعال</option>
                                                        </select>
                                                    </div>
                                                </div>
                                                
                                                <div class="d-flex justify-content-end gap-2">
                                                    <button type="button" class="btn btn-secondary" id="cancelUserForm">
                                                        <i class="fas fa-times me-2"></i>
                                                        <span data-i18n="buttons.cancel">لغوه کول</span>
                                                    </button>
                                                    <button type="submit" class="btn btn-success">
                                                        <i class="fas fa-save me-2"></i>
                                                        <span data-i18n="buttons.save">ذخیره کول</span>
                                                    </button>
                                                </div>
                                            </form>
                                        </div>
                                    </div>
                                    
                                    <div class="table-responsive">
                                        <table class="table table-hover" id="usersTable">
                                            <thead>
                                                <tr>
                                                    <th data-i18n="userManagement.tableNumber">شمیره</th>
                                                    <th data-i18n="userManagement.tableFullName">بشپړ نوم</th>
                                                    <th data-i18n="userManagement.tableUsername">د کارن نوم</th>
                                                    <th data-i18n="userManagement.tableEmail">ایمیل</th>
                                                    <th data-i18n="userManagement.tableRole">دنده</th>
                                                    <th data-i18n="userManagement.tableRegistrationDate">د ثبت نیټه</th>
                                                    <th data-i18n="userManagement.tableStatus">حالت</th>
                                                    <th data-i18n="userManagement.tableActions">عملونه</th>
                                                </tr>
                                            </thead>
                                            <tbody id="usersTableBody">
                                                <!-- Data will be populated from JavaScript -->
                                            </tbody>
                                        </table>
                                    </div>
                                    
                                    <div class="d-flex justify-content-between align-items-center mt-3">
                                        <div class="text-muted" id="usersTableInfo" data-i18n="userManagement.noUsers">هیڅ کارن نه دی موندل شوی</div>
                                        <div>
                                            <button class="btn btn-sm btn-outline-secondary" id="exportUsers">
                                                <i class="fas fa-download me-1"></i>
                                                <span data-i18n="userManagement.exportUsers">کارونکي صادرول</span>
                                            </button>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Registered Vehicles List Section -->
                <div class="tab-pane fade" id="list" role="tabpanel">
                    <div class="row fade-in">
                        <div class="col-md-12">
                            <div class="card">
                                <div class="card-header d-flex justify-content-between align-items-center">
                                    <div>
                                        <i class="fas fa-list me-2"></i>
                                        <span data-i18n="vehicleList.title">ټول ثبت شوي وسایط</span>
                                    </div>
                                    <div>
                                        <button class="btn btn-sm btn-outline-primary" id="filterAll" data-i18n="vehicleList.filterAll">ټول</button>
                                        <button class="btn btn-sm btn-outline-success" id="filterInside" data-i18n="vehicleList.filterInside">په سیستم کې</button>
                                        <button class="btn btn-sm btn-outline-info" id="filterLoaded" data-i18n="vehicleList.filterLoaded">بار شوي</button>
                                        <button class="btn btn-sm btn-outline-warning" id="filterExited" data-i18n="vehicleList.filterExited">خروج شوي</button>
                                        <button class="btn btn-sm btn-outline-secondary" id="filterWaiting" data-i18n="vehicleList.filterWaiting">د بار انتظار</button>
                                    </div>
                                </div>
                                <div class="card-body">
                                    <div class="table-responsive">
                                        <table class="table table-hover" id="vehiclesTable">
                                            <thead>
                                                <tr>
                                                    <th data-i18n="vehicleList.tableNumber">شمیره</th>
                                                    <th data-i18n="vehicleList.tablePlateNumber">پلیټ نمبر</th>
                                                    <th data-i18n="vehicleList.tableType">نوعیت</th>
                                                    <th data-i18n="vehicleList.tableCompany">شرکت</th>
                                                    <th data-i18n="vehicleList.tableDriver">ډریور</th>
                                                    <th data-i18n="vehicleList.tableZone">زون</th>
                                                    <th data-i18n="vehicleList.tableProvince">ولایت</th>
                                                    <th data-i18n="vehicleList.tableLoadType">د بار ډول</th>
                                                    <th data-i18n="vehicleList.tableRegistrationDate">د ثبت نیټه</th>
                                                    <th data-i18n="vehicleList.tableStatus">حالت</th>
                                                    <th data-i18n="vehicleList.tableActions">عملونه</th>
                                                </tr>
                                            </thead>
                                            <tbody id="vehiclesTableBody">
                                                <!-- Data will be populated from JavaScript -->
                                            </tbody>
                                        </table>
                                    </div>
                                    
                                    <div class="d-flex justify-content-between align-items-center mt-3">
                                        <div class="text-muted" id="tableInfo" data-i18n="vehicleList.noVehicles">هیڅ ثبت شوی وسیله نشته</div>
                                        <div>
                                            <button class="btn btn-sm btn-outline-secondary" id="printList">
                                                <i class="fas fa-print me-1"></i>
                                                <span data-i18n="buttons.print">چاپ</span>
                                            </button>
                                            <button class="btn btn-sm btn-outline-secondary" id="exportData">
                                                <i class="fas fa-download me-1"></i>
                                                <span data-i18n="buttons.export">صادرول</span>
                                            </button>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </main>

        <!-- Footer -->
        <footer>
            <div class="container">
                <div class="row">
                    <div class="col-md-6">
                        <h5 data-i18n="footer.title">د وسایطو مدیریت سیستم</h5>
                        <p data-i18n="footer.descriptionFull">دا سیستم د افغانستان د داخلي سفرونو د وسایطو د مدیریت لپاره جوړ شوی دی.</p>
                    </div>
                    <div class="col-md-3">
                        <h5 data-i18n="footer.links">لینکونه</h5>
                        <ul class="list-unstyled">
                            <li><a href="#register" class="text-light" data-i18n="footer.linkRegister">ثبت وسایط</a></li>
                            <li><a href="#entry" class="text-light" data-i18n="footer.linkEntry">ورودی دروازه</a></li>
                            <li><a href="#load" class="text-light" data-i18n="footer.linkLoad">بارګیری</a></li>
                            <li><a href="#exit" class="text-light" data-i18n="footer.linkExit">خروجی دروازه</a></li>
                        </ul>
                    </div>
                    <div class="col-md-3">
                        <h5 data-i18n="footer.contact">اړیکه</h5>
                        <p><i class="fas fa-phone me-2"></i> ۰۷۷۲۵۰۶۰۶۹</p>
                        <p><i class="fas fa-envelope me-2"></i> myaseentasal@gmail.com</p>
                    </div>
                </div>
                <hr class="bg-light">
                <div class="text-center">
                    <p>© ۲۰۲۶ <span data-i18n="footer.copyrightFull">د وسایطو مدیریت سیستم - ټول حقونه خوندي دي</span></p>
                    <p class="small" data-i18n="footer.version">د سیستم ورژن: ۲.۲</p>
                </div>
            </div>
        </footer>
    </div>

    <!-- JavaScript Links -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js"></script>
    <script>
        // Language data
        const translations = {
            ps: {
                // Login section
                "login.title": "د وسایطو مدیریت سیستم",
                "login.subtitle": "د افغانستان داخلي سفرونه",
                "login.formTitle": "د سیستم داخلیدل",
                "login.username": "د کارن نوم",
                "login.usernamePlaceholder": "خپل کارن نوم دننه کړئ",
                "login.password": "پاسورډ",
                "login.passwordPlaceholder": "خپل پاسورډ دننه کړئ",
                "login.remember": "ما په یاد ساتل",
                "login.loginButton": "د سیستم داخلیدل",
                "login.newUser": "څوک یاست؟",
                "login.registerLink": "نوی حساب جوړول",
                "login.forgotPassword": "پاسورډ هیر دی؟",
                
                // Registration form
                "register.title": "نوی حساب جوړول",
                "register.fullName": "بشپړ نوم",
                "register.fullNamePlaceholder": "لکه: محمد یاسین تسل",
                "register.username": "د کارن نوم",
                "register.usernamePlaceholder": "لکه: myaseen",
                "register.email": "ایمیل ادرس",
                "register.emailPlaceholder": "لکه: myaseen@example.com",
                "register.password": "پاسورډ",
                "register.passwordPlaceholder": "لږ تر لږه 6 حروف",
                "register.confirmPassword": "د پاسورډ تایید",
                "register.confirmPasswordPlaceholder": "پاسورډ بیا تکرار کړئ",
                "register.role": "دنده",
                "register.roleUser": "کاروونکی",
                "register.roleOperator": "اپریټر",
                "register.roleAdmin": "اډمین",
                "register.registerButton": "حساب جوړول",
                "register.haveAccount": "لا دمخه حساب لرئ؟",
                "register.loginLink": "داخلیدل",
                
                // Forgot password form
                "forgotPassword.title": "پاسورډ هیر دی؟",
                "forgotPassword.instructions": "خپل ایمیل ادرس دننه کړئ، موږ به تاسو ته د پاسورډ بیارغونې لینک واستوو.",
                "forgotPassword.email": "ایمیل ادرس",
                "forgotPassword.emailPlaceholder": "خپل ایمیل ادرس دننه کړئ",
                "forgotPassword.resetButton": "پاسورډ بیارغول",
                "forgotPassword.backToLogin": "بیرته داخیلیدو ته",
                
                // Settings
                "settings.title": "تنظیمات",
                "settings.themeMode": "مود (تاریک/روښانه)",
                "settings.darkMode": "تاریک مود",
                "settings.lightMode": "روښانه مود",
                "settings.language": "ژبه",
                "settings.background": "بیکګرونډ",
                "settings.systemInfo": "د سیستم معلومات",
                "settings.version": "نسخه",
                "settings.users": "کارونکي",
                "settings.vehicles": "وسایط",
                "settings.lastLogin": "وروستی لاګن",
                "settings.exportData": "ډیټا صادرول",
                "settings.exportAll": "ټول ډیټا صادرول",
                "settings.reset": "تنظیمات ریسیټ کړئ",
                
                // Header
                "header.title": "د وسایطو مدیریت سیستم",
                "header.subtitle": "د افغانستان داخلي سفرونه",
                
                // Statistics
                "stats.totalRegistered": "ټول ثبت شوي",
                "stats.enteredToday": "نن ورود شوي",
                "stats.loaded": "بار شوي",
                "stats.exitedToday": "نن خروج شوي",
                "stats.insideSystem": "په سیستم کې",
                "stats.waitingForLoad": "د بار انتظار",
                
                // Tabs
                "tabs.register": "ثبت وسایط",
                "tabs.entry": "ورودی دروازه",
                "tabs.load": "بارګیری",
                "tabs.exit": "خروجی دروازه",
                "tabs.users": "د کارونکي مدیریت",
                "tabs.list": "د ثبت شویو لیدل",
                
                // Vehicle registration form
                "registerVehicle.title": "د وسایطو نوی ثبت",
                "registerVehicle.vehicleType": "د موټر نوعیت",
                "registerVehicle.selectOption": "ټاکل...",
                "registerVehicle.plateNumber": "د موټر پلیټ نمبر",
                "registerVehicle.plateNumberPlaceholder": "لکه: کابل ۱۲۳۴۵",
                "registerVehicle.chassisNumber": "شاسی نمبر",
                "registerVehicle.engineNumber": "انجن نمبر",
                "registerVehicle.companyName": "د شرکت نوم",
                "registerVehicle.driverName": "د ډریور نوم",
                "registerVehicle.driverNamePlaceholder": "لکه:  تسل امینی",
                "registerVehicle.driverPhone": "د ډریور د اړیکې شمیره",
                "registerVehicle.driverPhonePlaceholder": "لکه: ۰۷۰۰۱۲۳۴۵۶",
                "registerVehicle.driverId": "د ډریور د تذکرې نمبر",
                "registerVehicle.driverIdPlaceholder": "لکه: ۱۲۳۴۵۶۷۸۹",
                
                // Guide
                "guide.title": "لارښود",
                "guide.registrationInstructions": "د ثبت کولو لارښوونې:",
                "guide.instruction1": "1. د موټر ټولې مالومات په سمه توګه ډک کړئ",
                "guide.instruction2": "2. ستاسو د ثبت شوي موټر پلیټ باید یوازې وي",
                "guide.instruction3": "3. د ثبتولو وروسته، موټر کولی شي د ورودی دروازې څخه داخل شي",
                "guide.instruction4": "4. وروسته له ورود، موټر باید بار ته معرفي شي",
                "guide.instruction5": "5. هر موټر باید د خروجي دروازې څخه تیریږي تر څو سیستم څخه پاک شي",
                "guide.categoriesList": "د کټګوریو لړلیک:",
                
                // Entry gate form
                "entryGate.title": "د ورودی دروازې مالومات",
                "entryGate.zone": "زون انتخاب",
                "entryGate.gateNumber": "د دروازې نمبر",
                "entryGate.vehicleCategory": "د وسیلې کټګوري",
                "entryGate.plateNumber": "د موټر پلیټ نمبر",
                "entryGate.plateNumberPlaceholder": "ثبت شوي پلیټ دننه کړئ",
                "entryGate.remarks": "اضافي یادښتونه",
                "entryGate.remarksPlaceholder": "د ورود په اړه اضافي معلومات...",
                
                // Zones information
                "zonesInfo.title": "د زونونو مالومات",
                "zonesInfo.zonesAndProvinces": "زونونه او ولایتونه:",
                "zonesInfo.noteTitle": "یادونه:",
                "zonesInfo.noteText": "په ورودی دروازه کې یوازې زون انتخاب کېږي. د ولایت انتخاب د بارګیری په وخت کې کېږي.",
                
                // Loading form
                "loadAssignment.title": "د وسایطو بارګیری",
                "loadAssignment.plateNumber": "د موټر پلیټ نمبر",
                "loadAssignment.plateNumberPlaceholder": "د بار کیدونکي موټر پلیټ",
                "loadAssignment.province": "ولایت انتخاب",
                "loadAssignment.selectProvinceOption": "لومړی پلیټ دننه کړئ...",
                "loadAssignment.loadType": "د بار ډول",
                "loadAssignment.selectOption": "ټاکل...",
                "loadAssignment.loadWeight": "د بار وزن (ټنه)",
                "loadAssignment.loadWeightPlaceholder": "لکه: ۵.۵",
                "loadAssignment.destination": "د بار مقصد",
                "loadAssignment.destinationPlaceholder": "لکه: کابل ښار",
                "loadAssignment.receiver": "د بار اخيستونکی نوم",
                "loadAssignment.receiverPlaceholder": "لکه: محمد یاسین تسل",
                "loadAssignment.description": "د بار تفصیل",
                "loadAssignment.descriptionPlaceholder": "د بار نور تفصیلات...",
                "loadAssignment.vehicleInfo": "د وسیلې مالومات:",
                "loadAssignment.vehicleInfoPlaceholder": "دلته به د وسیلې مالومات وښودل شي کله چې پلیټ نمبر داخل کړئ",
                
                // Waiting vehicles
                "waitingVehicles.title": "د بار انتظار وسایط",
                "waitingVehicles.empty": "تر اوسه هیڅ وسیله د بار انتظار نه دی",
                
                // Recent loads
                "recentLoads.title": "وروستي بارګیرۍ",
                "recentLoads.empty": "تر اوسه هیڅ بار ثبت نه دی شوی",
                
                // Exit gate form
                "exitGate.title": "د خروجي دروازې مالومات",
                "exitGate.infoTitle": "معلومات:",
                "exitGate.infoText": "د خروجي دروازې څخه تیریدو لپاره، موټر باید په سیستم کې ثبت، ورود او بار شوی وي.",
                "exitGate.plateNumber": "د موټر پلیټ نمبر",
                "exitGate.plateNumberPlaceholder": "د خروجي موټر پلیټ دننه کړئ",
                "exitGate.exitTime": "د خروج وخت",
                "exitGate.gateNumber": "د خروجي دروازې نمبر",
                "exitGate.remarks": "اضافي یادښتونه",
                "exitGate.remarksPlaceholder": "د خروج په اړه اضافي معلومات...",
                "exitGate.vehicleInfo": "د وسیلې مالومات:",
                "exitGate.vehicleInfoPlaceholder": "دلته به د وسیلې مالومات وښودل شي کله چې پلیټ نمبر داخل کړئ",
                
                // Recent exits
                "recentExits.title": "نني خروجونه",
                "recentExits.empty": "تر اوسه هیڅ خروج ثبت نه دی شوی",
                
                // Exit process guide
                "exitGuide.title": "د خروجي پروسې لارښود",
                "exitGuide.step1": "د خروجي موټر پلیټ نمبر دننه کړئ",
                "exitGuide.step2": "د وسیلې مالومات وګورئ",
                "exitGuide.step3": "د خروجي دروازې نمبر وټاکئ",
                "exitGuide.step4": "د خروج د ثبتولو تڼۍ ته فشار ورکړئ",
                
                // User management
                "userManagement.title": "د کارونکي مدیریت",
                "userManagement.addUser": "نوی کارن",
                "userManagement.createUser": "نوی کارن جوړول",
                "userManagement.fullName": "بشپړ نوم",
                "userManagement.username": "د کارن نوم",
                "userManagement.email": "ایمیل",
                "userManagement.password": "پاسورډ",
                "userManagement.role": "دنده",
                "userManagement.roleUser": "کاروونکی",
                "userManagement.roleOperator": "اپریټر",
                "userManagement.roleAdmin": "اډمین",
                "userManagement.status": "حالت",
                "userManagement.active": "فعال",
                "userManagement.inactive": "غیرفعال",
                "userManagement.tableNumber": "شمیره",
                "userManagement.tableFullName": "بشپړ نوم",
                "userManagement.tableUsername": "د کارن نوم",
                "userManagement.tableEmail": "ایمیل",
                "userManagement.tableRole": "دنده",
                "userManagement.tableRegistrationDate": "د ثبت نیټه",
                "userManagement.tableStatus": "حالت",
                "userManagement.tableActions": "عملونه",
                "userManagement.noUsers": "هیڅ کارن نه دی موندل شوی",
                "userManagement.exportUsers": "کارونکي صادرول",
                
                // Vehicle list
                "vehicleList.title": "ټول ثبت شوي وسایط",
                "vehicleList.filterAll": "ټول",
                "vehicleList.filterInside": "په سیستم کې",
                "vehicleList.filterLoaded": "بار شوي",
                "vehicleList.filterExited": "خروج شوي",
                "vehicleList.filterWaiting": "د بار انتظار",
                "vehicleList.tableNumber": "شمیره",
                "vehicleList.tablePlateNumber": "پلیټ نمبر",
                "vehicleList.tableType": "نوعیت",
                "vehicleList.tableCompany": "شرکت",
                "vehicleList.tableDriver": "ډریور",
                "vehicleList.tableZone": "زون",
                "vehicleList.tableProvince": "ولایت",
                "vehicleList.tableLoadType": "د بار ډول",
                "vehicleList.tableRegistrationDate": "د ثبت نیټه",
                "vehicleList.tableStatus": "حالت",
                "vehicleList.tableActions": "عملونه",
                "vehicleList.noVehicles": "هیڅ ثبت شوی وسیله نشته",
                
                // Buttons
                "buttons.reset": "پاکول",
                "buttons.register": "ثبتول",
                "buttons.registerEntry": "ورود ثبتول",
                "buttons.registerLoad": "بار ثبتول",
                "buttons.registerExit": "خروج ثبتول",
                "buttons.cancel": "لغوه کول",
                "buttons.save": "ذخیره کول",
                "buttons.print": "چاپ",
                "buttons.export": "صادرول",
                
                // Footer
                "footer.copyright": "د وسایطو مدیریت سیستم",
                "footer.description": "د افغانستان د داخلي سفرونو مدیریت",
                "footer.title": "د وسایطو مدیریت سیستم",
                "footer.descriptionFull": "دا سیستم د افغانستان د داخلي سفرونو د وسایطو د مدیریت لپاره جوړ شوی دی.",
                "footer.links": "لینکونه",
                "footer.linkRegister": "ثبت وسایط",
                "footer.linkEntry": "ورودی دروازه",
                "footer.linkLoad": "بارګیری",
                "footer.linkExit": "خروجی دروازه",
                "footer.contact": "اړیکه",
                "footer.copyrightFull": "د وسایطو مدیریت سیستم - ټول حقونه خوندي دي",
                "footer.version": "د سیستم ورژن: ۲.۲"
            },
            
            en: {
                // Login section
                "login.title": "Vehicle Management System",
                "login.subtitle": "Afghanistan Domestic Travels",
                "login.formTitle": "Login to System",
                "login.username": "Username",
                "login.usernamePlaceholder": "Enter your username",
                "login.password": "Password",
                "login.passwordPlaceholder": "Enter your password",
                "login.remember": "Remember me",
                "login.loginButton": "Login",
                "login.newUser": "New user?",
                "login.registerLink": "Create new account",
                "login.forgotPassword": "Forgot password?",
                
                // Registration form
                "register.title": "Create New Account",
                "register.fullName": "Full Name",
                "register.fullNamePlaceholder": "e.g. Muhammad Yaseen Tasal",
                "register.username": "Username",
                "register.usernamePlaceholder": "e.g. myaseen",
                "register.email": "Email Address",
                "register.emailPlaceholder": "e.g. myaseen@example.com",
                "register.password": "Password",
                "register.passwordPlaceholder": "At least 6 characters",
                "register.confirmPassword": "Confirm Password",
                "register.confirmPasswordPlaceholder": "Re-enter password",
                "register.role": "Role",
                "register.roleUser": "User",
                "register.roleOperator": "Operator",
                "register.roleAdmin": "Admin",
                "register.registerButton": "Create Account",
                "register.haveAccount": "Already have an account?",
                "register.loginLink": "Login",
                
                // Forgot password form
                "forgotPassword.title": "Forgot Password?",
                "forgotPassword.instructions": "Enter your email address, we will send you a password reset link.",
                "forgotPassword.email": "Email Address",
                "forgotPassword.emailPlaceholder": "Enter your email address",
                "forgotPassword.resetButton": "Reset Password",
                "forgotPassword.backToLogin": "Back to login",
                
                // Settings
                "settings.title": "Settings",
                "settings.themeMode": "Theme Mode (Dark/Light)",
                "settings.darkMode": "Dark Mode",
                "settings.lightMode": "Light Mode",
                "settings.language": "Language",
                "settings.background": "Background",
                "settings.systemInfo": "System Information",
                "settings.version": "Version",
                "settings.users": "Users",
                "settings.vehicles": "Vehicles",
                "settings.lastLogin": "Last Login",
                "settings.exportData": "Export Data",
                "settings.exportAll": "Export All Data",
                "settings.reset": "Reset Settings",
                
                // Header
                "header.title": "Vehicle Management System",
                "header.subtitle": "Afghanistan Domestic Travels",
                
                // Statistics
                "stats.totalRegistered": "Total Registered",
                "stats.enteredToday": "Entered Today",
                "stats.loaded": "Loaded",
                "stats.exitedToday": "Exited Today",
                "stats.insideSystem": "In System",
                "stats.waitingForLoad": "Waiting for Load",
                
                // Tabs
                "tabs.register": "Register Vehicles",
                "tabs.entry": "Entry Gate",
                "tabs.load": "Loading",
                "tabs.exit": "Exit Gate",
                "tabs.users": "User Management",
                "tabs.list": "View Registered",
                
                // Vehicle registration form
                "registerVehicle.title": "New Vehicle Registration",
                "registerVehicle.vehicleType": "Vehicle Type",
                "registerVehicle.selectOption": "Select...",
                "registerVehicle.plateNumber": "Vehicle Plate Number",
                "registerVehicle.plateNumberPlaceholder": "e.g. Kabul 12345",
                "registerVehicle.chassisNumber": "Chassis Number",
                "registerVehicle.engineNumber": "Engine Number",
                "registerVehicle.companyName": "Company Name",
                "registerVehicle.driverName": "Driver Name",
                "registerVehicle.driverNamePlaceholder": "e.g. Tasal Amini",
                "registerVehicle.driverPhone": "Driver Phone Number",
                "registerVehicle.driverPhonePlaceholder": "e.g. 0700123456",
                "registerVehicle.driverId": "Driver ID Number",
                "registerVehicle.driverIdPlaceholder": "e.g. 123456789",
                
                // Guide
                "guide.title": "Guide",
                "guide.registrationInstructions": "Registration Instructions:",
                "guide.instruction1": "1. Fill all vehicle information correctly",
                "guide.instruction2": "2. Your registered vehicle plate must be unique",
                "guide.instruction3": "3. After registration, vehicle can enter through entry gate",
                "guide.instruction4": "4. After entry, vehicle should be assigned to load",
                "guide.instruction5": "5. Every vehicle must pass through exit gate to clear from system",
                "guide.categoriesList": "Categories List:",
                
                // Entry gate form
                "entryGate.title": "Entry Gate Information",
                "entryGate.zone": "Select Zone",
                "entryGate.gateNumber": "Gate Number",
                "entryGate.vehicleCategory": "Vehicle Category",
                "entryGate.plateNumber": "Vehicle Plate Number",
                "entryGate.plateNumberPlaceholder": "Enter registered plate",
                "entryGate.remarks": "Additional Notes",
                "entryGate.remarksPlaceholder": "Additional information about entry...",
                
                // Zones information
                "zonesInfo.title": "Zones Information",
                "zonesInfo.zonesAndProvinces": "Zones and Provinces:",
                "zonesInfo.noteTitle": "Note:",
                "zonesInfo.noteText": "Only zone is selected at entry gate. Province selection is done during loading.",
                
                // Loading form
                "loadAssignment.title": "Vehicle Loading",
                "loadAssignment.plateNumber": "Vehicle Plate Number",
                "loadAssignment.plateNumberPlaceholder": "Loading vehicle plate",
                "loadAssignment.province": "Select Province",
                "loadAssignment.selectProvinceOption": "Enter plate first...",
                "loadAssignment.loadType": "Load Type",
                "loadAssignment.selectOption": "Select...",
                "loadAssignment.loadWeight": "Load Weight (Tons)",
                "loadAssignment.loadWeightPlaceholder": "e.g. 5.5",
                "loadAssignment.destination": "Load Destination",
                "loadAssignment.destinationPlaceholder": "e.g. Kabul City",
                "loadAssignment.receiver": "Load Receiver Name",
                "loadAssignment.receiverPlaceholder": "e.g. Muhammad Yaseen Tasal",
                "loadAssignment.description": "Load Description",
                "loadAssignment.descriptionPlaceholder": "More details about load...",
                "loadAssignment.vehicleInfo": "Vehicle Information:",
                "loadAssignment.vehicleInfoPlaceholder": "Vehicle information will appear here when you enter plate number",
                
                // Waiting vehicles
                "waitingVehicles.title": "Vehicles Waiting for Load",
                "waitingVehicles.empty": "No vehicles waiting for load yet",
                
                // Recent loads
                "recentLoads.title": "Recent Loadings",
                "recentLoads.empty": "No loads registered yet",
                
                // Exit gate form
                "exitGate.title": "Exit Gate Information",
                "exitGate.infoTitle": "Information:",
                "exitGate.infoText": "To pass through exit gate, vehicle must be registered, entered and loaded in the system.",
                "exitGate.plateNumber": "Vehicle Plate Number",
                "exitGate.plateNumberPlaceholder": "Enter exiting vehicle plate",
                "exitGate.exitTime": "Exit Time",
                "exitGate.gateNumber": "Exit Gate Number",
                "exitGate.remarks": "Additional Notes",
                "exitGate.remarksPlaceholder": "Additional information about exit...",
                "exitGate.vehicleInfo": "Vehicle Information:",
                "exitGate.vehicleInfoPlaceholder": "Vehicle information will appear here when you enter plate number",
                
                // Recent exits
                "recentExits.title": "Recent Exits",
                "recentExits.empty": "No exits registered yet",
                
                // Exit process guide
                "exitGuide.title": "Exit Process Guide",
                "exitGuide.step1": "Enter exiting vehicle plate number",
                "exitGuide.step2": "Review vehicle information",
                "exitGuide.step3": "Select exit gate number",
                "exitGuide.step4": "Press exit registration button",
                
                // User management
                "userManagement.title": "User Management",
                "userManagement.addUser": "New User",
                "userManagement.createUser": "Create New User",
                "userManagement.fullName": "Full Name",
                "userManagement.username": "Username",
                "userManagement.email": "Email",
                "userManagement.password": "Password",
                "userManagement.role": "Role",
                "userManagement.roleUser": "User",
                "userManagement.roleOperator": "Operator",
                "userManagement.roleAdmin": "Admin",
                "userManagement.status": "Status",
                "userManagement.active": "Active",
                "userManagement.inactive": "Inactive",
                "userManagement.tableNumber": "No.",
                "userManagement.tableFullName": "Full Name",
                "userManagement.tableUsername": "Username",
                "userManagement.tableEmail": "Email",
                "userManagement.tableRole": "Role",
                "userManagement.tableRegistrationDate": "Registration Date",
                "userManagement.tableStatus": "Status",
                "userManagement.tableActions": "Actions",
                "userManagement.noUsers": "No users found",
                "userManagement.exportUsers": "Export Users",
                
                // Vehicle list
                "vehicleList.title": "All Registered Vehicles",
                "vehicleList.filterAll": "All",
                "vehicleList.filterInside": "In System",
                "vehicleList.filterLoaded": "Loaded",
                "vehicleList.filterExited": "Exited",
                "vehicleList.filterWaiting": "Waiting",
                "vehicleList.tableNumber": "No.",
                "vehicleList.tablePlateNumber": "Plate Number",
                "vehicleList.tableType": "Type",
                "vehicleList.tableCompany": "Company",
                "vehicleList.tableDriver": "Driver",
                "vehicleList.tableZone": "Zone",
                "vehicleList.tableProvince": "Province",
                "vehicleList.tableLoadType": "Load Type",
                "vehicleList.tableRegistrationDate": "Registration Date",
                "vehicleList.tableStatus": "Status",
                "vehicleList.tableActions": "Actions",
                "vehicleList.noVehicles": "No vehicles registered",
                
                // Buttons
                "buttons.reset": "Clear",
                "buttons.register": "Register",
                "buttons.registerEntry": "Register Entry",
                "buttons.registerLoad": "Register Load",
                "buttons.registerExit": "Register Exit",
                "buttons.cancel": "Cancel",
                "buttons.save": "Save",
                "buttons.print": "Print",
                "buttons.export": "Export",
                
                // Footer
                "footer.copyright": "Vehicle Management System",
                "footer.description": "Afghanistan Domestic Travels Management",
                "footer.title": "Vehicle Management System",
                "footer.descriptionFull": "This system is designed for management of domestic travel vehicles in Afghanistan.",
                "footer.links": "Links",
                "footer.linkRegister": "Register Vehicles",
                "footer.linkEntry": "Entry Gate",
                "footer.linkLoad": "Loading",
                "footer.linkExit": "Exit Gate",
                "footer.contact": "Contact",
                "footer.copyrightFull": "Vehicle Management System - All rights reserved",
                "footer.version": "System Version: 2.2"
            },
            
            fa: {
                // Login section
                "login.title": "سیستم مدیریت وسایط",
                "login.subtitle": "سفرهای داخلی افغانستان",
                "login.formTitle": "ورود به سیستم",
                "login.username": "نام کاربری",
                "login.usernamePlaceholder": "نام کاربری خود را وارد کنید",
                "login.password": "رمز عبور",
                "login.passwordPlaceholder": "رمز عبور خود را وارد کنید",
                "login.remember": "مرا به خاطر بسپار",
                "login.loginButton": "ورود به سیستم",
                "login.newUser": "کاربر جدید هستید؟",
                "login.registerLink": "ایجاد حساب جدید",
                "login.forgotPassword": "رمز عبور را فراموش کرده‌اید؟",
                
                // Registration form
                "register.title": "ایجاد حساب جدید",
                "register.fullName": "نام کامل",
                "register.fullNamePlaceholder": "مثال: محمد یاسین تسل",
                "register.username": "نام کاربری",
                "register.usernamePlaceholder": "مثال: myaseen",
                "register.email": "آدرس ایمیل",
                "register.emailPlaceholder": "مثال: myaseen@example.com",
                "register.password": "رمز عبور",
                "register.passwordPlaceholder": "حداقل ۶ حرف",
                "register.confirmPassword": "تأیید رمز عبور",
                "register.confirmPasswordPlaceholder": "رمز عبور را دوباره وارد کنید",
                "register.role": "نقش",
                "register.roleUser": "کاربر",
                "register.roleOperator": "اپراتور",
                "register.roleAdmin": "ادمین",
                "register.registerButton": "ایجاد حساب",
                "register.haveAccount": "از قبل حساب دارید؟",
                "register.loginLink": "ورود",
                
                // Forgot password form
                "forgotPassword.title": "رمز عبور را فراموش کرده‌اید؟",
                "forgotPassword.instructions": "آدرس ایمیل خود را وارد کنید، ما لینک بازیابی رمز عبور را برای شما ارسال خواهیم کرد.",
                "forgotPassword.email": "آدرس ایمیل",
                "forgotPassword.emailPlaceholder": "آدرس ایمیل خود را وارد کنید",
                "forgotPassword.resetButton": "بازیابی رمز عبور",
                "forgotPassword.backToLogin": "بازگشت به ورود",
                
                // Settings
                "settings.title": "تنظیمات",
                "settings.themeMode": "مود (تاریک/روشن)",
                "settings.darkMode": "مود تاریک",
                "settings.lightMode": "مود روشن",
                "settings.language": "زبان",
                "settings.background": "پس‌زمینه",
                "settings.systemInfo": "اطلاعات سیستم",
                "settings.version": "نسخه",
                "settings.users": "کاربران",
                "settings.vehicles": "وسایط",
                "settings.lastLogin": "آخرین ورود",
                "settings.exportData": "صدور داده‌ها",
                "settings.exportAll": "صدور تمام داده‌ها",
                "settings.reset": "بازنشانی تنظیمات",
                
                // Header
                "header.title": "سیستم مدیریت وسایط",
                "header.subtitle": "سفرهای داخلی افغانستان",
                
                // Statistics
                "stats.totalRegistered": "کل ثبت شده",
                "stats.enteredToday": "امروز وارد شده",
                "stats.loaded": "بارگیری شده",
                "stats.exitedToday": "امروز خارج شده",
                "stats.insideSystem": "در سیستم",
                "stats.waitingForLoad": "در انتظار بارگیری",
                
                // Tabs
                "tabs.register": "ثبت وسایط",
                "tabs.entry": "دروازه ورودی",
                "tabs.load": "بارگیری",
                "tabs.exit": "دروازه خروجی",
                "tabs.users": "مدیریت کاربران",
                "tabs.list": "مشاهده ثبت‌شده‌ها",
                
                // Vehicle registration form
                "registerVehicle.title": "ثبت جدید وسایط",
                "registerVehicle.vehicleType": "نوع وسیله",
                "registerVehicle.selectOption": "انتخاب...",
                "registerVehicle.plateNumber": "شماره پلاک وسیله",
                "registerVehicle.plateNumberPlaceholder": "مثال: کابل ۱۲۳۴۵",
                "registerVehicle.chassisNumber": "شماره شاسی",
                "registerVehicle.engineNumber": "شماره موتور",
                "registerVehicle.companyName": "نام شرکت",
                "registerVehicle.driverName": "نام راننده",
                "registerVehicle.driverNamePlaceholder": "مثال: تسل امینی",
                "registerVehicle.driverPhone": "شماره تماس راننده",
                "registerVehicle.driverPhonePlaceholder": "مثال: ۰۷۰۰۱۲۳۴۵۶",
                "registerVehicle.driverId": "شماره تذکره راننده",
                "registerVehicle.driverIdPlaceholder": "مثال: ۱۲۳۴۵۶۷۸۹",
                
                // Guide
                "guide.title": "راهنما",
                "guide.registrationInstructions": "دستورالعمل‌های ثبت:",
                "guide.instruction1": "۱. تمام اطلاعات وسیله را به درستی پر کنید",
                "guide.instruction2": "۲. پلاک وسیله ثبت‌شده شما باید منحصر به فرد باشد",
                "guide.instruction3": "۳. پس از ثبت، وسیله می‌تواند از دروازه ورودی وارد شود",
                "guide.instruction4": "۴. پس از ورود، وسیله باید برای بارگیری معرفی شود",
                "guide.instruction5": "۵. هر وسیله باید از دروازه خروجی عبور کند تا از سیستم پاک شود",
                "guide.categoriesList": "لیست دسته‌بندی‌ها:",
                
                // Entry gate form
                "entryGate.title": "اطلاعات دروازه ورودی",
                "entryGate.zone": "انتخاب منطقه",
                "entryGate.gateNumber": "شماره دروازه",
                "entryGate.vehicleCategory": "دسته وسیله",
                "entryGate.plateNumber": "شماره پلاک وسیله",
                "entryGate.plateNumberPlaceholder": "پلاک ثبت‌شده را وارد کنید",
                "entryGate.remarks": "یادداشت‌های اضافی",
                "entryGate.remarksPlaceholder": "اطلاعات اضافی درباره ورود...",
                
                // Zones information
                "zonesInfo.title": "اطلاعات مناطق",
                "zonesInfo.zonesAndProvinces": "مناطق و ولایات:",
                "zonesInfo.noteTitle": "توجه:",
                "zonesInfo.noteText": "در دروازه ورودی فقط منطقه انتخاب می‌شود. انتخاب ولایت در زمان بارگیری انجام می‌شود.",
                
                // Loading form
                "loadAssignment.title": "بارگیری وسایط",
                "loadAssignment.plateNumber": "شماره پلاک وسیله",
                "loadAssignment.plateNumberPlaceholder": "پلاک وسیله بارگیری",
                "loadAssignment.province": "انتخاب ولایت",
                "loadAssignment.selectProvinceOption": "اول پلاک را وارد کنید...",
                "loadAssignment.loadType": "نوع بار",
                "loadAssignment.selectOption": "انتخاب...",
                "loadAssignment.loadWeight": "وزن بار (تن)",
                "loadAssignment.loadWeightPlaceholder": "مثال: ۵.۵",
                "loadAssignment.destination": "مقصد بار",
                "loadAssignment.destinationPlaceholder": "مثال: شهر کابل",
                "loadAssignment.receiver": "نام دریافت‌کننده بار",
                "loadAssignment.receiverPlaceholder": "مثال: محمد یاسین تسل",
                "loadAssignment.description": "توضیحات بار",
                "loadAssignment.descriptionPlaceholder": "جزئیات بیشتر درباره بار...",
                "loadAssignment.vehicleInfo": "اطلاعات وسیله:",
                "loadAssignment.vehicleInfoPlaceholder": "اطلاعات وسیله پس از وارد کردن شماره پلاک نمایش داده می‌شود",
                
                // Waiting vehicles
                "waitingVehicles.title": "وسایط در انتظار بارگیری",
                "waitingVehicles.empty": "هنوز هیچ وسیله‌ای در انتظار بارگیری نیست",
                
                // Recent loads
                "recentLoads.title": "بارگیری‌های اخیر",
                "recentLoads.empty": "هنوز هیچ باری ثبت نشده است",
                
                // Exit gate form
                "exitGate.title": "اطلاعات دروازه خروجی",
                "exitGate.infoTitle": "اطلاعات:",
                "exitGate.infoText": "برای عبور از دروازه خروجی، وسیله باید در سیستم ثبت، وارد و بارگیری شده باشد.",
                "exitGate.plateNumber": "شماره پلاک وسیله",
                "exitGate.plateNumberPlaceholder": "پلاک وسیله خروجی را وارد کنید",
                "exitGate.exitTime": "زمان خروج",
                "exitGate.gateNumber": "شماره دروازه خروجی",
                "exitGate.remarks": "یادداشت‌های اضافی",
                "exitGate.remarksPlaceholder": "اطلاعات اضافی درباره خروج...",
                "exitGate.vehicleInfo": "اطلاعات وسیله:",
                "exitGate.vehicleInfoPlaceholder": "اطلاعات وسیله پس از وارد کردن شماره پلاک نمایش داده می‌شود",
                
                // Recent exits
                "recentExits.title": "خروج‌های اخیر",
                "recentExits.empty": "هنوز هیچ خروجی ثبت نشده است",
                
                // Exit process guide
                "exitGuide.title": "راهنمای فرایند خروج",
                "exitGuide.step1": "شماره پلاک وسیله خروجی را وارد کنید",
                "exitGuide.step2": "اطلاعات وسیله را مرور کنید",
                "exitGuide.step3": "شماره دروازه خروجی را انتخاب کنید",
                "exitGuide.step4": "دکمه ثبت خروج را فشار دهید",
                
                // User management
                "userManagement.title": "مدیریت کاربران",
                "userManagement.addUser": "کاربر جدید",
                "userManagement.createUser": "ایجاد کاربر جدید",
                "userManagement.fullName": "نام کامل",
                "userManagement.username": "نام کاربری",
                "userManagement.email": "ایمیل",
                "userManagement.password": "رمز عبور",
                "userManagement.role": "نقش",
                "userManagement.roleUser": "کاربر",
                "userManagement.roleOperator": "اپراتور",
                "userManagement.roleAdmin": "ادمین",
                "userManagement.status": "وضعیت",
                "userManagement.active": "فعال",
                "userManagement.inactive": "غیرفعال",
                "userManagement.tableNumber": "شماره",
                "userManagement.tableFullName": "نام کامل",
                "userManagement.tableUsername": "نام کاربری",
                "userManagement.tableEmail": "ایمیل",
                "userManagement.tableRole": "نقش",
                "userManagement.tableRegistrationDate": "تاریخ ثبت",
                "userManagement.tableStatus": "وضعیت",
                "userManagement.tableActions": "عملیات",
                "userManagement.noUsers": "هیچ کاربری یافت نشد",
                "userManagement.exportUsers": "صدور کاربران",
                
                // Vehicle list
                "vehicleList.title": "تمام وسایط ثبت‌شده",
                "vehicleList.filterAll": "همه",
                "vehicleList.filterInside": "در سیستم",
                "vehicleList.filterLoaded": "بارگیری شده",
                "vehicleList.filterExited": "خارج شده",
                "vehicleList.filterWaiting": "در انتظار",
                "vehicleList.tableNumber": "شماره",
                "vehicleList.tablePlateNumber": "شماره پلاک",
                "vehicleList.tableType": "نوع",
                "vehicleList.tableCompany": "شرکت",
                "vehicleList.tableDriver": "راننده",
                "vehicleList.tableZone": "منطقه",
                "vehicleList.tableProvince": "ولایت",
                "vehicleList.tableLoadType": "نوع بار",
                "vehicleList.tableRegistrationDate": "تاریخ ثبت",
                "vehicleList.tableStatus": "وضعیت",
                "vehicleList.tableActions": "عملیات",
                "vehicleList.noVehicles": "هیچ وسیله‌ای ثبت نشده است",
                
                // Buttons
                "buttons.reset": "پاک کردن",
                "buttons.register": "ثبت",
                "buttons.registerEntry": "ثبت ورود",
                "buttons.registerLoad": "ثبت بار",
                "buttons.registerExit": "ثبت خروج",
                "buttons.cancel": "لغو",
                "buttons.save": "ذخیره",
                "buttons.print": "چاپ",
                "buttons.export": "صدور",
                
                // Footer
                "footer.copyright": "سیستم مدیریت وسایط",
                "footer.description": "مدیریت سفرهای داخلی افغانستان",
                "footer.title": "سیستم مدیریت وسایط",
                "footer.descriptionFull": "این سیستم برای مدیریت وسایط سفرهای داخلی افغانستان طراحی شده است.",
                "footer.links": "لینک‌ها",
                "footer.linkRegister": "ثبت وسایط",
                "footer.linkEntry": "دروازه ورودی",
                "footer.linkLoad": "بارگیری",
                "footer.linkExit": "دروازه خروجی",
                "footer.contact": "تماس",
                "footer.copyrightFull": "سیستم مدیریت وسایط - کلیه حقوق محفوظ است",
                "footer.version": "نسخه سیستم: ۲.۲"
            }
        };

        // System initialization data
        let currentUser = null;
        let currentLanguage = localStorage.getItem('vehicleSystemLanguage') || 'ps';
        let currentBackground = localStorage.getItem('vehicleSystemBackground') || 'dark-digital';
        let currentTheme = localStorage.getItem('vehicleSystemTheme') || 'dark';
        
        // Zones and provinces data
        const zonesData = {
            "هرات": ["هرات", "نیمروز", "فراه"],
            "قندهار": ["قندهار", "هلمند", "زابل", "اروزګان"],
            "ننګرهار": ["ننګرهار", "کنر", "لغمان", "نورستان"],
            "پکتیا": ["پکتیا", "مزارشریف", "بدخشان", "فاریاب"],
            "مرکزی": ["کابل", "پروان", "کاپیسا", "پنجشیر", "وردګ", "لوګر"]
        };

        // Load type classes
        const loadTypeClasses = {
            "خوراکي مواد": "load-food",
            "ساختماني مواد": "load-construction",
            "فرنیچر": "load-furniture",
            "کرنيز توليدات": "load-agriculture",
            "حیوانات": "load-other",
            "طبي توکي": "load-other",
            "برېښنايي توکي": "load-other",
            "کیمیاوي مواد": "load-other",
            "د سپورتو توکي": "load-other",
            "نور": "load-other"
        };

        // Role names
        const roleNames = {
            "admin": {ps: "اډمین", en: "Admin", fa: "ادمین"},
            "user": {ps: "کاروونکی", en: "User", fa: "کاربر"},
            "operator": {ps: "اپریټر", en: "Operator", fa: "اپراتور"}
        };

        // Role classes
        const roleClasses = {
            "admin": "role-admin",
            "user": "role-user",
            "operator": "role-operator"
        };
        
        // Language names
        const languageNames = {
            "ps": {ps: "پښتو", en: "Pashto", fa: "پشتو"},
            "en": {ps: "انګلیسي", en: "English", fa: "انگلیسی"},
            "fa": {ps: "دری", en: "Dari", fa: "دری"}
        };
        
        // Theme names
        const themeNames = {
            "dark": {ps: "تاریک مود", en: "Dark Mode", fa: "مود تاریک"},
            "light": {ps: "روښانه مود", en: "Light Mode", fa: "مود روشن"}
        };

        // Local storage functions
        function getUsers() {
            const users = localStorage.getItem('vehicleUsers');
            if (!users) {
                // Create default users for initialization
                const defaultUsers = [
                    {
                        id: 1,
                        fullName: "محمد یاسین تسل",
                        username: "admin",
                        email: "myaseentasal@gmail.com",
                        password: "admin123",
                        role: "admin",
                        registeredDate: new Date().toISOString(),
                        active: true,
                        lastLogin: new Date().toISOString()
                    },
                    {
                        id: 2,
                        fullName: "عمر فاروق",
                        username: "user",
                        email: "user@example.com",
                        password: "user123",
                        role: "user",
                        registeredDate: new Date().toISOString(),
                        active: true,
                        lastLogin: new Date().toISOString()
                    },
                    {
                        id: 3,
                        fullName: "احمد کریم",
                        username: "operator",
                        email: "operator@example.com",
                        password: "operator123",
                        role: "operator",
                        registeredDate: new Date().toISOString(),
                        active: true,
                        lastLogin: new Date().toISOString()
                    }
                ];
                saveUsers(defaultUsers);
                return defaultUsers;
            }
            return JSON.parse(users);
        }

        function saveUsers(users) {
            localStorage.setItem('vehicleUsers', JSON.stringify(users));
        }

        function getVehicles() {
            const vehicles = localStorage.getItem('vehicles');
            return vehicles ? JSON.parse(vehicles) : [];
        }

        function saveVehicles(vehicles) {
            localStorage.setItem('vehicles', JSON.stringify(vehicles));
        }

        function getEntries() {
            const entries = localStorage.getItem('entries');
            return entries ? JSON.parse(entries) : [];
        }

        function saveEntries(entries) {
            localStorage.setItem('entries', JSON.stringify(entries));
        }

        function getLoads() {
            const loads = localStorage.getItem('loads');
            return loads ? JSON.parse(loads) : [];
        }

        function saveLoads(loads) {
            localStorage.setItem('loads', JSON.stringify(loads));
        }

        function getExits() {
            const exits = localStorage.getItem('exits');
            return exits ? JSON.parse(exits) : [];
        }

        function saveExits(exits) {
            localStorage.setItem('exits', JSON.stringify(exits));
        }

        // Theme update function
        function updateTheme() {
            const theme = currentTheme;
            
            // Update body class
            if (theme === 'light') {
                document.body.classList.add('light-mode');
            } else {
                document.body.classList.remove('light-mode');
            }
            
            // Update theme toggle status
            const themeToggle = document.getElementById('themeToggle');
            const headerThemeToggle = document.getElementById('headerThemeToggle');
            const themeStatus = document.getElementById('themeStatus');
            
            if (themeToggle) themeToggle.checked = (theme === 'light');
            if (headerThemeToggle) headerThemeToggle.checked = (theme === 'light');
            if (themeStatus) themeStatus.textContent = themeNames[theme][currentLanguage];
            
            // Update theme in localStorage
            localStorage.setItem('vehicleSystemTheme', theme);
        }

        // Language update function
        function updateLanguage() {
            const lang = currentLanguage;
            const langData = translations[lang];
            
            // Set HTML direction and language
            document.getElementById('mainHtml').setAttribute('dir', lang === 'en' ? 'ltr' : 'rtl');
            document.getElementById('mainHtml').setAttribute('lang', lang === 'ps' ? 'prs' : lang);
            
            // Update all elements with data-i18n
            document.querySelectorAll('[data-i18n]').forEach(element => {
                const key = element.getAttribute('data-i18n');
                if (langData[key]) {
                    element.textContent = langData[key];
                }
            });
            
            // Update placeholders
            document.querySelectorAll('[data-i18n-placeholder]').forEach(element => {
                const key = element.getAttribute('data-i18n-placeholder');
                if (langData[key]) {
                    element.setAttribute('placeholder', langData[key]);
                }
            });
            
            // Update options with data-i18n
            document.querySelectorAll('option[data-i18n]').forEach(element => {
                const key = element.getAttribute('data-i18n');
                if (langData[key]) {
                    element.textContent = langData[key];
                }
            });
            
            // Update language name
            document.getElementById('currentLangText').textContent = languageNames[lang][lang];
            document.getElementById('headerLangText').textContent = languageNames[lang][lang];
            
            // Update user role
            if (currentUser) {
                document.getElementById('userRole').textContent = roleNames[currentUser.role][lang];
            }
            
            // Update theme status
            const themeStatus = document.getElementById('themeStatus');
            if (themeStatus) {
                themeStatus.textContent = themeNames[currentTheme][lang];
            }
        }

        // Background update function
        function updateBackground() {
            const bg = currentBackground;
            
            // Remove all background classes
            const bgClasses = [
                'bg-dark-digital', 'bg-blue-digital', 'bg-green-digital', 
                'bg-purple-digital', 'bg-red-digital', 'bg-circuit-board',
                'bg-binary-code', 'bg-data-flow', 'bg-network-grid',
                'bg-pixel-grid', 'bg-hexagon', 'bg-digital-waves', 'bg-matrix'
            ];
            
            document.body.classList.remove(...bgClasses);
            
            // Add new background class
            document.body.classList.add(bg);
            
            // Update active background option
            document.querySelectorAll('.bg-option').forEach(option => {
                option.classList.remove('active');
                if (option.getAttribute('data-bg') === bg) {
                    option.classList.add('active');
                }
            });
            
            // Update background in localStorage
            localStorage.setItem('vehicleSystemBackground', bg);
        }

        // Date and time display
        function updateDateTime() {
            const now = new Date();
            let options;
            
            if (currentLanguage === 'en') {
                options = { 
                    weekday: 'long', 
                    year: 'numeric', 
                    month: 'long', 
                    day: 'numeric',
                    hour: '2-digit',
                    minute: '2-digit',
                    second: '2-digit'
                };
            } else {
                options = { 
                    weekday: 'long', 
                    year: 'numeric', 
                    month: 'long', 
                    day: 'numeric',
                    hour: '2-digit',
                    minute: '2-digit',
                    second: '2-digit'
                };
            }
            
            const formatter = new Intl.DateTimeFormat(currentLanguage === 'ps' ? 'prs-AF' : 
                                                     currentLanguage === 'fa' ? 'fa-AF' : 'en-US', options);
            const dateTimeElement = document.getElementById('current-date-time');
            if (dateTimeElement) {
                dateTimeElement.textContent = formatter.format(now);
            }
            
            // Update exit time
            const exitTimeElement = document.getElementById('exitTime');
            if (exitTimeElement) {
                exitTimeElement.value = now.toLocaleTimeString(currentLanguage === 'ps' ? 'prs-AF' : 
                                                              currentLanguage === 'fa' ? 'fa-AF' : 'en-US');
            }
        }
        
        // Update time every second
        setInterval(updateDateTime, 1000);
        updateDateTime();

        // Show alert message
        function showAlert(message, type = 'success') {
            // Translate message based on language
            let translatedMessage = message;
            
            const alertHtml = `
                <div class="alert alert-${type} alert-dismissible fade show alert-custom" role="alert">
                    ${translatedMessage}
                    <button type="button" class="btn-close" data-bs-dismiss="alert"></button>
                </div>
            `;
            
            // Show message after tabs
            const systemTabs = document.getElementById('systemTabs');
            if (systemTabs) {
                systemTabs.insertAdjacentHTML('afterend', alertHtml);
            } else {
                // If system tabs not available, show at top
                document.body.insertAdjacentHTML('afterbegin', alertHtml);
            }
            
            // Auto close alert after 5 seconds
            setTimeout(() => {
                const alert = document.querySelector('.alert');
                if (alert) {
                    const bsAlert = new bootstrap.Alert(alert);
                    bsAlert.close();
                }
            }, 5000);
        }

        // Show user information
        function updateUserDisplay() {
            if (!currentUser) return;
            
            document.getElementById('userFullName').textContent = currentUser.fullName;
            document.getElementById('userRole').textContent = roleNames[currentUser.role][currentLanguage];
            
            // Create user avatar
            const userAvatar = document.getElementById('userAvatar');
            const firstLetter = currentUser.fullName.charAt(0);
            userAvatar.textContent = firstLetter;
            
            // Limit tabs based on role
            const usersTab = document.getElementById('users-tab');
            if (usersTab) {
                if (currentUser.role === 'user') {
                    // Only users can view registered vehicles tab
                    usersTab.style.display = 'none';
                } else if (currentUser.role === 'operator') {
                    // Operators can view all tabs except user management
                    usersTab.style.display = 'none';
                } else {
                    // Admin can view all tabs
                    usersTab.style.display = 'block';
                }
            }
        }

        // Show admin user creation form
        function showAdminUserForm() {
            const formContainer = document.getElementById('adminUserFormContainer');
            formContainer.style.display = 'block';
            document.getElementById('adminUserForm').reset();
        }

        // Hide admin user creation form
        function hideAdminUserForm() {
            const formContainer = document.getElementById('adminUserFormContainer');
            formContainer.style.display = 'none';
        }

        // Settings panel management
        function openSettingsPanel() {
            document.getElementById('settingsPanel').classList.add('show');
            // Update settings information
            updateSettingsInfo();
        }

        function closeSettingsPanel() {
            document.getElementById('settingsPanel').classList.remove('show');
        }

        function updateSettingsInfo() {
            const users = getUsers();
            const vehicles = getVehicles();
            
            document.getElementById('settingsUserCount').textContent = users.length;
            document.getElementById('settingsVehicleCount').textContent = vehicles.length;
            
            if (currentUser && currentUser.lastLogin) {
                const lastLoginDate = new Date(currentUser.lastLogin);
                document.getElementById('settingsLastLogin').textContent = lastLoginDate.toLocaleDateString(
                    currentLanguage === 'ps' ? 'prs-AF' : 
                    currentLanguage === 'fa' ? 'fa-AF' : 'en-US'
                ) + ' ' + lastLoginDate.toLocaleTimeString();
            }
        }

        // Main initialization
        document.addEventListener('DOMContentLoaded', function() {
            // Initialize theme, language, and background
            updateTheme();
            updateLanguage();
            updateBackground();
            
            // Password show/hide button
            document.getElementById('togglePassword')?.addEventListener('click', function() {
                const passwordInput = document.getElementById('loginPassword');
                const icon = this.querySelector('i');
                
                if (passwordInput.type === 'password') {
                    passwordInput.type = 'text';
                    icon.classList.remove('fa-eye');
                    icon.classList.add('fa-eye-slash');
                } else {
                    passwordInput.type = 'password';
                    icon.classList.remove('fa-eye-slash');
                    icon.classList.add('fa-eye');
                }
            });

            // Form switching
            document.getElementById('showRegisterForm')?.addEventListener('click', function(e) {
                e.preventDefault();
                document.getElementById('loginForm').style.display = 'none';
                document.getElementById('registerForm').style.display = 'block';
                document.getElementById('forgotPasswordForm').style.display = 'none';
            });

            document.getElementById('showLoginForm')?.addEventListener('click', function(e) {
                e.preventDefault();
                document.getElementById('loginForm').style.display = 'block';
                document.getElementById('registerForm').style.display = 'none';
                document.getElementById('forgotPasswordForm').style.display = 'none';
            });

            document.getElementById('showForgotPassword')?.addEventListener('click', function(e) {
                e.preventDefault();
                document.getElementById('loginForm').style.display = 'none';
                document.getElementById('registerForm').style.display = 'none';
                document.getElementById('forgotPasswordForm').style.display = 'block';
            });

            document.getElementById('showLoginFormFromForgot')?.addEventListener('click', function(e) {
                e.preventDefault();
                document.getElementById('loginForm').style.display = 'block';
                document.getElementById('registerForm').style.display = 'none';
                document.getElementById('forgotPasswordForm').style.display = 'none';
            });

            // Login process
            document.getElementById('loginButton')?.addEventListener('click', function() {
                const username = document.getElementById('loginUsername').value.trim();
                const password = document.getElementById('loginPassword').value.trim();
                
                if (!username || !password) {
                    showAlert('Please enter username and password!', 'danger');
                    return;
                }
                
                const users = getUsers();
                const user = users.find(u => u.username === username && u.password === password && u.active);
                
                if (!user) {
                    showAlert('Invalid username or password!', 'danger');
                    return;
                }
                
                // Save user information
                currentUser = { ...user };
                currentUser.lastLogin = new Date().toISOString();
                localStorage.setItem('currentVehicleUser', JSON.stringify(currentUser));
                
                // Update user's last login in database
                const updatedUsers = users.map(u => {
                    if (u.id === user.id) {
                        u.lastLogin = currentUser.lastLogin;
                    }
                    return u;
                });
                saveUsers(updatedUsers);
                
                // Hide login form and show main system
                document.getElementById('loginContainer').style.display = 'none';
                document.getElementById('mainContent').style.display = 'block';
                
                // Show user information
                updateUserDisplay();
                
                // Update system information
                updateStatistics();
                updateVehiclesTable();
                updateUsersTable();
                
                showAlert(`Welcome ${user.fullName}!`, 'success');
            });

            // Registration process
            document.getElementById('registerButton')?.addEventListener('click', function() {
                const fullName = document.getElementById('regFullName').value.trim();
                const username = document.getElementById('regUsername').value.trim();
                const email = document.getElementById('regEmail').value.trim();
                const password = document.getElementById('regPassword').value.trim();
                const confirmPassword = document.getElementById('regConfirmPassword').value.trim();
                const role = document.getElementById('regRole').value;
                
                // Validation
                if (!fullName || !username || !email || !password || !confirmPassword) {
                    showAlert('Please fill all required fields!', 'danger');
                    return;
                }
                
                if (password.length < 6) {
                    showAlert('Password must be at least 6 characters!', 'danger');
                    return;
                }
                
                if (password !== confirmPassword) {
                    showAlert('Passwords do not match!', 'danger');
                    return;
                }
                
                const users = getUsers();
                
                // Check for duplicate username and email
                if (users.some(u => u.username === username)) {
                    showAlert('This username already exists!', 'danger');
                    return;
                }
                
                if (users.some(u => u.email === email)) {
                    showAlert('This email address already exists!', 'danger');
                    return;
                }
                
                // Create new user
                const newUser = {
                    id: users.length > 0 ? Math.max(...users.map(u => u.id)) + 1 : 1,
                    fullName,
                    username,
                    email,
                    password,
                    role,
                    registeredDate: new Date().toISOString(),
                    active: true,
                    lastLogin: null
                };
                
                users.push(newUser);
                saveUsers(users);
                
                // Clear form
                document.getElementById('regFullName').value = '';
                document.getElementById('regUsername').value = '';
                document.getElementById('regEmail').value = '';
                document.getElementById('regPassword').value = '';
                document.getElementById('regConfirmPassword').value = '';
                
                // Return to login form
                document.getElementById('loginForm').style.display = 'block';
                document.getElementById('registerForm').style.display = 'none';
                
                showAlert('Your account has been created successfully! You can now login.', 'success');
            });

            // Password reset process
            document.getElementById('resetPasswordButton')?.addEventListener('click', function() {
                const email = document.getElementById('forgotEmail').value.trim();
                
                if (!email) {
                    showAlert('Please enter your email address!', 'danger');
                    return;
                }
                
                // In reality, send email link here, but for demo just show message
                showAlert('Password reset link has been sent to your email. Please check your email.', 'info');
                
                // Return to login form
                document.getElementById('loginForm').style.display = 'block';
                document.getElementById('forgotPasswordForm').style.display = 'none';
                document.getElementById('forgotEmail').value = '';
            });

            // Logout process
            document.getElementById('logoutButton')?.addEventListener('click', function() {
                if (confirm('Are you sure you want to logout?')) {
                    currentUser = null;
                    localStorage.removeItem('currentVehicleUser');
                    
                    // Hide main system and show login form
                    document.getElementById('mainContent').style.display = 'none';
                    document.getElementById('loginContainer').style.display = 'flex';
                    
                    // Reset login form
                    document.getElementById('loginUsername').value = '';
                    document.getElementById('loginPassword').value = '';
                    document.getElementById('loginForm').style.display = 'block';
                    document.getElementById('registerForm').style.display = 'none';
                    document.getElementById('forgotPasswordForm').style.display = 'none';
                    
                    showAlert('You have successfully logged out.', 'info');
                }
            });

            // Check if already logged in
            const savedUser = localStorage.getItem('currentVehicleUser');
            if (savedUser) {
                try {
                    currentUser = JSON.parse(savedUser);
                    const users = getUsers();
                    const userExists = users.some(u => u.id === currentUser.id && u.active);
                    
                    if (userExists) {
                        document.getElementById('loginContainer').style.display = 'none';
                        document.getElementById('mainContent').style.display = 'block';
                        updateUserDisplay();
                        updateStatistics();
                        updateVehiclesTable();
                        updateUsersTable();
                    } else {
                        localStorage.removeItem('currentVehicleUser');
                    }
                } catch (e) {
                    localStorage.removeItem('currentVehicleUser');
                }
            }
            
            // Theme toggle management
            document.getElementById('themeToggle')?.addEventListener('change', function() {
                currentTheme = this.checked ? 'light' : 'dark';
                updateTheme();
            });
            
            document.getElementById('headerThemeToggle')?.addEventListener('change', function() {
                currentTheme = this.checked ? 'light' : 'dark';
                updateTheme();
            });
            
            // Settings buttons management
            document.getElementById('settingsBtn')?.addEventListener('click', openSettingsPanel);
            document.getElementById('closeSettings')?.addEventListener('click', closeSettingsPanel);
            
            // Close settings panel when clicking outside
            document.addEventListener('click', function(event) {
                const settingsPanel = document.getElementById('settingsPanel');
                const settingsBtn = document.getElementById('settingsBtn');
                
                if (settingsPanel && settingsPanel.classList.contains('show') && 
                    !settingsPanel.contains(event.target) && 
                    !settingsBtn.contains(event.target)) {
                    closeSettingsPanel();
                }
            });
            
            // Language switching management
            document.querySelectorAll('.lang-option').forEach(option => {
                option.addEventListener('click', function() {
                    const lang = this.getAttribute('data-lang');
                    currentLanguage = lang;
                    localStorage.setItem('vehicleSystemLanguage', lang);
                    
                    // Update active language option
                    document.querySelectorAll('.lang-option').forEach(opt => {
                        opt.classList.remove('active');
                    });
                    this.classList.add('active');
                    
                    // Update language
                    updateLanguage();
                    updateDateTime();
                    updateUserDisplay();
                    updateUsersTable();
                    
                    // Update language display buttons
                    document.getElementById('currentLangText').textContent = languageNames[lang][lang];
                    document.getElementById('headerLangText').textContent = languageNames[lang][lang];
                    
                    // Hide language dropdown
                    document.querySelectorAll('.lang-dropdown').forEach(dropdown => {
                        dropdown.classList.remove('show');
                    });
                });
            });
            
            // Language dropdown show/hide
            document.getElementById('currentLangBtn')?.addEventListener('click', function(e) {
                e.stopPropagation();
                const dropdown = document.getElementById('langDropdown');
                dropdown.classList.toggle('show');
            });
            
            document.getElementById('headerLangBtn')?.addEventListener('click', function(e) {
                e.stopPropagation();
                const dropdown = document.getElementById('headerLangDropdown');
                dropdown.classList.toggle('show');
            });
            
            // Hide language dropdown when clicking outside
            document.addEventListener('click', function() {
                document.querySelectorAll('.lang-dropdown').forEach(dropdown => {
                    dropdown.classList.remove('show');
                });
            });
            
            // Background switching management
            document.querySelectorAll('.bg-option').forEach(option => {
                option.addEventListener('click', function() {
                    const bg = this.getAttribute('data-bg');
                    currentBackground = bg;
                    updateBackground();
                });
            });
            
            // Settings reset management
            document.getElementById('resetSettings')?.addEventListener('click', function() {
                if (confirm('Are you sure you want to reset settings?')) {
                    localStorage.removeItem('vehicleSystemLanguage');
                    localStorage.removeItem('vehicleSystemBackground');
                    localStorage.removeItem('vehicleSystemTheme');
                    
                    currentLanguage = 'ps';
                    currentBackground = 'dark-digital';
                    currentTheme = 'dark';
                    
                    updateLanguage();
                    updateBackground();
                    updateTheme();
                    
                    showAlert('Settings have been reset successfully.', 'success');
                }
            });
            
            // Admin user creation form management
            document.getElementById('addUserBtn')?.addEventListener('click', function() {
                if (!currentUser || currentUser.role !== 'admin') {
                    showAlert('Only admin can add new users!', 'danger');
                    return;
                }
                
                showAdminUserForm();
            });
            
            document.getElementById('cancelUserForm')?.addEventListener('click', function() {
                hideAdminUserForm();
            });
            
            document.getElementById('adminUserForm')?.addEventListener('submit', function(e) {
                e.preventDefault();
                
                const fullName = document.getElementById('adminFullName').value.trim();
                const username = document.getElementById('adminUsername').value.trim();
                const email = document.getElementById('adminEmail').value.trim();
                const password = document.getElementById('adminPassword').value.trim();
                const role = document.getElementById('adminRole').value;
                const status = document.getElementById('adminStatus').value;
                
                // Validation
                if (!fullName || !username || !email || !password) {
                    showAlert('Please fill all required fields!', 'danger');
                    return;
                }
                
                if (password.length < 6) {
                    showAlert('Password must be at least 6 characters!', 'danger');
                    return;
                }
                
                const users = getUsers();
                
                // Check for duplicate username and email
                if (users.some(u => u.username === username)) {
                    showAlert('This username already exists!', 'danger');
                    return;
                }
                
                if (users.some(u => u.email === email)) {
                    showAlert('This email address already exists!', 'danger');
                    return;
                }
                
                // Create new user
                const newUser = {
                    id: users.length > 0 ? Math.max(...users.map(u => u.id)) + 1 : 1,
                    fullName,
                    username,
                    email,
                    password,
                    role,
                    registeredDate: new Date().toISOString(),
                    active: status === 'active',
                    lastLogin: null
                };
                
                users.push(newUser);
                saveUsers(users);
                
                // Clear and hide form
                hideAdminUserForm();
                updateUsersTable();
                
                showAlert(`User ${fullName} has been added successfully!`, 'success');
            });
            
            // Export all data management
            document.getElementById('exportAllData')?.addEventListener('click', function() {
                const users = getUsers();
                const vehicles = getVehicles();
                const entries = getEntries();
                const loads = getLoads();
                const exits = getExits();
                
                const allData = {
                    users: users.map(u => ({
                        ...u,
                        password: '***' // Hide password for security
                    })),
                    vehicles,
                    entries,
                    loads,
                    exits,
                    exportDate: new Date().toISOString(),
                    exportedBy: currentUser ? currentUser.username : 'unknown'
                };
                
                const dataStr = JSON.stringify(allData, null, 2);
                const dataBlob = new Blob([dataStr], { type: 'application/json' });
                const url = URL.createObjectURL(dataBlob);
                const link = document.createElement('a');
                link.setAttribute('href', url);
                link.setAttribute('download', `vehicle_system_backup_${new Date().toISOString().slice(0, 10)}.json`);
                link.style.visibility = 'hidden';
                document.body.appendChild(link);
                link.click();
                document.body.removeChild(link);
                
                showAlert('All data exported successfully!', 'success');
            });
            
            // Initialize system forms and functionality
            initializeSystemForms();
        });

        // Initialize system forms and functionality
        function initializeSystemForms() {
            // Plate number check event listeners
            const entryPlateInput = document.getElementById('entryPlateNumber');
            const loadPlateInput = document.getElementById('loadPlateNumber');
            const exitPlateInput = document.getElementById('exitPlateNumber');
            
            if (entryPlateInput) {
                entryPlateInput.addEventListener('input', checkEntryPlateNumber);
            }
            
            if (loadPlateInput) {
                loadPlateInput.addEventListener('input', checkLoadPlateNumber);
            }
            
            if (exitPlateInput) {
                exitPlateInput.addEventListener('input', checkExitPlateNumber);
            }
            
            // Vehicle registration form
            const vehicleRegistrationForm = document.getElementById('vehicleRegistrationForm');
            if (vehicleRegistrationForm) {
                vehicleRegistrationForm.addEventListener('submit', function(e) {
                    e.preventDefault();
                    
                    // Check if user is logged in
                    if (!currentUser) {
                        showAlert('You must login first!', 'danger');
                        return;
                    }
                    
                    // Get form data
                    const vehicleType = document.getElementById('vehicleType').value;
                    const plateNumber = document.getElementById('plateNumber').value.trim();
                    const chassisNumber = document.getElementById('chassisNumber').value.trim();
                    const engineNumber = document.getElementById('engineNumber').value.trim();
                    const companyName = document.getElementById('companyName').value;
                    const driverName = document.getElementById('driverName').value.trim();
                    const driverPhone = document.getElementById('driverPhone').value.trim();
                    const driverId = document.getElementById('driverId').value.trim();
                    
                    // Check if plate number already exists
                    const existingVehicle = checkPlateNumber(plateNumber);
                    if (existingVehicle) {
                        showAlert(`Plate ${plateNumber} is already registered!`, 'danger');
                        return;
                    }
                    
                    // Create new vehicle
                    const newVehicle = {
                        vehicleType,
                        plateNumber,
                        chassisNumber,
                        engineNumber,
                        companyName,
                        driverName,
                        driverPhone,
                        driverId,
                        registrationDate: new Date().toISOString(),
                        registeredBy: currentUser.username
                    };
                    
                    // Save to localStorage
                    const vehicles = getVehicles();
                    vehicles.push(newVehicle);
                    saveVehicles(vehicles);
                    
                    // Update statistics
                    updateStatistics();
                    
                    // Update list
                    updateVehiclesTable();
                    
                    // Clear form
                    this.reset();
                    
                    // Show success message
                    showAlert(`Vehicle ${plateNumber} registered successfully!`, 'success');
                    
                    // Switch to entry tab
                    const entryTab = document.getElementById('entry-tab');
                    if (entryTab) {
                        const bsTab = new bootstrap.Tab(entryTab);
                        bsTab.show();
                    }
                });
            }
            
            // Entry gate form
            const entryGateForm = document.getElementById('entryGateForm');
            if (entryGateForm) {
                entryGateForm.addEventListener('submit', function(e) {
                    e.preventDefault();
                    
                    // Check if user is logged in
                    if (!currentUser) {
                        showAlert('You must login first!', 'danger');
                        return;
                    }
                    
                    // Get form data
                    const zone = document.getElementById('entryZone').value;
                    const gateNumber = document.getElementById('entryGateNumber').value;
                    const category = document.getElementById('entryVehicleCategory').value;
                    const plateNumber = document.getElementById('entryPlateNumber').value.trim();
                    const remarks = document.getElementById('entryRemarks').value.trim();
                    
                    // Check if plate number is registered
                    const vehicle = checkPlateNumber(plateNumber);
                    if (!vehicle) {
                        showAlert(`Plate ${plateNumber} is not registered in the system!`, 'danger');
                        return;
                    }
                    
                    // Check if vehicle already entered
                    const entries = getEntries();
                    const existingEntry = entries.find(e => e.plateNumber === plateNumber);
                    if (existingEntry) {
                        // If vehicle already entered, check if it exited
                        const exits = getExits();
                        const hasExited = exits.some(e => e.plateNumber === plateNumber);
                        
                        if (!hasExited) {
                            showAlert(`Vehicle ${plateNumber} has already entered through entry gate!`, 'warning');
                            return;
                        }
                    }
                    
                    // Create new entry
                    const newEntry = {
                        plateNumber,
                        zone,
                        gateNumber,
                        category,
                        remarks,
                        entryTime: new Date().toISOString(),
                        enteredBy: currentUser.username
                    };
                    
                    entries.push(newEntry);
                    saveEntries(entries);
                    
                    // Update statistics
                    updateStatistics();
                    
                    // Update list
                    updateVehiclesTable();
                    
                    // Update waiting vehicles list for loading
                    updateWaitingVehiclesList();
                    
                    // Clear form
                    this.reset();
                    const plateCheckResult = document.getElementById('plateCheckResult');
                    if (plateCheckResult) {
                        plateCheckResult.textContent = '';
                    }
                    
                    // Show success message
                    showAlert(`Vehicle ${plateNumber} entered successfully from ${zone} zone!`, 'success');
                    
                    // Switch to loading tab
                    const loadTab = document.getElementById('load-tab');
                    if (loadTab) {
                        const bsTab = new bootstrap.Tab(loadTab);
                        bsTab.show();
                    }
                });
            }
            
            // Loading form
            const loadAssignmentForm = document.getElementById('loadAssignmentForm');
            if (loadAssignmentForm) {
                loadAssignmentForm.addEventListener('submit', function(e) {
                    e.preventDefault();
                    
                    // Check if user is logged in
                    if (!currentUser) {
                        showAlert('You must login first!', 'danger');
                        return;
                    }
                    
                    // Get form data
                    const plateNumber = document.getElementById('loadPlateNumber').value.trim();
                    const province = document.getElementById('loadProvince').value;
                    const loadType = document.getElementById('loadType').value;
                    const loadWeight = document.getElementById('loadWeight').value;
                    const destination = document.getElementById('loadDestination').value.trim();
                    const receiver = document.getElementById('loadReceiver').value.trim();
                    const description = document.getElementById('loadDescription').value.trim();
                    
                    // Check plate number
                    const vehicle = checkPlateNumber(plateNumber);
                    if (!vehicle) {
                        showAlert(`Plate ${plateNumber} is not registered in the system!`, 'danger');
                        return;
                    }
                    
                    // Check if vehicle has entered
                    const entries = getEntries();
                    const entry = entries.find(e => e.plateNumber === plateNumber);
                    if (!entry) {
                        showAlert(`Vehicle ${plateNumber} has not entered through entry gate yet!`, 'danger');
                        return;
                    }
                    
                    // Check if vehicle already loaded
                    const loads = getLoads();
                    const existingLoad = loads.find(l => l.plateNumber === plateNumber);
                    if (existingLoad) {
                        showAlert(`Vehicle ${plateNumber} is already loaded!`, 'warning');
                        return;
                    }
                    
                    // Create new load
                    const newLoad = {
                        plateNumber,
                        province,
                        loadType,
                        weight: loadWeight,
                        destination,
                        receiver,
                        description,
                        loadTime: new Date().toISOString(),
                        loadedBy: currentUser.username
                    };
                    
                    loads.push(newLoad);
                    saveLoads(loads);
                    
                    // Update statistics
                    updateStatistics();
                    
                    // Update list
                    updateVehiclesTable();
                    
                    // Update waiting vehicles list
                    updateWaitingVehiclesList();
                    
                    // Update recent loads list
                    updateRecentLoadsList();
                    
                    // Clear form
                    this.reset();
                    const provinceSelect = document.getElementById('loadProvince');
                    if (provinceSelect) {
                        provinceSelect.disabled = true;
                        provinceSelect.innerHTML = '<option value="" selected disabled>Enter plate first...</option>';
                    }
                    
                    const loadVehicleInfoDetails = document.getElementById('loadVehicleInfoDetails');
                    if (loadVehicleInfoDetails) {
                        loadVehicleInfoDetails.innerHTML = 'Vehicle information will appear here when you enter plate number';
                    }
                    
                    const loadVehicleInfoTitle = document.getElementById('loadVehicleInfoTitle');
                    if (loadVehicleInfoTitle) {
                        loadVehicleInfoTitle.innerHTML = 'Vehicle Information:';
                    }
                    
                    const loadPlateCheckResult = document.getElementById('loadPlateCheckResult');
                    if (loadPlateCheckResult) {
                        loadPlateCheckResult.textContent = '';
                    }
                    
                    // Show success message
                    showAlert(`Vehicle ${plateNumber} loaded successfully! Province: ${province}`, 'success');
                    
                    // Switch to exit tab
                    const exitTab = document.getElementById('exit-tab');
                    if (exitTab) {
                        const bsTab = new bootstrap.Tab(exitTab);
                        bsTab.show();
                    }
                });
            }
            
            // Exit gate form
            const exitGateForm = document.getElementById('exitGateForm');
            if (exitGateForm) {
                exitGateForm.addEventListener('submit', function(e) {
                    e.preventDefault();
                    
                    // Check if user is logged in
                    if (!currentUser) {
                        showAlert('You must login first!', 'danger');
                        return;
                    }
                    
                    // Get form data
                    const plateNumber = document.getElementById('exitPlateNumber').value.trim();
                    const gateNumber = document.getElementById('exitGateNumber').value;
                    const remarks = document.getElementById('exitRemarks').value.trim();
                    
                    // Check plate number
                    const vehicle = checkPlateNumber(plateNumber);
                    if (!vehicle) {
                        showAlert(`Plate ${plateNumber} is not registered in the system!`, 'danger');
                        return;
                    }
                    
                    // Check if vehicle has entered
                    const entries = getEntries();
                    const entry = entries.find(e => e.plateNumber === plateNumber);
                    if (!entry) {
                        showAlert(`Vehicle ${plateNumber} has not entered through entry gate yet!`, 'danger');
                        return;
                    }
                    
                    // Check if vehicle is loaded
                    const loads = getLoads();
                    const load = loads.find(l => l.plateNumber === plateNumber);
                    if (!load) {
                        showAlert(`Vehicle ${plateNumber} is not loaded yet!`, 'danger');
                        return;
                    }
                    
                    // Check if vehicle already exited
                    const exits = getExits();
                    const existingExit = exits.find(e => e.plateNumber === plateNumber);
                    if (existingExit) {
                        showAlert(`Vehicle ${plateNumber} has already exited!`, 'warning');
                        return;
                    }
                    
                    // Create new exit
                    const newExit = {
                        plateNumber,
                        gateNumber,
                        remarks,
                        exitTime: new Date().toISOString(),
                        exitedBy: currentUser.username
                    };
                    
                    exits.push(newExit);
                    saveExits(exits);
                    
                    // Update statistics
                    updateStatistics();
                    
                    // Update list
                    updateVehiclesTable();
                    
                    // Update recent exits list
                    updateRecentExitsList();
                    
                    // Clear form
                    this.reset();
                    const exitVehicleInfoDetails = document.getElementById('exitVehicleInfoDetails');
                    if (exitVehicleInfoDetails) {
                        exitVehicleInfoDetails.innerHTML = 'Vehicle information will appear here when you enter plate number';
                    }
                    
                    const exitVehicleInfoTitle = document.getElementById('exitVehicleInfoTitle');
                    if (exitVehicleInfoTitle) {
                        exitVehicleInfoTitle.innerHTML = 'Vehicle Information:';
                    }
                    
                    const exitPlateCheckResult = document.getElementById('exitPlateCheckResult');
                    if (exitPlateCheckResult) {
                        exitPlateCheckResult.textContent = '';
                    }
                    
                    // Show success message
                    showAlert(`Vehicle ${plateNumber} exited successfully!`, 'success');
                });
            }
            
            // List filter buttons
            const filterAllBtn = document.getElementById('filterAll');
            const filterInsideBtn = document.getElementById('filterInside');
            const filterLoadedBtn = document.getElementById('filterLoaded');
            const filterExitedBtn = document.getElementById('filterExited');
            const filterWaitingBtn = document.getElementById('filterWaiting');
            
            if (filterAllBtn) filterAllBtn.addEventListener('click', () => updateVehiclesTable('all'));
            if (filterInsideBtn) filterInsideBtn.addEventListener('click', () => updateVehiclesTable('inside'));
            if (filterLoadedBtn) filterLoadedBtn.addEventListener('click', () => updateVehiclesTable('loaded'));
            if (filterExitedBtn) filterExitedBtn.addEventListener('click', () => updateVehiclesTable('exited'));
            if (filterWaitingBtn) filterWaitingBtn.addEventListener('click', () => updateVehiclesTable('waiting'));
            
            // Event delegation for dynamic elements
            document.addEventListener('click', function(e) {
                // View details button
                if (e.target.closest('.view-details')) {
                    const plateNumber = e.target.closest('.view-details').dataset.plate;
                    showVehicleDetails(plateNumber);
                }
                
                // Delete user button
                if (e.target.closest('.delete-user')) {
                    const userId = parseInt(e.target.closest('.delete-user').dataset.id);
                    
                    if (currentUser && currentUser.id === userId) {
                        showAlert('You cannot delete your own account!', 'danger');
                        return;
                    }
                    
                    if (confirm('Are you sure you want to delete this user?')) {
                        const users = getUsers();
                        const updatedUsers = users.filter(user => user.id !== userId);
                        saveUsers(updatedUsers);
                        updateUsersTable();
                        showAlert('User deleted successfully!', 'success');
                    }
                }
                
                // Edit user button
                if (e.target.closest('.edit-user')) {
                    const userId = parseInt(e.target.closest('.edit-user').dataset.id);
                    const users = getUsers();
                    const user = users.find(u => u.id === userId);
                    
                    if (user) {
                        // Show edit form
                        document.getElementById('adminFullName').value = user.fullName;
                        document.getElementById('adminUsername').value = user.username;
                        document.getElementById('adminEmail').value = user.email;
                        document.getElementById('adminPassword').value = ''; // Don't show password for security
                        document.getElementById('adminRole').value = user.role;
                        document.getElementById('adminStatus').value = user.active ? 'active' : 'inactive';
                        
                        // Show edit form
                        showAdminUserForm();
                        
                        // Handle form submission for editing
                        const adminUserForm = document.getElementById('adminUserForm');
                        const originalSubmit = adminUserForm.onsubmit;
                        
                        adminUserForm.onsubmit = function(e) {
                            e.preventDefault();
                            
                            const fullName = document.getElementById('adminFullName').value.trim();
                            const username = document.getElementById('adminUsername').value.trim();
                            const email = document.getElementById('adminEmail').value.trim();
                            const password = document.getElementById('adminPassword').value.trim();
                            const role = document.getElementById('adminRole').value;
                            const status = document.getElementById('adminStatus').value;
                            
                            // Update user information
                            const updatedUsers = users.map(u => {
                                if (u.id === userId) {
                                    u.fullName = fullName;
                                    u.username = username;
                                    u.email = email;
                                    if (password) {
                                        u.password = password;
                                    }
                                    u.role = role;
                                    u.active = status === 'active';
                                }
                                return u;
                            });
                            
                            saveUsers(updatedUsers);
                            updateUsersTable();
                            hideAdminUserForm();
                            
                            showAlert(`User ${fullName} updated successfully!`, 'success');
                            
                            // Restore original form handler
                            adminUserForm.onsubmit = originalSubmit;
                        };
                    }
                }
            });
            
            // Print button
            const printListBtn = document.getElementById('printList');
            if (printListBtn) {
                printListBtn.addEventListener('click', function() {
                    window.print();
                });
            }
            
            // Export data button
            const exportDataBtn = document.getElementById('exportData');
            if (exportDataBtn) {
                exportDataBtn.addEventListener('click', function() {
                    const vehicles = getVehicles();
                    const entries = getEntries();
                    const loads = getLoads();
                    const exits = getExits();
                    
                    // Prepare data for export
                    const exportData = vehicles.map(vehicle => {
                        const entry = entries.find(e => e.plateNumber === vehicle.plateNumber);
                        const load = loads.find(l => l.plateNumber === vehicle.plateNumber);
                        const exit = exits.find(e => e.plateNumber === vehicle.plateNumber);
                        
                        let status = 'Registered';
                        if (exit) {
                            status = 'Exited';
                        } else if (load) {
                            status = 'Loaded';
                        } else if (entry) {
                            status = 'In System';
                        }
                        
                        return {
                            'Plate Number': vehicle.plateNumber,
                            'Type': vehicle.vehicleType,
                            'Company': vehicle.companyName,
                            'Driver': vehicle.driverName,
                            'Registration Date': new Date(vehicle.registrationDate).toLocaleDateString('prs-AF'),
                            'Zone': entry ? entry.zone : 'Not Available',
                            'Province': load ? load.province : (entry ? 'Waiting' : 'Not Available'),
                            'Load Type': load ? load.loadType : 'Not Available',
                            'Load Weight': load ? load.weight + ' Tons' : 'Not Available',
                            'Entry Time': entry ? new Date(entry.entryTime).toLocaleString('prs-AF') : 'Not Available',
                            'Load Time': load ? new Date(load.loadTime).toLocaleString('prs-AF') : 'Not Available',
                            'Exit Time': exit ? new Date(exit.exitTime).toLocaleString('prs-AF') : 'Not Available',
                            'Status': status
                        };
                    });
                    
                    // Create CSV file
                    const headers = Object.keys(exportData[0] || {});
                    const csvContent = [
                        headers.join(','),
                        ...exportData.map(row => headers.map(header => `"${row[header]}"`).join(','))
                    ].join('\n');
                    
                    // Download CSV file
                    const blob = new Blob(['\ufeff' + csvContent], { type: 'text/csv;charset=utf-8;' });
                    const url = URL.createObjectURL(blob);
                    const link = document.createElement('a');
                    link.setAttribute('href', url);
                    link.setAttribute('download', `vehicles_${new Date().toISOString().slice(0, 10)}.csv`);
                    link.style.visibility = 'hidden';
                    document.body.appendChild(link);
                    link.click();
                    document.body.removeChild(link);
                    
                    showAlert('Data exported successfully!', 'success');
                });
            }
            
            // Export users button
            const exportUsersBtn = document.getElementById('exportUsers');
            if (exportUsersBtn) {
                exportUsersBtn.addEventListener('click', function() {
                    const users = getUsers();
                    
                    // Prepare data for export
                    const exportData = users.map(user => {
                        return {
                            'Full Name': user.fullName,
                            'Username': user.username,
                            'Email': user.email,
                            'Role': roleNames[user.role][currentLanguage],
                            'Registration Date': new Date(user.registeredDate).toLocaleDateString('prs-AF'),
                            'Status': user.active ? 'Active' : 'Inactive'
                        };
                    });
                    
                    // Create CSV file
                    const headers = Object.keys(exportData[0] || {});
                    const csvContent = [
                        headers.join(','),
                        ...exportData.map(row => headers.map(header => `"${row[header]}"`).join(','))
                    ].join('\n');
                    
                    // Download CSV file
                    const blob = new Blob(['\ufeff' + csvContent], { type: 'text/csv;charset=utf-8;' });
                    const url = URL.createObjectURL(blob);
                    const link = document.createElement('a');
                    link.setAttribute('href', url);
                    link.setAttribute('download', `users_${new Date().toISOString().slice(0, 10)}.csv`);
                    link.style.visibility = 'hidden';
                    document.body.appendChild(link);
                    link.click();
                    document.body.removeChild(link);
                    
                    showAlert('Users exported successfully!', 'success');
                });
            }
            
            // Tab change animation
            const tabButtons = document.querySelectorAll('button[data-bs-toggle="tab"]');
            tabButtons.forEach(button => {
                button.addEventListener('shown.bs.tab', function() {
                    const targetId = this.getAttribute('data-bs-target');
                    const targetPane = document.querySelector(targetId);
                    if (targetPane) {
                        targetPane.classList.add('fade-in');
                        
                        // Refresh data based on tab
                        if (targetId === '#list') {
                            updateVehiclesTable();
                        }
                        
                        if (targetId === '#load') {
                            updateWaitingVehiclesList();
                            updateRecentLoadsList();
                        }
                        
                        if (targetId === '#exit') {
                            updateRecentExitsList();
                        }
                        
                        if (targetId === '#users') {
                            updateUsersTable();
                        }
                    }
                });
            });
            
            // Initialize data if user is logged in
            if (currentUser) {
                updateWaitingVehiclesList();
                updateRecentLoadsList();
                updateRecentExitsList();
            }
        }

        // Update statistics
        function updateStatistics() {
            const vehicles = getVehicles();
            const entries = getEntries();
            const loads = getLoads();
            const exits = getExits();
            
            // Today's entered vehicles
            const today = new Date().toDateString();
            const todayEntries = entries.filter(entry => {
                const entryDate = new Date(entry.entryTime).toDateString();
                return entryDate === today;
            });
            
            // Today's loaded vehicles
            const todayLoads = loads.filter(load => {
                const loadDate = new Date(load.loadTime).toDateString();
                return loadDate === today;
            });
            
            // Today's exited vehicles
            const todayExits = exits.filter(exit => {
                const exitDate = new Date(exit.exitTime).toDateString();
                return exitDate === today;
            });
            
            // Currently in system vehicles (entered but not exited)
            const insideVehicles = entries.filter(entry => {
                return !exits.some(exit => exit.plateNumber === entry.plateNumber);
            });
            
            // Vehicles waiting for load (entered but not loaded and not exited)
            const waitingVehicles = entries.filter(entry => {
                return !loads.some(load => load.plateNumber === entry.plateNumber) && 
                       !exits.some(exit => exit.plateNumber === entry.plateNumber);
            });
            
            document.getElementById('total-vehicles').textContent = vehicles.length;
            document.getElementById('entered-vehicles').textContent = todayEntries.length;
            document.getElementById('loaded-vehicles').textContent = todayLoads.length;
            document.getElementById('exited-vehicles').textContent = todayExits.length;
            document.getElementById('inside-vehicles').textContent = insideVehicles.length;
            document.getElementById('waiting-vehicles').textContent = waitingVehicles.length;
        }

        // Update registered vehicles table
        function updateVehiclesTable(filter = 'all') {
            const vehicles = getVehicles();
            const entries = getEntries();
            const loads = getLoads();
            const exits = getExits();
            const tbody = document.getElementById('vehiclesTableBody');
            
            if (!tbody) return;
            
            tbody.innerHTML = '';
            
            if (vehicles.length === 0) {
                tbody.innerHTML = '<tr><td colspan="11" class="text-center">No vehicles registered yet</td></tr>';
                document.getElementById('tableInfo').textContent = 'No vehicles registered yet';
                return;
            }
            
            let filteredVehicles = vehicles;
            
            if (filter === 'inside') {
                // Only vehicles currently in system
                filteredVehicles = vehicles.filter(vehicle => {
                    const hasEntry = entries.some(entry => entry.plateNumber === vehicle.plateNumber);
                    const hasExit = exits.some(exit => exit.plateNumber === vehicle.plateNumber);
                    return hasEntry && !hasExit;
                });
            } else if (filter === 'loaded') {
                // Only loaded vehicles
                filteredVehicles = vehicles.filter(vehicle => {
                    return loads.some(load => load.plateNumber === vehicle.plateNumber);
                });
            } else if (filter === 'exited') {
                // Only exited vehicles
                filteredVehicles = vehicles.filter(vehicle => {
                    return exits.some(exit => exit.plateNumber === vehicle.plateNumber);
                });
            } else if (filter === 'waiting') {
                // Only vehicles waiting for load
                filteredVehicles = vehicles.filter(vehicle => {
                    const hasEntry = entries.some(entry => entry.plateNumber === vehicle.plateNumber);
                    const hasLoad = loads.some(load => load.plateNumber === vehicle.plateNumber);
                    const hasExit = exits.some(exit => exit.plateNumber === vehicle.plateNumber);
                    return hasEntry && !hasLoad && !hasExit;
                });
            }
            
            filteredVehicles.forEach((vehicle, index) => {
                const entry = entries.find(e => e.plateNumber === vehicle.plateNumber);
                const load = loads.find(l => l.plateNumber === vehicle.plateNumber);
                const exit = exits.find(e => e.plateNumber === vehicle.plateNumber);
                
                let status = 'Registered';
                let statusClass = 'status-registered';
                
                if (exit) {
                    status = 'Exited';
                    statusClass = 'status-exited';
                } else if (load) {
                    status = 'Loaded';
                    statusClass = 'status-loaded';
                } else if (entry) {
                    status = 'In System';
                    statusClass = 'status-entered';
                }
                
                // Create load type badge
                let loadTypeBadge = '';
                if (load) {
                    const loadClass = loadTypeClasses[load.loadType] || 'load-other';
                    loadTypeBadge = `<span class="load-type-badge ${loadClass}">${load.loadType}</span>`;
                }
                
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td>${index + 1}</td>
                    <td><strong>${vehicle.plateNumber}</strong></td>
                    <td>${vehicle.vehicleType}</td>
                    <td>${vehicle.companyName}</td>
                    <td>${vehicle.driverName}</td>
                    <td>${entry ? entry.zone : 'Not Available'}</td>
                    <td>${load ? load.province : (entry ? 'Waiting' : 'Not Available')}</td>
                    <td>${loadTypeBadge || 'Not Available'}</td>
                    <td>${new Date(vehicle.registrationDate).toLocaleDateString('prs-AF')}</td>
                    <td><span class="status-badge ${statusClass}">${status}</span></td>
                    <td>
                        <button class="btn btn-sm btn-outline-info view-details" data-plate="${vehicle.plateNumber}">
                            <i class="fas fa-eye"></i>
                        </button>
                    </td>
                `;
                tbody.appendChild(row);
            });
            
            document.getElementById('tableInfo').textContent = `${filteredVehicles.length} vehicles found`;
        }

        // Update users table
        function updateUsersTable() {
            const users = getUsers();
            const tbody = document.getElementById('usersTableBody');
            
            if (!tbody) return;
            
            tbody.innerHTML = '';
            
            if (users.length === 0) {
                tbody.innerHTML = '<tr><td colspan="8" class="text-center">No users found</td></tr>';
                document.getElementById('usersTableInfo').textContent = 'No users found';
                return;
            }
            
            users.forEach((user, index) => {
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td>${index + 1}</td>
                    <td>${user.fullName}</td>
                    <td>${user.username}</td>
                    <td>${user.email}</td>
                    <td><span class="user-role-badge ${roleClasses[user.role]}">${roleNames[user.role][currentLanguage]}</span></td>
                    <td>${new Date(user.registeredDate).toLocaleDateString('prs-AF')}</td>
                    <td>${user.active ? '<span class="text-success">Active</span>' : '<span class="text-danger">Inactive</span>'}</td>
                    <td>
                        <button class="btn btn-sm btn-outline-warning edit-user" data-id="${user.id}" ${currentUser && currentUser.id === user.id ? 'disabled' : ''}>
                            <i class="fas fa-edit"></i>
                        </button>
                        <button class="btn btn-sm btn-outline-danger delete-user" data-id="${user.id}" ${currentUser && currentUser.id === user.id ? 'disabled' : ''}>
                            <i class="fas fa-trash"></i>
                        </button>
                    </td>
                `;
                tbody.appendChild(row);
            });
            
            document.getElementById('usersTableInfo').textContent = `${users.length} users found`;
        }

        // Show vehicle details
        function showVehicleDetails(plateNumber) {
            const vehicles = getVehicles();
            const entries = getEntries();
            const loads = getLoads();
            const exits = getExits();
            
            const vehicle = vehicles.find(v => v.plateNumber === plateNumber);
            if (!vehicle) return;
            
            const entry = entries.find(e => e.plateNumber === plateNumber);
            const load = loads.find(l => l.plateNumber === plateNumber);
            const exit = exits.find(e => e.plateNumber === plateNumber);
            
            let detailsHtml = `
                <div class="row">
                    <div class="col-md-6">
                        <p><strong>Plate Number:</strong> ${vehicle.plateNumber}</p>
                        <p><strong>Type:</strong> ${vehicle.vehicleType}</p>
                        <p><strong>Company:</strong> ${vehicle.companyName}</p>
                        <p><strong>Driver:</strong> ${vehicle.driverName}</p>
                        <p><strong>Driver Phone:</strong> ${vehicle.driverPhone || 'Not Available'}</p>
                    </div>
                    <div class="col-md-6">
                        <p><strong>Chassis Number:</strong> ${vehicle.chassisNumber}</p>
                        <p><strong>Engine Number:</strong> ${vehicle.engineNumber}</p>
                        <p><strong>Driver ID:</strong> ${vehicle.driverId || 'Not Available'}</p>
                        <p><strong>Registration Date:</strong> ${new Date(vehicle.registrationDate).toLocaleDateString('prs-AF')}</p>
                    </div>
                </div>
            `;
            
            if (entry) {
                detailsHtml += `
                    <div class="row mt-3">
                        <div class="col-12">
                            <h6>Entry Information:</h6>
                            <p><strong>Zone:</strong> ${entry.zone}</p>
                            <p><strong>Gate Number:</strong> ${entry.gateNumber || 'Not Available'}</p>
                            <p><strong>Vehicle Category:</strong> ${entry.category}</p>
                            <p><strong>Entry Time:</strong> ${new Date(entry.entryTime).toLocaleString('prs-AF')}</p>
                            ${entry.remarks ? `<p><strong>Notes:</strong> ${entry.remarks}</p>` : ''}
                        </div>
                    </div>
                `;
            }
            
            if (load) {
                const loadClass = loadTypeClasses[load.loadType] || 'load-other';
                detailsHtml += `
                    <div class="row mt-3">
                        <div class="col-12">
                            <h6>Load Information:</h6>
                            <p><strong>Province:</strong> ${load.province}</p>
                            <p><strong>Load Type:</strong> <span class="load-type-badge ${loadClass}">${load.loadType}</span></p>
                            <p><strong>Load Weight:</strong> ${load.weight} Tons</p>
                            <p><strong>Destination:</strong> ${load.destination}</p>
                            ${load.receiver ? `<p><strong>Receiver:</strong> ${load.receiver}</p>` : ''}
                            ${load.description ? `<p><strong>Description:</strong> ${load.description}</p>` : ''}
                            <p><strong>Load Time:</strong> ${new Date(load.loadTime).toLocaleString('prs-AF')}</p>
                        </div>
                    </div>
                `;
            }
            
            if (exit) {
                detailsHtml += `
                    <div class="row mt-3">
                        <div class="col-12">
                            <h6>Exit Information:</h6>
                            <p><strong>Gate Number:</strong> ${exit.gateNumber || 'Not Available'}</p>
                            <p><strong>Exit Time:</strong> ${new Date(exit.exitTime).toLocaleString('prs-AF')}</p>
                            ${exit.remarks ? `<p><strong>Notes:</strong> ${exit.remarks}</p>` : ''}
                        </div>
                    </div>
                `;
            }
            
            // Create and show modal
            const modalHtml = `
                <div class="modal fade" id="vehicleDetailsModal" tabindex="-1">
                    <div class="modal-dialog modal-lg">
                        <div class="modal-content">
                            <div class="modal-header">
                                <h5 class="modal-title">Vehicle ${vehicle.plateNumber} Details</h5>
                                <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
                            </div>
                            <div class="modal-body">
                                ${detailsHtml}
                            </div>
                            <div class="modal-footer">
                                <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
                            </div>
                        </div>
                    </div>
                </div>
            `;
            
            // Remove existing modal if exists
            const existingModal = document.getElementById('vehicleDetailsModal');
            if (existingModal) {
                existingModal.remove();
            }
            
            // Add new modal
            document.body.insertAdjacentHTML('beforeend', modalHtml);
            const modal = new bootstrap.Modal(document.getElementById('vehicleDetailsModal'));
            modal.show();
        }

        // Check if plate number is registered
        function checkPlateNumber(plateNumber) {
            const vehicles = getVehicles();
            return vehicles.find(v => v.plateNumber === plateNumber);
        }

        // Check plate number at entry gate
        function checkEntryPlateNumber() {
            const plateNumber = document.getElementById('entryPlateNumber').value.trim();
            const resultDiv = document.getElementById('plateCheckResult');
            
            if (!plateNumber) {
                resultDiv.textContent = '';
                resultDiv.className = 'form-text';
                return;
            }
            
            const vehicle = checkPlateNumber(plateNumber);
            if (vehicle) {
                resultDiv.textContent = `✓ This plate is registered. Driver: ${vehicle.driverName}`;
                resultDiv.className = 'form-text text-success';
            } else {
                resultDiv.textContent = '✗ This plate is not registered. Please register first.';
                resultDiv.className = 'form-text text-danger';
            }
        }

        // Check plate number at loading
        function checkLoadPlateNumber() {
            const plateNumber = document.getElementById('loadPlateNumber').value.trim();
            const resultDiv = document.getElementById('loadPlateCheckResult');
            const infoDiv = document.getElementById('loadVehicleInfoDetails');
            const titleDiv = document.getElementById('loadVehicleInfoTitle');
            const provinceSelect = document.getElementById('loadProvince');
            
            if (!plateNumber) {
                resultDiv.textContent = '';
                resultDiv.className = 'form-text';
                infoDiv.innerHTML = 'Vehicle information will appear here when you enter plate number';
                titleDiv.innerHTML = 'Vehicle Information:';
                provinceSelect.innerHTML = '<option value="" selected disabled>Enter plate first...</option>';
                provinceSelect.disabled = true;
                return;
            }
            
            const vehicle = checkPlateNumber(plateNumber);
            const entries = getEntries();
            const loads = getLoads();
            
            const entry = entries.find(e => e.plateNumber === plateNumber);
            const load = loads.find(l => l.plateNumber === plateNumber);
            
            if (!vehicle) {
                resultDiv.textContent = '✗ This plate is not registered.';
                resultDiv.className = 'form-text text-danger';
                infoDiv.innerHTML = '<div class="text-danger">This plate is not registered in the system.</div>';
                titleDiv.innerHTML = '<span class="text-danger">Vehicle Information:</span>';
                provinceSelect.innerHTML = '<option value="" selected disabled>Enter plate first...</option>';
                provinceSelect.disabled = true;
                return;
            }
            
            if (!entry) {
                resultDiv.textContent = '✗ This vehicle has not entered through entry gate yet.';
                resultDiv.className = 'form-text text-danger';
                infoDiv.innerHTML = `
                    <div class="text-danger">
                        <p>This vehicle has not entered through entry gate yet.</p>
                        <p><strong>Driver:</strong> ${vehicle.driverName}</p>
                        <p><strong>Type:</strong> ${vehicle.vehicleType}</p>
                    </div>
                `;
                titleDiv.innerHTML = '<span class="text-danger">Vehicle Information:</span>';
                provinceSelect.innerHTML = '<option value="" selected disabled>Enter plate first...</option>';
                provinceSelect.disabled = true;
                return;
            }
            
            if (load) {
                resultDiv.textContent = '✗ This vehicle is already loaded.';
                resultDiv.className = 'form-text text-danger';
                infoDiv.innerHTML = `
                    <div class="text-danger">
                        <p>This vehicle is already loaded at ${new Date(load.loadTime).toLocaleString('prs-AF')}.</p>
                        <p><strong>Driver:</strong> ${vehicle.driverName}</p>
                        <p><strong>Type:</strong> ${vehicle.vehicleType}</p>
                        <p><strong>Province:</strong> ${load.province}</p>
                    </div>
                `;
                titleDiv.innerHTML = '<span class="text-danger">Vehicle Information:</span>';
                provinceSelect.innerHTML = '<option value="" selected disabled>Enter plate first...</option>';
                provinceSelect.disabled = true;
                return;
            }
            
            // If vehicle is registered, entered and not loaded
            resultDiv.textContent = '✓ This vehicle is ready for loading.';
            resultDiv.className = 'form-text text-success';
            infoDiv.innerHTML = `
                <div>
                    <p><strong>Driver:</strong> ${vehicle.driverName}</p>
                    <p><strong>Type:</strong> ${vehicle.vehicleType}</p>
                    <p><strong>Company:</strong> ${vehicle.companyName}</p>
                    <p><strong>Entry Time:</strong> ${new Date(entry.entryTime).toLocaleString('prs-AF')}</p>
                    <p><strong>Entry Zone:</strong> ${entry.zone}</p>
                </div>
            `;
            titleDiv.innerHTML = '<span class="text-success">Vehicle Information:</span>';
            
            // Update province list based on zone
            const provinces = zonesData[entry.zone] || [];
            provinceSelect.innerHTML = '<option value="" selected disabled>Select...</option>';
            
            provinces.forEach(province => {
                const option = document.createElement('option');
                option.value = province;
                option.textContent = province;
                provinceSelect.appendChild(option);
            });
            
            provinceSelect.disabled = false;
        }

        // Check plate number at exit gate
        function checkExitPlateNumber() {
            const plateNumber = document.getElementById('exitPlateNumber').value.trim();
            const resultDiv = document.getElementById('exitPlateCheckResult');
            const infoDiv = document.getElementById('exitVehicleInfoDetails');
            const titleDiv = document.getElementById('exitVehicleInfoTitle');
            
            if (!plateNumber) {
                resultDiv.textContent = '';
                resultDiv.className = 'form-text';
                infoDiv.innerHTML = 'Vehicle information will appear here when you enter plate number';
                titleDiv.innerHTML = 'Vehicle Information:';
                return;
            }
            
            const vehicle = checkPlateNumber(plateNumber);
            const entries = getEntries();
            const loads = getLoads();
            const exits = getExits();
            
            const entry = entries.find(e => e.plateNumber === plateNumber);
            const load = loads.find(l => l.plateNumber === plateNumber);
            const exit = exits.find(e => e.plateNumber === plateNumber);
            
            if (!vehicle) {
                resultDiv.textContent = '✗ This plate is not registered.';
                resultDiv.className = 'form-text text-danger';
                infoDiv.innerHTML = '<div class="text-danger">This plate is not registered in the system.</div>';
                titleDiv.innerHTML = '<span class="text-danger">Vehicle Information:</span>';
                return;
            }
            
            if (!entry) {
                resultDiv.textContent = '✗ This vehicle has not entered through entry gate yet.';
                resultDiv.className = 'form-text text-danger';
                infoDiv.innerHTML = `
                    <div class="text-danger">
                        <p>This vehicle has not entered through entry gate yet.</p>
                        <p><strong>Driver:</strong> ${vehicle.driverName}</p>
                        <p><strong>Type:</strong> ${vehicle.vehicleType}</p>
                    </div>
                `;
                titleDiv.innerHTML = '<span class="text-danger">Vehicle Information:</span>';
                return;
            }
            
            if (!load) {
                resultDiv.textContent = '✗ This vehicle is not loaded yet.';
                resultDiv.className = 'form-text text-danger';
                infoDiv.innerHTML = `
                    <div class="text-danger">
                        <p>This vehicle is not loaded yet.</p>
                        <p><strong>Driver:</strong> ${vehicle.driverName}</p>
                        <p><strong>Type:</strong> ${vehicle.vehicleType}</p>
                        <p><strong>Zone:</strong> ${entry.zone}</p>
                    </div>
                `;
                titleDiv.innerHTML = '<span class="text-danger">Vehicle Information:</span>';
                return;
            }
            
            if (exit) {
                resultDiv.textContent = '✗ This vehicle has already exited.';
                resultDiv.className = 'form-text text-danger';
                infoDiv.innerHTML = `
                    <div class="text-danger">
                        <p>This vehicle has already exited at ${new Date(exit.exitTime).toLocaleString('prs-AF')}.</p>
                        <p><strong>Driver:</strong> ${vehicle.driverName}</p>
                        <p><strong>Type:</strong> ${vehicle.vehicleType}</p>
                    </div>
                `;
                titleDiv.innerHTML = '<span class="text-danger">Vehicle Information:</span>';
                return;
            }
            
            // If vehicle is registered, entered, loaded and not exited
            resultDiv.textContent = '✓ This vehicle is ready for exit.';
            resultDiv.className = 'form-text text-success';
            infoDiv.innerHTML = `
                <div>
                    <p><strong>Driver:</strong> ${vehicle.driverName}</p>
                    <p><strong>Type:</strong> ${vehicle.vehicleType}</p>
                    <p><strong>Company:</strong> ${vehicle.companyName}</p>
                    <p><strong>Entry Time:</strong> ${new Date(entry.entryTime).toLocaleString('prs-AF')}</p>
                    <p><strong>Load Time:</strong> ${new Date(load.loadTime).toLocaleString('prs-AF')}</p>
                    <p><strong>Province:</strong> ${load.province}</p>
                    <p><strong>Load Type:</strong> ${load.loadType}</p>
                    <p><strong>Load Weight:</strong> ${load.weight} Tons</p>
                </div>
            `;
            titleDiv.innerHTML = '<span class="text-success">Vehicle Information:</span>';
        }

        // Update waiting vehicles list for loading
        function updateWaitingVehiclesList() {
            const vehicles = getVehicles();
            const entries = getEntries();
            const loads = getLoads();
            const exits = getExits();
            
            // Vehicles waiting for load (entered but not loaded and not exited)
            const waitingVehicles = entries.filter(entry => {
                return !loads.some(load => load.plateNumber === entry.plateNumber) && 
                       !exits.some(exit => exit.plateNumber === entry.plateNumber);
            });
            
            const waitingListDiv = document.getElementById('waitingVehiclesList');
            
            if (!waitingListDiv) return;
            
            if (waitingVehicles.length === 0) {
                waitingListDiv.innerHTML = '<p class="text-muted">No vehicles waiting for load yet</p>';
                return;
            }
            
            let html = '<div class="list-group">';
            
            waitingVehicles.forEach(entry => {
                const vehicle = vehicles.find(v => v.plateNumber === entry.plateNumber);
                const driverName = vehicle ? vehicle.driverName : 'Invalid Plate';
                
                html += `
                    <div class="list-group-item list-group-item-action">
                        <div class="d-flex w-100 justify-content-between">
                            <h6 class="mb-1">${entry.plateNumber}</h6>
                            <small>${new Date(entry.entryTime).toLocaleTimeString('prs-AF')}</small>
                        </div>
                        <p class="mb-1">${driverName}</p>
                        <small>Zone: ${entry.zone}</small>
                    </div>
                `;
            });
            
            html += '</div>';
            waitingListDiv.innerHTML = html;
        }

        // Update recent loads list
        function updateRecentLoadsList() {
            const loads = getLoads();
            const vehicles = getVehicles();
            const recentLoadsDiv = document.getElementById('recentLoadsList');
            
            if (!recentLoadsDiv) return;
            
            if (loads.length === 0) {
                recentLoadsDiv.innerHTML = '<p class="text-muted">No loads registered yet</p>';
                return;
            }
            
            // Show only last 5 loads
            const recentLoads = loads.slice(-5).reverse();
            let html = '<div class="list-group">';
            
            recentLoads.forEach(load => {
                const vehicle = vehicles.find(v => v.plateNumber === load.plateNumber);
                const driverName = vehicle ? vehicle.driverName : 'Invalid Plate';
                
                html += `
                    <div class="list-group-item list-group-item-action">
                        <div class="d-flex w-100 justify-content-between">
                            <h6 class="mb-1">${load.plateNumber}</h6>
                            <small>${new Date(load.loadTime).toLocaleTimeString('prs-AF')}</small>
                        </div>
                        <p class="mb-1">${driverName}</p>
                        <small>Province: ${load.province} | Load: ${load.loadType}</small>
                    </div>
                `;
            });
            
            html += '</div>';
            recentLoadsDiv.innerHTML = html;
        }

        // Update recent exits list
        function updateRecentExitsList() {
            const exits = getExits();
            const vehicles = getVehicles();
            const recentExitsDiv = document.getElementById('recentExitsList');
            
            if (!recentExitsDiv) return;
            
            if (exits.length === 0) {
                recentExitsDiv.innerHTML = '<p class="text-muted">No exits registered yet</p>';
                return;
            }
            
            // Show only last 5 exits
            const recentExits = exits.slice(-5).reverse();
            let html = '<div class="list-group">';
            
            recentExits.forEach(exit => {
                const vehicle = vehicles.find(v => v.plateNumber === exit.plateNumber);
                const driverName = vehicle ? vehicle.driverName : 'Invalid Plate';
                
                html += `
                    <div class="list-group-item list-group-item-action">
                        <div class="d-flex w-100 justify-content-between">
                            <h6 class="mb-1">${exit.plateNumber}</h6>
                            <small>${new Date(exit.exitTime).toLocaleTimeString('prs-AF')}</small>
                        </div>
                        <p class="mb-1">${driverName}</p>
                    </div>
                `;
            });
            
            html += '</div>';
            recentExitsDiv.innerHTML = html;
        }
    </script>
</body>
</html>
