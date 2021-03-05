---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/copy-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Copy-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Copy-AzStorageBlob.md
ms.openlocfilehash: 76e89c90da10e8e232a564fb5fb7e5f8cc807327
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988759"
---
# <span data-ttu-id="6e68f-101">Copy-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="6e68f-101">Copy-AzStorageBlob</span></span>

## <span data-ttu-id="6e68f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e68f-102">SYNOPSIS</span></span>
<span data-ttu-id="6e68f-103">Blob을 동기적으로 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="6e68f-103">Copy a blob synchronously.</span></span>

## <span data-ttu-id="6e68f-104">구문</span><span class="sxs-lookup"><span data-stu-id="6e68f-104">SYNTAX</span></span>

### <span data-ttu-id="6e68f-105">ContainerName(기본값)</span><span class="sxs-lookup"><span data-stu-id="6e68f-105">ContainerName (Default)</span></span>
```
Copy-AzStorageBlob [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-EncryptionScope <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e68f-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="6e68f-106">BlobInstance</span></span>
```
Copy-AzStorageBlob [-BlobBaseClient <BlobBaseClient>] -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-EncryptionScope <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e68f-107">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="6e68f-107">UriPipeline</span></span>
```
Copy-AzStorageBlob -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-EncryptionScope <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e68f-108">설명</span><span class="sxs-lookup"><span data-stu-id="6e68f-108">DESCRIPTION</span></span>
<span data-ttu-id="6e68f-109">**Copy-AzStorageBlob** cmdlet은 Blob을 동기적으로 복사하고 현재 블록 Blob만 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6e68f-109">The **Copy-AzStorageBlob** cmdlet copies a blob synchronously, currently only support block blob.</span></span>

## <span data-ttu-id="6e68f-110">예제</span><span class="sxs-lookup"><span data-stu-id="6e68f-110">EXAMPLES</span></span>

### <span data-ttu-id="6e68f-111">예제 1: 명명된 Blob을 다른 Blob에 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="6e68f-111">Example 1: Copy a named blob to another</span></span>
```
C:\PS> $destBlob = Copy-AzStorageBlob -SrcContainer "sourcecontainername" -SrcBlob "srcblobname" -DestContainer "destcontainername" -DestBlob "destblobname"
```

<span data-ttu-id="6e68f-112">이 명령은 새 Blob 이름으로 Blob을 원본 컨테이너에서 대상 컨테이너로 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="6e68f-112">This command copies a blob from source container to the destination container with a new blob name.</span></span> 

### <span data-ttu-id="6e68f-113">예제 2: Blob 개체에서 Blob 복사</span><span class="sxs-lookup"><span data-stu-id="6e68f-113">Example 2: Copy blob from a blob object</span></span>
```
C:\PS> $srcBlob = Get-AzStorageBlob -Container $containerName -Blob $blobName  -Context $ctx 
C:\PS> $destBlob =  $srcBlob | Copy-AzStorageBlob  -DestContainer "destcontainername" -DestBlob "destblobname"
```

<span data-ttu-id="6e68f-114">이 명령은 새 Blob 이름을 사용하여 원본 Blob 개체에서 대상 컨테이너로 Blob을 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="6e68f-114">This command copies a blob from source blob object to the destination container with a new blob name.</span></span>

### <span data-ttu-id="6e68f-115">예제 3: Blob Uri에서 Blob 복사</span><span class="sxs-lookup"><span data-stu-id="6e68f-115">Example 3: Copy blob from a blob Uri</span></span>
```
C:\PS> $srcBlobUri = New-AzStorageBlobSASToken -Container $srcContainerName -Blob $srcBlobName -Permission rt -ExpiryTime (Get-Date).AddDays(7) -FullUri 
C:\PS> $destBlob = Copy-AzStorageBlob -AbsoluteUri $srcBlobUri -DestContainer "destcontainername" -DestBlob "destblobname"
```

<span data-ttu-id="6e68f-116">첫 번째 명령은 사용 권한 "rt"의 sas 토큰을 사용하여 원본 Blob의 Blob Uri를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6e68f-116">The first command creates a blob Uri of the source blob, with sas token of permission "rt".</span></span> <span data-ttu-id="6e68f-117">두 번째 명령은 원본 Blob Uri에서 대상 Blob으로 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="6e68f-117">The second command copies from source blob Uri to the destination blob.</span></span>

### <span data-ttu-id="6e68f-118">예제 4: 블록 Blob 암호화 범위 업데이트</span><span class="sxs-lookup"><span data-stu-id="6e68f-118">Example 4: Update a block blob encryption scope</span></span>
```
C:\PS> $blob = Copy-AzStorageBlob -SrcContainer $containerName -SrcBlob $blobname -DestContainer $containername -EncryptionScope $newScopeName -Force
```

<span data-ttu-id="6e68f-119">이 명령은 블록 Blob 암호화 범위를 새 암호화 범위로 자체로 복사하여 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6e68f-119">This command update a block blob encryption scope by copy it to itself with a new encryption scope.</span></span>

## <span data-ttu-id="6e68f-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6e68f-120">PARAMETERS</span></span>

### <span data-ttu-id="6e68f-121">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="6e68f-121">-AbsoluteUri</span></span>
<span data-ttu-id="6e68f-122">원본 Blob uri</span><span class="sxs-lookup"><span data-stu-id="6e68f-122">Source blob uri</span></span>

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e68f-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e68f-123">-AsJob</span></span>
<span data-ttu-id="6e68f-124">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6e68f-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e68f-125">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="6e68f-125">-BlobBaseClient</span></span>
<span data-ttu-id="6e68f-126">BlobBaseClient 개체</span><span class="sxs-lookup"><span data-stu-id="6e68f-126">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobInstance
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e68f-127">-Context</span><span class="sxs-lookup"><span data-stu-id="6e68f-127">-Context</span></span>
<span data-ttu-id="6e68f-128">원본 Azure Storage 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="6e68f-128">Source Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, BlobInstance
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e68f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e68f-129">-DefaultProfile</span></span>
<span data-ttu-id="6e68f-130">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6e68f-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e68f-131">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="6e68f-131">-DestBlob</span></span>
<span data-ttu-id="6e68f-132">대상 Blob 이름</span><span class="sxs-lookup"><span data-stu-id="6e68f-132">Destination blob name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e68f-133">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="6e68f-133">-DestContainer</span></span>
<span data-ttu-id="6e68f-134">대상 컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="6e68f-134">Destination container name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e68f-135">-DestContext</span><span class="sxs-lookup"><span data-stu-id="6e68f-135">-DestContext</span></span>
<span data-ttu-id="6e68f-136">대상 저장소 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="6e68f-136">Destination Storage context object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e68f-137">-EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="6e68f-137">-EncryptionScope</span></span>
<span data-ttu-id="6e68f-138">dest Blob에 요청을 할 때 사용할 암호화 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="6e68f-138">Encryption scope to be used when making requests to the dest blob.</span></span>

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

### <span data-ttu-id="6e68f-139">-Force</span><span class="sxs-lookup"><span data-stu-id="6e68f-139">-Force</span></span>
<span data-ttu-id="6e68f-140">기존 Blob 또는 파일을 강제로 덮어 덮어 덮어 던지기</span><span class="sxs-lookup"><span data-stu-id="6e68f-140">Force to overwrite the existing blob or file</span></span>

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

### <span data-ttu-id="6e68f-141">-RehydratePriority</span><span class="sxs-lookup"><span data-stu-id="6e68f-141">-RehydratePriority</span></span>
<span data-ttu-id="6e68f-142">Blob RehydratePriority를 차단합니다.</span><span class="sxs-lookup"><span data-stu-id="6e68f-142">Block Blob RehydratePriority.</span></span>
<span data-ttu-id="6e68f-143">보관된 Blob을 다시하이드레이션할 우선 순위를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6e68f-143">Indicates the priority with which to rehydrate an archived blob.</span></span>
<span data-ttu-id="6e68f-144">유효한 값은 높음/표준입니다.</span><span class="sxs-lookup"><span data-stu-id="6e68f-144">Valid values are High/Standard.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.RehydratePriority
Parameter Sets: (All)
Aliases:
Accepted values: Standard, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e68f-145">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="6e68f-145">-SrcBlob</span></span>
<span data-ttu-id="6e68f-146">Blob 이름</span><span class="sxs-lookup"><span data-stu-id="6e68f-146">Blob name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e68f-147">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="6e68f-147">-SrcContainer</span></span>
<span data-ttu-id="6e68f-148">원본 컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="6e68f-148">Source Container name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e68f-149">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="6e68f-149">-StandardBlobTier</span></span>
<span data-ttu-id="6e68f-150">블록 Blob 계층, 유효한 값은 Hot/Cool/Archive입니다.</span><span class="sxs-lookup"><span data-stu-id="6e68f-150">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="6e68f-151">자세한 정보 보기 https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="6e68f-151">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="6e68f-152">-확인</span><span class="sxs-lookup"><span data-stu-id="6e68f-152">-Confirm</span></span>
<span data-ttu-id="6e68f-153">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e68f-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e68f-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e68f-154">-WhatIf</span></span>
<span data-ttu-id="6e68f-155">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6e68f-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e68f-156">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e68f-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e68f-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e68f-157">CommonParameters</span></span>
<span data-ttu-id="6e68f-158">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6e68f-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e68f-159">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6e68f-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e68f-160">입력</span><span class="sxs-lookup"><span data-stu-id="6e68f-160">INPUTS</span></span>

### <span data-ttu-id="6e68f-161">Azure.Storage.Blobs.Specialized.BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="6e68f-161">Azure.Storage.Blobs.Specialized.BlobBaseClient</span></span>

### <span data-ttu-id="6e68f-162">System.String</span><span class="sxs-lookup"><span data-stu-id="6e68f-162">System.String</span></span>

### <span data-ttu-id="6e68f-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6e68f-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6e68f-164">출력</span><span class="sxs-lookup"><span data-stu-id="6e68f-164">OUTPUTS</span></span>

### <span data-ttu-id="6e68f-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="6e68f-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="6e68f-166">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6e68f-166">NOTES</span></span>

## <span data-ttu-id="6e68f-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e68f-167">RELATED LINKS</span></span>
