# User-stories_Test-cases_project2

https://openweathermap.org/our-initiatives


US_010.01 | Our Initiatives > Visibility, сlickability, correct redirection

As a User, I want to be aware of company’s initiatives, so that I can figure out whether I can use them to fulfill my needs.

Acceptance criteria:
Ensure the User able to:

open the Our initiatives page
click on links on the page
see the following sections: ‘Education’, ‘Healthcare', ‘Open source’ and ‘Weather stations'
to be directed to the correspong page by clicking on links in these sections
****************************************************************************************************
TC_010.01.01 | Our Initiatives > Visibility, сlickability, correct redirection > Section titles visibility

Precondition:
Page Our Initiatives is opened

Steps:

Verify the titles of the following sections: "Education", "Healthcare", "Open source" and "Weather stations" are displayed
Expected result:

The titles of the following sections: "Education", "Healthcare", "Open source" and "Weather stations" are displayed


******************************************************************************************************
TC_010.01.02 | Our Initiatives > Visibility, сlickability, correct redirection > Clickability > Link for registration is displayed and enabled

Page Our Initiatives is opened

Steps:

Verify that link "Learn more" is displayed and enabled
Expected result:

Verify that link "Learn more" is displayed and enabled

US_015.01 | Support > FAQ > Visibility, сlickability, correct links redirection and dropdown

As a User, I want to be able to visit "FAQ" page, so that I can find brief answers for my questions

Acceptance criteria:
Ensure the User able to:

Open the FAQ page
See the hidden text by clicking on related heading
Click on links and be directed to the corresponding pages
***************************************************************************************************
TC_010.01.03 | Our Initiatives > Visibility, сlickability, correct redirection > Correct redirection

Precondition:

Page https://openweathermap.org/our-initiatives  is opened

Steps:

Verify a link redirection

Expected result:

Link for redirection ("Learn more") works correctly
*****************************************************************************************************
US_014.01 | Sign in > Visibility

As a User I want to be able to see all the provided elements on the Sign in page for authorization or registration so that I can interact with them

Ensure the User able to:

see a "Sign In To Your Account" module title see the fields for entering a registered User data see possibility of activation the "Remember me" feature see a link for registration see a link for password recovery
*************************************************************************************************
TC_014.01.01 | Sign In > Visibility, structure > Verify of the Sign In form title display

Precondition:

Page https://home.openweathermap.org/users/sign_in  is opened

Steps:

Find the Sign In form on the page

Verify if the title "Sign In To Your Account" is displayed in the Sign In form

Expected result:

The Form title "Sign In To Your Account" is displayed

https://github.com/RedRoverSchool/OpenWeatherPython_06/pull/691

REGISTRATION_FORM_DISPLAY = (By.CSS_SELECTOR, ".sign-form")

    def check_registration_form_is_visible(self):
        registration_form = self.element_is_visible(self.locators.REGISTRATION_FORM_DISPLAY)
        assert registration_form.is_displayed(), "Sign In To Your Account is not visible"

    def test_tc_014_01_01_verify_registration_form_visibility(self, driver):
        page = SignInPage(driver, SignInUrls.url_sign_in_page)
        page.open_page()
        page.check_registration_form_is_visible()
***********************************************************************************************
TC_014.01.02 | Sign In > Visibility, structure > Verify of the Enter email field display
Precondition:

Page https://home.openweathermap.org/users/sign_in  is opened

Steps:

Find the Sign In form on the page

Verify if the Enter email field is displayed in the Sign In form

Expected result:

The field for entering "Enter email" is displayed


