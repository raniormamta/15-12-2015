# 15-12-2015



ALTER DATABASE DATAFILE 'C:\oraclexe\oradata\XE\SYSTEM.DBF'
AUTOEXTEND ON NEXT 1M MAXSIZE 1024M;

-----------------------------------------------------------


ALTER DATABASE DATAFILE 'C:\oraclexe\oradata\XE\SYSTEM.DBF'
AUTOEXTEND ON NEXT 2M MAXSIZE 2024M;

sqlplus /  as sysdba

shutdown immediate

startup

CREATE TABLE M_App(APID number NOT NULL, action varchar(5), id number, ref varchar(30), aValidate varchar(10) DEFAULT 'Yes', aspiration varchar(100), aspirationId number, assetAction varchar(10),  assetId number, assetRef varchar(10), assetValidate varchar(10) DEFAULT 'Yes', assetItemOrder number, assetItemRef varchar(10), assetItemName varchar(50), baseVehicle varchar(100), baseVehicleId number, bedLengthId number, bedTypeId number, bodyNumDoorsId number, bodyTypeId number, brakeABSId number, brakeSystemId number, cylinderHeadTypeId number, displayOrder number, driveTypeId number, engineBase varchar(50), engineBaseId number, engineDesignation varchar(100), engineDesignationId number, engineMfrId number, engineVersion varchar(50), engineVersionId number, engineVIN varchar(50), engineVINId number, frontBrakeTypeId number, frontSpringTypeId number, fuelDeliverySubTypeId number, fuelDeliveryTypeId number, fuelSystemControlTypeId number, fuelSystemDesignId number, fuelTypeId number, ignitionSystemTypeId number, makeId number, mfrLabel varchar(30), mfrBodyCodeId number, modelId number, note varchar(4000), noteId number, noteLang varchar(10), part varchar(30), partBrandAAIAId varchar(30), partType varchar(100), partTypeId number, position varchar(50), positionId number, powerOutputId number, qualId number, qParamUom varchar(20), qParamValue varchar(50), qParamAltValue varchar(20), qParamAltUom varchar(50), qPText varchar(20), qty number, rearBrakeTypeId number, rearSpringTypeId number, regionId number, steeringTypeId number, steeringSystemId number, subModel varchar(100), subModelId number, transElecContolledId number, transmissionMfrId number, transmissionMfrCodeId number, transmissionBaseId number, transmissionControlTypeId number, transmissionNumSpeedsId number, transmissionTypeId number, valvesPerEngineId number, vehicleTypeId number, wheelBaseId number, yearsFrom varchar(10), yearsTo varchar(10), version varchar(20), headerId number, footerId number, PRIMARY KEY (APID));

CREATE SEQUENCE app_sequence INCREMENT BY 1 START WITH 1 NOMAXVALUE NOCYCLE NOCACHE;

INSERT INTO App(APID, action, id, ref, aValidate, aspiration, aspirationId , assetAction, assetId, assetRef, assetValidate, assetItemOrder, assetItemRef, assetItemName, baseVehicle, baseVehicleId, bedLengthId, bedTypeId, bodyNumDoorsId, bodyTypeId, brakeABSId, brakeSystemId, cylinderHeadTypeId, displayOrder, driveTypeId, engineBase, engineBaseId, engineDesignation, engineDesignationId, engineMfrId, engineVersion, engineVersionId, engineVIN, engineVINId, frontBrakeTypeId, frontSpringTypeId, fuelDeliverySubTypeId, fuelDeliveryTypeId, fuelSystemControlTypeId, fuelSystemDesignId, fuelTypeId, ignitionSystemTypeId, makeId, mfrLabel, mfrBodyCodeId, modelId, note, noteId, noteLang, part, partBrandAAIAId, partType, partTypeId, position, positionId, powerOutputId, qualId, qParamUom, qParamValue, qParamAltValue, qParamAltUom, qPText, qty, rearBrakeTypeId, rearSpringTypeId, regionId, steeringTypeId, steeringSystemId, subModel, subModelId, transElecContolledId, transmissionMfrId, transmissionMfrCodeId, transmissionBaseId, transmissionControlTypeId, transmissionNumSpeedsId, transmissionTypeId, valvesPerEngineId, vehicleTypeId, wheelBaseId, yearsFrom, yearsTo, version, headerId, footerId) VALUES (app_sequence.NEXTVAL, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?);

SELECT action, id, ref, aValidate, aspiration, aspirationId , assetAction, assetId, assetRef, assetValidate, assetItemOrder, assetItemRef, assetItemName, baseVehicle, baseVehicleId, bedLengthId, bedTypeId, bodyNumDoorsId, bodyTypeId, brakeABSId, brakeSystemId, cylinderHeadTypeId, displayOrder, driveTypeId, engineBase, engineBaseId, engineDesignation, engineDesignationId, engineMfrId, engineVersion, engineVersionId, engineVIN, engineVINId, frontBrakeTypeId, frontSpringTypeId, fuelDeliverySubTypeId, fuelDeliveryTypeId, fuelSystemControlTypeId, fuelSystemDesignId, fuelTypeId, ignitionSystemTypeId, makeId, mfrLabel, mfrBodyCodeId, modelId, note, noteId, noteLang, part, partBrandAAIAId, partType, partTypeId, position, positionId, powerOutputId, qualId, qParamUom, qParamValue, qParamAltValue, qParamAltUom, qPText, qty, rearBrakeTypeId, rearSpringTypeId, regionId, steeringTypeId, steeringSystemId, subModel, subModelId, transElecContolledId, transmissionMfrId, transmissionMfrCodeId, transmissionBaseId, transmissionControlTypeId, transmissionNumSpeedsId, transmissionTypeId, valvesPerEngineId, vehicleTypeId, wheelBaseId, yearsFrom, yearsTo, version From M_App where ;
		


