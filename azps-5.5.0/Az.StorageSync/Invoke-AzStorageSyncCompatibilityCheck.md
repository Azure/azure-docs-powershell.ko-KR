---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 51882269c342e766a3b714f931486eca437b9e58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197452"
---
# Invoke-AzStorageSyncCompatibilityCheck

## SYNOPSIS
시스템과 Azure 파일 동기화 간의 잠재적인 호환성 문제를 확인합니다.

## 구문

### PathBased(기본값)
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### ComputerNameBased
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## 설명
**Invoke-AzStorageSyncCompatibilityCheck** cmdlet은 시스템과 Azure 파일 동기화 간의 잠재적인 호환성 문제를 확인합니다. 로컬 또는 원격 경로가 주어지면 시스템 및 파일 네임스페이스에서 유효성 검사 집합을 수행한 다음 발견된 호환성 문제를 반환합니다.
시스템 검사:
- OS 호환성 파일 네임스페이스 확인:
- 비지원 문자
- 최대 파일 크기
- 최대 경로 길이
- 최대 파일 길이
- 최대 데이터 세트 크기
- 최대 디렉터리 깊이

## 예제

### 예제 1
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

이 명령은 시스템과 C:\DATA의 파일 및 폴더의 호환성을 확인합니다.

### 예제 2
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

이 명령은 C:\DATA에서 파일 및 폴더의 호환성을 검사하지만 시스템 호환성 검사를 수행하지 않습니다.

### 예제 3
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

이 명령은 시스템과 C:\DATA의 파일 및 폴더의 호환성을 확인한 다음 결과를 C:\results로 CSV 파일로 내보낼 수 있습니다.

## PARAMETERS

### -ComputerName
이 확인을 수행하는 컴퓨터입니다.

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
유효성을 검사하는 공유에 대한 자격 증명입니다.

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
유효성을 검사하는 공유의 UNC 경로입니다.

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

### -SkipNamespaceChecks
파일 네임스페이스 유효성 검사를 건너뛰고 시스템 유효성 검사만 수행하기 위해 이 플래그를 설정합니다.

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
시스템 유효성 검사를 건너뛰고 파일 네임스페이스 유효성 검사만 수행하기 위해 이 플래그를 설정합니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### 없음

## 출력

### Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult

## 참고 사항
* 키워드: azure, Az, arm, 리소스, 관리, 저장소ync, 파일ync

## 관련 링크
