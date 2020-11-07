---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: d9a602e3e946e28dd04b67c030aeec2aecc3ec93
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698544"
---
# <span data-ttu-id="fc1b7-101">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="fc1b7-101">Set-AzStorageBlobContent</span></span>

## <span data-ttu-id="fc1b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc1b7-102">SYNOPSIS</span></span>
<span data-ttu-id="fc1b7-103">Azure 저장소 blob에 로컬 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="fc1b7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fc1b7-104">SYNTAX</span></span>

### <span data-ttu-id="fc1b7-105">SendManual (기본값)</span><span class="sxs-lookup"><span data-stu-id="fc1b7-105">SendManual (Default)</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc1b7-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="fc1b7-106">ContainerPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force] [-AsJob] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc1b7-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="fc1b7-107">BlobPipeline</span></span>
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>] [-Properties <Hashtable>]
 [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc1b7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="fc1b7-108">DESCRIPTION</span></span>
<span data-ttu-id="fc1b7-109">**AzStorageBlobContent** cmdlet은 로컬 파일을 Azure Storage blob에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-109">The **Set-AzStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="fc1b7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fc1b7-110">EXAMPLES</span></span>

### <span data-ttu-id="fc1b7-111">예제 1: 명명 된 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="fc1b7-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="fc1b7-112">이 명령은 PlanningData 이라는 파일을 Planning2015 라는 blob에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="fc1b7-113">예제 2: 현재 폴더 아래의 모든 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="fc1b7-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="fc1b7-114">이 명령은 핵심 Windows PowerShell cmdlet Get-ChildItem를 사용 하 여 현재 폴더 및 하위 폴더에 있는 모든 파일을 가져오고 파이프라인 연산자를 사용 하 여 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fc1b7-115">**AzStorageBlobContent** Cmdlet은 ContosoUploads 라는 컨테이너에 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-115">The **Set-AzStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="fc1b7-116">예제 3: 기존 blob 덮어쓰기</span><span class="sxs-lookup"><span data-stu-id="fc1b7-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="fc1b7-117">이 명령은 Get-AzStorageBlob cmdlet을 사용 하 여 ContosoUploads 컨테이너의 Planning2015 라는 blob을 가져온 다음 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="fc1b7-118">명령이 ContosoPlanning as Planning2015 라는 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="fc1b7-119">이 명령은 *Force* 매개 변수를 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="fc1b7-120">명령에서 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="fc1b7-121">명령을 확인 하면 cmdlet이 기존 blob을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="fc1b7-122">예제 4: 파이프라인을 사용 하 여 컨테이너에 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="fc1b7-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="fc1b7-123">이 명령은 **AzStorageContainer** cmdlet을 사용 하 여 ContosoUpload 문자열로 시작 하는 컨테이너를 가져온 다음 현재 cmdlet에 해당 blob을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="fc1b7-124">명령이 ContosoPlanning as Planning2015 라는 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="fc1b7-125">예제 5: 메타 데이터 및 PremiumPageBlobTier as P10를 사용 하 여 페이지 blob에 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="fc1b7-125">Example 5: Upload a file to page blob with metadata and PremiumPageBlobTier as P10</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

<span data-ttu-id="fc1b7-126">첫 번째 명령은 blob에 대 한 메타 데이터를 포함 하는 해시 테이블을 만들고이 해시 테이블을 $Metadata 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>
<span data-ttu-id="fc1b7-127">두 번째 명령은 ContosoPlanning 이라는 파일을 ContosoUploads 이라는 컨테이너에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="fc1b7-128">Blob에는 $Metadata에 저장 된 메타 데이터가 포함 되며 P10로 PremiumPageBlobTier 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-128">The blob includes the metadata stored in $Metadata, and has PremiumPageBlobTier as P10.</span></span>

### <span data-ttu-id="fc1b7-129">예제 6: 지정 된 blob 속성으로 파일을 blob에 업로드</span><span class="sxs-lookup"><span data-stu-id="fc1b7-129">Example 6: Upload a file to blob with specified blob properties</span></span>
```
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Properties @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="}
```

<span data-ttu-id="fc1b7-130">이 명령은 ContosoPlanning 이라는 파일을 지정 된 blob 속성을 갖는 ContosoUploads 이라는 컨테이너에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-130">This command  uploads the file that is named ContosoPlanning to the container named ContosoUploads with specified blob properties.</span></span>

## <span data-ttu-id="fc1b7-131">변수</span><span class="sxs-lookup"><span data-stu-id="fc1b7-131">PARAMETERS</span></span>

### <span data-ttu-id="fc1b7-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc1b7-132">-AsJob</span></span>
<span data-ttu-id="fc1b7-133">백그라운드에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-133">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="fc1b7-134">-Blob</span><span class="sxs-lookup"><span data-stu-id="fc1b7-134">-Blob</span></span>
<span data-ttu-id="fc1b7-135">Blob의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-135">Specifies the name of a blob.</span></span>
<span data-ttu-id="fc1b7-136">이 cmdlet은이 매개 변수에서 지정 하는 Azure 저장소 blob에 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-136">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="fc1b7-137">-BlobType</span><span class="sxs-lookup"><span data-stu-id="fc1b7-137">-BlobType</span></span>
<span data-ttu-id="fc1b7-138">이 cmdlet이 업로드 하는 blob의 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-138">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="fc1b7-139">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fc1b7-140">않도록</span><span class="sxs-lookup"><span data-stu-id="fc1b7-140">Block</span></span>
- <span data-ttu-id="fc1b7-141">페이지 기본값은 Block입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-141">Page The default value is Block.</span></span>

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

### <span data-ttu-id="fc1b7-142">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fc1b7-142">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fc1b7-143">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-143">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="fc1b7-144">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-144">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="fc1b7-145">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-145">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="fc1b7-146">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="fc1b7-146">-CloudBlob</span></span>
<span data-ttu-id="fc1b7-147">**CloudBlob** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-147">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="fc1b7-148">**CloudBlob** 개체를 가져오려면 Get-AzStorageBlob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-148">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc1b7-149">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="fc1b7-149">-CloudBlobContainer</span></span>
<span data-ttu-id="fc1b7-150">Azure Storage 클라이언트 라이브러리에서 **CloudBlobContainer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-150">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="fc1b7-151">이 cmdlet은이 매개 변수에서 지정 하는 컨테이너의 blob에 콘텐츠를 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-151">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="fc1b7-152">**CloudBlobContainer** 개체를 가져오려면 Get-AzStorageContainer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-152">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc1b7-153">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fc1b7-153">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fc1b7-154">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-154">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="fc1b7-155">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-155">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="fc1b7-156">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-156">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="fc1b7-157">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-157">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="fc1b7-158">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-158">The default value is 10.</span></span>

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

### <span data-ttu-id="fc1b7-159">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="fc1b7-159">-Container</span></span>
<span data-ttu-id="fc1b7-160">컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-160">Specifies the name of a container.</span></span>
<span data-ttu-id="fc1b7-161">이 cmdlet은이 매개 변수에서 지정 하는 컨테이너의 blob에 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-161">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="fc1b7-162">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="fc1b7-162">-Context</span></span>
<span data-ttu-id="fc1b7-163">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-163">Specifies an Azure storage context.</span></span>
<span data-ttu-id="fc1b7-164">저장소 컨텍스트를 얻으려면 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-164">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="fc1b7-165">읽기 권한 없이 SAS 토큰에서 만들어진 저장소 컨텍스트를 사용 하려면-Force 매개 변수 추가를 생략 하 여 blob existance 검사를 건너뛰십시오.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-165">To use a storage context created from a SAS Token without read permission, need add -Force parameter to skip check blob existance.</span></span>

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

### <span data-ttu-id="fc1b7-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc1b7-166">-DefaultProfile</span></span>
<span data-ttu-id="fc1b7-167">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-167">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc1b7-168">-파일</span><span class="sxs-lookup"><span data-stu-id="fc1b7-168">-File</span></span>
<span data-ttu-id="fc1b7-169">Blob content로 업로드할 파일의 로컬 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-169">Specifies a local file path for a file to upload as blob content.</span></span>

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

### <span data-ttu-id="fc1b7-170">-Force</span><span class="sxs-lookup"><span data-stu-id="fc1b7-170">-Force</span></span>
<span data-ttu-id="fc1b7-171">이 cmdlet이 확인 메시지를 표시 하지 않고 기존 blob을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-171">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="fc1b7-172">-Metadata</span><span class="sxs-lookup"><span data-stu-id="fc1b7-172">-Metadata</span></span>
<span data-ttu-id="fc1b7-173">업로드 된 blob에 대 한 메타 데이터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-173">Specifies metadata for the uploaded blob.</span></span>

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

### <span data-ttu-id="fc1b7-174">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="fc1b7-174">-PremiumPageBlobTier</span></span>
<span data-ttu-id="fc1b7-175">페이지 Blob 계층</span><span class="sxs-lookup"><span data-stu-id="fc1b7-175">Page Blob Tier</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc1b7-176">-속성</span><span class="sxs-lookup"><span data-stu-id="fc1b7-176">-Properties</span></span>
<span data-ttu-id="fc1b7-177">업로드 된 blob에 대 한 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-177">Specifies properties for the uploaded blob.</span></span> <span data-ttu-id="fc1b7-178">지원 되는 속성은 CacheControl, ContentDisposition, Contentdisposition, Contentdisposition, ContentMD5, ContentType입니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-178">The supported properties are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>

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

### <span data-ttu-id="fc1b7-179">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fc1b7-179">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fc1b7-180">요청에 대 한 서비스 측 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-180">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="fc1b7-181">서비스가 요청을 처리 하기 전에 지정 된 간격이 경과 하면 저장소 서비스에서 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-181">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="fc1b7-182">-확인</span><span class="sxs-lookup"><span data-stu-id="fc1b7-182">-Confirm</span></span>
<span data-ttu-id="fc1b7-183">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc1b7-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc1b7-184">-WhatIf</span></span>
<span data-ttu-id="fc1b7-185">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc1b7-186">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc1b7-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc1b7-187">CommonParameters</span></span>
<span data-ttu-id="fc1b7-188">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc1b7-189">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc1b7-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc1b7-190">입력</span><span class="sxs-lookup"><span data-stu-id="fc1b7-190">INPUTS</span></span>

### <span data-ttu-id="fc1b7-191">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fc1b7-191">System.String</span></span>

### <span data-ttu-id="fc1b7-192">WindowsAzure. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="fc1b7-192">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="fc1b7-193">WindowsAzure. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="fc1b7-193">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="fc1b7-194">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fc1b7-194">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fc1b7-195">출력</span><span class="sxs-lookup"><span data-stu-id="fc1b7-195">OUTPUTS</span></span>

### <span data-ttu-id="fc1b7-196">WindowsAzure. ResourceModel. m b m.</span><span class="sxs-lookup"><span data-stu-id="fc1b7-196">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="fc1b7-197">상속자</span><span class="sxs-lookup"><span data-stu-id="fc1b7-197">NOTES</span></span>

## <span data-ttu-id="fc1b7-198">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc1b7-198">RELATED LINKS</span></span>

[<span data-ttu-id="fc1b7-199">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="fc1b7-199">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="fc1b7-200">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="fc1b7-200">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="fc1b7-201">제거-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="fc1b7-201">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
