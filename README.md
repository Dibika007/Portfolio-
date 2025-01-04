# Portfolio-
Learning is the process it never ends 
from fpdf import FPDF

# Initialize the PDF
pdf = FPDF()
pdf.set_auto_page_break(auto=True, margin=15)
pdf.add_page()
pdf.set_font("Arial", size=12)

# Add Header
pdf.set_font("Arial", style="B", size=16)
pdf.set_text_color(33, 37, 41)
pdf.cell(0, 10, "DIBIKA P", ln=True, align="C")
pdf.set_font("Arial", size=12)
pdf.set_text_color(100, 100, 100)
pdf.cell(0, 10, "24b, Puthagaram, Kolathur, Chennai - 600099", ln=True, align="C")
pdf.cell(0, 10, "9791812652 | dibika007@gmail.com | LinkedIn: linkedin.com/in/dibika-p-7aaa32323", ln=True, align="C")
pdf.ln(10)

# Objective Section
pdf.set_font("Arial", style="B", size=14)
pdf.set_text_color(33, 37, 41)
pdf.cell(0, 10, "Professional Objective", ln=True)
pdf.ln(2)
pdf.set_font("Arial", size=12)
pdf.set_text_color(50, 50, 50)
objective = """Aspiring Electronics and Communication Engineer with a strong foundation in C programming, Python, 
and problem-solving. Passionate about contributing to innovative solutions in embedded systems, IoT, 
and signal processing. Seeking an opportunity to apply my technical knowledge and skills to solve real-world challenges."""
pdf.multi_cell(0, 10, objective)
pdf.ln(5)

# Education Section
pdf.set_font("Arial", style="B", size=14)
pdf.set_text_color(33, 37, 41)
pdf.cell(0, 10, "Education", ln=True)
pdf.ln(2)
pdf.set_font("Arial", size=12)
pdf.set_text_color(50, 50, 50)
education = [
    "Bachelor of Engineering (Electronics and Communication)",
    "Panimalar Engineering College (Expected Graduation: 2024)\n",
    "Higher Secondary Certificate (HSC)",
    "Jai Gopal Garodia Matriculation Higher Secondary School - Percentage: 84% (2022)\n",
    "Secondary School Leaving Certificate (SSLC)",
    "Don Bosco Matriculation Higher Secondary School - Percentage: 87.5% (2020)\n"
]
for line in education:
    pdf.cell(0, 10, line, ln=True)
pdf.ln(5)

# Technical Skills Section
pdf.set_font("Arial", style="B", size=14)
pdf.set_text_color(33, 37, 41)
pdf.cell(0, 10, "Technical Skills", ln=True)
pdf.ln(2)
pdf.set_font("Arial", size=12)
pdf.set_text_color(50, 50, 50)
skills = [
    "Programming Languages: C, Python",
    "Tools & Technologies: MATLAB, PCB Design (e.g., Eagle, KiCad), IoT platforms",
    "Core Concepts: Embedded Systems, Digital Signal Processing, VLSI Basics",
    "Soft Skills: Communication, Problem-Solving, Team Collaboration"
]
for skill in skills:
    pdf.cell(0, 10, f"- {skill}", ln=True)
pdf.ln(5)

# Projects Section
pdf.set_font("Arial", style="B", size=14)
pdf.set_text_color(33, 37, 41)
pdf.cell(0, 10, "Technical Projects", ln=True)
pdf.ln(2)
pdf.set_font("Arial", size=12)
pdf.set_text_color(50, 50, 50)
projects = [
    "Smart Home Automation using IoT",
    "  - Developed an IoT-based system to control home appliances via smartphone.",
    "  - Utilized Arduino, sensors, and NodeMCU for system integration.",
    "  - Improved energy efficiency by 20% through automated scheduling.\n",
    "Obstacle Avoidance Robot",
    "  - Designed and programmed an autonomous robot using ultrasonic sensors and Arduino.",
    "  - Implemented real-time obstacle detection algorithms for smooth navigation."
]
for project in projects:
    pdf.cell(0, 10, project, ln=True)
pdf.ln(5)

# Achievements Section
pdf.set_font("Arial", style="B", size=14)
pdf.set_text_color(33, 37, 41)
pdf.cell(0, 10, "Achievements & Awards", ln=True)
pdf.ln(2)
pdf.set_font("Arial", size=12)
pdf.set_text_color(50, 50, 50)
achievements = [
    "First Place in Chess Competition (2024) – Panimalar Engineering College",
    "Third Place in Elocution (2018) – Don Bosco Matriculation Higher Secondary School",
    "Third Place in Quiz Competition (2019) – Don Bosco Matriculation Higher Secondary School"
]
for achievement in achievements:
    pdf.cell(0, 10, f"- {achievement}", ln=True)
pdf.ln(5)

# Extracurricular Interests Section
pdf.set_font("Arial", style="B", size=14)
pdf.set_text_color(33, 37, 41)
pdf.cell(0, 10, "Extracurricular Interests", ln=True)
pdf.ln(2)
pdf.set_font("Arial", size=12)
pdf.set_text_color(50, 50, 50)
interests = [
    "Chess (National Level Player)",
    "Drawing and Digital Art",
    "Singing and Podcast Enthusiast"
]
for interest in interests:
    pdf.cell(0, 10, f"- {interest}", ln=True)
pdf.ln(5)

# Personal Details Section
pdf.set_font("Arial", style="B", size=14)
pdf.set_text_color(33, 37, 41)
pdf.cell(0, 10, "Personal Details", ln=True)
pdf.ln(2)
pdf.set_font("Arial", size=12)
pdf.set_text_color(50, 50, 50)
pdf.cell(0, 10, "Date of Birth: 02/06/2006", ln=True)

# Save the PDF
output_path = "/mnt/data/Dibika_P_Resume.pdf"
pdf.output(output_path)
output_path
