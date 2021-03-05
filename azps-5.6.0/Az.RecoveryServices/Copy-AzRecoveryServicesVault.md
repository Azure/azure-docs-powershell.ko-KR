---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: 5b4c7153a844bdc10d2ec487e51ef9f07be0c5c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960256"
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

### 예제 1: Vault1에서 vault2로 데이터 복사
```
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```

처음 두 cmdlet은 Recovery Services Vault - 자격 증명 모음1 및 자격 증명 모음2를 각각 페치합니다.
두 번째 명령은 자격 증명 모음1에서 vault2로 전체 데이터 이동을 트리거합니다. 

### 예제 2: 실패한 항목만 사용하여 Vault1에서 vault2로 데이터 복사
```
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
```

처음 두 cmdlet은 Recovery Services Vault - 자격 증명 모음1 및 자격 증명 모음2를 각각 페치합니다.
두 번째 명령은 이전 이동 작업에서 실패한 항목만 사용하여 Vault1에서 vault2로 부분 데이터 이동을 트리거합니다.

## 매개 변수

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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
대상 자격 증명 모음 저장소 중복 유형에 대한 확인을 요청하지 않고 데이터 이동 작업(확인 대화 상자 방지)을 강제로 합니다. 이 매개 변수는 선택 사항입니다. 

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
매개 변수를 전환하여 아직 이동되지 않은 원본 자격 증명 모음의 컨테이너에만 데이터 이동을 시도합니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### Microsoft.Azure.Commands.RecoveryServices.ARSVault

## 출력

### System.String

## 참고 사항

## 관련 링크
