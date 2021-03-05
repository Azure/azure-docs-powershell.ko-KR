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
# <span data-ttu-id="b8969-101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b8969-101">Set-AzStorageBlobContent</span></span>

## <span data-ttu-id="b8969-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8969-102">SYNOPSIS</span></span>
<span data-ttu-id="b8969-103">로컬 파일을 Azure Storage Blob에 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="b8969-104">구문</span><span class="sxs-lookup"><span data-stu-id="b8969-104">SYNTAX</span></span>

### <span data-ttu-id="b8969-105">SendManual(기본값)</span><span class="sxs-lookup"><span data-stu-id="b8969-105">SendManual (Default)</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>]
 [-StandardBlobTier <String>] [-EncryptionScope <String>] [-Force] [-AsJob] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8969-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="b8969-106">ContainerPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-EncryptionScope <String>] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8969-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="b8969-107">BlobPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>] [-Properties <Hashtable>]
 [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-EncryptionScope <String>] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8969-108">설명</span><span class="sxs-lookup"><span data-stu-id="b8969-108">DESCRIPTION</span></span>
<span data-ttu-id="b8969-109">**Set-AzStorageBlobContent** cmdlet은 로컬 파일을 Azure Storage Blob에 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-109">The **Set-AzStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="b8969-110">예제</span><span class="sxs-lookup"><span data-stu-id="b8969-110">EXAMPLES</span></span>

### <span data-ttu-id="b8969-111">예제 1: 명명된 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="b8969-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="b8969-112">이 명령은 PlanningData라는 파일을 Planning2015라는 Blob에 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="b8969-113">예제 2: 현재 폴더 아래에 있는 모든 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="b8969-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="b8969-114">이 명령은 핵심 Windows PowerShell cmdlet Get-ChildItem 사용하여 현재 폴더 및 하위 폴더에 있는 모든 파일을 얻은 다음 파이프라인 연산자를 사용하여 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b8969-115">**Set-AzStorageBlobContent** cmdlet은 ContosoUploads라는 컨테이너에 파일을 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-115">The **Set-AzStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="b8969-116">예제 3: 기존 Blob 덮어 덮어 덮어 덮어 사용</span><span class="sxs-lookup"><span data-stu-id="b8969-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="b8969-117">이 명령은 contosoUploads 컨테이너에서 Planning2015라는 blob을 Get-AzStorageBlob cmdlet을 사용하여 해당 blob을 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="b8969-118">명령은 Planning2015로 ContosoPlanning이라는 파일을 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="b8969-119">이 명령은 Force 매개 변수를 *지정하지* 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="b8969-120">명령을 통해 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="b8969-121">명령을 확인하면 cmdlet이 기존 Blob을 덮어 덮어 덮어 덮어</span><span class="sxs-lookup"><span data-stu-id="b8969-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="b8969-122">예제 4: 파이프라인을 사용하여 컨테이너에 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="b8969-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="b8969-123">이 명령은 **Get-AzStorageContainer** cmdlet을 사용하여 ContosoUpload 문자열로 시작하는 컨테이너를 얻은 다음 해당 Blob을 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="b8969-124">명령은 Planning2015로 ContosoPlanning이라는 파일을 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="b8969-125">예제 5: 메타데이터 및 PremiumPageBlobTier를 P10으로 사용하여 페이지 Blob에 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="b8969-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="b8969-126">첫 번째 명령은 Blob에 대한 메타데이터를 포함하는 해시 테이블을 만들고, 해시 테이블을 $Metadata 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="b8969-127">두 번째 명령은 ContosoUploads라는 컨테이너에 ContosoPlanning이라는 파일을 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="b8969-128">Blob에 저장된 메타데이터를 $Metadata PremiumPageBlobTier를 P10으로 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="b8969-129">예제 6: 지정된 Blob 속성을 사용하여 Blob에 파일을 업로드하고 StandardBlobTier를 Cool으로 설정</span><span class="sxs-lookup"><span data-stu-id="b8969-129">Example 6: Upload a file to blob with specified blob properties, and set StandardBlobTier as Cool</span></span>
```
PS C:\> $filepath = "c:\temp\index.html"
PS C:\> Set-AzStorageBlobContent -File $filepath -Container "contosouploads" -Properties @{"ContentType" = [System.Web.MimeMapping]::GetMimeMapping($filepath); "ContentMD5" = "i727sP7HigloQDsqadNLHw=="} -StandardBlobTier Cool

   AccountName: storageaccountname, ContainerName: contosouploads

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
index.html           BlockBlob 403116          text/html                      2020-09-22 08:06:53Z Cool                                    False
```