CREATE TABLE M_Header(HID Number NOT NULL, approvedFor varchar(10), brandAIAID varchar(10), company varchar(30), docFormNumber varchar(10), documentTitle varchar(30), effectiveDate varchar(30),  mapperCompany varchar(50), mapperContact varchar(30), mapperEmail varchar(30), mapperPhone varchar(20), mapperPhoneExt varchar(10), pcdbVersionDate varchar(30), qdbVersionDate varchar(30), senderName varchar(30), senderPhone varchar(20), senderPhoneExt varchar(10), submissionType varchar(10), transferDate varchar(30), vcdbVersionDate varchar(30), PRIMARY KEY (HID)); 

CREATE SEQUENCE header_sequence INCREMENT BY 1 START WITH 1 NOMAXVALUE NOCYCLE NOCACHE;

INSERT INTO Header(HId, approvedFor, brandAIAID, company, docFormNumber, documentTitle, effectiveDate, mapperCompany, mapperContact, mapperEmail, mapperPhone, mapperPhoneExt, pcdbVersionDate, qdbVersionDate, senderName, senderPhone, senderPhoneExt, submissionType, transferDate, vcdbVersionDate) VALUES (hdr_sequence.NEXTVAL, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?)";

CREATE TABLE M_Footer(FID Number NOT NULL, R_COUNT Number, PRIMARY KEY (fID));

CREATE SEQUENCE footer_sequence INCREMENT BY 1 START WITH 1 NOMAXVALUE NOCYCLE NOCACHE;

INSERT INTO Footer (FId,R_Count) VALUES (footer_sequence.NEXTVAL,?)


drop table app;
drop table footer;
drop table header;

select count(*) from App;
select count(*) from Footer;
select count(*) from Header;

CREATE TABLE App(APID number NOT NULL, action varchar(50), id number, ref varchar(300), aValidate varchar(50) DEFAULT 'Yes', aspiration varchar(200), aspirationId number, assetAction varchar(50),  assetId 
number, assetRef varchar(300), assetValidate varchar(50) DEFAULT 'Yes', assetItemOrder number, assetItemRef varchar(300), assetItemName varchar(350), baseVehicle varchar(300), baseVehicleId number, bedLengthId 
number, bedTypeId number, bodyNumDoorsId number, bodyTypeId number, brakeABSId number, brakeSystemId number, cylinderHeadTypeId number, displayOrder number, driveTypeId number, engineBase varchar(350), 
engineBaseId number, engineDesignation varchar(300), engineDesignationId number, engineMfrId number, engineVersion varchar(300), engineVersionId number, engineVIN varchar(300), engineVINId number, 
frontBrakeTypeId number, frontSpringTypeId number, fuelDeliverySubTypeId number, fuelDeliveryTypeId number, fuelSystemControlTypeId number, fuelSystemDesignId number, fuelTypeId number, ignitionSystemTypeId 
number, makeId number, mfrLabel varchar(300), mfrBodyCodeId number, modelId number, note varchar(4000), noteId number, noteLang varchar(100), part varchar(300), partBrandAAIAId varchar(300), partType varchar
(300), partTypeId number, position varchar(100), positionId number, powerOutputId number, qualId number, qParamUom varchar(100), qParamValue varchar(100), qParamAltValue varchar(100), qParamAltUom varchar(100), 
qPText varchar(300), qty number, rearBrakeTypeId number, rearSpringTypeId number, regionId number, steeringTypeId number, steeringSystemId number, subModel varchar(300), subModelId number, 
transElecContolledId number, transmissionMfrId number, transmissionMfrCodeId number, transmissionBaseId number, transmissionControlTypeId number, transmissionNumSpeedsId number, transmissionTypeId number, 
valvesPerEngineId number, vehicleTypeId number, wheelBaseId number, yearsFrom varchar(100), yearsTo varchar(100), driveType varchar(300), headerId number, footerId number, PRIMARY KEY (APID));

CREATE TABLE Header(HID Number NOT NULL, approvedFor varchar(10), brandAIAID varchar(10), company varchar(30), docFormNumber varchar(10), documentTitle varchar(30), effectiveDate varchar(30),  
mapperCompany varchar(50), mapperContact varchar(30), mapperEmail varchar(30), mapperPhone varchar(20), mapperPhoneExt varchar(10), pcdbVersionDate varchar(30), qdbVersionDate varchar(30), senderName 
varchar(30), senderPhone varchar(20), senderPhoneExt varchar(10), submissionType varchar(10), transferDate varchar(30), vcdbVersionDate varchar(30), PRIMARY KEY (HID)); 

CREATE TABLE Footer(FID Number NOT NULL, R_COUNT Number, PRIMARY KEY (fID));

truncate table App;
truncate table Header;
truncate table Footer;


CREATE SEQUENCE app_sequence INCREMENT BY 1 START WITH 1 NOMAXVALUE NOCYCLE NOCACHE;
CREATE SEQUENCE header_sequence INCREMENT BY 1 START WITH 1 NOMAXVALUE NOCYCLE NOCACHE;
CREATE SEQUENCE footer_sequence INCREMENT BY 1 START WITH 1 NOMAXVALUE NOCYCLE NOCACHE;

drop sequence header_sequence;
drop sequence footer_sequence;
drop sequence app_sequence;











