---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/start-azurestoragefilecopy
schema: 2.0.0
ms.openlocfilehash: e12240ed399c458c176ab7e9439752ee6551f190
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882713"
---
# <span data-ttu-id="eaf05-101">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="eaf05-101">Start-AzureStorageFileCopy</span></span>

## <span data-ttu-id="eaf05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eaf05-102">SYNOPSIS</span></span>
<span data-ttu-id="eaf05-103">원본 파일 복사를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-103">Starts to copy a source file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eaf05-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eaf05-104">SYNTAX</span></span>

### <span data-ttu-id="eaf05-105">ContainerName</span><span class="sxs-lookup"><span data-stu-id="eaf05-105">ContainerName</span></span>
```
Start-AzureStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eaf05-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="eaf05-106">ContainerInstance</span></span>
```
Start-AzureStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eaf05-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="eaf05-107">BlobInstanceFilePath</span></span>
```
Start-AzureStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eaf05-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="eaf05-108">BlobInstanceFileInstance</span></span>
```
Start-AzureStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eaf05-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="eaf05-109">ShareName</span></span>
```
Start-AzureStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eaf05-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="eaf05-110">ShareInstance</span></span>
```
Start-AzureStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eaf05-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="eaf05-111">FileInstanceToFilePath</span></span>
```
Start-AzureStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eaf05-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="eaf05-112">FileInstanceToFileInstance</span></span>
```
Start-AzureStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eaf05-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="eaf05-113">UriToFilePath</span></span>
```
Start-AzureStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eaf05-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="eaf05-114">UriToFileInstance</span></span>
```
Start-AzureStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eaf05-115">설명은</span><span class="sxs-lookup"><span data-stu-id="eaf05-115">DESCRIPTION</span></span>
<span data-ttu-id="eaf05-116">**AzureStorageFileCopy** cmdlet은 원본 파일을 대상 파일에 복사 하는 데부터 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-116">The **Start-AzureStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="eaf05-117">예제의</span><span class="sxs-lookup"><span data-stu-id="eaf05-117">EXAMPLES</span></span>

### <span data-ttu-id="eaf05-118">예제 1: 공유 이름 및 파일 이름을 사용 하 여 파일에서 파일에 복사 작업 시작</span><span class="sxs-lookup"><span data-stu-id="eaf05-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzureStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="eaf05-119">이 명령은 파일에서 파일에 복사 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="eaf05-120">명령은 공유 이름 및 파일 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="eaf05-121">예제 2: 컨테이너 이름과 blob 이름을 사용 하 여 blob에서 파일로 복사 작업 시작</span><span class="sxs-lookup"><span data-stu-id="eaf05-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzureStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="eaf05-122">이 명령은 blob에서 파일로 복사 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="eaf05-123">명령이 컨테이너 이름 및 blob 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="eaf05-124">변수</span><span class="sxs-lookup"><span data-stu-id="eaf05-124">PARAMETERS</span></span>

### <span data-ttu-id="eaf05-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="eaf05-125">-AbsoluteUri</span></span>
<span data-ttu-id="eaf05-126">원본 파일의 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="eaf05-127">원본 위치에 자격 증명이 필요한 경우이를 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-127">If the source location requires a credential, you must provide one.</span></span>