<span data-ttu-id="b8969-130">이 명령은 c:\temp\index.htmBlob 속성을 사용하여 contosouploads라는 컨테이너에 l을 업로드하고 StandardBlobTier를 Cool으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-130">This command uploads the file c:\temp\index.html to the container named contosouploads with specified blob properties, and set StandardBlobTier as Cool.</span></span>
<span data-ttu-id="b8969-131">이 명령은 [System.Web.MimeMapping]::GetMimeMapping() API를 통해 ContentType 값을 Blob 속성으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-131">This command gets ContentType value set to blob properties by [System.Web.MimeMapping]::GetMimeMapping() API.</span></span>

### <span data-ttu-id="b8969-132">예제 7: 암호화 범위가 있는 Blob에 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="b8969-132">Example 7: Upload a file to a blob with Encryption Scope</span></span>
```
PS C:\> $blob = Set-AzStorageBlobContent  -File "mylocalfile" -Container "mycontainer" -Blob "myblob"  -EncryptionScope "myencryptscope"

PS C:\> $blob.BlobProperties.EncryptionScope
myencryptscope
```

<span data-ttu-id="b8969-133">이 명령은 암호화 범위를 사용하여 Blob에 파일을 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-133">This command  uploads a file to a blob with Encryption Scope.</span></span>

## <span data-ttu-id="b8969-134">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b8969-134">PARAMETERS</span></span>

### <span data-ttu-id="b8969-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8969-135">-AsJob</span></span>
<span data-ttu-id="b8969-136">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-136">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="b8969-137">-Blob</span><span class="sxs-lookup"><span data-stu-id="b8969-137">-Blob</span></span>
<span data-ttu-id="b8969-138">Blob의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-138">Specifies the name of a blob.</span></span>
<span data-ttu-id="b8969-139">이 cmdlet은 이 매개 변수가 지정하는 Azure Storage Blob에 파일을 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-139">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="b8969-140">-BlobType</span><span class="sxs-lookup"><span data-stu-id="b8969-140">-BlobType</span></span>
<span data-ttu-id="b8969-141">이 cmdlet이 업로드하는 Blob의 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-141">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="b8969-142">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b8969-143">블록</span><span class="sxs-lookup"><span data-stu-id="b8969-143">Block</span></span>
- <span data-ttu-id="b8969-144">페이지</span><span class="sxs-lookup"><span data-stu-id="b8969-144">Page</span></span>
- <span data-ttu-id="b8969-145">추가 기본값은 블록입니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-145">Append The default value is Block.</span></span>

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

### <span data-ttu-id="b8969-146">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b8969-146">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b8969-147">하나의 서비스 요청에 대해 클라이언트 쪽 시간 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-147">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b8969-148">지정된 간격에서 이전 호출이 실패하면 이 cmdlet에서 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-148">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b8969-149">간격이 경과하기 전에 이 cmdlet에서 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-149">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b8969-150">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="b8969-150">-CloudBlob</span></span>
<span data-ttu-id="b8969-151">**CloudBlob 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="b8969-151">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="b8969-152">**CloudBlob** 개체를 얻으면 Get-AzStorageBlob cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-152">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="b8969-153">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b8969-153">-CloudBlobContainer</span></span>
<span data-ttu-id="b8969-154">Azure Storage 클라이언트 라이브러리에서 **CloudBlobContainer** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-154">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="b8969-155">이 cmdlet은 이 매개 변수가 지정하는 컨테이너의 Blob에 콘텐츠를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-155">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="b8969-156">**CloudBlobContainer** 개체를 얻은 경우 Get-AzStorageContainer cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-156">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="b8969-157">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b8969-157">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b8969-158">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-158">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b8969-159">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 로컬 CPU 및 대역폭 사용량을 제한하는 동시성 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-159">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b8969-160">지정된 값은 절대 개수로 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-160">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b8969-161">이 매개 변수는 초당 100킬로비트와 같은 대역폭이 낮은 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-161">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b8969-162">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-162">The default value is 10.</span></span>

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

