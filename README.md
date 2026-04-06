# H.O.M.E.

An interactive virtual app for personal reflection and growth, inspired by bible study styles. Explore layers of conversation in a house metaphor.

## Features

- Navigate through rooms: Entry, Foundation, Blueprint, Structure, Vision, Sustainability
- Each room includes a scripture passage for reflection
- Save multiple reflections per room with AI-generated insights
- View previous reflections as expandable threads
- Export journal to Word or PDF
- Personal growth analysis based on all reflections

## Setup

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Create a `.env` file with your API keys:
   ```
   OPENAI_API_KEY=your_openai_key
   ```

3. Set up Snowflake database with table:
   ```sql
   CREATE TABLE HOME_REFLECTIONS (
       USER_ID VARCHAR,
       ROOM VARCHAR,
       REFLECTION TEXT,
       INSIGHT TEXT,
       TIMESTAMP TIMESTAMP
   );
   ```
   Update the connection details in `home_app.py`.

4. Run the app:
   ```bash
   streamlit run home_app.py
   ```

## Usage

- Enter your name in the sidebar
- Navigate through rooms using the selectbox or Next/Previous buttons
- Read the scripture and reflect
- Save your reflections and generate insights
- Explore previous reflections in each room 
