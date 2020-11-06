---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHub.md
ms.openlocfilehash: 890180c024a004652406e04530a7e3291def13ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537156"
---
# Get-AzureRmIotHub

## SYNOPSIS
구독에서 IotHubs에 대 한 정보를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ListIotHubsByResourceGroup (기본값)
```
Get-AzureRmIotHub [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetIotHubByName
```
Get-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
구독에서 IotHubs에 대 한 정보를 가져옵니다.
구독에서 모든 IotHub 인스턴스를 보거나 리소스 그룹 또는 특정 IotHub 이름을 기준으로 결과를 필터링 할 수 있습니다.

## 예제의

### 예제 1
```
PS C:\> Get-AzureRmIotHub
```

구독에 있는 모든 IotHubs를 가져옵니다.

### 예제 2
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup"
```

"Myresourcegroup" 이라는 리소스 이름에 속하는 구독의 모든 IotHubs를 가져옵니다.

### 예제 3
```
PS C:\> Get-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

이름이 "myiothub" 인 IotHub에 대 한 정보를 가져옵니다.

## 변수

### -이름
IotHub의 이름입니다.

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
ResourceGroup의 이름입니다.

```yaml
Type: System.String
Parameter Sets: ListIotHubsByResourceGroup
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotHubByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### IotHub. PSIotHub/. *
\` \[ \[ PSIotHub, IotHub, Version = 1.0.0.0, Culture = 중립, PublicKeyToken = Null 인 경우 목록 1에 있는. a. i a.\]\]

## 상속자

## 관련 링크

