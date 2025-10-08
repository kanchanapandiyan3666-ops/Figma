# Ex09 Event Registration Web Application
## Date:8.10.25

## AIM:
To design, develop and deploy a web application for event registration.

## DESIGN STEPS:

### Step 1:
Create a new frame.

### Step 2:
Select any one preset size of your choice.

### Step 3:
Select the shapes you need.

### Step 4:
Import images as needed.

### Step 5:
Create pages based on your need and link them.

### Step 6:

Validate the HTML and CSS code.

### Step 6:

Publish the website in the given URL.

## DESIGN TOOL:
Figma

## CODE:
~~~
import tkinter as tk
from tkinter import messagebox

# --- Functions ---
def open_events():
    home_frame.pack_forget()
    events_frame.pack()

def open_form():
    events_frame.pack_forget()
    form_frame.pack()

def submit_form():
    name = entry_name.get()
    age = entry_age.get()
    dept = entry_dept.get()
    event = entry_event.get()

    if not name or not age or not dept or not event:
        messagebox.showwarning("Warning", "Please fill all fields!")
    else:
        form_frame.pack_forget()
        thankyou_frame.pack()

def back_to_home():
    thankyou_frame.pack_forget()
    home_frame.pack()

# --- Main Window ---
root = tk.Tk()
root.title("Sports Day Registration")
root.geometry("400x500")
root.config(bg="#e3f2fd")

# --- Frame 1: Home ---
home_frame = tk.Frame(root, bg="#ffc1e3")
tk.Label(home_frame, text="SAVETHA ENGINEERING COLLEGE", font=("Arial", 12, "bold"), bg="#ffc1e3").pack(pady=20)
tk.Label(home_frame, text="SPORTS DAY 2025", font=("Arial", 16, "bold"), bg="#ffc1e3").pack(pady=10)
tk.Button(home_frame, text="REGISTER", font=("Arial", 14), bg="red", fg="white", command=open_events).pack(pady=20)
home_frame.pack(fill="both", expand=True)

# --- Frame 2: Events ---
events_frame = tk.Frame(root, bg="#d1c4e9")
tk.Label(events_frame, text="SPORTS DAY EVENTS", font=("Arial", 16, "bold"), bg="#d1c4e9").pack(pady=10)
events = ["Cricket", "Badminton", "Volleyball", "100 mts", "200 mts", "400 mts", "4x100 Relay"]
for e in events:
    tk.Label(events_frame, text=e, font=("Arial", 12), bg="#d1c4e9").pack()
tk.Button(events_frame, text="NEXT", bg="red", fg="white", font=("Arial", 12), command=open_form).pack(pady=20)

# --- Frame 3: Form ---
form_frame = tk.Frame(root, bg="#bbdefb")
tk.Label(form_frame, text="EVENT REGISTRATION FORM", font=("Arial", 14, "bold"), bg="#bbdefb").pack(pady=10)

tk.Label(form_frame, text="Full Name:", bg="#bbdefb").pack()
entry_name = tk.Entry(form_frame)
entry_name.pack()

tk.Label(form_frame, text="Age:", bg="#bbdefb").pack()
entry_age = tk.Entry(form_frame)
entry_age.pack()

tk.Label(form_frame, text="Department:", bg="#bbdefb").pack()
entry_dept = tk.Entry(form_frame)
entry_dept.pack()

tk.Label(form_frame, text="Event to Register:", bg="#bbdefb").pack()
entry_event = tk.Entry(form_frame)
entry_event.pack()

tk.Button(form_frame, text="SUBMIT", bg="red", fg="white", font=("Arial", 12), command=submit_form).pack(pady=15)

# --- Frame 4: Thank You ---
thankyou_frame = tk.Frame(root, bg="#c8e6c9")
tk.Label(thankyou_frame, text="THANK YOU!", font=("Arial", 18, "bold"), bg="#c8e6c9").pack(pady=20)
tk.Label(thankyou_frame, text="We are eagerly waiting for your participation!", bg="#c8e6c9", font=("Arial", 12)).pack(pady=10)
tk.Button(thankyou_frame, text="BACK TO HOME", bg="red", fg="white", command=back_to_home).pack(pady=20)

root.mainloop()

~~~

## OUTPUT:

![alt text](<Screenshot 2025-10-08 132522.png>)


## RESULT:
The program to design, develop and deploy a web application for event registration is completed successfully.
