---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 95FF3F7A-5CC6-4AA6-A393-5EBB5579D9A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
ms.openlocfilehash: 18383ffeb35b1ce6bb2651be041e07b6164e55da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711210"
---
# Get-AzureRmBackupVault

## SYNOPSIS
백업 자격 증명 모음을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmBackupVault [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**Get-AzureRmBackupVault** Cmdlet은 Azure Backup 자격 증명 모음을 가져옵니다.
이 cmdlet은 다른 cmdlet에 사용할 **AzureRmBackupVault** 개체를 반환 합니다.

## 예제의

### 예제 1: 모든 백업 자격 증명 모음 보기
```
PS C:\>Get-AzureRmBackupVault
```

이 명령은 모든 Azure Backup 자격 증명 모음을 가져옵니다.

### 예제 2: 미국에서 만든 모든 볼트 보기
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Region -eq "westus" }
```

이 명령은 모든 백업 자격 증명 모음을 가져옵니다.
파이프라인 연산자를 사용 하 여이 명령을 Where-Object cmdlet에 전달 합니다.
해당 cmdlet은 **Region** 속성을 기준으로 결과를 필터링 합니다.
자세한 내용은을 입력 `Get-Help Where-Object` 하세요.

### 예제 3: 특정 자격 증명 모음 가져오기
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup011/providers/Microsoft.Backup
                    /BackupVault/Vault
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

이 명령은 Vault03 이라는 자격 증명 모음을 가져옵니다.

### 예제 4: 로컬에서 중복 저장소를 사용 하는 자격 증명 모음 수 계산
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Storage -match "LocallyRedundant" } | Measure-Object
Count    : 4
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property :
```

이 명령은 모든 Azure Backup 자격 증명 모음을 가져옵니다.
명령이 해당 위치에 **저장** 속성을 기준으로 결과를 필터링 하는 **개체를 여기** 에 전달 합니다.
Measure-Object LocallyRedundant 값이 있는 명령을 해당 명령에 전달 하 여 결과를 계산 하는 cmdlet을 사용 합니다.
자세한 내용은을 입력 `Get-Help Measure-Object` 하세요.

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

### -이름
이 cmdlet이 가져오는 백업 자격 증명 모음의 이름을 지정 합니다.
두 개 이상의 백업 자격 증명 모음이 동일한 이름을 가진 경우이 cmdlet은 모두 반환 합니다.
*ResourceGroupName* 매개 변수를 지정 하 여 고유한 자격 증명 모음을 가져옵니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
이 cmdlet이 백업 자격 증명 모음을 가져오는 Azure 리소스 그룹의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

### AzureRmBackupVault

## 상속자
* 않아야

## 관련 링크

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[새로운 AzureRmBackupVault](./New-AzureRmBackupVault.md)

[제거-AzureRmBackupVault](./Remove-AzureRmBackupVault.md)

[Set-AzureRmBackupVault](./Set-AzureRmBackupVault.md)


