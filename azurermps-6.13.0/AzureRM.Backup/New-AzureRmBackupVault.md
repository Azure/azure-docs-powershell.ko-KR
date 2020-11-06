---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 015E3BC9-C535-4EA2-8A30-C728385DBFF8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
ms.openlocfilehash: ad3619d2d0fcb9b60639a19b0c7d3fea45833857
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531475"
---
# New-AzureRmBackupVault

## SYNOPSIS
백업 자격 증명 모음을 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
New-AzureRmBackupVault [-ResourceGroupName] <String> [-Name] <String> [-Region] <String>
 [[-Storage] <AzureBackupVaultStorageType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmBackupVault** Cmdlet은 Azure Backup 자격 증명 모음을 만듭니다.
이 cmdlet은 자격 증명 모음 엔터티에 대 한 참조 역할을 하는 **AzureRmBackupVault** 개체를 반환 합니다.

## 예제의

### 예제 1: 백업 자격 증명 모음 만들기
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup01" -Name "Vault03" -Region "westus"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup01/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

이 명령은 Vault03 이라는 Azure 백업 자격 증명 모음을 만듭니다.
자격 증명 모음이 미국 지역의 ResourceGroup01 이라는 리소스 그룹에 있습니다.
자격 증명 모음에서는 기본 GeoRedundant 저장소 형식을 사용 합니다.

### 예제 2: 로컬에서 중복 저장소를 사용 하는 백업 자격 증명 모음 만들기
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup02" -Name "Vault03" -Region "westus" -Storage LocallyRedundant
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup02/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup02
Region            : westus
Storage           : LocallyRedundant
```

이 명령은 Vault03 이라는 Azure 백업 자격 증명 모음을 만듭니다.
자격 증명 모음이 미국 지역의 ResourceGroup02 이라는 리소스 그룹에 있습니다.
자격 증명 모음이 LocallyRedundant 저장소 유형을 사용 합니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

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

### -이름
Azure Backup vault의 이름을 지정 합니다.
이름은 리소스 그룹에서 고유 해야 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -지역
백업 자격 증명 모음이 존재 하는 Azure 지역을 지정 합니다.
하이브리드 백업 시나리오의 경우 대기 시간을 줄이기 위해 온-프레미스 서버 가까이에 있는 영역에 자격 증명 모음을 만드는 것이 좋습니다.
Azure 인프라를 서비스 (IaaS) 가상 컴퓨터로 백업 하는 경우 자격 증명 모음이 로컬 가상 컴퓨터에 대 한 검색 지점이 됩니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
이 cmdlet이 백업 자격 증명 모음을 만드는 기존 Azure 리소스 그룹의 이름을 지정 합니다.
리소스 그룹을 만들려면 New-AzureRMResourceGroup cmdlet을 사용 합니다.
리소스 그룹과 Azure Backup 자격 증명 모음이 동일한 지역에 있을 필요는 없습니다.

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

### -저장소
백업 데이터의 저장소 유형을 지정 합니다.
이 매개 변수에 허용 되는 값은 LocallyRedundant 및 GeoRedundant입니다.
기본 값은 GeoRedundant입니다.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### AzureRMBackupVault를 통한 명령.

## 상속자
* 않아야

## 관련 링크

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[제거-AzureRmBackupVault](./Remove-AzureRmBackupVault.md)

[Set-AzureRmBackupVault](./Set-AzureRmBackupVault.md)


