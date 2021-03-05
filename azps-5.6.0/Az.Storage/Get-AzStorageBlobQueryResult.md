---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/get-azstorageblobqueryresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobQueryResult.md
ms.openlocfilehash: 7a790610d9ff3334494276eee7bb85af5b9ba3fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002704"
---
# <span data-ttu-id="26358-101">Get-AzStorageBlobQueryResult</span><span class="sxs-lookup"><span data-stu-id="26358-101">Get-AzStorageBlobQueryResult</span></span>

## <span data-ttu-id="26358-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26358-102">SYNOPSIS</span></span>
<span data-ttu-id="26358-103">Blob의 콘텐츠에 구조적 쿼리 언어(SQL) 문을 적용하고 데이터의 검색된 하위 집합만 로컬 파일에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="26358-103">Applies a simple Structured Query Language (SQL) statement on a blob's contents and save only the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="26358-104">구문</span><span class="sxs-lookup"><span data-stu-id="26358-104">SYNTAX</span></span>

### <span data-ttu-id="26358-105">NamePipeline(기본값)</span><span class="sxs-lookup"><span data-stu-id="26358-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobQueryResult [-Blob] <String> [-Container] <String> [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26358-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="26358-106">BlobPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobBaseClient <BlobBaseClient> -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26358-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="26358-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobQueryResult -BlobContainerClient <BlobContainerClient> [-Blob] <String>
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] -QueryString <String> -ResultFile <String>
 [-InputTextConfiguration <PSBlobQueryTextConfiguration>]
 [-OutputTextConfiguration <PSBlobQueryTextConfiguration>] [-PassThru] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26358-108">설명</span><span class="sxs-lookup"><span data-stu-id="26358-108">DESCRIPTION</span></span>
<span data-ttu-id="26358-109">**Get-AzStorageBlobQueryResult** cmdlet은 Blob의 콘텐츠에 구조적 쿼리 언어(SQL) 명령문을 적용하고 데이터의 검색된 하위 집합을 로컬 파일에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="26358-109">The **Get-AzStorageBlobQueryResult** cmdlet applies a simple Structured Query Language (SQL) statement on a blob's contents and save the queried subset of the data to a local file.</span></span>

## <span data-ttu-id="26358-110">예제</span><span class="sxs-lookup"><span data-stu-id="26358-110">EXAMPLES</span></span>

### <span data-ttu-id="26358-111">예제 1: Blob 쿼리</span><span class="sxs-lookup"><span data-stu-id="26358-111">Example 1: Query a blob</span></span>
```powershell
PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE Name = 'a'"

PS C:\> $result = Get-AzStorageBlobQueryResult -Container $containerName -Blob $blobName -QueryString $queryString -ResultFile "c:\resultfile.json" -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig -Context $ctx

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
         449            0
```

<span data-ttu-id="26358-112">이 명령은 csv로 입력 구성을 사용하여 Blob succsfully를 쿼리하고 출력 구성을 json으로 쿼리하고 출력을 "c:\resultfile.js설정"에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="26358-112">This command querys a blob succsssfully with input config as csv, and output config as json, and save the output to local file "c:\resultfile.json".</span></span>

### <span data-ttu-id="26358-113">예제 2: Blob 스냅숏 쿼리</span><span class="sxs-lookup"><span data-stu-id="26358-113">Example 2: Query a blob snapshot</span></span>
```powershell
PS C:\> $blob = Get-AzStorageBlob -Container $containerName -Blob $blobName -SnapshotTime "2020-07-29T11:08:21.1097874Z" -Context $ctx

PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -ColumnSeparator "," -QuotationCharacter """" -EscapeCharacter "\" -RecordSeparator "`n" -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson -RecordSeparator "`n" 

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE _1 LIKE '1%%'"

PS C:\> $result = $blob | Get-AzStorageBlobQueryResult -QueryString $queryString -ResultFile $localFilePath -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
   187064971            1 {ParseError}  



PS C:\> $result.BlobQueryError

Name       Description                                                   IsFatal Position
----       -----------                                                   ------- --------
ParseError Unexpected token '1' at [byte: 3077737]. Expecting token ','.    True  7270632
```

<span data-ttu-id="26358-114">이 명령은 먼저 Blob 스냅숏에 대한 Blob 개체를 만든 다음 Blob 스냅숏을 쿼리하고 결과에 쿼리 오류가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="26358-114">This command first gets a blob object for blob snapshot, then queries the blob snapshot and show the result include query error.</span></span>

## <span data-ttu-id="26358-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="26358-115">PARAMETERS</span></span>

### <span data-ttu-id="26358-116">-Blob</span><span class="sxs-lookup"><span data-stu-id="26358-116">-Blob</span></span>
<span data-ttu-id="26358-117">Blob 이름</span><span class="sxs-lookup"><span data-stu-id="26358-117">Blob name</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26358-118">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="26358-118">-BlobBaseClient</span></span>
<span data-ttu-id="26358-119">BlobBaseClient 개체</span><span class="sxs-lookup"><span data-stu-id="26358-119">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26358-120">-BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="26358-120">-BlobContainerClient</span></span>
<span data-ttu-id="26358-121">BlobContainerClient 개체</span><span class="sxs-lookup"><span data-stu-id="26358-121">BlobContainerClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.BlobContainerClient
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26358-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="26358-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="26358-123">클라이언트 쪽에서 각 요청에 대한 최대 실행 시간(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="26358-123">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="26358-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="26358-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="26358-125">동시 비동기 작업의 총 양입니다.</span><span class="sxs-lookup"><span data-stu-id="26358-125">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="26358-126">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="26358-126">The default value is 10.</span></span>

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

