---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 9a9fbf8c25eba6206b3852476b5a72a2f96be423
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340682"
---
# Remove-AzRecoveryServicesAsrServicesProvider

## SYNOPSIS
복구 서비스 자격 증명 모음에서 지정된 Azure Site Recovery 복구 서비스 공급자를 삭제/등록을 등록하지 않습니다.

## 구문

```
Remove-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Remove-AzRecoveryServicesAsrServicesProvider** cmdlet은 자격 증명 모음에서 지정된 Azure Site Recovery 복구 서비스 공급자를 제거합니다.

## 예제

### 예제 1
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

지정된 Azure Site Recovery 서비스 공급자의 지우기/등록을 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.

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

### -Force
추가 경고를 제공하지 않고 명령을 강제로 실행합니다.

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

### -InputObject
cmdlet에 대한 입력 개체: 삭제할 ASR 복구 서비스 공급자에 해당하는 ASR 복구 서비스 공급자 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm
확인이 필요한지 지정합니다. 확인을 건너뛰기 위해 confirm 매개 $false 값으로 설정합니다.

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
cmdlet을 실제로 실행하지 않고 cmdlet을 실행하면 어떤 일이 일어나는지 보여줍니다.

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

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider

## 출력

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob

## 참고 사항

## 관련 링크

[Get-AzRecoveryServicesAsrServicesProvider](./Get-AzRecoveryServicesAsrServicesProvider.md)

[Update-AzRecoveryServicesAsrServicesProvider](./Update-AzRecoveryServicesAsrServicesProvider.md)
