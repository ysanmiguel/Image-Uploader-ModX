# Image-Uploader-ModX
Upload, crop, resize image from the front end and save it in it's own user folder.

<p>This snippet form ModX Revolution based on a ModX forum post https://forums.modx.com/thread/?thread=47603<br>
Rigth now it's being used with the **Registratio/UpdateProfile** forms to upload the profile image.</p>
  
<p>Modified to Resize, Crop the uploaded image and move it into a folder created based on the profile "username" if the user is already registered or in the "username" input field if the user is going to register for first time.</p>


INSTRUCTIONS
Before start it's necessary that you have the **pThumb** ModX extra already installed.

1. Include the upload file input in your **Registratio/UpdateProfile** forms:
```
<input class="custom-file-input " id="photo" type="file" name="photo" accept=".jpg, .jpeg, .png" value="">
```
2. Create a snippet called "imageUpload" include the code on the file **imageUpload.snippet**
3. Include the snippet as preHook in your FormIt, Login/Registration or Login/UpdateProfile snippet calls:
```
&preHooks=`imageUpload`
```
4. The new file will be saved in **/assets/web/userfiles/~USERNAME~/**<br>
and saved in the **User Photo** field inside the user profile in the **Users** area in the manager.
5. To display the image path just use the placeholder [[+photo]]
6. use the snippet [[!Profile]] in the same page in case the [[+photo]] placeholder is not retreaving the image path.
6. Done!
---

Enjoy it!
