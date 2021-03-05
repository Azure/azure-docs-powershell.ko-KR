---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
ms.openlocfilehash: c86a2d616334729df6b7fa57a25cc51750bbff1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981499"
---
# <span data-ttu-id="f6707-101">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="f6707-101">Get-AzStorageFileCopyState</span></span>

## <span data-ttu-id="f6707-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6707-102">SYNOPSIS</span></span>
<span data-ttu-id="f6707-103">복사 작업의 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f6707-103">Gets the state of a copy operation.</span></span>

## <span data-ttu-id="f6707-104">구문</span><span class="sxs-lookup"><span data-stu-id="f6707-104">SYNTAX</span></span>

### <span data-ttu-id="f6707-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="f6707-105">ShareName</span></span>
```
Get-AzStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="f6707-106">파일</span><span class="sxs-lookup"><span data-stu-id="f6707-106">File</span></span>
```
Get-AzStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6707-107">설명</span><span class="sxs-lookup"><span data-stu-id="f6707-107">DESCRIPTION</span></span>
<span data-ttu-id="f6707-108">**Get-AzStorageFileCopyState** cmdlet은 Azure Storage 파일 복사 작업의 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f6707-108">The **Get-AzStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>
<span data-ttu-id="f6707-109">복사 대상 파일에서 실행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6707-109">It should run on the copy destination file.</span></span>

## <span data-ttu-id="f6707-110">예제</span><span class="sxs-lookup"><span data-stu-id="f6707-110">EXAMPLES</span></span>

### <span data-ttu-id="f6707-111">예제 1: 파일 이름으로 복사 상태 얻기</span><span class="sxs-lookup"><span data-stu-id="f6707-111">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="f6707-112">이 명령은 지정된 이름이 있는 파일에 대한 복사 작업의 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f6707-112">This command gets the state of the copy operation for a file that has the specified name.</span></span>

### <span data-ttu-id="f6707-113">예제 2: 복사 및 파이프라인 시작을 통해 복사 상태를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6707-113">Example 2: Start Copy and pipeline to get the copy status</span></span>
```
C:\PS> $destfile = Start-AzStorageFileCopy -SrcShareName "contososhare" -SrcFilePath "contosofile" -DestShareName "contososhare2" -destfilepath "contosofile_copy"  

C:\PS> $destfile | Get-AzStorageFileCopyState
```

<span data-ttu-id="f6707-114">첫 번째 명령은 복사 파일 "contosofile"을 "contosofile_copy"로 시작하고 destiantion 파일 개체를 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="f6707-114">The first command starts copy file "contosofile" to "contosofile_copy", and output the destiantion file object.</span></span> <span data-ttu-id="f6707-115">두 번째 명령 파이프라인은 Get-AzStorageFileCopyState로 destiantion 파일 개체를 파이프라인하여 파일 복사 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f6707-115">The second command pipeline the destiantion file object to Get-AzStorageFileCopyState, to get file copy state.</span></span>

## <span data-ttu-id="f6707-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f6707-116">PARAMETERS</span></span>

### <span data-ttu-id="f6707-117">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f6707-117">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f6707-118">하나의 서비스 요청에 대해 클라이언트 쪽 시간 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6707-118">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f6707-119">지정된 간격에서 이전 호출이 실패하면 이 cmdlet에서 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="f6707-119">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f6707-120">간격이 경과하기 전에 이 cmdlet에서 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f6707-120">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f6707-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f6707-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f6707-122">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6707-122">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f6707-123">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 로컬 CPU 및 대역폭 사용량을 제한하는 동시성 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6707-123">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f6707-124">지정된 값은 절대 개수로 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f6707-124">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f6707-125">이 매개 변수는 초당 100킬로비트와 같은 대역폭이 낮은 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6707-125">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f6707-126">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="f6707-126">The default value is 10.</span></span>

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

### <span data-ttu-id="f6707-127">-Context</span><span class="sxs-lookup"><span data-stu-id="f6707-127">-Context</span></span>
<span data-ttu-id="f6707-128">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6707-128">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="f6707-129">컨텍스트를 얻은 경우 [New-AzStorageContext](./New-AzStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6707-129">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="f6707-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6707-130">-DefaultProfile</span></span>
<span data-ttu-id="f6707-131">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f6707-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6707-132">-File</span><span class="sxs-lookup"><span data-stu-id="f6707-132">-File</span></span>
<span data-ttu-id="f6707-133">**CloudFile 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="f6707-133">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="f6707-134">클라우드 파일을 만들거나 cmdlet을 사용하여 Get-AzStorageFile 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6707-134">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="f6707-135">-FilePath</span><span class="sxs-lookup"><span data-stu-id="f6707-135">-FilePath</span></span>
<span data-ttu-id="f6707-136">Azure Storage 공유를 상대로 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6707-136">Specifies the path of the file relative to an Azure Storage share.</span></span>

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

### <span data-ttu-id="f6707-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f6707-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f6707-138">요청의 서버 부분에 대한 시간 제한 기간의 길이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6707-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="f6707-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="f6707-139">-ShareName</span></span>
<span data-ttu-id="f6707-140">공유의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6707-140">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="f6707-141">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="f6707-141">-WaitForComplete</span></span>
<span data-ttu-id="f6707-142">이 cmdlet은 복사본이 완료될 때까지 기다렸다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="f6707-142">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="f6707-143">이 매개 변수를 지정하지 않으면 이 cmdlet은 결과를 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f6707-143">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="f6707-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6707-144">CommonParameters</span></span>
<span data-ttu-id="f6707-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f6707-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6707-146">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f6707-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6707-147">입력</span><span class="sxs-lookup"><span data-stu-id="f6707-147">INPUTS</span></span>

### <span data-ttu-id="f6707-148">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="f6707-148">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="f6707-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f6707-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f6707-150">출력</span><span class="sxs-lookup"><span data-stu-id="f6707-150">OUTPUTS</span></span>

### <span data-ttu-id="f6707-151">Microsoft.Azure.Storage.File.CopyState</span><span class="sxs-lookup"><span data-stu-id="f6707-151">Microsoft.Azure.Storage.File.CopyState</span></span>

## <span data-ttu-id="f6707-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f6707-152">NOTES</span></span>

## <span data-ttu-id="f6707-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f6707-153">RELATED LINKS</span></span>

[<span data-ttu-id="f6707-154">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="f6707-154">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="f6707-155">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f6707-155">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="f6707-156">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f6707-156">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)

[<span data-ttu-id="f6707-157">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f6707-157">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
