---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: 388adccb9578c695055815ab6e6de5478958621f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491255"
---
# <span data-ttu-id="7d1b6-101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7d1b6-101">Set-AzStorageBlobContent</span></span>

## <span data-ttu-id="7d1b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d1b6-102">SYNOPSIS</span></span>
<span data-ttu-id="7d1b6-103">Azure Storage Blob에 로컬 파일을 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="7d1b6-104">구문</span><span class="sxs-lookup"><span data-stu-id="7d1b6-104">SYNTAX</span></span>

### <span data-ttu-id="7d1b6-105">SendManual(기본값)</span><span class="sxs-lookup"><span data-stu-id="7d1b6-105">SendManual (Default)</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>]
 [-StandardBlobTier <String>] [-EncryptionScope <String>] [-Force] [-AsJob] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d1b6-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="7d1b6-106">ContainerPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-EncryptionScope <String>] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d1b6-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="7d1b6-107">BlobPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>] [-Properties <Hashtable>]
 [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-EncryptionScope <String>] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d1b6-108">설명</span><span class="sxs-lookup"><span data-stu-id="7d1b6-108">DESCRIPTION</span></span>
<span data-ttu-id="7d1b6-109">**Set-AzStorageBlobContent** cmdlet은 로컬 파일을 Azure Storage Blob에 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-109">The **Set-AzStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="7d1b6-110">예제</span><span class="sxs-lookup"><span data-stu-id="7d1b6-110">EXAMPLES</span></span>

### <span data-ttu-id="7d1b6-111">예제 1: 명명된 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="7d1b6-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="7d1b6-112">이 명령은 PlanningData라는 파일을 Planning2015라는 Blob에 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="7d1b6-113">예제 2: 현재 폴더 아래에 있는 모든 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="7d1b6-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="7d1b6-114">이 명령은 core Windows PowerShell cmdlet Get-ChildItem 사용하여 현재 폴더 및 하위 폴더에 있는 모든 파일을 다운로드한 다음 파이프라인 연산자를 사용하여 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7d1b6-115">**Set-AzStorageBlobContent** cmdlet은 ContosoUploads라는 컨테이너에 파일을 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-115">The **Set-AzStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="7d1b6-116">예제 3: 기존 Blob 덮어 사용</span><span class="sxs-lookup"><span data-stu-id="7d1b6-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="7d1b6-117">이 명령은 Get-AzStorageBlob cmdlet을 사용하여 ContosoUploads 컨테이너에서 Planning2015라는 Blob을 끈 다음 해당 blob을 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="7d1b6-118">이 명령은 ContosoPlanning이라는 파일을 Planning2015로 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="7d1b6-119">이 명령은 Force 매개 *변수를 지정하지* 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="7d1b6-120">이 명령은 확인을 요청하는 메시지를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="7d1b6-121">명령을 확인하는 경우 cmdlet은 기존 Blob을 덮어 덮어 습니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="7d1b6-122">예제 4: 파이프라인을 사용하여 컨테이너에 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="7d1b6-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="7d1b6-123">이 명령은 **Get-AzStorageContainer** cmdlet을 사용하여 ContosoUpload 문자열로 시작하는 컨테이너를 끈 다음, 해당 Blob을 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="7d1b6-124">이 명령은 ContosoPlanning이라는 파일을 Planning2015로 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="7d1b6-125">예제 5: 메타데이터가 있는 페이지 Blob에 파일 업로드 및 PremiumPageBlobTier를 P10으로 업로드</span><span class="sxs-lookup"><span data-stu-id="7d1b6-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="7d1b6-126">첫 번째 명령은 Blob에 대한 메타데이터를 포함하는 해시 테이블을 만들고 해당 해시 테이블을 $Metadata.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="7d1b6-127">두 번째 명령은 ContosoPlanning이라는 파일을 ContosoUploads라는 컨테이너에 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="7d1b6-128">Blob은 $Metadata 메타데이터를 포함하며 PremiumPageBlobTier를 P10으로 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="7d1b6-129">예제 6: 지정된 Blob 속성을 사용하여 Blob에 파일을 업로드하고 StandardBlobTier를 쿨로 설정</span><span class="sxs-lookup"><span data-stu-id="7d1b6-129">Example 6: Upload a file to blob with specified blob properties, and set StandardBlobTier as Cool</span></span>
```
PS C:\> $filepath = "c:\temp\index.html"
PS C:\> Set-AzStorageBlobContent -File $filepath -Container "contosouploads" -Properties @{"ContentType" = [System.Web.MimeMapping]::GetMimeMapping($filepath); "ContentMD5" = "i727sP7HigloQDsqadNLHw=="} -StandardBlobTier Cool

   AccountName: storageaccountname, ContainerName: contosouploads

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
index.html           BlockBlob 403116          text/html                      2020-09-22 08:06:53Z Cool                                    False
```

