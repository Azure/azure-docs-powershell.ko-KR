---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 53da56d932d3e2b57c2b2bbf17107918c9c1226d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195665"
---
# New-AzStorageSyncServerEndpoint

## SYNOPSIS
이 명령은 등록된 서버에 새 서버 엔드포인트를 만듭니다. 이렇게 하면 서버의 지정된 경로가 동기화 그룹의 다른 엔드포인트와 파일 동기화를 시작할 수 있습니다.

## 구문

### StringParameterSet(기본값)
```
New-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -ServerResourceId <String> -ServerLocalPath <String> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ObjectParameterSet
```
New-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ParentStringParameterSet
```
New-AzStorageSyncServerEndpoint [-ParentResourceId] <String> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
이 명령은 등록된 서버에 새 서버 엔드포인트를 만듭니다. 이렇게 하면 서버의 지정된 경로가 동기화 그룹의 다른 엔드포인트와 파일 동기화를 시작할 수 있습니다. 동기화 그룹의 다른 엔드포인트에 이미 파일이 있으며 새로 추가된 위치에도 파일이 포함되어 있는 경우, 화해 프로세스는 파일이 실제로 다른 엔드포인트와 동일한 폴더에 있는지 확인하려고 합니다. 네임스페이스는 병합 및 해결을 통해 충돌 파일을 방지하는 데 도움이 됩니다. 다른 서버 엔드포인트에 파일이 있는 경우 클라우드의 파일이 빠른 재해 복구라는 자동 프로세스에서 서버로 이동하기 위해 이 서버의 빈 위치로 시작하는 것이 좋습니다. 네임스페이스 메타데이터가 먼저 동기화된 다음 각 파일의 데이터 스트림이 다운로드됩니다. 사용자 또는 애플리케이션이 다운로드 순서를 어서 파일을 요청하는 경우 해당 파일은 액세스 요청을 충족하기 위해 우선 순위에 따라 회수됩니다. 선택적으로 이 서버 엔드포인트에서 클라우드 계층을 사용하여 이 엔드포인트가 클라우드의 전체 파일 집합의 캐시가 되기로 해야 하는지 확인할 수 있습니다. 클라우드 계층화가 사용되는 경우 설정할 수 있는 클라우드 계층화 정책에 정의된 지점에서 파일 콘텐츠 다운로드가 중지됩니다.

## 예제

### 예제 1
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> New-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName" -ServerResourceId $RegisteredServer.ResourceId -ServerLocalPath "myServerLocalPath" -CloudTiering -OfflineDataTransfer -OfflineDataTransferShareName "myOfflineDataTransferShareName" -TierFilesOlderThanDays "myTierFilesOlderThanDays"
```

이 명령은 등록된 서버에 새 서버 엔드포인트를 만들고 동기화 그룹에 삽입합니다. 다른 엔드포인트 및 파일 메타데이터 및 콘텐츠의 토폴로지의 일부인 THis 방식은 동기화 그룹의 엔드포인트로 참조되는 모든 위치 간에 즉시 동기화를 시작하게 됩니다.

## PARAMETERS

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

### -CloudTiering
클라우드 계층화 매개 변수

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

### -Name
ServerEndpoint의 이름입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OfflineDataTransfer
클라우드 시드 데이터 매개 변수

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

### -OfflineDataTransferShareName
클라우드 시드 데이터 파일 공유 URI 매개 변수

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -initialDownloadPolicy
로컬 캐시 모드 매개 변수

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -localCacheMode
로컬 캐시 모드 매개 변수

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParentObject
일반적으로 매개 변수를 통해 전달되는 SyncGroup 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ParentResourceId
SyncGroup 부모 리소스 ID

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerLocalPath
서버 로컬 경로 매개 변수

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerResourceId
RegisteredServer 리소스 ID

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageSyncServiceName
StorageSyncService의 이름입니다.

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SyncGroupName
SyncGroup의 이름입니다.

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TierFilesOlderThanDays
일보다 오래된 계층 파일 매개 변수

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VolumeFreeSpacePercent
볼륨 사용 공간 백분율 매개 변수

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우의 결과 표시 cmdlet이 실행되지 않습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup

### System.String

## 출력

### Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint

## 참고 사항

## 관련 링크
