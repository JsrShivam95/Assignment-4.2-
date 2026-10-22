<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Job Application Form</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
    }

    body {
      background-color: #f1f5f9;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      padding: 40px 16px;
    }

    .form-card {
      background: #ffffff;
      padding: 36px 32px;
      border-radius: 12px;
      box-shadow: 0 4px 16px rgba(0, 0, 0, 0.08);
      max-width: 620px;
      width: 100%;
    }

    h2 {
      color: #0f172a;
      font-size: 24px;
      margin-bottom: 6px;
      text-align: center;
    }

    .subtitle {
      color: #64748b;
      font-size: 14px;
      text-align: center;
      margin-bottom: 28px;
    }

    .form-group {
      margin-bottom: 18px;
    }

    label.field-label {
      display: block;
      margin-bottom: 6px;
      font-size: 14px;
      font-weight: 600;
      color: #334155;
    }

    .required-star {
      color: #ef4444;
    }

    input[type="text"],
    input[type="email"],
    input[type="tel"],
    input[type="date"],
    input[type="url"],
    select,
    textarea {
      width: 100%;
      padding: 10px 14px;
      font-size: 15px;
      border: 1px solid #cbd5e1;
      border-radius: 6px;
      outline: none;
      background-color: #ffffff;
      color: #1e293b;
      transition: border-color 0.2s, box-shadow 0.2s;
    }

    input:focus,
    select:focus,
    textarea:focus {
      border-color: #2563eb;
      box-shadow: 0 0 0 3px rgba(37, 99, 235, 0.15);
    }

    input:disabled {
      background-color: #f1f5f9;
      color: #94a3b8;
      cursor: not-allowed;
      border-style: dashed;
    }

    .options-group {
      display: flex;
      flex-wrap: wrap;
      gap: 16px;
      margin-top: 6px;
    }

    .inline-option {
      display: flex;
      align-items: center;
      gap: 6px;
      font-size: 14px;
      color: #334155;
      cursor: pointer;
    }

    .inline-option input {
      cursor: pointer;
      width: 16px;
      height: 16px;
      accent-color: #2563eb;
    }

    textarea {
      resize: vertical;
      min-height: 110px;
    }

    .btn-submit {
      width: 100%;
      padding: 12px;
      background-color: #2563eb;
      color: #ffffff;
      border: none;
      border-radius: 6px;
      font-size: 16px;
      font-weight: 600;
      cursor: pointer;
      margin-top: 12px;
      transition: background-color 0.2s ease;
    }

    .btn-submit:hover {
      background-color: #1d4ed8;
    }
  </style>
</head>
<body>

  <div class="form-card">
    <h2>Job Application Form</h2>
    <p class="subtitle">Please complete the form below to apply for the position.</p>

    <form action="#" method="POST">

      <!-- Disabled Field Example -->
      <div class="form-group">
        <label for="appId" class="field-label">Application ID (Auto-Generated)</label>
        <input 
          type="text" 
          id="appId" 
          name="appId" 
          value="APP-2026-0941" 
          disabled
        >
      </div>

      <!-- 1. Full Name -->
      <div class="form-group">
        <label for="fullName" class="field-label">Full Name <span class="required-star">*</span></label>
        <input 
          type="text" 
          id="fullName" 
          name="fullName" 
          placeholder="e.g. John Doe" 
          required
        >
      </div>

      <!-- 1. Email -->
      <div class="form-group">
        <label for="email" class="field-label">Email Address <span class="required-star">*</span></label>
        <input 
          type="email" 
          id="email" 
          name="email" 
          placeholder="e.g. john.doe@example.com" 
          required
        >
      </div>

      <!-- 1. Phone -->
      <div class="form-group">
        <label for="phone" class="field-label">Phone Number <span class="required-star">*</span></label>
        <input 
          type="tel" 
          id="phone" 
          name="phone" 
          placeholder="e.g. +1 555-012-3456" 
          required
        >
      </div>

      <!-- 2. Date of Birth -->
      <div class="form-group">
        <label for="dob" class="field-label">Date of Birth <span class="required-star">*</span></label>
        <input 
          type="date" 
          id="dob" 
          name="dob" 
          required
        >
      </div>

      <!-- 3. Portfolio URL -->
      <div class="form-group">
        <label for="portfolioUrl" class="field-label">Portfolio URL <span class="required-star">*</span></label>
        <input 
          type="url" 
          id="portfolioUrl" 
          name="portfolioUrl" 
          placeholder="https://yourportfolio.com" 
          required
        >
      </div>

      <!-- 4. Radio Buttons (Preferred Shift) - All share name="preferredShift" -->
      <div class="form-group">
        <label class="field-label">Preferred Shift <span class="required-star">*</span></label>
        <div class="options-group">
          <label class="inline-option" for="shiftDay">
            <input type="radio" id="shiftDay" name="preferredShift" value="day" required>
            Day Shift
          </label>
          <label class="inline-option" for="shiftNight">
            <input type="radio" id="shiftNight" name="preferredShift" value="night">
            Night Shift
          </label>
          <label class="inline-option" for="shiftFlexible">
            <input type="radio" id="shiftFlexible" name="preferredShift" value="flexible">
            Flexible
          </label>
        </div>
      </div>

      <!-- 5. Checkboxes (Skills) -->
      <div class="form-group">
        <label class="field-label">Key Technical Skills</label>
        <div class="options-group">
          <label class="inline-option" for="skillHtml">
            <input type="checkbox" id="skillHtml" name="skills" value="html">
            HTML5
          </label>
          <label class="inline-option" for="skillCss">
            <input type="checkbox" id="skillCss" name="skills" value="css">
            CSS3
          </label>
          <label class="inline-option" for="skillJs">
            <input type="checkbox" id="skillJs" name="skills" value="javascript">
            JavaScript
          </label>
          <label class="inline-option" for="skillGit">
            <input type="checkbox" id="skillGit" name="skills" value="git">
            Git & GitHub
          </label>
        </div>
      </div>

      <!-- 6. Dropdown (Job Role) -->
      <div class="form-group">
        <label for="jobRole" class="field-label">Applying for Position <span class="required-star">*</span></label>
        <select id="jobRole" name="jobRole" required>
          <option value="" disabled selected>-- Select a Job Role --</option>
          <option value="frontend-dev">Frontend Developer</option>
          <option value="backend-dev">Backend Developer</option>
          <option value="fullstack-dev">Full Stack Developer</option>
          <option value="ui-ux-designer">UI/UX Designer</option>
          <option value="qa-engineer">QA Engineer</option>
        </select>
      </div>

      <!-- 7. Textarea (Cover Letter) -->
      <div class="form-group">
        <label for="coverLetter" class="field-label">Cover Letter <span class="required-star">*</span></label>
        <textarea 
          id="coverLetter" 
          name="coverLetter" 
          rows="4" 
          placeholder="Tell us why you are a great fit for this position..." 
          required
        ></textarea>
      </div>

      <!-- 8. Submit Button -->
      <button type="submit" class="btn-submit">Submit Application</button>

    </form>
  </div>

</body>
</html>