<span data-ttu-id="7d1b6-130">이 명령은 지정된 blob 속성을 c:\temp\index.htmcontosouploads라는 컨테이너에 파일 c:\temp\index.htm파일을 업로드하고 StandardBlobTier를 쿨로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-130">This command uploads the file c:\temp\index.html to the container named contosouploads with specified blob properties, and set StandardBlobTier as Cool.</span></span>
<span data-ttu-id="7d1b6-131">이 명령은 [System.Web.MimeMapping]::GetMimeMapping() API를 통해 ContentType 값을 Blob 속성으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-131">This command gets ContentType value set to blob properties by [System.Web.MimeMapping]::GetMimeMapping() API.</span></span>

### <span data-ttu-id="7d1b6-132">예제 7: 암호화 범위를 사용하여 Blob에 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="7d1b6-132">Example 7: Upload a file to a blob with Encryption Scope</span></span>
```
PS C:\> $blob = Set-AzStorageBlobContent  -File "mylocalfile" -Container "mycontainer" -Blob "myblob"  -EncryptionScope "myencryptscope"

PS C:\> $blob.BlobProperties.EncryptionScope
myencryptscope
```

<span data-ttu-id="7d1b6-133">이 명령은 암호화 범위를 사용하여 Blob에 파일을 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-133">This command  uploads a file to a blob with Encryption Scope.</span></span>

## <span data-ttu-id="7d1b6-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d1b6-134">PARAMETERS</span></span>

### <span data-ttu-id="7d1b6-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d1b6-135">-AsJob</span></span>
<span data-ttu-id="7d1b6-136">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-136">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="7d1b6-137">-Blob</span><span class="sxs-lookup"><span data-stu-id="7d1b6-137">-Blob</span></span>
<span data-ttu-id="7d1b6-138">Blob의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-138">Specifies the name of a blob.</span></span>
<span data-ttu-id="7d1b6-139">이 cmdlet은 이 매개 변수가 지정하는 Azure Storage Blob에 파일을 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-139">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="7d1b6-140">-BlobType</span><span class="sxs-lookup"><span data-stu-id="7d1b6-140">-BlobType</span></span>
<span data-ttu-id="7d1b6-141">이 cmdlet이 업로드하는 Blob의 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-141">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="7d1b6-142">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="7d1b6-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7d1b6-143">차단</span><span class="sxs-lookup"><span data-stu-id="7d1b6-143">Block</span></span>
- <span data-ttu-id="7d1b6-144">페이지</span><span class="sxs-lookup"><span data-stu-id="7d1b6-144">Page</span></span>
- <span data-ttu-id="7d1b6-145">추가 기본값은 Block입니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-145">Append The default value is Block.</span></span>

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

### <span data-ttu-id="7d1b6-146">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7d1b6-146">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7d1b6-147">하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-147">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7d1b6-148">이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-148">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7d1b6-149">이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-149">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7d1b6-150">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="7d1b6-150">-CloudBlob</span></span>
<span data-ttu-id="7d1b6-151">**CloudBlob** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-151">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="7d1b6-152">**CloudBlob 개체를 얻으면** Get-AzStorageBlob cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-152">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="7d1b6-153">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="7d1b6-153">-CloudBlobContainer</span></span>
<span data-ttu-id="7d1b6-154">Azure Storage 클라이언트 라이브러리에서 **CloudBlobContainer** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-154">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="7d1b6-155">이 cmdlet은 이 매개 변수가 지정하는 컨테이너의 Blob에 콘텐츠를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-155">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="7d1b6-156">**CloudBlobContainer** 개체를 얻습니다. Get-AzStorageContainer cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-156">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="7d1b6-157">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7d1b6-157">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7d1b6-158">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-158">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7d1b6-159">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-159">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7d1b6-160">지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-160">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7d1b6-161">이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-161">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7d1b6-162">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-162">The default value is 10.</span></span>

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

