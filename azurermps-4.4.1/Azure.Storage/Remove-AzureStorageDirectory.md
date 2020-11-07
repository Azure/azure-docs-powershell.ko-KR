---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageDirectory.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: cdd52b1e1bab28956605d70e1089d7804b8ccff7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702888"
---
# <span data-ttu-id="ecdae-101">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="ecdae-101">Remove-AzureStorageDirectory</span></span>

## <span data-ttu-id="ecdae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecdae-102">SYNOPSIS</span></span>
<span data-ttu-id="ecdae-103">디렉터리를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-103">Deletes a directory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecdae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ecdae-104">SYNTAX</span></span>

### <span data-ttu-id="ecdae-105">ShareName (기본값)</span><span class="sxs-lookup"><span data-stu-id="ecdae-105">ShareName (Default)</span></span>
```
Remove-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecdae-106">공유</span><span class="sxs-lookup"><span data-stu-id="ecdae-106">Share</span></span>
```
Remove-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecdae-107">디렉토리로</span><span class="sxs-lookup"><span data-stu-id="ecdae-107">Directory</span></span>
```
Remove-AzureStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecdae-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ecdae-108">DESCRIPTION</span></span>
<span data-ttu-id="ecdae-109">**제거-AzureStorageDirectory** cmdlet은 디렉터리를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-109">The **Remove-AzureStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="ecdae-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ecdae-110">EXAMPLES</span></span>

### <span data-ttu-id="ecdae-111">예제 1: 폴더 삭제</span><span class="sxs-lookup"><span data-stu-id="ecdae-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="ecdae-112">이 명령은 ContosoShare06 이라는 파일 공유에서 ContosoWorkingFolder 이라는 폴더를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="ecdae-113">변수</span><span class="sxs-lookup"><span data-stu-id="ecdae-113">PARAMETERS</span></span>

### <span data-ttu-id="ecdae-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ecdae-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ecdae-115">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ecdae-116">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ecdae-117">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecdae-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ecdae-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ecdae-119">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ecdae-120">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ecdae-121">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ecdae-122">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ecdae-123">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-123">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecdae-124">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="ecdae-124">-Context</span></span>
<span data-ttu-id="ecdae-125">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ecdae-126">저장소 컨텍스트를 얻으려면 [새로운-AzureStorageContext](./New-AzureStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-126">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecdae-127">-디렉터리</span><span class="sxs-lookup"><span data-stu-id="ecdae-127">-Directory</span></span>
<span data-ttu-id="ecdae-128">폴더를 **Cloudfiledirectory** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-128">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="ecdae-129">이 cmdlet은이 매개 변수에서 지정 하는 폴더를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-129">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="ecdae-130">디렉터리를 가져오려면 New-AzureStorageDirectory cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-130">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="ecdae-131">**Get-AzureStorageFile** cmdlet을 사용 하 여 디렉터리를 가져올 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-131">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecdae-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecdae-132">-PassThru</span></span>
<span data-ttu-id="ecdae-133">이 cmdlet이 성공한 경우 $True 값을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-133">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="ecdae-134">이 매개 변수를 지정 하 고 _Path_ 매개 변수에 적절 하지 않은 값으로 인해 cmdlet이 실패 하는 경우 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-134">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="ecdae-135">이 매개 변수를 지정 하지 않으면이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-135">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecdae-136">-Path</span><span class="sxs-lookup"><span data-stu-id="ecdae-136">-Path</span></span>
<span data-ttu-id="ecdae-137">폴더의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-137">Specifies the path of a folder.</span></span>
<span data-ttu-id="ecdae-138">이 매개 변수가 지정 하는 폴더가 비어 있으면이 cmdlet은 해당 폴더를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-138">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="ecdae-139">폴더가 비어 있지 않은 경우이 cmdlet은 아무런 변화가 없으며 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-139">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, Share
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Directory
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecdae-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ecdae-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ecdae-141">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-141">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecdae-142">-공유</span><span class="sxs-lookup"><span data-stu-id="ecdae-142">-Share</span></span>
<span data-ttu-id="ecdae-143">**Cloudfileshare** 되지 않는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="ecdae-144">이 cmdlet은이 매개 변수에서 지정 하는 파일 공유 아래에 있는 폴더를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-144">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="ecdae-145">**Cloudfileshare** 되지 않는 개체를 가져오려면 Get-AzureStorageShare cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-145">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="ecdae-146">이 개체는 저장소 컨텍스트를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-146">This object contains the storage context.</span></span>
<span data-ttu-id="ecdae-147">이 매개 변수를 지정 하는 경우 *컨텍스트* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="ecdae-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecdae-148">-ShareName</span><span class="sxs-lookup"><span data-stu-id="ecdae-148">-ShareName</span></span>
<span data-ttu-id="ecdae-149">파일 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-149">Specifies the name of the file share.</span></span>
<span data-ttu-id="ecdae-150">이 cmdlet은이 매개 변수에서 지정 하는 파일 공유 아래에 있는 폴더를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-150">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecdae-151">-확인</span><span class="sxs-lookup"><span data-stu-id="ecdae-151">-Confirm</span></span>
<span data-ttu-id="ecdae-152">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecdae-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecdae-153">-WhatIf</span></span>
<span data-ttu-id="ecdae-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecdae-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-155">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecdae-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecdae-156">CommonParameters</span></span>
<span data-ttu-id="ecdae-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecdae-158">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecdae-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecdae-159">입력</span><span class="sxs-lookup"><span data-stu-id="ecdae-159">INPUTS</span></span>

### <span data-ttu-id="ecdae-160">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ecdae-160">IStorageContext</span></span>

<span data-ttu-id="ecdae-161">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-161">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="ecdae-162">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="ecdae-162">CloudFileDirectory</span></span>

<span data-ttu-id="ecdae-163">' Directory ' 매개 변수는 파이프라인에서 ' CloudFileDirectory ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-163">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="ecdae-164">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="ecdae-164">CloudFileShare</span></span>

<span data-ttu-id="ecdae-165">' Share ' 매개 변수는 파이프라인에서 ' CloudFileShare 범위 ' 형식의 값을 받아들입니다.</span><span class="sxs-lookup"><span data-stu-id="ecdae-165">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="ecdae-166">출력</span><span class="sxs-lookup"><span data-stu-id="ecdae-166">OUTPUTS</span></span>

## <span data-ttu-id="ecdae-167">상속자</span><span class="sxs-lookup"><span data-stu-id="ecdae-167">NOTES</span></span>

## <span data-ttu-id="ecdae-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ecdae-168">RELATED LINKS</span></span>

[<span data-ttu-id="ecdae-169">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="ecdae-169">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="ecdae-170">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ecdae-170">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="ecdae-171">새-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="ecdae-171">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)
