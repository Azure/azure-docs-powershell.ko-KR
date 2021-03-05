---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
ms.openlocfilehash: 6f44f1545eea4e515064873cdc77f8b34819fabc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002475"
---
# <span data-ttu-id="46227-101">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="46227-101">New-AzStorageDirectory</span></span>

## <span data-ttu-id="46227-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46227-102">SYNOPSIS</span></span>
<span data-ttu-id="46227-103">디렉터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="46227-103">Creates a directory.</span></span>

## <span data-ttu-id="46227-104">구문</span><span class="sxs-lookup"><span data-stu-id="46227-104">SYNTAX</span></span>

### <span data-ttu-id="46227-105">ShareName(기본값)</span><span class="sxs-lookup"><span data-stu-id="46227-105">ShareName (Default)</span></span>
```
New-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="46227-106">공유</span><span class="sxs-lookup"><span data-stu-id="46227-106">Share</span></span>
```
New-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="46227-107">디렉터리</span><span class="sxs-lookup"><span data-stu-id="46227-107">Directory</span></span>
```
New-AzStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="46227-108">설명</span><span class="sxs-lookup"><span data-stu-id="46227-108">DESCRIPTION</span></span>
<span data-ttu-id="46227-109">**New-AzStorageDirectory** cmdlet은 디렉터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="46227-109">The **New-AzStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="46227-110">이 cmdlet은 **CloudFileDirectory 개체를 반환합니다.**</span><span class="sxs-lookup"><span data-stu-id="46227-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="46227-111">예제</span><span class="sxs-lookup"><span data-stu-id="46227-111">EXAMPLES</span></span>

### <span data-ttu-id="46227-112">예제 1: 파일 공유에서 폴더 만들기</span><span class="sxs-lookup"><span data-stu-id="46227-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="46227-113">이 명령은 ContosoShare06이라는 파일 공유에 ContosoWorkingFolder라는 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="46227-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="46227-114">예제 2: 파일 공유 개체에 지정된 파일 공유에서 폴더 만들기</span><span class="sxs-lookup"><span data-stu-id="46227-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | New-AzStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="46227-115">이 명령은 **Get-AzStorageShare** cmdlet을 사용하여 ContosoShare06이라는 파일 공유를 얻은 다음 파이프라인 연산자를 사용하여 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="46227-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="46227-116">현재 cmdlet은 ContosoShare06에서 ContosoWorkingFolder라는 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="46227-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="46227-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="46227-117">PARAMETERS</span></span>

### <span data-ttu-id="46227-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="46227-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="46227-119">하나의 서비스 요청에 대해 클라이언트 쪽 시간 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="46227-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="46227-120">지정된 간격에서 이전 호출이 실패하면 이 cmdlet에서 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="46227-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="46227-121">간격이 경과하기 전에 이 cmdlet에서 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="46227-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="46227-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="46227-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="46227-123">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="46227-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="46227-124">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 로컬 CPU 및 대역폭 사용량을 제한하는 동시성 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46227-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="46227-125">지정된 값은 절대 개수로 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46227-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="46227-126">이 매개 변수는 초당 100킬로비트와 같은 대역폭이 낮은 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46227-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="46227-127">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="46227-127">The default value is 10.</span></span>

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

### <span data-ttu-id="46227-128">-Context</span><span class="sxs-lookup"><span data-stu-id="46227-128">-Context</span></span>
<span data-ttu-id="46227-129">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="46227-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="46227-130">저장소 컨텍스트를 구하기 위해 [New-AzStorageContext](./New-AzStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="46227-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="46227-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46227-131">-DefaultProfile</span></span>
<span data-ttu-id="46227-132">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="46227-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46227-133">-Directory</span><span class="sxs-lookup"><span data-stu-id="46227-133">-Directory</span></span>
<span data-ttu-id="46227-134">폴더를 **CloudFileDirectory 개체로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="46227-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="46227-135">이 cmdlet은 이 매개 변수가 지정하는 위치에 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="46227-135">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="46227-136">디렉터리를 구하기 위해 New-AzStorageDirectory cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="46227-136">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="46227-137">또한 Get-AzStorageFile cmdlet을 사용하여 디렉터리를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46227-137">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46227-138">-Path</span><span class="sxs-lookup"><span data-stu-id="46227-138">-Path</span></span>
<span data-ttu-id="46227-139">폴더의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="46227-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="46227-140">이 cmdlet은 이 cmdlet이 지정하는 경로에 대한 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="46227-140">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46227-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="46227-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="46227-142">요청의 서버 부분에 대한 시간 제한 기간의 길이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="46227-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="46227-143">-Share</span><span class="sxs-lookup"><span data-stu-id="46227-143">-Share</span></span>
<span data-ttu-id="46227-144">**CloudFileShare 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="46227-144">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="46227-145">이 cmdlet은 이 매개 변수가 지정하는 파일 공유에 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="46227-145">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="46227-146">**CloudFileShare** 개체를 얻은 경우 Get-AzStorageShare cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="46227-146">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="46227-147">이 개체에는 저장소 컨텍스트가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46227-147">This object contains the storage context.</span></span>
<span data-ttu-id="46227-148">이 매개 변수를 지정하는 경우 Context 매개 변수를 *지정하지* 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46227-148">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46227-149">-ShareName</span><span class="sxs-lookup"><span data-stu-id="46227-149">-ShareName</span></span>
<span data-ttu-id="46227-150">파일 공유의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="46227-150">Specifies the name of the file share.</span></span>
<span data-ttu-id="46227-151">이 cmdlet은 이 매개 변수가 지정하는 파일 공유에 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="46227-151">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="46227-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46227-152">CommonParameters</span></span>
<span data-ttu-id="46227-153">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="46227-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46227-154">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="46227-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46227-155">입력</span><span class="sxs-lookup"><span data-stu-id="46227-155">INPUTS</span></span>

### <span data-ttu-id="46227-156">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="46227-156">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="46227-157">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="46227-157">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="46227-158">System.String</span><span class="sxs-lookup"><span data-stu-id="46227-158">System.String</span></span>

### <span data-ttu-id="46227-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="46227-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="46227-160">출력</span><span class="sxs-lookup"><span data-stu-id="46227-160">OUTPUTS</span></span>

### <span data-ttu-id="46227-161">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span><span class="sxs-lookup"><span data-stu-id="46227-161">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span></span>

## <span data-ttu-id="46227-162">참고 사항</span><span class="sxs-lookup"><span data-stu-id="46227-162">NOTES</span></span>

## <span data-ttu-id="46227-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46227-163">RELATED LINKS</span></span>

[<span data-ttu-id="46227-164">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="46227-164">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="46227-165">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="46227-165">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="46227-166">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="46227-166">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="46227-167">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="46227-167">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="46227-168">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="46227-168">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)
