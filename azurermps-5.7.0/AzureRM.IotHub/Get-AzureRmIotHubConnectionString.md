---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
ms.openlocfilehash: ef4ac5058c1ce85e19a9854bcd11fc2fac5ac69e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530505"
---
# Get-AzureRmIotHubConnectionString

## SYNOPSIS
IotHub connectionstrings를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
IotHub connectionstrings를 가져옵니다.
모든 키에 대해 connectionstrings를 가져오거나 특정 키 이름으로 필터링 할 수 있습니다.

## 예제의

### 예제 1 모든 IotHub connectionstrings 가져오기
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

"Myiothub" iothub의 모든 키에 대 한 connectionstrings를 가져옵니다.

### 예제 2 특정 키에 대 한 IotHub connectionstrings 가져오기
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

"Myiothub" 이라는 iothub에 대 한 "mykey" 키의 connectionstrings를 가져옵니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

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

### -KeyName
키 이름

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
IotHub의 이름입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름

```yaml
Type: String
Parameter Sets: (All)
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

### IotHub를 호출 합니다. Pssharedaccess서명 Authorizationrule
System.webserver. \` \[ \[ IotHub는 1. IotHub, Version = 1.0.0.0, Culture = 중립, PublicKeyToken = l a n,이에 해당 하는. m a.\]\]

## 상속자

## 관련 링크

