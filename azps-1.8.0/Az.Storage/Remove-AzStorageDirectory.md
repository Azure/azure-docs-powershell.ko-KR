---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
ms.openlocfilehash: cc57638e1620e8c9177f3635074f6964ef38afb8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698568"
---
# <span data-ttu-id="d0a1a-101">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="d0a1a-101">Remove-AzStorageDirectory</span></span>

## <span data-ttu-id="d0a1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0a1a-102">SYNOPSIS</span></span>
<span data-ttu-id="d0a1a-103">디렉터리를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-103">Deletes a directory.</span></span>

## <span data-ttu-id="d0a1a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d0a1a-104">SYNTAX</span></span>

### <span data-ttu-id="d0a1a-105">ShareName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d0a1a-105">ShareName (Default)</span></span>
```
Remove-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0a1a-106">공유</span><span class="sxs-lookup"><span data-stu-id="d0a1a-106">Share</span></span>
```
Remove-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0a1a-107">디렉토리로</span><span class="sxs-lookup"><span data-stu-id="d0a1a-107">Directory</span></span>
```
Remove-AzStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0a1a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d0a1a-108">DESCRIPTION</span></span>
<span data-ttu-id="d0a1a-109">**AzStorageDirectory** cmdlet은 디렉터리를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-109">The **Remove-AzStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="d0a1a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d0a1a-110">EXAMPLES</span></span>

### <span data-ttu-id="d0a1a-111">예제 1: 폴더 삭제</span><span class="sxs-lookup"><span data-stu-id="d0a1a-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="d0a1a-112">이 명령은 ContosoShare06 이라는 파일 공유에서 ContosoWorkingFolder 이라는 폴더를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="d0a1a-113">변수</span><span class="sxs-lookup"><span data-stu-id="d0a1a-113">PARAMETERS</span></span>

### <span data-ttu-id="d0a1a-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d0a1a-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d0a1a-115">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d0a1a-116">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d0a1a-117">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d0a1a-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d0a1a-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d0a1a-119">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d0a1a-120">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d0a1a-121">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d0a1a-122">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d0a1a-123">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-123">The default value is 10.</span></span>

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

### <span data-ttu-id="d0a1a-124">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="d0a1a-124">-Context</span></span>
<span data-ttu-id="d0a1a-125">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d0a1a-126">저장소 컨텍스트를 얻으려면 [New AzStorageContext](./New-AzStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-126">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="d0a1a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0a1a-127">-DefaultProfile</span></span>
<span data-ttu-id="d0a1a-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0a1a-129">-디렉터리</span><span class="sxs-lookup"><span data-stu-id="d0a1a-129">-Directory</span></span>
<span data-ttu-id="d0a1a-130">폴더를 **Cloudfiledirectory** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-130">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="d0a1a-131">이 cmdlet은이 매개 변수에서 지정 하는 폴더를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-131">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="d0a1a-132">디렉터리를 가져오려면 New-AzStorageDirectory cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-132">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="d0a1a-133">**Get-AzStorageFile** cmdlet을 사용 하 여 디렉터리를 가져올 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-133">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="d0a1a-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0a1a-134">-PassThru</span></span>
<span data-ttu-id="d0a1a-135">이 cmdlet이 성공한 경우 $True 값을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-135">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="d0a1a-136">이 매개 변수를 지정 하 고 _Path_ 매개 변수에 적절 하지 않은 값으로 인해 cmdlet이 실패 하는 경우 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-136">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="d0a1a-137">이 매개 변수를 지정 하지 않으면이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-137">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="d0a1a-138">-Path</span><span class="sxs-lookup"><span data-stu-id="d0a1a-138">-Path</span></span>
<span data-ttu-id="d0a1a-139">폴더의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="d0a1a-140">이 매개 변수가 지정 하는 폴더가 비어 있으면이 cmdlet은 해당 폴더를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-140">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="d0a1a-141">폴더가 비어 있지 않은 경우이 cmdlet은 아무런 변화가 없으며 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-141">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Directory
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0a1a-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d0a1a-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d0a1a-143">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-143">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="d0a1a-144">-공유</span><span class="sxs-lookup"><span data-stu-id="d0a1a-144">-Share</span></span>
<span data-ttu-id="d0a1a-145">**Cloudfileshare** 되지 않는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-145">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="d0a1a-146">이 cmdlet은이 매개 변수에서 지정 하는 파일 공유 아래에 있는 폴더를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-146">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="d0a1a-147">**Cloudfileshare** 되지 않는 개체를 가져오려면 Get-AzStorageShare cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-147">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="d0a1a-148">이 개체는 저장소 컨텍스트를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-148">This object contains the storage context.</span></span>
<span data-ttu-id="d0a1a-149">이 매개 변수를 지정 하는 경우 *컨텍스트* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-149">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="d0a1a-150">-ShareName</span><span class="sxs-lookup"><span data-stu-id="d0a1a-150">-ShareName</span></span>
<span data-ttu-id="d0a1a-151">파일 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-151">Specifies the name of the file share.</span></span>
<span data-ttu-id="d0a1a-152">이 cmdlet은이 매개 변수에서 지정 하는 파일 공유 아래에 있는 폴더를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-152">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="d0a1a-153">-확인</span><span class="sxs-lookup"><span data-stu-id="d0a1a-153">-Confirm</span></span>
<span data-ttu-id="d0a1a-154">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0a1a-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0a1a-155">-WhatIf</span></span>
<span data-ttu-id="d0a1a-156">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0a1a-157">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0a1a-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0a1a-158">CommonParameters</span></span>
<span data-ttu-id="d0a1a-159">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0a1a-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0a1a-160">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0a1a-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0a1a-161">입력</span><span class="sxs-lookup"><span data-stu-id="d0a1a-161">INPUTS</span></span>

### <span data-ttu-id="d0a1a-162">WindowsAzure 파일. c a c 공유</span><span class="sxs-lookup"><span data-stu-id="d0a1a-162">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="d0a1a-163">WindowsAzure. c l i 파일 디렉터리</span><span class="sxs-lookup"><span data-stu-id="d0a1a-163">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="d0a1a-164">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d0a1a-164">System.String</span></span>

### <span data-ttu-id="d0a1a-165">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d0a1a-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d0a1a-166">출력</span><span class="sxs-lookup"><span data-stu-id="d0a1a-166">OUTPUTS</span></span>

### <span data-ttu-id="d0a1a-167">WindowsAzure. c l i 파일 디렉터리</span><span class="sxs-lookup"><span data-stu-id="d0a1a-167">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>

## <span data-ttu-id="d0a1a-168">상속자</span><span class="sxs-lookup"><span data-stu-id="d0a1a-168">NOTES</span></span>

## <span data-ttu-id="d0a1a-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d0a1a-169">RELATED LINKS</span></span>

[<span data-ttu-id="d0a1a-170">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="d0a1a-170">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="d0a1a-171">새로운 AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d0a1a-171">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="d0a1a-172">새로운 AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="d0a1a-172">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)
