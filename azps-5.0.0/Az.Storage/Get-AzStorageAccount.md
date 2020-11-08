---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: ae7a43da35ce0aa41a34639521bc610d69843062
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226481"
---
# Get-AzStorageAccount

## SYNOPSIS
저장소 계정을 가져옵니다.

## 구문과

### ResourceGroupParameterSet
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### AccountNameParameterSet
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeGeoReplicationStats] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BlobRestoreStatusParameterSet
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeBlobRestoreStatus] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzStorageAccount** cmdlet은 지정 된 저장소 계정 또는 리소스 그룹 또는 구독에 있는 모든 저장소 계정을 가져옵니다.

## 예제의

### 예제 1: 지정 된 저장소 계정 가져오기
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -Name "mystorageaccount"
```

이 명령은 지정 된 저장소 계정을 가져옵니다.

### 예제 2: 리소스 그룹의 모든 저장소 계정 가져오기
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

이 명령은 리소스 그룹의 모든 저장소 계정을 가져옵니다.

### 예제 3: 구독에서 모든 저장소 계정 가져오기
```
PS C:\>Get-AzStorageAccount
```

이 명령은 구독에 있는 모든 저장소 계정을 가져옵니다.

### 예제 4: blob 복원 상태를 사용 하 여 저장소 계정 가져오기
```
PS C:\> $account = Get-AzStorageAccount -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -IncludeBlobRestoreStatus

PS C:\> $account.BlobRestoreStatus

Status     RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                 
------     ---------                            ------------- ------------------------     ---------------------                 
InProgress a70cd4a1-f223-4c86-959f-cc13eb4795a8               2020-02-10T13:45:04.7155962Z [container1/blob1 -> container2/blob2]
```

이 명령은 blob 복원 상태를 사용 하 여 저장소 계정을 가져오고 blob 복원 상태를 표시 합니다.

## 변수

### -AsJob
백그라운드에서 cmdlet 실행

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

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -IncludeBlobRestoreStatus
저장소 계정의 BlobRestoreStatus를 가져옵니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BlobRestoreStatusParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeGeoReplicationStats
저장소 계정의 GeoReplicationStats를 가져옵니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
가져올 저장소 계정의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet, BlobRestoreStatusParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
가져올 저장소 계정이 포함 된 리소스 그룹의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet, BlobRestoreStatusParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### Microsoft. Azure.. i m a. 모델. PSStorageAccount

## 상속자

## 관련 링크

[새로운 AzStorageAccount](./New-AzStorageAccount.md)

[제거-AzStorageAccount](./Remove-AzStorageAccount.md)

[Set-AzStorageAccount](./Set-AzStorageAccount.md)


