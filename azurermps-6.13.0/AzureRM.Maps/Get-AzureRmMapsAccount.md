---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/get-azurermmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccount.md
ms.openlocfilehash: 68ccff91f6e233862ba1ee5aa94a3a3d0d8422b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535815"
---
# Get-AzureRmMapsAccount

## SYNOPSIS
계정을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ResourceGroupParameterSet (기본값)
```
Get-AzureRmMapsAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### AccountNameParameterSet
```
Get-AzureRmMapsAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzureRmMapsAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
Get-AzureRmMapsAccount cmdlet은 리소스 그룹과 이름 또는 리소스 id를 기준으로 프로 비전 된 Azure Maps 계정을 가져옵니다. 또한이는 ResourceGroup의 모든 계정이 나 현재 구독에 대 한 모든 Azure Maps 계정 목록을 반환할 수 있습니다.

## 예제의

### 예제 1
```powershell
PS C:\> Get-AzureRmMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

리소스 그룹 MyResourceGroup에 내 계정 이라는 계정이 있는 경우 가져옵니다.

### 예제 2
```powershell
PS C:\> Get-AzureRmMapsAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

리소스 그룹 MyResourceGroup의 모든 Azure Maps 계정을 가져옵니다.

### 예제 3
```powershell
PS C:\> Get-AzureRmMapsAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

현재 구독의 모든 Azure Maps 계정을 가져옵니다.

### 예제 4
```powershell
PS C:\> Get-AzureRmMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

리소스 Id로 지정 된 지도 계정을 가져옵니다.

## 변수

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

### -이름
계정 이름을 매핑합니다.

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Maps 계정 ResourceId.

```yaml
Type: System.String
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

### Microsoft Azure. *. *. *.

## 상속자

## 관련 링크
