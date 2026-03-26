<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fiberhome SCaaS Readiness - Pindamonhangaba</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-blue: #004B87;
            --accent-orange: #FF6A13;
            --bg-light: #F4F7F6;
            --text-dark: #333333;
        }
        body, html {
            margin: 0;
            padding: 0;
            font-family: 'Roboto', sans-serif;
            background-color: var(--bg-light);
            color: var(--text-dark);
            height: 100%;
            overflow-x: hidden;
        }
        /* Slider Container */
        .slider-container {
            width: 100vw;
            height: 100vh;
            display: flex;
            overflow-x: auto;
            scroll-snap-type: x mandatory;
            scroll-behavior: smooth;
        }
        /* Hide scrollbar */
        .slider-container::-webkit-scrollbar {
            display: none;
        }
        .slider-container {
            -ms-overflow-style: none;
            scrollbar-width: none;
        }
        /* Individual Slide */
        .slide {
            min-width: 100vw;
            height: 100vh;
            scroll-snap-align: start;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 40px;
            box-sizing: border-box;
            position: relative;
        }
        .slide-content {
            background: white;
            padding: 50px;
            border-radius: 12px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            max-width: 900px;
            width: 100%;
            border-top: 6px solid var(--primary-blue);
        }
        /* Typography */
        h1 {
            color: var(--primary-blue);
            font-size: 2.5rem;
            margin-bottom: 10px;
        }
        h2 {
            color: var(--accent-orange);
            font-size: 1.8rem;
            margin-bottom: 20px;
            border-bottom: 2px solid #eee;
            padding-bottom: 10px;
        }
        h3 {
            color: var(--primary-blue);
            font-size: 1.3rem;
            margin-top: 25px;
        }
        p, li {
            font-size: 1.1rem;
            line-height: 1.6;
        }
        ul {
            margin-left: 20px;
        }
        /* Badges */
        .badge {
            display: inline-block;
            padding: 4px 10px;
            border-radius: 4px;
            font-size: 0.9rem;
            font-weight: bold;
            color: white;
            margin-left: 10px;
            vertical-align: middle;
        }
        .badge-match { background-color: #27ae60; }
        .badge-partner { background-color: #f39c12; }
        
        /* Navigation Arrows */
        .nav-hint {
            position: absolute;
            bottom: 30px;
            color: #888;
            font-size: 0.9rem;
            animation: bounce 2s infinite;
        }
        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% {transform: translateX(0);}
            40% {transform: translateX(10px);}
            60% {transform: translateX(5px);}
        }
        /* Cover Slide Specifics */
        .cover-slide {
            text-align: center;
            background: linear-gradient(135deg, var(--primary-blue) 0%, #002D52 100%);
        }
        .cover-slide .slide-content {
            background: transparent;
            box-shadow: none;
            border-top: none;
