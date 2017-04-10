<template>
  <f7-page>
    <f7-navbar title="Bug Info" back-link="Back" sliding>
    <f7-nav-right>
      <f7-link icon-size="22">save</f7-link>
    </f7-nav-right>
    </f7-navbar>
    <f7-block-title>21630927 format report overridden </f7-block-title>
    <f7-list form>
      <f7-list-item>
        <f7-label>bugId</f7-label>
        <f7-input type="text" placeholder="Name"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-label>Filed</f7-label>
        <f7-input type="text" placeholder="demo"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-label>Assigned</f7-label>
        <f7-input type="text" placeholder="demo"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-label>Mail</f7-label>
        <f7-input type="email" placeholder="E-mail"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-label>Custom</f7-label>
        <f7-input type="text" placeholder="demo"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-label>Status</f7-label>
        <f7-input type="text" placeholder="demo"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-label>Fixed by</f7-label>
        <f7-input type="text" placeholder="demo"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-label>Introduced in</f7-label>
        <f7-input type="text" placeholder="demo"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-label>Component</f7-label>
        <f7-input type="text" placeholder="demo"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-label>Component</f7-label>
        <f7-input type="text" placeholder="demo"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-label>Component</f7-label>
        <f7-input type="text" placeholder="demo"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-label>Component</f7-label>
        <f7-input type="text" placeholder="demo"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-label>Component</f7-label>
        <f7-input type="text" placeholder="demo"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-label>Component</f7-label>
        <f7-input type="text" placeholder="demo"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-label>Component</f7-label>
        <f7-input type="text" placeholder="demo"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-label>URL</f7-label>
        <f7-input type="url" placeholder="URL"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-label>Phone</f7-label>
        <f7-input type="tel" placeholder="Phone"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-label>Birth date</f7-label>
        <f7-input type="date" placeholder="Birth date" value="2014-04-30"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-label>Date time</f7-label>
        <f7-input type="datetime-local"></f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-label>Gender</f7-label>
        <f7-input type="select">
          <option value="1">Male</option>
          <option value="1">Female</option>
        </f7-input>
      </f7-list-item>
      <f7-list-item>
        <f7-label>Textarea</f7-label>
        <f7-input type="textarea" placeholder="Textarea"></f7-input>
      </f7-list-item>
    </f7-list>

    <f7-block-title>Updates</f7-block-title>
    <f7-list form>
      <f7-list-item v-for="n in 3" checkbox name="my-checkbox" :value="n" :title="'Checkbox ' + n"></f7-list-item>
    </f7-list>

    <f7-block-title>Checkboxes</f7-block-title>
    <f7-list form>
      <f7-list-item v-for="n in 3" checkbox name="my-checkbox" :value="n" :title="'Checkbox ' + n"></f7-list-item>
    </f7-list>

    <f7-block-title>Radios</f7-block-title>
    <f7-list form>
      <f7-list-item v-for="n in 3" radio name="my-radio" :checked="n === 1" :value="n" :title="'Radio ' + n"></f7-list-item>
    </f7-list>
  </f7-page>
</template>

<script>
export default {}
</script>
