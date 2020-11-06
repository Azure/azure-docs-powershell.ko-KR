---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageDirectory.md
ms.openlocfilehash: b5d28a2c156572909f5d1e943473dbbf2c527d18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531551"
---
# <span data-ttu-id="dae7b-101">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="dae7b-101">New-AzureStorageDirectory</span></span>

## <span data-ttu-id="dae7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dae7b-102">SYNOPSIS</span></span>
<span data-ttu-id="dae7b-103">디렉터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-103">Creates a directory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dae7b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dae7b-104">SYNTAX</span></span>

### <span data-ttu-id="dae7b-105">ShareName (기본값)</span><span class="sxs-lookup"><span data-stu-id="dae7b-105">ShareName (Default)</span></span>
```
New-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="dae7b-106">공유</span><span class="sxs-lookup"><span data-stu-id="dae7b-106">Share</span></span>
```
New-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="dae7b-107">디렉토리로</span><span class="sxs-lookup"><span data-stu-id="dae7b-107">Directory</span></span>
```
New-AzureStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="dae7b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="dae7b-108">DESCRIPTION</span></span>
<span data-ttu-id="dae7b-109">**새-AzureStorageDirectory** cmdlet은 디렉터리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-109">The **New-AzureStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="dae7b-110">이 cmdlet은 **Cloudfiledirectory** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="dae7b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="dae7b-111">EXAMPLES</span></span>

### <span data-ttu-id="dae7b-112">예제 1: 파일 공유에 폴더 만들기</span><span class="sxs-lookup"><span data-stu-id="dae7b-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="dae7b-113">이 명령은 ContosoShare06 이라는 파일 공유에 ContosoWorkingFolder 이라는 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="dae7b-114">예제 2: 파일 공유 개체에 지정 된 파일 공유에 폴더 만들기</span><span class="sxs-lookup"><span data-stu-id="dae7b-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" | New-AzureStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="dae7b-115">이 명령은 **AzureStorageShare** cmdlet을 사용 하 여 ContosoShare06 이라는 이름의 파일 공유를 가져오고 파이프라인 연산자를 사용 하 여 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-115">This command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="dae7b-116">현재 cmdlet은 ContosoShare06에 ContosoWorkingFolder 이라는 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="dae7b-117">변수</span><span class="sxs-lookup"><span data-stu-id="dae7b-117">PARAMETERS</span></span>

### <span data-ttu-id="dae7b-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="dae7b-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="dae7b-119">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="dae7b-120">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="dae7b-121">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="dae7b-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="dae7b-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="dae7b-123">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="dae7b-124">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="dae7b-125">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="dae7b-126">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="dae7b-127">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-127">The default value is 10.</span></span>

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

### <span data-ttu-id="dae7b-128">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="dae7b-128">-Context</span></span>
<span data-ttu-id="dae7b-129">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="dae7b-130">저장소 컨텍스트를 얻으려면 [새로운-AzureStorageContext](./New-AzureStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-130">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="dae7b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dae7b-131">-DefaultProfile</span></span>
<span data-ttu-id="dae7b-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dae7b-133">-디렉터리</span><span class="sxs-lookup"><span data-stu-id="dae7b-133">-Directory</span></span>
<span data-ttu-id="dae7b-134">폴더를 **Cloudfiledirectory** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="dae7b-135">이 cmdlet은이 매개 변수에서 지정 하는 위치에 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-135">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="dae7b-136">디렉터리를 가져오려면 New-AzureStorageDirectory cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-136">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="dae7b-137">또한 Get-AzureStorageFile cmdlet을 사용 하 여 디렉터리를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-137">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dae7b-138">-Path</span><span class="sxs-lookup"><span data-stu-id="dae7b-138">-Path</span></span>
<span data-ttu-id="dae7b-139">폴더의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="dae7b-140">이 cmdlet은이 cmdlet에서 지정 하는 경로에 대 한 폴더를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-140">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="dae7b-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="dae7b-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="dae7b-142">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="dae7b-143">-공유</span><span class="sxs-lookup"><span data-stu-id="dae7b-143">-Share</span></span>
<span data-ttu-id="dae7b-144">**Cloudfileshare** 되지 않는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-144">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="dae7b-145">이 cmdlet은이 매개 변수에서 지정 하는 폴더를 파일 공유에 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-145">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="dae7b-146">**Cloudfileshare** 되지 않는 개체를 가져오려면 Get-AzureStorageShare cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-146">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="dae7b-147">이 개체는 저장소 컨텍스트를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-147">This object contains the storage context.</span></span>
<span data-ttu-id="dae7b-148">이 매개 변수를 지정 하는 경우 *컨텍스트* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="dae7b-148">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dae7b-149">-ShareName</span><span class="sxs-lookup"><span data-stu-id="dae7b-149">-ShareName</span></span>
<span data-ttu-id="dae7b-150">파일 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-150">Specifies the name of the file share.</span></span>
<span data-ttu-id="dae7b-151">이 cmdlet은이 매개 변수에서 지정 하는 폴더를 파일 공유에 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-151">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="dae7b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dae7b-152">CommonParameters</span></span>
<span data-ttu-id="dae7b-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dae7b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dae7b-154">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dae7b-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dae7b-155">입력</span><span class="sxs-lookup"><span data-stu-id="dae7b-155">INPUTS</span></span>

### <span data-ttu-id="dae7b-156">WindowsAzure 파일. c a c 공유</span><span class="sxs-lookup"><span data-stu-id="dae7b-156">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="dae7b-157">매개 변수: Share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dae7b-157">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="dae7b-158">WindowsAzure. c l i 파일 디렉터리</span><span class="sxs-lookup"><span data-stu-id="dae7b-158">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="dae7b-159">매개 변수: Directory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dae7b-159">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="dae7b-160">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dae7b-160">System.String</span></span>

### <span data-ttu-id="dae7b-161">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="dae7b-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="dae7b-162">출력</span><span class="sxs-lookup"><span data-stu-id="dae7b-162">OUTPUTS</span></span>

### <span data-ttu-id="dae7b-163">WindowsAzure. c l i 파일 디렉터리</span><span class="sxs-lookup"><span data-stu-id="dae7b-163">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>

## <span data-ttu-id="dae7b-164">상속자</span><span class="sxs-lookup"><span data-stu-id="dae7b-164">NOTES</span></span>

## <span data-ttu-id="dae7b-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dae7b-165">RELATED LINKS</span></span>

[<span data-ttu-id="dae7b-166">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="dae7b-166">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="dae7b-167">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="dae7b-167">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="dae7b-168">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="dae7b-168">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="dae7b-169">새-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="dae7b-169">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="dae7b-170">-AzureStorageDirectory 제거</span><span class="sxs-lookup"><span data-stu-id="dae7b-170">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)