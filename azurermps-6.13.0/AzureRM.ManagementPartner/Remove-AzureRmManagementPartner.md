---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393045
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Remove-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Remove-AzureRmManagementPartner.md
ms.openlocfilehash: 3bb1b54abf947d5fc2a05538cc31ce53fb794ab7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535823"
---
# Remove-AzureRmManagementPartner

## SYNOPSIS
현재 인증 된 사용자 또는 서비스 주체의 MPN (Microsoft 파트너 네트워크) ID를 삭제 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Remove-AzureRmManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
현재 인증 된 사용자 또는 서비스 주체의 MPN (Microsoft 파트너 네트워크) ID를 삭제 합니다.

## 예제의

### 예제 1
```powershell
PS C:\>Remove-AzureRmManagementPartner -PartnerId 123457 -PassThru
true
```

관리 파트너 제거 

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

### -(또는)-(Id)
관리 파트너 id로 6 자리 숫자입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
{{Fill PassThru 설명}}

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### 시스템 부울

## 상속자

## 관련 링크

[새로운 AzureRmManagementPartner](./New-AzureRmManagementPartner.md)

[Get-AzureRmManagementPartner](./Get-AzureRmManagementPartner.md)

[업데이트-AzureRmManagementPartner](./Update-AzureRmManagementPartner.md)