### <span data-ttu-id="7d1b6-163">-Container</span><span class="sxs-lookup"><span data-stu-id="7d1b6-163">-Container</span></span>
<span data-ttu-id="7d1b6-164">컨테이너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-164">Specifies the name of a container.</span></span>
<span data-ttu-id="7d1b6-165">이 cmdlet은 이 매개 변수가 지정하는 컨테이너의 Blob에 파일을 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-165">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="7d1b6-166">-Context</span><span class="sxs-lookup"><span data-stu-id="7d1b6-166">-Context</span></span>
<span data-ttu-id="7d1b6-167">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-167">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7d1b6-168">저장소 컨텍스트를 얻습니다. New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-168">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="7d1b6-169">읽기 권한 없이 SAS 토큰에서 만든 저장소 컨텍스트를 사용하려면 -Force 매개 변수를 추가하여 Blob 존재 확인을 건너뛰야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-169">To use a storage context created from a SAS Token without read permission, need add -Force parameter to skip check blob existence.</span></span>

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

### <span data-ttu-id="7d1b6-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d1b6-170">-DefaultProfile</span></span>
<span data-ttu-id="7d1b6-171">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-171">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d1b6-172">-EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="7d1b6-172">-EncryptionScope</span></span>
<span data-ttu-id="7d1b6-173">Blob에 요청을 할 때 사용할 암호화 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-173">Encryption scope to be used when making requests to the blob.</span></span>

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

### <span data-ttu-id="7d1b6-174">-File</span><span class="sxs-lookup"><span data-stu-id="7d1b6-174">-File</span></span>
<span data-ttu-id="7d1b6-175">Blob 콘텐츠로 업로드할 파일의 로컬 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-175">Specifies a local file path for a file to upload as blob content.</span></span>

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

### <span data-ttu-id="7d1b6-176">-Force</span><span class="sxs-lookup"><span data-stu-id="7d1b6-176">-Force</span></span>
<span data-ttu-id="7d1b6-177">이 cmdlet이 확인을 묻는 메시지를 표시하지 않고 기존 Blob을 덮어 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-177">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="7d1b6-178">-Metadata</span><span class="sxs-lookup"><span data-stu-id="7d1b6-178">-Metadata</span></span>
<span data-ttu-id="7d1b6-179">업로드된 Blob에 대한 메타데이터를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-179">Specifies metadata for the uploaded blob.</span></span>

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

### <span data-ttu-id="7d1b6-180">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="7d1b6-180">-PremiumPageBlobTier</span></span>
<span data-ttu-id="7d1b6-181">페이지 Blob 계층</span><span class="sxs-lookup"><span data-stu-id="7d1b6-181">Page Blob Tier</span></span>

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

### <span data-ttu-id="7d1b6-182">-Properties</span><span class="sxs-lookup"><span data-stu-id="7d1b6-182">-Properties</span></span>
<span data-ttu-id="7d1b6-183">업로드된 Blob에 대한 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-183">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="7d1b6-184">지원되는 속성은 CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType입니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-184">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

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

### <span data-ttu-id="7d1b6-185">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7d1b6-185">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7d1b6-186">요청에 대한 서비스 쪽 시간제한 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-186">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="7d1b6-187">지정된 간격이 서비스에서 요청을 처리하기 전에 경과하면 저장소 서비스가 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-187">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="7d1b6-188">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="7d1b6-188">-StandardBlobTier</span></span>
<span data-ttu-id="7d1b6-189">블록 Blob 계층, 유효한 값은 핫/쿨/보관입니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-189">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="7d1b6-190">세부 정보 보기 https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="7d1b6-190">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="7d1b6-191">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d1b6-191">-Confirm</span></span>
<span data-ttu-id="7d1b6-192">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d1b6-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d1b6-193">-WhatIf</span></span>
<span data-ttu-id="7d1b6-194">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7d1b6-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d1b6-195">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d1b6-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d1b6-196">CommonParameters</span></span>
<span data-ttu-id="7d1b6-197">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d1b6-198">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7d1b6-198">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d1b6-199">입력</span><span class="sxs-lookup"><span data-stu-id="7d1b6-199">INPUTS</span></span>

### <span data-ttu-id="7d1b6-200">System.String</span><span class="sxs-lookup"><span data-stu-id="7d1b6-200">System.String</span></span>

### <span data-ttu-id="7d1b6-201">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="7d1b6-201">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="7d1b6-202">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="7d1b6-202">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="7d1b6-203">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7d1b6-203">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7d1b6-204">출력</span><span class="sxs-lookup"><span data-stu-id="7d1b6-204">OUTPUTS</span></span>

### <span data-ttu-id="7d1b6-205">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="7d1b6-205">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="7d1b6-206">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7d1b6-206">NOTES</span></span>

## <span data-ttu-id="7d1b6-207">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d1b6-207">RELATED LINKS</span></span>

[<span data-ttu-id="7d1b6-208">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7d1b6-208">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="7d1b6-209">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="7d1b6-209">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="7d1b6-210">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="7d1b6-210">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
