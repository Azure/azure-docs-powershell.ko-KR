---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
ms.openlocfilehash: 09cbfb953118e5d6e29f2af25cd4653939135f07
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002507"
---
# New-AzStorageContainerSASToken

## SYNOPSIS
Azure 저장소 컨테이너에 대한 SAS 토큰을 생성합니다.

## 구문

### SasPolicy
```
New-AzStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SasPermission
```
New-AzStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명
**New-AzStorageContainerSASToken** cmdlet은 Azure 저장소 컨테이너에 대한 SAS(공유 액세스 서명) 토큰을 생성합니다.

## 예제

### 예제 1: 전체 컨테이너 사용 권한이 있는 컨테이너 SAS 토큰 생성
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Permission rwdl
```

이 예제에서는 전체 컨테이너 권한이 있는 컨테이너 SAS 토큰을 생성합니다.

### 예제 2: 파이프라인에 의해 여러 컨테이너 SAS 토큰 생성
```
PS C:\>Get-AzStorageContainer -Container test* | New-AzStorageContainerSASToken -Permission rwdl
```

이 예제에서는 파이프라인을 사용하여 여러 컨테이너 SAS 토큰을 생성합니다.

### 예제 3: 공유 액세스 정책으로 컨테이너 SAS 토큰 생성
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

이 예제에서는 공유 액세스 정책이 있는 컨테이너 SAS 토큰을 생성합니다.

### 예제 3: OAuth 인증을 기반으로 저장소 컨텍스트를 사용하여 사용자 ID 컨테이너 SAS 토큰 생성
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageContainerSASToken -Name "ContainerName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

이 예제에서는 OAuth 인증을 기반으로 저장소 컨텍스트가 있는 사용자 ID 컨테이너 SAS 토큰을 생성합니다.

## 매개 변수

### -Context
Azure Storage 컨텍스트를 지정합니다.
New-AzStorageContext cmdlet을 사용하여 만들 수 있습니다.
저장소 컨텍스트가 OAuth 인증을 기반으로 하는 경우 사용자 ID 컨테이너 SAS 토큰을 생성합니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpiryTime
공유 액세스 서명이 유효하지 않은 시간을 지정합니다.
사용자가 시작 시간을 설정하지만 만료 시간이 아닌 경우 만료 시간은 시작 시간과 1시간으로 설정됩니다.
시작 시간이나 만료 시간이 지정되지 않은 경우 만료 시간은 현재 시간과 1시간으로 설정됩니다.
저장소 컨텍스트가 OAuth 인증을 기반으로 하는 경우 만료 시간은 현재 시간에서 7일이 되어야 합니다. 현재 시간보다 더 일찍 되어야 합니다.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FullUri
이 cmdlet은 전체 Blob URI 및 공유 액세스 서명 토큰을 반환합니다.

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

### -IPAddressOrRange
168.1.5.65 또는 168.5.60-168.1.5.70과 같은 요청을 수락할 IP 주소 또는 범위를 지정합니다.
범위는 포괄적입니다.

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

### -Name
Azure Storage 컨테이너 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -권한
저장소 컨테이너에 대한 권한을 지정합니다.
이 문자열은 읽기, 쓰기 및 삭제와 같은 `rwd` 문자열입니다.

```yaml
Type: System.String
Parameter Sets: SasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Policy
Azure 저장된 액세스 정책을 지정합니다.

```yaml
Type: System.String
Parameter Sets: SasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol
요청에 대해 허용되는 프로토콜을 지정합니다.
이 매개 변수에 대해 허용되는 값은 다음입니다.
* HttpsOnly
* HttpsOrHttp 기본값은 HttpsOrHttp입니다.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
공유 액세스 서명이 유효한 시간을 지정합니다.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -확인
cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다. cmdlet이 실행되지 않습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## 출력

### System.String

## 참고 사항

## 관련 링크

[New-AzStorageBlobSASToken](./New-AzStorageBlobSASToken.md)