### <span data-ttu-id="26358-127">-Container</span><span class="sxs-lookup"><span data-stu-id="26358-127">-Container</span></span>
<span data-ttu-id="26358-128">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="26358-128">Container name</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26358-129">-Context</span><span class="sxs-lookup"><span data-stu-id="26358-129">-Context</span></span>
<span data-ttu-id="26358-130">Azure Storage 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="26358-130">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="26358-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26358-131">-DefaultProfile</span></span>
<span data-ttu-id="26358-132">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="26358-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26358-133">-Force</span><span class="sxs-lookup"><span data-stu-id="26358-133">-Force</span></span>
<span data-ttu-id="26358-134">기존 파일을 강제로 덮어 덮습니다.</span><span class="sxs-lookup"><span data-stu-id="26358-134">Force to overwrite the existing file.</span></span>

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

### <span data-ttu-id="26358-135">-InputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="26358-135">-InputTextConfiguration</span></span>
<span data-ttu-id="26358-136">쿼리 입력 텍스트를 처리하는 데 사용되는 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="26358-136">The configuration used to handled the query input text.</span></span> <span data-ttu-id="26358-137">New-AzStorageBlobQueryConfig를 사용하여 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26358-137">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26358-138">-OutputTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="26358-138">-OutputTextConfiguration</span></span>
<span data-ttu-id="26358-139">쿼리 출력 텍스트를 처리하는 데 사용되는 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="26358-139">The configuration used to handled the query output text.</span></span> <span data-ttu-id="26358-140">New-AzStorageBlobQueryConfig를 사용하여 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="26358-140">Create configuration object the with New-AzStorageBlobQueryConfig.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26358-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26358-141">-PassThru</span></span>
<span data-ttu-id="26358-142">지정된 Blob을 성공적으로 퀘이크할지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="26358-142">Return whether the specified blob is successfully queried.</span></span>

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

### <span data-ttu-id="26358-143">-QueryString</span><span class="sxs-lookup"><span data-stu-id="26358-143">-QueryString</span></span>
<span data-ttu-id="26358-144">쿼리 문자열은 다음에서 자세한 내용을 참조합니다. https://docs.microsoft.com/azure/storage/blobs/query-acceleration-sql-reference</span><span class="sxs-lookup"><span data-stu-id="26358-144">Query string, see more details in: https://docs.microsoft.com/azure/storage/blobs/query-acceleration-sql-reference</span></span>

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

### <span data-ttu-id="26358-145">-ResultFile</span><span class="sxs-lookup"><span data-stu-id="26358-145">-ResultFile</span></span>
<span data-ttu-id="26358-146">쿼리 결과를 저장하는 로컬 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="26358-146">Local file path to save the query result.</span></span>

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

### <span data-ttu-id="26358-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="26358-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="26358-148">각 요청에 대한 서버 시간(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="26358-148">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="26358-149">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="26358-149">-SnapshotTime</span></span>
<span data-ttu-id="26358-150">Blob SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="26358-150">Blob SnapshotTime</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26358-151">-VersionId</span><span class="sxs-lookup"><span data-stu-id="26358-151">-VersionId</span></span>
<span data-ttu-id="26358-152">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="26358-152">Blob VersionId</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26358-153">-확인</span><span class="sxs-lookup"><span data-stu-id="26358-153">-Confirm</span></span>
<span data-ttu-id="26358-154">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="26358-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26358-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26358-155">-WhatIf</span></span>
<span data-ttu-id="26358-156">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="26358-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26358-157">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26358-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26358-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26358-158">CommonParameters</span></span>
<span data-ttu-id="26358-159">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="26358-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26358-160">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="26358-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26358-161">입력</span><span class="sxs-lookup"><span data-stu-id="26358-161">INPUTS</span></span>

### <span data-ttu-id="26358-162">Azure.Storage.Blobs.Specialized.BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="26358-162">Azure.Storage.Blobs.Specialized.BlobBaseClient</span></span>

### <span data-ttu-id="26358-163">Azure.Storage.Blobs.BlobContainerClient</span><span class="sxs-lookup"><span data-stu-id="26358-163">Azure.Storage.Blobs.BlobContainerClient</span></span>

### <span data-ttu-id="26358-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="26358-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="26358-165">출력</span><span class="sxs-lookup"><span data-stu-id="26358-165">OUTPUTS</span></span>

### <span data-ttu-id="26358-166">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="26358-166">System.Boolean</span></span>

## <span data-ttu-id="26358-167">참고 사항</span><span class="sxs-lookup"><span data-stu-id="26358-167">NOTES</span></span>

## <span data-ttu-id="26358-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26358-168">RELATED LINKS</span></span>