### <span data-ttu-id="b8969-163">-Container</span><span class="sxs-lookup"><span data-stu-id="b8969-163">-Container</span></span>
<span data-ttu-id="b8969-164">컨테이너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-164">Specifies the name of a container.</span></span>
<span data-ttu-id="b8969-165">이 cmdlet은 이 매개 변수가 지정하는 컨테이너의 Blob에 파일을 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-165">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="b8969-166">-Context</span><span class="sxs-lookup"><span data-stu-id="b8969-166">-Context</span></span>
<span data-ttu-id="b8969-167">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-167">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b8969-168">저장소 컨텍스트를 구하기 위해 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-168">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="b8969-169">읽기 권한 없이 SAS 토큰에서 만든 저장소 컨텍스트를 사용하려면 검사 Blob 존재를 건너뛰기 위해 -Force 매개 변수를 추가해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-169">To use a storage context created from a SAS Token without read permission, need add -Force parameter to skip check blob existence.</span></span>

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

### <span data-ttu-id="b8969-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8969-170">-DefaultProfile</span></span>
<span data-ttu-id="b8969-171">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-171">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8969-172">-EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="b8969-172">-EncryptionScope</span></span>
<span data-ttu-id="b8969-173">Blob에 요청을 할 때 사용할 암호화 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-173">Encryption scope to be used when making requests to the blob.</span></span>

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

### <span data-ttu-id="b8969-174">-File</span><span class="sxs-lookup"><span data-stu-id="b8969-174">-File</span></span>
<span data-ttu-id="b8969-175">파일을 Blob 콘텐츠로 업로드할 로컬 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-175">Specifies a local file path for a file to upload as blob content.</span></span>

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

### <span data-ttu-id="b8969-176">-Force</span><span class="sxs-lookup"><span data-stu-id="b8969-176">-Force</span></span>
<span data-ttu-id="b8969-177">이 cmdlet이 확인을 요청하지 않고 기존 Blob을 덮어 묻는 메시지를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-177">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="b8969-178">-메타데이터</span><span class="sxs-lookup"><span data-stu-id="b8969-178">-Metadata</span></span>
<span data-ttu-id="b8969-179">업로드된 Blob에 대한 메타데이터를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-179">Specifies metadata for the uploaded blob.</span></span>

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

### <span data-ttu-id="b8969-180">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="b8969-180">-PremiumPageBlobTier</span></span>
<span data-ttu-id="b8969-181">페이지 Blob 계층</span><span class="sxs-lookup"><span data-stu-id="b8969-181">Page Blob Tier</span></span>

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

### <span data-ttu-id="b8969-182">-속성</span><span class="sxs-lookup"><span data-stu-id="b8969-182">-Properties</span></span>
<span data-ttu-id="b8969-183">업로드된 Blob에 대한 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-183">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="b8969-184">지원되는 속성은 CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType입니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-184">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

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

### <span data-ttu-id="b8969-185">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b8969-185">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b8969-186">요청에 대해 서비스 쪽 시간 시간 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-186">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="b8969-187">서비스가 요청을 처리하기 전에 지정된 간격이 경과하면 저장소 서비스가 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-187">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="b8969-188">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="b8969-188">-StandardBlobTier</span></span>
<span data-ttu-id="b8969-189">블록 Blob 계층, 유효한 값은 Hot/Cool/Archive입니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-189">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="b8969-190">자세한 정보 보기 https://docs.microsoft.com/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="b8969-190">See detail in https://docs.microsoft.com/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="b8969-191">-확인</span><span class="sxs-lookup"><span data-stu-id="b8969-191">-Confirm</span></span>
<span data-ttu-id="b8969-192">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8969-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8969-193">-WhatIf</span></span>
<span data-ttu-id="b8969-194">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8969-195">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8969-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8969-196">CommonParameters</span></span>
<span data-ttu-id="b8969-197">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b8969-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8969-198">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b8969-198">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8969-199">입력</span><span class="sxs-lookup"><span data-stu-id="b8969-199">INPUTS</span></span>

### <span data-ttu-id="b8969-200">System.String</span><span class="sxs-lookup"><span data-stu-id="b8969-200">System.String</span></span>

### <span data-ttu-id="b8969-201">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b8969-201">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="b8969-202">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="b8969-202">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="b8969-203">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b8969-203">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b8969-204">출력</span><span class="sxs-lookup"><span data-stu-id="b8969-204">OUTPUTS</span></span>

### <span data-ttu-id="b8969-205">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b8969-205">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="b8969-206">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b8969-206">NOTES</span></span>

## <span data-ttu-id="b8969-207">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8969-207">RELATED LINKS</span></span>

[<span data-ttu-id="b8969-208">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b8969-208">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="b8969-209">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b8969-209">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="b8969-210">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b8969-210">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
