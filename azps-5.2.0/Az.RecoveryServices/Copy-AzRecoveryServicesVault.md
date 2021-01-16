---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: 68c2914c694dbfb89044597fc35582a83f426b6c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341582"
---
# Copy-AzRecoveryServicesVault

## SYNOPSIS
한 지역의 자격 증명 모음에서 다른 지역의 자격 증명 모음으로 데이터를 복사합니다.

## 구문

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## 설명
**Copy-AzRecoveryServicesVault** cmdlet은 한 지역의 자격 증명 모음에서 다른 지역의 자격 증명 모음으로 데이터를 복사합니다. 현재 자격 증명 모음 수준 데이터 이동만 지원됩니다.

## 예제

### 예제 1: vault1에서 vault2로 데이터 복사
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```

처음 두 cmdlet은 Recovery Services 자격 증명 모음(vault1 및 vault2)을 각각 페치합니다.
두 번째 명령은 vault1에서 vault2로 전체 데이터 이동을 트리거합니다. 

### 예제 2: 실패한 항목만 있는 vault1에서 vault2로 데이터 복사
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
``` 

처음 두 cmdlet은 Recovery Services 자격 증명 모음(vault1 및 vault2)을 각각 페치합니다.
두 번째 명령은 이전 이동 작업에서 실패한 항목만 사용하여 vault1에서 vault2로 부분 데이터 이동을 트리거합니다.

## PARAMETERS

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
대상 자격 증명 모음 저장소 중복 유형에 대한 확인을 요청하지 않고 데이터 이동 작업(확인 대화 상자 방지)을 강제합니다. 이 매개 변수는 선택 사항입니다. 

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetryOnlyFailed
매개 변수를 전환하여 아직 이동되지 않은 원본 자격 증명 모음의 컨테이너에 대한 데이터 이동만 시도합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceVault
이동할 원본 자격 증명 모음 개체입니다.

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TargetVault
데이터를 이동해야 하는 대상 자격 증명 모음 개체입니다.

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.Commands.RecoveryServices.ARSVault

## 출력

### System.String

## 참고 사항

## 관련 링크
