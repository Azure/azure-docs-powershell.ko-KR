---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubcertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificateVerificationCode.md
ms.openlocfilehash: a2c4c72f93597f3275e9edb1fecb6139eafbeb50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535900"
---
# Get-AzureRmIotHubCertificateVerificationCode

## SYNOPSIS
Azure IoT Hub 인증서에 대 한 확인 코드를 생성 합니다. 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ResourceSet (기본값)
```
Get-AzureRmIotHubCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObjectSet
```
Get-AzureRmIotHubCertificateVerificationCode [-InputObject] <PSCertificateDescription>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdSet
```
Get-AzureRmIotHubCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
이 확인 코드는 인증서에 대 한 소유 단계 증명을 완료 하는 데 사용 됩니다. 이 확인 코드를 루트 인증서 개인 키를 사용 하 여 서명 된 새 인증서의 CN으로 사용 합니다.
Azure IoT Hub의 CA 인증서에 대 한 자세한 설명은 다음을 참조 하세요. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview

## 예제의

### 예제 1
```
PS C:\> Get-AzureRmIotHubCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
VerificationCode    : 47292AB6260DB02CCD2D07C601B7303DD49858B6
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

MyCertificate에 대 한 확인 코드를 생성 합니다. 

## 변수

### -CertificateName
인증서 이름

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Etag
인증서의 Etag

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
인증서 개체

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -이름
Iot Hub의 이름

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름입니다.

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
인증서 리소스 Id

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### IotHub. PSCertificateDescription/. *
매개 변수: InputObject (ByValue)

### System. 문자열

## 출력

### IotHub. PSCertificateWithNonceDescription/. *

## 상속자

## 관련 링크