```yaml
Type: System.String
Parameter Sets: UriToFilePath, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf05-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="eaf05-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="eaf05-129">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="eaf05-130">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="eaf05-131">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="eaf05-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="eaf05-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="eaf05-133">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="eaf05-134">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="eaf05-135">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="eaf05-136">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="eaf05-137">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-137">The default value is 10.</span></span>

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

### <span data-ttu-id="eaf05-138">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="eaf05-138">-Context</span></span>
<span data-ttu-id="eaf05-139">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="eaf05-140">컨텍스트를 가져오려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-140">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, ShareName
Aliases: SrcContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf05-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaf05-141">-DefaultProfile</span></span>
<span data-ttu-id="eaf05-142">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf05-143">DestContext</span><span class="sxs-lookup"><span data-stu-id="eaf05-143">-DestContext</span></span>
<span data-ttu-id="eaf05-144">대상의 Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-144">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="eaf05-145">컨텍스트를 얻으려면 **새-AzureStorageContext** 를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-145">To obtain a context, use **New-AzureStorageContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf05-146">-DestFile</span><span class="sxs-lookup"><span data-stu-id="eaf05-146">-DestFile</span></span>
<span data-ttu-id="eaf05-147">**Cloudfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-147">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="eaf05-148">클라우드 파일을 만들거나 Get-AzureStorageFile cmdlet을 사용 하 여 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-148">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: BlobInstanceFileInstance, FileInstanceToFileInstance, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf05-149">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="eaf05-149">-DestFilePath</span></span>
<span data-ttu-id="eaf05-150">대상 공유를 기준으로 대상 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-150">Specifies the path of the destination file relative to the destination share.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf05-151">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="eaf05-151">-DestShareName</span></span>
<span data-ttu-id="eaf05-152">대상 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-152">Specifies the name of the destination share.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance, BlobInstanceFilePath, ShareName, ShareInstance, FileInstanceToFilePath, UriToFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf05-153">-Force</span><span class="sxs-lookup"><span data-stu-id="eaf05-153">-Force</span></span>
<span data-ttu-id="eaf05-154">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="eaf05-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="eaf05-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="eaf05-156">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="eaf05-157">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="eaf05-157">-SrcBlob</span></span>
<span data-ttu-id="eaf05-158">**CloudBlob** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-158">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="eaf05-159">클라우드 blob을 만들거나 Get-AzureStorageBlob cmdlet을 사용 하 여 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-159">You can create a cloud blob or obtain one by using the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceFilePath, BlobInstanceFileInstance
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf05-160">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="eaf05-160">-SrcBlobName</span></span>
<span data-ttu-id="eaf05-161">원본 blob의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-161">Specifies the name of the source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf05-162">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="eaf05-162">-SrcContainer</span></span>
<span data-ttu-id="eaf05-163">클라우드 blob 컨테이너 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-163">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="eaf05-164">클라우드 blob 컨테이너 개체를 만들거나 Get-AzureStorageContainer cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-164">You can create cloud blob container object or use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf05-165">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="eaf05-165">-SrcContainerName</span></span>
<span data-ttu-id="eaf05-166">원본 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-166">Specifies the name of the source container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf05-167">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="eaf05-167">-SrcFile</span></span>
<span data-ttu-id="eaf05-168">**Cloudfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-168">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="eaf05-169">클라우드 파일을 만들거나 **AzureStorageFile** 를 사용 하 여 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-169">You can create a cloud file or obtain one by using **Get-AzureStorageFile**.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: FileInstanceToFilePath, FileInstanceToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eaf05-170">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="eaf05-170">-SrcFilePath</span></span>
<span data-ttu-id="eaf05-171">원본 디렉터리 또는 원본 공유에 상대적인 원본 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-171">Specifies the path of the source file relative to the source directory or source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, ShareInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf05-172">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="eaf05-172">-SrcShare</span></span>
<span data-ttu-id="eaf05-173">클라우드 파일 공유 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-173">Specifies a cloud file share object.</span></span>
<span data-ttu-id="eaf05-174">클라우드 파일 공유를 만들거나 Get-AzureStorageShare cmdlet을 사용 하 여 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-174">You can create a cloud file share or obtain one by using the Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf05-175">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="eaf05-175">-SrcShareName</span></span>
<span data-ttu-id="eaf05-176">원본 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-176">Specifies the name of the source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaf05-177">-확인</span><span class="sxs-lookup"><span data-stu-id="eaf05-177">-Confirm</span></span>
<span data-ttu-id="eaf05-178">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaf05-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaf05-179">-WhatIf</span></span>
<span data-ttu-id="eaf05-180">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eaf05-181">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaf05-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaf05-182">CommonParameters</span></span>
<span data-ttu-id="eaf05-183">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaf05-184">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaf05-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaf05-185">입력</span><span class="sxs-lookup"><span data-stu-id="eaf05-185">INPUTS</span></span>

### <span data-ttu-id="eaf05-186">WindowsAzure. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="eaf05-186">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="eaf05-187">WindowsAzure 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaf05-187">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="eaf05-188">매개 변수: SrcFile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="eaf05-188">Parameters: SrcFile (ByValue)</span></span>

### <span data-ttu-id="eaf05-189">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="eaf05-189">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="eaf05-190">출력</span><span class="sxs-lookup"><span data-stu-id="eaf05-190">OUTPUTS</span></span>

### <span data-ttu-id="eaf05-191">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="eaf05-191">System.Void</span></span>

## <span data-ttu-id="eaf05-192">상속자</span><span class="sxs-lookup"><span data-stu-id="eaf05-192">NOTES</span></span>

## <span data-ttu-id="eaf05-193">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eaf05-193">RELATED LINKS</span></span>

[<span data-ttu-id="eaf05-194">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="eaf05-194">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="eaf05-195">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="eaf05-195">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="eaf05-196">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="eaf05-196">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="eaf05-197">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="eaf05-197">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="eaf05-198">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="eaf05-198">Get-AzureStorageFileCopyState</span></span>](./Get-AzureStorageFileCopyState.md)

[<span data-ttu-id="eaf05-199">중지-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="eaf05-199">Stop-AzureStorageFileCopy</span></span>](./Stop-AzureStorageFileCopy.md)