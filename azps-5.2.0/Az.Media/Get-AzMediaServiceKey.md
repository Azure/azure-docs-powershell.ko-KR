---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
ms.openlocfilehash: a01aeaa5868ece4f376dd5be934ba1029379958b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372597"
---
# Get-AzMediaServiceKey

## SYNOPSIS
미디어 서비스에 연결된 REST 엔드포인트에 액세스하기 위한 주요 정보를 얻습니다.

## 구문

```
Get-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzMediaServiceKey** cmdlet은 Azure 미디어 서비스에 연결된 REST(Representational State Transfer) 엔드포인트에 액세스하기 위한 주요 정보를 얻습니다.

## 예제

### 예제 1: 미디어 서비스에 액세스하기 위한 주요 정보 얻기
```
PS C:\>Get-AzMediaServiceKey -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

이 명령은 ResourceGroup001이라는 리소스 그룹에 속하는 MediaService001이라는 미디어 서비스에 액세스하기 위한 주요 정보를 얻습니다.

## PARAMETERS

### -AccountName
이 cmdlet이 미디어 서비스 키를 받을 미디어 서비스의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
미디어 서비스를 포함하는 리소스 그룹의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.Media.Models.PSServiceKeys

## 참고 사항

## 관련 링크

[Set-AzMediaServiceKey](./Set-AzMediaServiceKey.md)


