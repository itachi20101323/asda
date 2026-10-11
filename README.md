.product-card {
  background: rgba(20, 20, 30, 0.6);
  backdrop-filter: blur(16px);
  border: 1px solid rgba(0, 240, 255, 0.1);
  border-radius: 16px;
  transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  position: relative;
  overflow: hidden;
  color: #fff;
}

.product-card:hover {
  transform: translateY(-10px) scale(1.03);
  border-color: #00f0ff;
  box-shadow: 0 15px 35px rgba(0, 240, 255, 0.2), 
              inset 0 0 20px rgba(0, 240, 255, 0.05);
}

/* Subtle Light Sweep Effect */
.product-card::before {
  content: '';
  position: absolute;
  top: 0; left: -100%;
  width: 50%; height: 100%;
  background: linear-gradient(to right, transparent, rgba(255,255,255,0.1), transparent);
  transform: skewX(-25deg);
  transition: all 0.7s ease;
}

.product-card:hover::before {
  left: 200%;
}
