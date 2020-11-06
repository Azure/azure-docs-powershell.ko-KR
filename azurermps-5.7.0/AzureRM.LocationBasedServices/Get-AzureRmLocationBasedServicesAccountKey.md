---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/get-azurermlocationbasedservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccountKey.md
ms.openlocfilehash: 1f528bb0a80f039b9a2be7cb4cb6e4c7fbc740c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536772"
---
# Get-AzureRmLocationBasedServicesAccountKey

## SYNOPSIS
계정에 대 한 API 키를 가져옵니다. 이러한 키는 Azure 위치 기반 서비스에 대 한 후속 호출에 사용 되는 인증 메커니즘입니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### NameParameterSet (기본값)
```
Get-AzureRmLocationBasedServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObjectParameterSet
```
Get-AzureRmLocationBasedServicesAccountKey [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzureRmLocationBasedServicesAccountKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzureRmLocationBasedServicesAccountKey** cmdlet은 프로 비전 된 위치 기반 서비스 계정에 대 한 API 키를 가져옵니다.

위치 기반 서비스 계정에는 기본 및 보조의 두 가지 API 키가 있습니다.
키를 사용 하 여 위치 기반 서비스 계정 끝점과 상호 작용할 수 있습니다.

[New-AzureRmLocationBasedServicesAccountKey](New-AzureRmLocationBasedServicesAccountKey.md) 를 사용 하 여 키를 다시 생성 합니다.

## 예제의

### 예제 1
```
PS C:\> Get-AzureRmLocationBasedServicesAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

리소스 그룹 MyResourceGroup의 내 계정 이라는 계정에 대 한 키를 반환 합니다.

### 예제 2
```
PS C:\> Get-AzureRmLocationBasedServicesAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

PrimaryKey                                  SecondaryKey
----------                                  ------------
******************************************* *******************************************
```

지정 된 위치 기반 서비스 계정에 대 한 키를 반환 합니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Location 기반 서비스 계정이 [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md)에서 파이프 합니다.

```yaml
Type: PSLocationBasedServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -이름
위치 기반 서비스 계정 이름입니다.

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
위치 기반 서비스 계정 ResourceId.
```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
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

### System. 문자열

## 출력

### LocationBasedServices. PSLocationBasedServicesAccountKeys/.

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 상속자

## 관련 링크
