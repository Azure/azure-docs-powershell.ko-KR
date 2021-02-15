---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
ms.openlocfilehash: 84f6ae7f80eb7af3c4fccad08b0d9d2a20b0caeb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190865"
---
# <span data-ttu-id="de11d-101">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="de11d-101">New-AzStorageDirectory</span></span>

## <span data-ttu-id="de11d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de11d-102">SYNOPSIS</span></span>
<span data-ttu-id="de11d-103">디렉터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-103">Creates a directory.</span></span>

## <span data-ttu-id="de11d-104">구문</span><span class="sxs-lookup"><span data-stu-id="de11d-104">SYNTAX</span></span>

### <span data-ttu-id="de11d-105">ShareName(기본값)</span><span class="sxs-lookup"><span data-stu-id="de11d-105">ShareName (Default)</span></span>
```
New-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="de11d-106">공유</span><span class="sxs-lookup"><span data-stu-id="de11d-106">Share</span></span>
```
New-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="de11d-107">디렉터리</span><span class="sxs-lookup"><span data-stu-id="de11d-107">Directory</span></span>
```
New-AzStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="de11d-108">설명</span><span class="sxs-lookup"><span data-stu-id="de11d-108">DESCRIPTION</span></span>
<span data-ttu-id="de11d-109">**New-AzStorageDirectory** cmdlet은 디렉터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-109">The **New-AzStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="de11d-110">이 cmdlet은 **CloudFileDirectory 개체를 반환합니다.**</span><span class="sxs-lookup"><span data-stu-id="de11d-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="de11d-111">예제</span><span class="sxs-lookup"><span data-stu-id="de11d-111">EXAMPLES</span></span>

### <span data-ttu-id="de11d-112">예제 1: 파일 공유에 폴더 만들기</span><span class="sxs-lookup"><span data-stu-id="de11d-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="de11d-113">이 명령은 ContosoShare06이라는 파일 공유에 ContosoWorkingFolder라는 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="de11d-114">예제 2: 파일 공유 개체에 지정된 파일 공유에 폴더 만들기</span><span class="sxs-lookup"><span data-stu-id="de11d-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | New-AzStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="de11d-115">이 명령은 **Get-AzStorageShare** cmdlet을 사용하여 ContosoShare06이라는 파일 공유를 다운로드한 다음 파이프라인 연산자를 사용하여 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="de11d-116">현재 cmdlet은 ContosoShare06에 ContosoWorkingFolder라는 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="de11d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de11d-117">PARAMETERS</span></span>

### <span data-ttu-id="de11d-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="de11d-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="de11d-119">하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="de11d-120">이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="de11d-121">이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="de11d-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="de11d-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="de11d-123">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="de11d-124">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="de11d-125">지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="de11d-126">이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="de11d-127">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-127">The default value is 10.</span></span>

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

### <span data-ttu-id="de11d-128">-Context</span><span class="sxs-lookup"><span data-stu-id="de11d-128">-Context</span></span>
<span data-ttu-id="de11d-129">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="de11d-130">저장소 컨텍스트를 얻습니다. [New-AzStorageContext](./New-AzStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="de11d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de11d-131">-DefaultProfile</span></span>
<span data-ttu-id="de11d-132">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de11d-133">-Directory</span><span class="sxs-lookup"><span data-stu-id="de11d-133">-Directory</span></span>
<span data-ttu-id="de11d-134">폴더를 **CloudFileDirectory 개체로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="de11d-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="de11d-135">이 cmdlet은 이 매개 변수가 지정하는 위치에 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-135">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="de11d-136">디렉터리를 얻습니다. New-AzStorageDirectory cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-136">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="de11d-137">또한 Get-AzStorageFile cmdlet을 사용하여 디렉터리를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-137">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="de11d-138">-Path</span><span class="sxs-lookup"><span data-stu-id="de11d-138">-Path</span></span>
<span data-ttu-id="de11d-139">폴더의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="de11d-140">이 cmdlet은 이 cmdlet이 지정하는 경로에 대한 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-140">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="de11d-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="de11d-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="de11d-142">요청의 서버 부분에 대한 시간 제한 기간의 길이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="de11d-143">-Share</span><span class="sxs-lookup"><span data-stu-id="de11d-143">-Share</span></span>
<span data-ttu-id="de11d-144">**CloudFileShare 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="de11d-144">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="de11d-145">이 cmdlet은 이 매개 변수가 지정하는 폴더를 파일 공유에 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-145">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="de11d-146">**CloudFileShare** 개체를 얻습니다. Get-AzStorageShare cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-146">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="de11d-147">이 개체에는 저장소 컨텍스트가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-147">This object contains the storage context.</span></span>
<span data-ttu-id="de11d-148">이 매개 변수를 지정하는 경우 Context 매개 변수를 *지정하지* 않습니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-148">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="de11d-149">-ShareName</span><span class="sxs-lookup"><span data-stu-id="de11d-149">-ShareName</span></span>
<span data-ttu-id="de11d-150">파일 공유의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-150">Specifies the name of the file share.</span></span>
<span data-ttu-id="de11d-151">이 cmdlet은 이 매개 변수가 지정하는 폴더를 파일 공유에 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-151">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="de11d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de11d-152">CommonParameters</span></span>
<span data-ttu-id="de11d-153">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="de11d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de11d-154">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="de11d-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de11d-155">입력</span><span class="sxs-lookup"><span data-stu-id="de11d-155">INPUTS</span></span>

### <span data-ttu-id="de11d-156">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="de11d-156">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="de11d-157">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="de11d-157">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="de11d-158">System.String</span><span class="sxs-lookup"><span data-stu-id="de11d-158">System.String</span></span>

### <span data-ttu-id="de11d-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="de11d-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="de11d-160">출력</span><span class="sxs-lookup"><span data-stu-id="de11d-160">OUTPUTS</span></span>

### <span data-ttu-id="de11d-161">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span><span class="sxs-lookup"><span data-stu-id="de11d-161">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span></span>

## <span data-ttu-id="de11d-162">참고 사항</span><span class="sxs-lookup"><span data-stu-id="de11d-162">NOTES</span></span>

## <span data-ttu-id="de11d-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="de11d-163">RELATED LINKS</span></span>

[<span data-ttu-id="de11d-164">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="de11d-164">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="de11d-165">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="de11d-165">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="de11d-166">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="de11d-166">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="de11d-167">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="de11d-167">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="de11d-168">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="de11d-168">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)
