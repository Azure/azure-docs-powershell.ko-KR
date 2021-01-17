---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: d99bde2839e1b4e91d6299cd47319827a57f4f33
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348297"
---
# <span data-ttu-id="116f4-101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="116f4-101">Set-AzStorageBlobContent</span></span>

## <span data-ttu-id="116f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="116f4-102">SYNOPSIS</span></span>
<span data-ttu-id="116f4-103">Azure Storage Blob에 로컬 파일을 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="116f4-104">구문</span><span class="sxs-lookup"><span data-stu-id="116f4-104">SYNTAX</span></span>

### <span data-ttu-id="116f4-105">SendManual(기본값)</span><span class="sxs-lookup"><span data-stu-id="116f4-105">SendManual (Default)</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>]
 [-StandardBlobTier <String>] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="116f4-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="116f4-106">ContainerPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="116f4-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="116f4-107">BlobPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>] [-Properties <Hashtable>]
 [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="116f4-108">설명</span><span class="sxs-lookup"><span data-stu-id="116f4-108">DESCRIPTION</span></span>
<span data-ttu-id="116f4-109">**Set-AzStorageBlobContent** cmdlet은 로컬 파일을 Azure Storage Blob에 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-109">The **Set-AzStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="116f4-110">예제</span><span class="sxs-lookup"><span data-stu-id="116f4-110">EXAMPLES</span></span>

### <span data-ttu-id="116f4-111">예제 1: 명명된 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="116f4-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="116f4-112">이 명령은 PlanningData라는 파일을 Planning2015라는 Blob에 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="116f4-113">예제 2: 현재 폴더 아래에 있는 모든 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="116f4-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="116f4-114">이 명령은 core Windows PowerShell cmdlet Get-ChildItem 사용하여 현재 폴더 및 하위 폴더에 있는 모든 파일을 다운로드한 다음 파이프라인 연산자를 사용하여 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="116f4-115">**Set-AzStorageBlobContent** cmdlet은 ContosoUploads라는 컨테이너에 파일을 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-115">The **Set-AzStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="116f4-116">예제 3: 기존 Blob 덮어 사용</span><span class="sxs-lookup"><span data-stu-id="116f4-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="116f4-117">이 명령은 Get-AzStorageBlob cmdlet을 사용하여 ContosoUploads 컨테이너에서 Planning2015라는 Blob을 끈 다음 해당 blob을 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="116f4-118">이 명령은 ContosoPlanning이라는 파일을 Planning2015로 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="116f4-119">이 명령은 Force 매개 *변수를 지정하지* 않습니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="116f4-120">이 명령은 확인을 요청하는 메시지를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="116f4-121">명령을 확인하는 경우 cmdlet은 기존 Blob을 덮어 덮어 습니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="116f4-122">예제 4: 파이프라인을 사용하여 컨테이너에 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="116f4-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="116f4-123">이 명령은 **Get-AzStorageContainer** cmdlet을 사용하여 ContosoUpload 문자열로 시작하는 컨테이너를 끈 다음, 해당 Blob을 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="116f4-124">이 명령은 ContosoPlanning이라는 파일을 Planning2015로 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="116f4-125">예제 5: 메타데이터가 있는 페이지 Blob에 파일 업로드 및 PremiumPageBlobTier를 P10으로 업로드</span><span class="sxs-lookup"><span data-stu-id="116f4-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="116f4-126">첫 번째 명령은 Blob에 대한 메타데이터를 포함하는 해시 테이블을 만들고 해당 해시 테이블을 $Metadata.</span><span class="sxs-lookup"><span data-stu-id="116f4-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="116f4-127">두 번째 명령은 ContosoPlanning이라는 파일을 ContosoUploads라는 컨테이너에 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="116f4-128">Blob은 $Metadata 메타데이터를 포함하며 PremiumPageBlobTier를 P10으로 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="116f4-129">예제 6: 지정된 Blob 속성을 사용하여 Blob에 파일을 업로드하고 StandardBlobTier를 쿨로 설정</span><span class="sxs-lookup"><span data-stu-id="116f4-129">Example 6: Upload a file to blob with specified blob properties, and set StandardBlobTier as Cool</span></span>
```
PS C:\> $filepath = "c:\temp\index.html"
PS C:\> Set-AzStorageBlobContent -File $filepath -Container "contosouploads" -Properties @{"ContentType" = [System.Web.MimeMapping]::GetMimeMapping($filepath); "ContentMD5" = "i727sP7HigloQDsqadNLHw=="} -StandardBlobTier Cool

   AccountName: storageaccountname, ContainerName: contosouploads

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
index.html           BlockBlob 403116          text/html                      2020-09-22 08:06:53Z Cool                                    False
```

<span data-ttu-id="116f4-130">이 명령은 지정된 blob 속성을 c:\temp\index.htmcontosouploads라는 컨테이너에 파일 c:\temp\index.htm파일을 업로드하고 StandardBlobTier를 쿨로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-130">This command uploads the file c:\temp\index.html to the container named contosouploads with specified blob properties, and set StandardBlobTier as Cool.</span></span>
<span data-ttu-id="116f4-131">이 명령은 [System.Web.MimeMapping]::GetMimeMapping() API를 통해 ContentType 값을 Blob 속성으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-131">This command gets ContentType value set to blob properties by [System.Web.MimeMapping]::GetMimeMapping() API.</span></span>

## <span data-ttu-id="116f4-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="116f4-132">PARAMETERS</span></span>

### <span data-ttu-id="116f4-133">-AsJob</span><span class="sxs-lookup"><span data-stu-id="116f4-133">-AsJob</span></span>
<span data-ttu-id="116f4-134">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-134">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="116f4-135">-Blob</span><span class="sxs-lookup"><span data-stu-id="116f4-135">-Blob</span></span>
<span data-ttu-id="116f4-136">Blob의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-136">Specifies the name of a blob.</span></span>
<span data-ttu-id="116f4-137">이 cmdlet은 이 매개 변수가 지정하는 Azure Storage Blob에 파일을 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-137">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="116f4-138">-BlobType</span><span class="sxs-lookup"><span data-stu-id="116f4-138">-BlobType</span></span>
<span data-ttu-id="116f4-139">이 cmdlet이 업로드하는 Blob의 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-139">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="116f4-140">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="116f4-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="116f4-141">차단</span><span class="sxs-lookup"><span data-stu-id="116f4-141">Block</span></span>
- <span data-ttu-id="116f4-142">페이지</span><span class="sxs-lookup"><span data-stu-id="116f4-142">Page</span></span>
- <span data-ttu-id="116f4-143">추가 기본값은 Block입니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-143">Append The default value is Block.</span></span>

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

### <span data-ttu-id="116f4-144">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="116f4-144">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="116f4-145">하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-145">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="116f4-146">이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-146">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="116f4-147">이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-147">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="116f4-148">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="116f4-148">-CloudBlob</span></span>
<span data-ttu-id="116f4-149">**CloudBlob** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-149">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="116f4-150">**CloudBlob 개체를 얻으면** Get-AzStorageBlob cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-150">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="116f4-151">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="116f4-151">-CloudBlobContainer</span></span>
<span data-ttu-id="116f4-152">Azure Storage 클라이언트 라이브러리에서 **CloudBlobContainer** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-152">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="116f4-153">이 cmdlet은 이 매개 변수가 지정하는 컨테이너의 Blob에 콘텐츠를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-153">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="116f4-154">**CloudBlobContainer** 개체를 얻습니다. Get-AzStorageContainer cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-154">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="116f4-155">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="116f4-155">-ConcurrentTaskCount</span></span>
<span data-ttu-id="116f4-156">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-156">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="116f4-157">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-157">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="116f4-158">지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-158">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="116f4-159">이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-159">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="116f4-160">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-160">The default value is 10.</span></span>

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

### <span data-ttu-id="116f4-161">-Container</span><span class="sxs-lookup"><span data-stu-id="116f4-161">-Container</span></span>
<span data-ttu-id="116f4-162">컨테이너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-162">Specifies the name of a container.</span></span>
<span data-ttu-id="116f4-163">이 cmdlet은 이 매개 변수가 지정하는 컨테이너의 Blob에 파일을 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-163">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="116f4-164">-Context</span><span class="sxs-lookup"><span data-stu-id="116f4-164">-Context</span></span>
<span data-ttu-id="116f4-165">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-165">Specifies an Azure storage context.</span></span>
<span data-ttu-id="116f4-166">저장소 컨텍스트를 얻습니다. New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-166">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="116f4-167">읽기 권한 없이 SAS 토큰에서 만든 저장소 컨텍스트를 사용하려면 -Force 매개 변수를 추가하여 Blob 존재 확인을 건너뛰야 합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-167">To use a storage context created from a SAS Token without read permission, need add -Force parameter to skip check blob existence.</span></span>

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

### <span data-ttu-id="116f4-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="116f4-168">-DefaultProfile</span></span>
<span data-ttu-id="116f4-169">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-169">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="116f4-170">-File</span><span class="sxs-lookup"><span data-stu-id="116f4-170">-File</span></span>
<span data-ttu-id="116f4-171">Blob 콘텐츠로 업로드할 파일의 로컬 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-171">Specifies a local file path for a file to upload as blob content.</span></span>

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

### <span data-ttu-id="116f4-172">-Force</span><span class="sxs-lookup"><span data-stu-id="116f4-172">-Force</span></span>
<span data-ttu-id="116f4-173">이 cmdlet이 확인을 묻는 메시지를 표시하지 않고 기존 Blob을 덮어 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-173">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="116f4-174">-Metadata</span><span class="sxs-lookup"><span data-stu-id="116f4-174">-Metadata</span></span>
<span data-ttu-id="116f4-175">업로드된 Blob에 대한 메타데이터를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-175">Specifies metadata for the uploaded blob.</span></span>

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

### <span data-ttu-id="116f4-176">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="116f4-176">-PremiumPageBlobTier</span></span>
<span data-ttu-id="116f4-177">페이지 Blob 계층</span><span class="sxs-lookup"><span data-stu-id="116f4-177">Page Blob Tier</span></span>

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

### <span data-ttu-id="116f4-178">-Properties</span><span class="sxs-lookup"><span data-stu-id="116f4-178">-Properties</span></span>
<span data-ttu-id="116f4-179">업로드된 Blob에 대한 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-179">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="116f4-180">지원되는 속성은 CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType입니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-180">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

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

### <span data-ttu-id="116f4-181">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="116f4-181">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="116f4-182">요청에 대한 서비스 쪽 시간제한 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-182">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="116f4-183">지정된 간격이 서비스에서 요청을 처리하기 전에 경과하면 저장소 서비스가 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-183">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="116f4-184">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="116f4-184">-StandardBlobTier</span></span>
<span data-ttu-id="116f4-185">블록 Blob 계층, 유효한 값은 핫/쿨/보관입니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-185">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="116f4-186">세부 정보 보기 https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="116f4-186">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

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

### <span data-ttu-id="116f4-187">-Confirm</span><span class="sxs-lookup"><span data-stu-id="116f4-187">-Confirm</span></span>
<span data-ttu-id="116f4-188">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="116f4-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="116f4-189">-WhatIf</span></span>
<span data-ttu-id="116f4-190">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="116f4-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="116f4-191">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="116f4-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="116f4-192">CommonParameters</span></span>
<span data-ttu-id="116f4-193">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="116f4-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="116f4-194">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="116f4-194">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="116f4-195">입력</span><span class="sxs-lookup"><span data-stu-id="116f4-195">INPUTS</span></span>

### <span data-ttu-id="116f4-196">System.String</span><span class="sxs-lookup"><span data-stu-id="116f4-196">System.String</span></span>

### <span data-ttu-id="116f4-197">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="116f4-197">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="116f4-198">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="116f4-198">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="116f4-199">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="116f4-199">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="116f4-200">출력</span><span class="sxs-lookup"><span data-stu-id="116f4-200">OUTPUTS</span></span>

### <span data-ttu-id="116f4-201">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="116f4-201">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="116f4-202">참고 사항</span><span class="sxs-lookup"><span data-stu-id="116f4-202">NOTES</span></span>

## <span data-ttu-id="116f4-203">관련 링크</span><span class="sxs-lookup"><span data-stu-id="116f4-203">RELATED LINKS</span></span>

[<span data-ttu-id="116f4-204">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="116f4-204">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="116f4-205">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="116f4-205">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="116f4-206">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="116f4-206">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
