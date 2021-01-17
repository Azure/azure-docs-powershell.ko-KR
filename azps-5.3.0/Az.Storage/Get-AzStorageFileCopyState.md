---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
ms.openlocfilehash: b87c4169fb2a7d417f56051c4996cf0428ceafe7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489292"
---
# <span data-ttu-id="ef992-101">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="ef992-101">Get-AzStorageFileCopyState</span></span>

## <span data-ttu-id="ef992-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef992-102">SYNOPSIS</span></span>
<span data-ttu-id="ef992-103">복사 작업의 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ef992-103">Gets the state of a copy operation.</span></span>

## <span data-ttu-id="ef992-104">구문</span><span class="sxs-lookup"><span data-stu-id="ef992-104">SYNTAX</span></span>

### <span data-ttu-id="ef992-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="ef992-105">ShareName</span></span>
```
Get-AzStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="ef992-106">파일</span><span class="sxs-lookup"><span data-stu-id="ef992-106">File</span></span>
```
Get-AzStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef992-107">설명</span><span class="sxs-lookup"><span data-stu-id="ef992-107">DESCRIPTION</span></span>
<span data-ttu-id="ef992-108">**Get-AzStorageFileCopyState** cmdlet은 Azure Storage 파일 복사 작업의 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ef992-108">The **Get-AzStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>
<span data-ttu-id="ef992-109">복사 대상 파일에서 실행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef992-109">It should run on the copy destination file.</span></span>

## <span data-ttu-id="ef992-110">예제</span><span class="sxs-lookup"><span data-stu-id="ef992-110">EXAMPLES</span></span>

### <span data-ttu-id="ef992-111">예제 1: 파일 이름으로 복사 상태 얻기</span><span class="sxs-lookup"><span data-stu-id="ef992-111">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="ef992-112">이 명령은 지정된 이름이 있는 파일에 대한 복사 작업의 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ef992-112">This command gets the state of the copy operation for a file that has the specified name.</span></span>

### <span data-ttu-id="ef992-113">예제 2: 복사 및 파이프라인을 시작하여 복사 상태 얻기</span><span class="sxs-lookup"><span data-stu-id="ef992-113">Example 2: Start Copy and pipeline to get the copy status</span></span>
```
C:\PS> $destfile = Start-AzStorageFileCopy -SrcShareName "contososhare" -SrcFilePath "contosofile" -DestShareName "contososhare2" -destfilepath "contosofile_copy"  

C:\PS> $destfile | Get-AzStorageFileCopyState
```

<span data-ttu-id="ef992-114">첫 번째 명령은 "contosofile" 파일을 "contosofile_copy"로 복사하고 destiantion 파일 개체를 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="ef992-114">The first command starts copy file "contosofile" to "contosofile_copy", and output the destiantion file object.</span></span> <span data-ttu-id="ef992-115">두 번째 명령 파이프라인은 Destiantion 파일 개체를 Get-AzStorageFileCopyState로 파이프라인하여 파일 복사 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ef992-115">The second command pipeline the destiantion file object to Get-AzStorageFileCopyState, to get file copy state.</span></span>

## <span data-ttu-id="ef992-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef992-116">PARAMETERS</span></span>

### <span data-ttu-id="ef992-117">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ef992-117">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ef992-118">하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef992-118">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ef992-119">이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="ef992-119">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ef992-120">이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ef992-120">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ef992-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ef992-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ef992-122">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef992-122">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ef992-123">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef992-123">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ef992-124">지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ef992-124">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ef992-125">이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef992-125">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ef992-126">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="ef992-126">The default value is 10.</span></span>

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

### <span data-ttu-id="ef992-127">-Context</span><span class="sxs-lookup"><span data-stu-id="ef992-127">-Context</span></span>
<span data-ttu-id="ef992-128">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef992-128">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="ef992-129">컨텍스트를 얻습니다. [New-AzStorageContext](./New-AzStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef992-129">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef992-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef992-130">-DefaultProfile</span></span>
<span data-ttu-id="ef992-131">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ef992-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef992-132">-File</span><span class="sxs-lookup"><span data-stu-id="ef992-132">-File</span></span>
<span data-ttu-id="ef992-133">**CloudFile** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef992-133">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="ef992-134">클라우드 파일을 만들거나 다음 cmdlet을 사용하여 Get-AzStorageFile 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef992-134">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef992-135">-FilePath</span><span class="sxs-lookup"><span data-stu-id="ef992-135">-FilePath</span></span>
<span data-ttu-id="ef992-136">Azure Storage 공유를 상대로 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef992-136">Specifies the path of the file relative to an Azure Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef992-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ef992-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ef992-138">요청의 서버 부분에 대한 시간 제한 기간의 길이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef992-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="ef992-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="ef992-139">-ShareName</span></span>
<span data-ttu-id="ef992-140">공유의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef992-140">Specifies the name of a share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef992-141">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="ef992-141">-WaitForComplete</span></span>
<span data-ttu-id="ef992-142">이 cmdlet이 복사본이 완료될 때까지 기다렸다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ef992-142">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="ef992-143">이 매개 변수를 지정하지 않으면 이 cmdlet은 결과를 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ef992-143">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="ef992-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef992-144">CommonParameters</span></span>
<span data-ttu-id="ef992-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ef992-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef992-146">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ef992-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef992-147">입력</span><span class="sxs-lookup"><span data-stu-id="ef992-147">INPUTS</span></span>

### <span data-ttu-id="ef992-148">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="ef992-148">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="ef992-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ef992-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ef992-150">출력</span><span class="sxs-lookup"><span data-stu-id="ef992-150">OUTPUTS</span></span>

### <span data-ttu-id="ef992-151">Microsoft.Azure.Storage.File.CopyState</span><span class="sxs-lookup"><span data-stu-id="ef992-151">Microsoft.Azure.Storage.File.CopyState</span></span>

## <span data-ttu-id="ef992-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ef992-152">NOTES</span></span>

## <span data-ttu-id="ef992-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef992-153">RELATED LINKS</span></span>

[<span data-ttu-id="ef992-154">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="ef992-154">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="ef992-155">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ef992-155">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="ef992-156">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ef992-156">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)

[<span data-ttu-id="ef992-157">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ef992-157">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
