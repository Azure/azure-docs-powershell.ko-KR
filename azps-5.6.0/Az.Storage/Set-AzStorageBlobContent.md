---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: 66cad13b7c3b1596b2ce369b454f5a0f9ff54b8e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976160"
---
# Set-AzStorageBlobContent

## SYNOPSIS
로컬 파일을 Azure Storage Blob에 업로드합니다.

## 구문

### SendManual(기본값)
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>]
 [-StandardBlobTier <String>] [-EncryptionScope <String>] [-Force] [-AsJob] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ContainerPipeline
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-EncryptionScope <String>] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### BlobPipeline
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>] [-Properties <Hashtable>]
 [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-EncryptionScope <String>] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Set-AzStorageBlobContent** cmdlet은 로컬 파일을 Azure Storage Blob에 업로드합니다.

## 예제

### 예제 1: 명명된 파일 업로드
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

이 명령은 PlanningData라는 파일을 Planning2015라는 Blob에 업로드합니다.

### 예제 2: 현재 폴더 아래에 있는 모든 파일 업로드
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

이 명령은 핵심 Windows PowerShell cmdlet Get-ChildItem 사용하여 현재 폴더 및 하위 폴더에 있는 모든 파일을 얻은 다음 파이프라인 연산자를 사용하여 현재 cmdlet에 전달합니다.
**Set-AzStorageBlobContent** cmdlet은 ContosoUploads라는 컨테이너에 파일을 업로드합니다.

### 예제 3: 기존 Blob 덮어 덮어 덮어 덮어 사용
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

이 명령은 contosoUploads 컨테이너에서 Planning2015라는 blob을 Get-AzStorageBlob cmdlet을 사용하여 해당 blob을 현재 cmdlet에 전달합니다.
명령은 Planning2015로 ContosoPlanning이라는 파일을 업로드합니다.
이 명령은 Force 매개 변수를 *지정하지* 않습니다.
명령을 통해 확인을 묻는 메시지가 표시됩니다.
명령을 확인하면 cmdlet이 기존 Blob을 덮어 덮어 덮어 덮어

### 예제 4: 파이프라인을 사용하여 컨테이너에 파일 업로드
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

이 명령은 **Get-AzStorageContainer** cmdlet을 사용하여 ContosoUpload 문자열로 시작하는 컨테이너를 얻은 다음 해당 Blob을 현재 cmdlet에 전달합니다.
명령은 Planning2015로 ContosoPlanning이라는 파일을 업로드합니다.

### 예제 5: 메타데이터 및 PremiumPageBlobTier를 P10으로 사용하여 페이지 Blob에 파일 업로드
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

첫 번째 명령은 Blob에 대한 메타데이터를 포함하는 해시 테이블을 만들고, 해시 테이블을 $Metadata 저장합니다.
두 번째 명령은 ContosoUploads라는 컨테이너에 ContosoPlanning이라는 파일을 업로드합니다.
Blob에 저장된 메타데이터를 $Metadata PremiumPageBlobTier를 P10으로 포함합니다.

### 예제 6: 지정된 Blob 속성을 사용하여 Blob에 파일을 업로드하고 StandardBlobTier를 Cool으로 설정
```
PS C:\> $filepath = "c:\temp\index.html"
PS C:\> Set-AzStorageBlobContent -File $filepath -Container "contosouploads" -Properties @{"ContentType" = [System.Web.MimeMapping]::GetMimeMapping($filepath); "ContentMD5" = "i727sP7HigloQDsqadNLHw=="} -StandardBlobTier Cool

   AccountName: storageaccountname, ContainerName: contosouploads

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
index.html           BlockBlob 403116          text/html                      2020-09-22 08:06:53Z Cool                                    False
```

이 명령은 c:\temp\index.htmBlob 속성을 사용하여 contosouploads라는 컨테이너에 l을 업로드하고 StandardBlobTier를 Cool으로 설정합니다.
이 명령은 [System.Web.MimeMapping]::GetMimeMapping() API를 통해 ContentType 값을 Blob 속성으로 설정합니다.

