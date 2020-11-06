---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: c76bd152f64b337ca818c9e86b14fddbdaaf38cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536247"
---
# Get-AzureRmRecoveryServicesBackupManagementServer

## SYNOPSIS
SCDPM 및 Azure 백업 관리 서버를 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Get-AzureRmRecoveryServicesBackupManagementServer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzureRmRecoveryServicesBackupManagementServer** cmdlet은 자격 증명 모음에 등록 된 백업 관리 서버의 목록을 가져옵니다.

백업 관리 서버에는 SCDPM (System Center Data Protection Manager) 및 Azure Backup 관리 서버가 두 가지 유형이 있습니다.
백업 관리 서버는 개별적으로 설치 되어 백업 오케스트레이션을 관리 합니다.

현재 cmdlet을 사용 하기 전에 Set-AzureRmRecoveryServicesVaultContext cmdlet을 사용 하 여 자격 증명 모음 컨텍스트를 설정 합니다.

## 예제의

### 예제 1: 모든 백업 관리 서버 가져오기
```
PS C:\>Get-AzureRmRecoveryServicesBackupManagementServer
```

이 명령은 자격 증명 모음에 등록 된 모든 백업 관리 서버를 가져옵니다.

## 변수

### -이름
가져올 백업 관리 서버의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
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

### BackupEngineBase에서. i. i m/.

### System.webserver. IList ' 1 [Microsoft Azure. e. BackupEngineBase]을 (를)

## 상속자

## 관련 링크

[등록 취소-AzureRmRecoveryServicesBackupManagementServer](./Unregister-AzureRmRecoveryServicesBackupManagementServer.md)


