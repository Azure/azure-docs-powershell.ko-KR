---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/copy-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Copy-AzRecoveryServicesVault.md
ms.openlocfilehash: 630dc1a3a14beec147dec3f7bd2601ed0666ad78
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056104"
---
# Copy-AzRecoveryServicesVault

## SYNOPSIS
한 영역의 보관소에서 다른 지역의 보관소로 데이터를 복사 합니다.

## 구문과

```
Copy-AzRecoveryServicesVault [-Force] [-DefaultProfile <IAzureContextContainer>] [-SourceVault] <ARSVault>
 [-TargetVault] <ARSVault> [-RetryOnlyFailed] [<CommonParameters>]
```

## 설명은
**AzRecoveryServicesVault** cmdlet은 한 영역의 자격 증명 모음에서 다른 지역의 자격 증명 모음으로 데이터를 복사 합니다. 현재는 볼트 수준 데이터 이동만 지원 합니다.

## 예제의

### 예제 1: vault1에서 vault2로 데이터 복사
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault
```git 

The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.
The second command triggers a complete data move from vault1 to vault2. 

### Example 2: Copy data from vault1 to vault2 with only failed items
```powershell
PS C:\> $sourceVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName1" -Name "vault1"
PS C:\> $targetVault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName2" -Name "vault2"
PS C:\> Copy-AzRecoveryServicesVault -SourceVault $sourceVault -TargetVault $targetVault -RetryOnlyFailed
```git 

The first two cmdlets fetch Recovery Services Vault - vault1 and vault2 respectively.
The second command triggers a partial data move from vault1 to vault2 with only those items which failed in previous move operations.

## PARAMETERS

### -DefaultProfile
The credentials, account, tenant, and subscription used for communication with Azure.

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
대상 자격 증명 저장소 중복 유형에 대 한 확인 메시지를 표시 하지 않고 데이터 이동 작업 (확인 대화 상자 방지)을 강제 합니다. 이 매개 변수는 선택 사항입니다. 

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
스위치 매개 변수를 사용 하 여 아직 이동 하지 않은 원본 보관소의 컨테이너에 대해서만 데이터 이동을 시도 합니다.

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
데이터를 이동 해야 하는 대상 보관소 개체입니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### ARSVault를 통한 명령

## 출력

### System. 문자열

## 상속자

## 관련 링크
