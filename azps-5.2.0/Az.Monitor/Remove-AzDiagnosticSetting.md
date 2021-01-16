---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
ms.openlocfilehash: f165396d5b3af823d91e7c06d2f1cb93eb2eaafd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328558"
---
# Remove-AzDiagnosticSetting

## SYNOPSIS
리소스에 대한 진단 설정을 제거합니다.

## 구문

```
Remove-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Remove-AzDiagnosticSetting** cmdlet은 특정 리소스에 대한 진단 설정을 제거합니다.
이 cmdlet은 ShouldProcess 패턴을 구현합니다. 즉, 리소스를 실제로 만들거나 수정하거나 제거하기 전에 사용자로부터 확인을 요청할 수 있습니다.

## 예제

### 예제 1: 리소스에 대한 기본 진단 설정(서비스) 제거
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01"
```

이 명령은 Resource01이라는 리소스에 대한 기본 진단 설정(서비스)을 제거합니다.

### 예제 2: 리소스에 대해 지정한 이름으로 식별된 기본 진단 설정 제거
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01" -Name myDiagSetting
```

이 명령은 Resource01이라는 리소스에 대한 myDiagSetting이라는 진단 설정을 제거합니다.

## PARAMETERS

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -Name
진단 설정의 이름입니다. 호출 기본값을 이전 API와 동일하게 지정하지 않은 경우 이 cmdlet은 메트릭/로그에 대한 모든 범주만 비활성화합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
리소스의 ID를 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우의 결과 표시 cmdlet이 실행되지 않습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

## 출력

### Microsoft.Azure.AzureOperationResponse

## 참고 사항

## 관련 링크

[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)
