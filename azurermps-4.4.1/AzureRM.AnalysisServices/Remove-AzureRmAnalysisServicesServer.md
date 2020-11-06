---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Remove-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: fb55eec3dc0bf3cf83032251e017749a07970f2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525823"
---
# Remove-AzureRmAnalysisServicesServer

## SYNOPSIS
Analysis Services 서버 인스턴스 삭제

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Remove-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
Remove-AzureRmAnalysisServicesServer cmdlet은 Analysis Services 서버의 인스턴스를 삭제 합니다.

## 예제의

### 예제 1
```
PS C:\> Remove-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

이 명령은 resourcegroup testserver에서 testserver 라는 서버를 제거 합니다.

## 변수

### -이름
Analysis Services 서버의 이름입니다.

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

### -PassThru
작업이 성공적으로 완료 되 면 삭제 된 서버 세부 정보를 반환 합니다.

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

### -ResourceGroupName
서버가 속한 Azure 리소스 그룹의 이름

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
사용자에 게 작업 수행 여부 확인 메시지 표시

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
현재 작업이 실제로 수행 하지 않고 수행 하는 작업에 대해 설명 합니다.

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

## 출력

### AnalysisServices. AzureAnalysisServicesServer/.

## 상속자
별칭: Remove-AzureAs

## 관련 링크

[Get-AzureRmAnalysisServicesServer](./Get-AzureRmAnalysisServicesServer.md)

[새로운 AzureRmAnalysisServicesServer](./New-AzureRmAnalysisServicesServer.md)
