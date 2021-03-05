---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A96A1A67-6C9C-499F-9935-B90F7ACEB50E
online version: https://docs.microsoft.com/powershell/module/az.storage/start-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageFileCopy.md
ms.openlocfilehash: 2b3bea343e5d4e2267c2bec14d60564392914a0d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960075"
---
# <span data-ttu-id="f0730-101">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f0730-101">Start-AzStorageFileCopy</span></span>

## <span data-ttu-id="f0730-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0730-102">SYNOPSIS</span></span>
<span data-ttu-id="f0730-103">원본 파일을 복사하기 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-103">Starts to copy a source file.</span></span>

## <span data-ttu-id="f0730-104">구문</span><span class="sxs-lookup"><span data-stu-id="f0730-104">SYNTAX</span></span>

### <span data-ttu-id="f0730-105">ContainerName</span><span class="sxs-lookup"><span data-stu-id="f0730-105">ContainerName</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainerName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0730-106">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="f0730-106">ContainerInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlobName <String> -SrcContainer <CloudBlobContainer> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0730-107">BlobInstanceFilePath</span><span class="sxs-lookup"><span data-stu-id="f0730-107">BlobInstanceFilePath</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0730-108">BlobInstanceFileInstance</span><span class="sxs-lookup"><span data-stu-id="f0730-108">BlobInstanceFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcBlob <CloudBlob> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0730-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="f0730-109">ShareName</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShareName <String> -DestShareName <String>
 -DestFilePath <String> [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0730-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="f0730-110">ShareInstance</span></span>
```
Start-AzStorageFileCopy -SrcFilePath <String> -SrcShare <CloudFileShare> -DestShareName <String>
 -DestFilePath <String> [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0730-111">FileInstanceToFilePath</span><span class="sxs-lookup"><span data-stu-id="f0730-111">FileInstanceToFilePath</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0730-112">FileInstanceToFileInstance</span><span class="sxs-lookup"><span data-stu-id="f0730-112">FileInstanceToFileInstance</span></span>
```
Start-AzStorageFileCopy -SrcFile <CloudFile> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0730-113">UriToFilePath</span><span class="sxs-lookup"><span data-stu-id="f0730-113">UriToFilePath</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestShareName <String> -DestFilePath <String>
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0730-114">UriToFileInstance</span><span class="sxs-lookup"><span data-stu-id="f0730-114">UriToFileInstance</span></span>
```
Start-AzStorageFileCopy -AbsoluteUri <String> -DestFile <CloudFile> [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0730-115">설명</span><span class="sxs-lookup"><span data-stu-id="f0730-115">DESCRIPTION</span></span>
<span data-ttu-id="f0730-116">**Start-AzStorageFileCopy** cmdlet은 원본 파일을 대상 파일에 복사하기 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-116">The **Start-AzStorageFileCopy** cmdlet starts to copy a source file to a destination file.</span></span>

## <span data-ttu-id="f0730-117">예제</span><span class="sxs-lookup"><span data-stu-id="f0730-117">EXAMPLES</span></span>

### <span data-ttu-id="f0730-118">예제 1: 공유 이름 및 파일 이름을 사용하여 파일에서 파일로 복사 작업 시작</span><span class="sxs-lookup"><span data-stu-id="f0730-118">Example 1: Start copy operation from file to file by using share name and file name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcShareName "ContosoShare01" -SrcFilePath "FilePath01" -DestShareName "ContosoShare02" -DestFilePath "FilePath02"
```

<span data-ttu-id="f0730-119">이 명령은 파일에서 파일로 복사 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-119">This command starts a copy operation from file to file.</span></span>
<span data-ttu-id="f0730-120">명령은 공유 이름 및 파일 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-120">The command specifies share name and file name</span></span>

### <span data-ttu-id="f0730-121">예제 2: 컨테이너 이름 및 Blob 이름을 사용하여 Blob에서 파일로 복사 작업 시작</span><span class="sxs-lookup"><span data-stu-id="f0730-121">Example 2: Start copy operation from blob to file by using container name and blob name</span></span>
```
PS C:\>Start-AzStorageFileCopy -SrcContainerName "ContosoContainer01" -SrcBlobName "ContosoBlob01" -DestShareName "ContosoShare" -DestFilePath "FilePath02"
```

<span data-ttu-id="f0730-122">이 명령은 Blob에서 파일로 복사 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-122">This command starts a copy operation from blob to file.</span></span>
<span data-ttu-id="f0730-123">명령은 컨테이너 이름 및 Blob 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-123">The command specifies container name and blob name</span></span>

## <span data-ttu-id="f0730-124">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f0730-124">PARAMETERS</span></span>

### <span data-ttu-id="f0730-125">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="f0730-125">-AbsoluteUri</span></span>
<span data-ttu-id="f0730-126">원본 파일의 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-126">Specifies the URI of the source file.</span></span>
<span data-ttu-id="f0730-127">원본 위치에 자격 증명이 필요한 경우 자격 증명을 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-127">If the source location requires a credential, you must provide one.</span></span>

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

### <span data-ttu-id="f0730-128">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f0730-128">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f0730-129">하나의 서비스 요청에 대해 클라이언트 쪽 시간 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-129">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f0730-130">지정된 간격에서 이전 호출이 실패하면 이 cmdlet에서 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-130">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f0730-131">간격이 경과하기 전에 이 cmdlet에서 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-131">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f0730-132">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f0730-132">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f0730-133">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-133">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f0730-134">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 로컬 CPU 및 대역폭 사용량을 제한하는 동시성 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-134">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f0730-135">지정된 값은 절대 개수로 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-135">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f0730-136">이 매개 변수는 초당 100킬로비트와 같은 대역폭이 낮은 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-136">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f0730-137">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-137">The default value is 10.</span></span>

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

### <span data-ttu-id="f0730-138">-Context</span><span class="sxs-lookup"><span data-stu-id="f0730-138">-Context</span></span>
<span data-ttu-id="f0730-139">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-139">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="f0730-140">컨텍스트를 얻지 위해 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-140">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f0730-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0730-141">-DefaultProfile</span></span>
<span data-ttu-id="f0730-142">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0730-143">-DestContext</span><span class="sxs-lookup"><span data-stu-id="f0730-143">-DestContext</span></span>
<span data-ttu-id="f0730-144">대상의 Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-144">Specifies the Azure Storage context of the destination.</span></span>
<span data-ttu-id="f0730-145">컨텍스트를 얻은 경우 **New-AzStorageContext 를 사용 합니다.**</span><span class="sxs-lookup"><span data-stu-id="f0730-145">To obtain a context, use **New-AzStorageContext**.</span></span>

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

### <span data-ttu-id="f0730-146">-DestFile</span><span class="sxs-lookup"><span data-stu-id="f0730-146">-DestFile</span></span>
<span data-ttu-id="f0730-147">**CloudFile 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="f0730-147">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="f0730-148">클라우드 파일을 만들거나 cmdlet을 사용하여 Get-AzStorageFile 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-148">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: BlobInstanceFileInstance, FileInstanceToFileInstance, UriToFileInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0730-149">-DestFilePath</span><span class="sxs-lookup"><span data-stu-id="f0730-149">-DestFilePath</span></span>
<span data-ttu-id="f0730-150">대상 공유를 상대로 대상 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-150">Specifies the path of the destination file relative to the destination share.</span></span>

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

### <span data-ttu-id="f0730-151">-DestShareName</span><span class="sxs-lookup"><span data-stu-id="f0730-151">-DestShareName</span></span>
<span data-ttu-id="f0730-152">대상 공유의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-152">Specifies the name of the destination share.</span></span>

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

### <span data-ttu-id="f0730-153">-Force</span><span class="sxs-lookup"><span data-stu-id="f0730-153">-Force</span></span>
<span data-ttu-id="f0730-154">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-154">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f0730-155">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f0730-155">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f0730-156">요청의 서버 부분에 대한 시간 제한 기간의 길이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-156">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="f0730-157">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="f0730-157">-SrcBlob</span></span>
<span data-ttu-id="f0730-158">**CloudBlob 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="f0730-158">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="f0730-159">클라우드 Blob을 만들거나 cmdlet을 사용하여 클라우드 blob을 만들거나 Get-AzStorageBlob 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-159">You can create a cloud blob or obtain one by using the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceFilePath, BlobInstanceFileInstance
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0730-160">-SrcBlobName</span><span class="sxs-lookup"><span data-stu-id="f0730-160">-SrcBlobName</span></span>
<span data-ttu-id="f0730-161">원본 Blob의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-161">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="f0730-162">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="f0730-162">-SrcContainer</span></span>
<span data-ttu-id="f0730-163">클라우드 Blob 컨테이너 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-163">Specifies a cloud blob container object.</span></span>
<span data-ttu-id="f0730-164">클라우드 Blob 컨테이너 개체를 만들거나 cmdlet을 Get-AzStorageContainer 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-164">You can create cloud blob container object or use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0730-165">-SrcContainerName</span><span class="sxs-lookup"><span data-stu-id="f0730-165">-SrcContainerName</span></span>
<span data-ttu-id="f0730-166">원본 컨테이너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-166">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="f0730-167">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="f0730-167">-SrcFile</span></span>
<span data-ttu-id="f0730-168">**CloudFile 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="f0730-168">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="f0730-169">**Get-AzStorageFile** 을 사용하여 클라우드 파일을 만들거나 파일을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-169">You can create a cloud file or obtain one by using **Get-AzStorageFile**.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileInstanceToFilePath, FileInstanceToFileInstance
Aliases: CloudFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0730-170">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="f0730-170">-SrcFilePath</span></span>
<span data-ttu-id="f0730-171">원본 디렉터리 또는 원본 공유를 상대로 원본 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-171">Specifies the path of the source file relative to the source directory or source share.</span></span>

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

### <span data-ttu-id="f0730-172">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="f0730-172">-SrcShare</span></span>
<span data-ttu-id="f0730-173">클라우드 파일 공유 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-173">Specifies a cloud file share object.</span></span>
<span data-ttu-id="f0730-174">클라우드 파일 공유를 만들거나 cmdlet을 사용하여 Get-AzStorageShare 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-174">You can create a cloud file share or obtain one by using the Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases: CloudFileShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0730-175">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="f0730-175">-SrcShareName</span></span>
<span data-ttu-id="f0730-176">원본 공유의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-176">Specifies the name of the source share.</span></span>

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

### <span data-ttu-id="f0730-177">-확인</span><span class="sxs-lookup"><span data-stu-id="f0730-177">-Confirm</span></span>
<span data-ttu-id="f0730-178">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-178">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0730-179">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0730-179">-WhatIf</span></span>
<span data-ttu-id="f0730-180">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-180">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0730-181">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-181">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0730-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0730-182">CommonParameters</span></span>
<span data-ttu-id="f0730-183">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f0730-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0730-184">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f0730-184">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0730-185">입력</span><span class="sxs-lookup"><span data-stu-id="f0730-185">INPUTS</span></span>

### <span data-ttu-id="f0730-186">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="f0730-186">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="f0730-187">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="f0730-187">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="f0730-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f0730-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f0730-189">출력</span><span class="sxs-lookup"><span data-stu-id="f0730-189">OUTPUTS</span></span>

### <span data-ttu-id="f0730-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="f0730-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="f0730-191">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f0730-191">NOTES</span></span>

## <span data-ttu-id="f0730-192">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f0730-192">RELATED LINKS</span></span>

[<span data-ttu-id="f0730-193">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="f0730-193">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="f0730-194">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f0730-194">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="f0730-195">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="f0730-195">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="f0730-196">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="f0730-196">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="f0730-197">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="f0730-197">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="f0730-198">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f0730-198">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