### 예제 7: 암호화 범위가 있는 Blob에 파일 업로드
```
PS C:\> $blob = Set-AzStorageBlobContent  -File "mylocalfile" -Container "mycontainer" -Blob "myblob"  -EncryptionScope "myencryptscope"

PS C:\> $blob.BlobProperties.EncryptionScope
myencryptscope
```

이 명령은 암호화 범위를 사용하여 Blob에 파일을 업로드합니다.

## 매개 변수

### -AsJob
백그라운드에서 cmdlet을 실행합니다.

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

### -Blob
Blob의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 Azure Storage Blob에 파일을 업로드합니다.

```yaml
Type: System.String
Parameter Sets: SendManual, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlobType
이 cmdlet이 업로드하는 Blob의 형식을 지정합니다.
이 매개 변수에 대해 허용되는 값은 다음입니다.
- 블록
- 페이지
- 추가 기본값은 블록입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Block, Page, Append

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientTimeoutPerRequest
하나의 서비스 요청에 대해 클라이언트 쪽 시간 간격(초)을 지정합니다.
지정된 간격에서 이전 호출이 실패하면 이 cmdlet에서 요청을 다시 검색합니다.
간격이 경과하기 전에 이 cmdlet에서 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CloudBlob
**CloudBlob 개체를 지정합니다.**
**CloudBlob** 개체를 얻으면 Get-AzStorageBlob cmdlet을 사용합니다.

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CloudBlobContainer
Azure Storage 클라이언트 라이브러리에서 **CloudBlobContainer** 개체를 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 컨테이너의 Blob에 콘텐츠를 업로드합니다.
**CloudBlobContainer** 개체를 얻은 경우 Get-AzStorageContainer cmdlet을 사용합니다.

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConcurrentTaskCount
최대 동시 네트워크 호출을 지정합니다.
이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 로컬 CPU 및 대역폭 사용량을 제한하는 동시성 제한할 수 있습니다.
지정된 값은 절대 개수로 코어 수에 곱하지 않습니다.
이 매개 변수는 초당 100킬로비트와 같은 대역폭이 낮은 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.
기본값은 10입니다.

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

### -Container
컨테이너의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 컨테이너의 Blob에 파일을 업로드합니다.

```yaml
Type: System.String
Parameter Sets: SendManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Context
Azure Storage 컨텍스트를 지정합니다.
저장소 컨텍스트를 구하기 위해 New-AzStorageContext cmdlet을 사용 합니다.
읽기 권한 없이 SAS 토큰에서 만든 저장소 컨텍스트를 사용하려면 검사 Blob 존재를 건너뛰기 위해 -Force 매개 변수를 추가해야 합니다.

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

### -EncryptionScope
Blob에 요청을 할 때 사용할 암호화 범위입니다.

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

### -File
파일을 Blob 콘텐츠로 업로드할 로컬 파일 경로를 지정합니다.

```yaml
Type: System.String
Parameter Sets: SendManual
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ContainerPipeline, BlobPipeline
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
이 cmdlet이 확인을 요청하지 않고 기존 Blob을 덮어 묻는 메시지를 나타냅니다.

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

### -메타데이터
업로드된 Blob에 대한 메타데이터를 지정합니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PremiumPageBlobTier
페이지 Blob 계층

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60, P70, P80

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -속성
업로드된 Blob에 대한 속성을 지정합니다. 지원되는 속성은 CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType입니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
요청에 대해 서비스 쪽 시간 시간 간격(초)을 지정합니다.
서비스가 요청을 처리하기 전에 지정된 간격이 경과하면 저장소 서비스가 오류를 반환합니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StandardBlobTier
블록 Blob 계층, 유효한 값은 Hot/Cool/Archive입니다.
자세한 정보 보기 https://docs.microsoft.com/azure/storage/blobs/storage-blob-storage-tiers

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool, Archive

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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.
cmdlet이 실행되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### System.String

### Microsoft.Azure.Storage.Blob.CloudBlobContainer

### Microsoft.Azure.Storage.Blob.CloudBlob

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## 출력

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob

## 참고 사항

## 관련 링크

[Get-AzStorageBlobContent](./Get-AzStorageBlobContent.md)

[Get-AzStorageBlob](./Get-AzStorageBlob.md)

[Remove-AzStorageBlob](./Remove-AzStorageBlob.md)
