<template>
    <DxForm :form-data="formData">
      <template #avatar-template="{}">
        <div class="form-avatar"/>
      </template>
      <DxGroupItem
        :col-count="4"
        css-class="form-group"
      >
        <DxSimpleItem template="avatar-template"/>
        <DxGroupItem :col-span="3">
          <DxSimpleItem data-field="FirstName"/>
          <DxSimpleItem data-field="LastName"/>
          <DxSimpleItem
            :editor-options="birthDateOptions"
            data-field="BirthDate"
            editor-type="dxDateBox"
          />
        </DxGroupItem>
      </DxGroupItem>
      <DxGroupItem
        :col-count="2"
        css-class="form-group"
      >
        <DxGroupItem>
          <DxSimpleItem data-field="Address"/>
          <DxSimpleItem data-field="City"/>
          <DxSimpleItem
            :editor-options="positionOptions"
            data-field="Position"
            editor-type="dxSelectBox"
          />
        </DxGroupItem>
        <DxGroupItem>
          <DxSimpleItem
            :editor-options="stateOptions"
            data-field="State"
            editor-type="dxSelectBox"
          />
          <DxSimpleItem data-field="ZipCode"/>
          <DxSimpleItem
            :editor-options="phoneOptions"
            data-field="Mobile"
          >
            <DxLabel text="Phone"/>
          </DxSimpleItem>
        </DxGroupItem>
        <DxSimpleItem
          :col-span="2"
          :editor-options="notesOptions"
          data-field="Notes"
          editor-type="dxTextArea"
        />
      </DxGroupItem>
    </DxForm>
  </template>
  <script setup>


  import {
    DxForm,
    DxSimpleItem,
    DxGroupItem,
    DxLabel,
  } from 'devextreme-vue/form';
import { DxButton, DxFileUploader, DxSelectBox, DxTextBox } from "devextreme-vue";
  import { DxTextArea } from 'devextreme-vue/text-area'; // needs for editor-type="dxTextArea"
  
   const employee = {
    ID: 1,
    FirstName: 'John',
    LastName: 'Heart',
    Position: 'CEO',
    BirthDate: '1964/03/16',
    HireDate: '1995/01/15',
    Notes: 'John has been in the Audio/Video industry since 1990. He has led DevAV as its CEO since 2003.\r\nWhen not working hard as the CEO, John loves to golf and bowl. He once bowled a perfect game of 300.',
    Address: '351 S Hill St.',
    City: 'Los Angeles',
    State: 'CA',
    ZipCode: '90013',
    Home: '555-684-1334',
    Mobile: '555-684-1335',
    Email: 'jheart@dx-email.com',
    Skype: 'jheart_DX_skype',
  };
  
   const positions = [
    'HR Manager',
    'IT Manager',
    'Controller',
    'CEO',
    'Sales Manager',
    'Support Manager',
    'Shipping Manager',
  ];
  
   const states = ['AL', 'AK', 'AZ', 'AR', 'CA', 'CO', 'CT', 'DE', 'FL', 'GA', 'HI', 'ID', 'IL', 'IN', 'IA', 'KS', 'KY', 'LA', 'ME', 'MD', 'MA', 'MI', 'MN', 'MS', 'MO', 'MT', 'NE', 'NV', 'NH', 'NJ', 'NM', 'NY', 'NC', 'ND', 'OH', 'OK', 'OR', 'PA', 'RI', 'SC', 'SD', 'TN', 'TX', 'UT', 'VT', 'VA', 'WA', 'WV', 'WI', 'WY'];
  

  const formData = employee;
  const birthDateOptions = { width: '100%' };
  const positionOptions = {
    items: positions,
    value: '',
  };
  const stateOptions = {
    items: states,
  };
  const phoneOptions = { mask: '+1 (000) 000-0000' };
  const notesOptions = { height: 140 };
  </script>
  <style>
  .form-group {
    padding: 20px;
  }
  
  .form-avatar {
    height: 128px;
    width: 128px;
    margin-right: 10px;
    border: 1px solid #d2d3d5;
    border-radius: 50%;
    background-size: contain;
    background-repeat: no-repeat;
    background-position: center;
  }
  </style>
  