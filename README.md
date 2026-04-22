import streamlit as st
import pandas as pd
import numpy as np
from survey_module import create_survey_form
from risk_predictor import predict_risk
from gdpr_checker import check_gdpr_compliance

# Thiết lập trang Streamlit
st.set_page_config(
    page_title="AI Ethical Guardian",
    page_icon="🛡️",
    layout="wide"
)

# Tiêu đề chính
st.title("🛡️ AI Ethical Guardian")
st.markdown("### Đánh giá rủi ro đạo đức và an ninh của các ứng dụng AI")

# Menu chính
menu = st.sidebar.radio(
    "📌 Chọn chức năng:",
    ["🏠 Trang chủ", "📋 Khảo sát", "📊 Dự báo rủi ro", "✅ Kiểm định GDPR"]
)

# Trang chủ
if menu == "🏠 Trang chủ":
    st.markdown("""
    ## 👋 Chào mừng đến AI Ethical Guardian!
    
    Dự án này giúp bạn:
    - 📋 **Khảo sát người dùng** về nhận thức rủi ro AI
    - 📊 **Dự báo rủi ro** sử dụng mô hình hồi quy tuyến tính
    - ✅ **Kiểm định GDPR** để đảm bảo tuân thủ quy định bảo vệ dữ liệu
    
    ### 📐 Cơ sở toán học
    
    **Hồi quy tuyến tính:** y = mx + b
    
    **Sai số tuyệt đối:** Δx = |x - a|
    
    Hãy bắt đầu từ menu bên trái! 🚀
    """)

# Khảo sát người dùng
elif menu == "📋 Khảo sát":
    st.header("📋 Khảo Sát Người Dùng")
    create_survey_form()

# Dự báo rủi ro
elif menu == "📊 Dự báo rủi ro":
    st.header("📊 Dự Báo Rủi Ro")
    predict_risk()

# Kiểm định GDPR
elif menu == "✅ Kiểm định GDPR":
    st.header("✅ Kiểm Định Tuân Thủ GDPR")
    check_gdpr_compliance()

# Footer
st.markdown("---")
st.markdown("""
<div align="center">
    <p>🛡️ <b>AI Ethical Guardian</b> - Bảo vệ đạo đức trong thế giới AI</p>
    <p>👤 Tác giả: <b>Phạm Đình Gia Khánh (9A6)</b></p>
</div>
""", unsafe_allow_html=True)
