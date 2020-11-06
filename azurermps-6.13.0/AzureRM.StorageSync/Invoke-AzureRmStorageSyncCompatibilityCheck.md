---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: AzureRM.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storagesync/invoke-azurermstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 73e0f00fe184a5462141b060717ca64567d4a67e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531303"
---
# Invoke-AzureRmStorageSyncCompatibilityCheck

## SYNOPSIS
시스템 및 Azure 파일 동기화 간에 발생할 수 있는 호환성 문제가 있는지 확인 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### PathBased (기본값)
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [-Quiet] [<CommonParameters>]
```

### ComputerNameBased
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [-Quiet] [<CommonParameters>]
```

## 설명은
**AzureRmStorageSyncCompatibilityCheck** cmdlet은 시스템 및 Azure 파일 동기화 간에 발생할 수 있는 잠재적인 호환성 문제를 검사 합니다. 로컬 또는 원격 경로를 지정 하면 시스템 및 파일 네임 스페이스에 대 한 유효성 검사 집합을 수행한 다음 발견 되는 호환성 문제를 반환 합니다.
시스템 검사:
- OS 호환성 파일 네임 스페이스 검사:
- 지원 되지 않는 문자
- 최대 파일 크기
- 최대 경로 길이
- 최대 파일 길이
- 최대 데이터 집합 크기
- 최대 디렉터리 깊이

## 예제의

### 예제 1
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
```

이 명령은 시스템의 호환성 및 C:\DATA. 파일 및 폴더도 검사 합니다.

### 예제 2
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

이 명령은 C:\DATA의 파일 및 폴더 호환성을 검사 하지만 시스템 호환성 검사를 수행 하지는 않습니다.

### 예제 3
```powershell
PS C:\> $errors = Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
PS C:\> $errors | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results
```

이 명령은 시스템의 호환성 및 C:\DATA에서 파일 및 폴더를 검사 한 다음 결과를 CSV 파일로 서 C:\results.에 내보냅니다.

## 변수

### -ComputerName
이 검사를 수행 하는 컴퓨터입니다.

```yaml
Type: System.String
Parameter Sets: ComputerNameBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
유효성을 검사 중인 공유에 대 한 자격 증명입니다.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
유효성을 검사할 공유의 UNC 경로입니다.

```yaml
Type: System.String
Parameter Sets: PathBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Quiet
콘솔에 출력 보고서 작성을 표시 하지 않습니다.

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

### -SkipNamespaceChecks
이 플래그를 설정 하 여 파일 네임 스페이스 유효성 검사를 건너뛰고 시스템 유효성 검사만 수행 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PathBased
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipSystemChecks
시스템 유효성 검사를 건너뛰고 파일 네임 스페이스 유효성 검사만 수행 하도록이 플래그를 설정 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### StorageSync. PSValidationResult를 실행 합니다.

## 상속자
* 키워드: azure, azurerm, arm, resource, management, storagesync, filesync

## 관련 링크
