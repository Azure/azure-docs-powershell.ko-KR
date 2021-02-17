---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShare.md
ms.openlocfilehash: d51980303d4cb0bcd3ba7ec9e4f976634d37c689
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207760"
---
# <span data-ttu-id="443e4-101">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="443e4-101">Remove-AzStorageShare</span></span>

## <span data-ttu-id="443e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="443e4-102">SYNOPSIS</span></span>
<span data-ttu-id="443e4-103">파일 공유를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="443e4-103">Deletes a file share.</span></span>

## <span data-ttu-id="443e4-104">구문</span><span class="sxs-lookup"><span data-stu-id="443e4-104">SYNTAX</span></span>

### <span data-ttu-id="443e4-105">ShareName(기본값)</span><span class="sxs-lookup"><span data-stu-id="443e4-105">ShareName (Default)</span></span>
```
Remove-AzStorageShare [-Name] <String> [-IncludeAllSnapshot] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="443e4-106">공유</span><span class="sxs-lookup"><span data-stu-id="443e4-106">Share</span></span>
```
Remove-AzStorageShare [-Share] <CloudFileShare> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="443e4-107">설명</span><span class="sxs-lookup"><span data-stu-id="443e4-107">DESCRIPTION</span></span>
<span data-ttu-id="443e4-108">**Remove-AzStorageShare** cmdlet은 파일 공유를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="443e4-108">The **Remove-AzStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="443e4-109">예제</span><span class="sxs-lookup"><span data-stu-id="443e4-109">EXAMPLES</span></span>

### <span data-ttu-id="443e4-110">예제 1: 파일 공유 제거</span><span class="sxs-lookup"><span data-stu-id="443e4-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="443e4-111">이 명령은 ContosoShare06이라는 파일 공유를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="443e4-111">This command removes the file share named ContosoShare06.</span></span>

### <span data-ttu-id="443e4-112">예제 2: 파일 공유 및 모든 스냅숏 제거</span><span class="sxs-lookup"><span data-stu-id="443e4-112">Example 2: Remove a file share and all its snapshots</span></span>
```
PS C:\>Remove-AzStorageShare -Name "ContosoShare06" -IncludeAllSnapshot
```

<span data-ttu-id="443e4-113">이 명령은 ContosoShare06이라는 파일 공유 및 모든 스냅숏을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="443e4-113">This command removes the file share named ContosoShare06 and all its snapshots.</span></span>

## <span data-ttu-id="443e4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="443e4-114">PARAMETERS</span></span>

### <span data-ttu-id="443e4-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="443e4-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="443e4-116">하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="443e4-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="443e4-117">이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="443e4-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="443e4-118">이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="443e4-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="443e4-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="443e4-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="443e4-120">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="443e4-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="443e4-121">이 매개 변수를 사용하면 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="443e4-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="443e4-122">지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="443e4-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="443e4-123">이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="443e4-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="443e4-124">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="443e4-124">The default value is 10.</span></span>

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

### <span data-ttu-id="443e4-125">-Context</span><span class="sxs-lookup"><span data-stu-id="443e4-125">-Context</span></span>
<span data-ttu-id="443e4-126">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="443e4-126">Specifies an Azure storage context.</span></span>
<span data-ttu-id="443e4-127">저장소 컨텍스트를 얻습니다. [New-AzStorageContext](./New-AzStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="443e4-127">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="443e4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="443e4-128">-DefaultProfile</span></span>
<span data-ttu-id="443e4-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="443e4-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="443e4-130">-Force</span><span class="sxs-lookup"><span data-stu-id="443e4-130">-Force</span></span>
<span data-ttu-id="443e4-131">모든 스냅숏 및 모든 콘텐츠가 있는 공유를 강제로 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="443e4-131">Force to remove the share with all of its snapshots, and all content.</span></span>

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

### <span data-ttu-id="443e4-132">-IncludeAllSnapshot</span><span class="sxs-lookup"><span data-stu-id="443e4-132">-IncludeAllSnapshot</span></span>
<span data-ttu-id="443e4-133">모든 스냅숏으로 파일 공유 제거</span><span class="sxs-lookup"><span data-stu-id="443e4-133">Remove File Share with all of its snapshots</span></span>

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

### <span data-ttu-id="443e4-134">-Name</span><span class="sxs-lookup"><span data-stu-id="443e4-134">-Name</span></span>
<span data-ttu-id="443e4-135">파일 공유의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="443e4-135">Specifies the name of the file share.</span></span>
<span data-ttu-id="443e4-136">이 cmdlet은 이 매개 변수가 지정하는 파일 공유를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="443e4-136">This cmdlet deletes the file share that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="443e4-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="443e4-137">-PassThru</span></span>
<span data-ttu-id="443e4-138">이 cmdlet은 작업의  성공을 반영하는 부울을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="443e4-138">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="443e4-139">기본적으로 이 cmdlet은 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="443e4-139">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="443e4-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="443e4-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="443e4-141">요청의 서버 부분에 대한 시간 제한 기간의 길이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="443e4-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="443e4-142">-Share</span><span class="sxs-lookup"><span data-stu-id="443e4-142">-Share</span></span>
<span data-ttu-id="443e4-143">**CloudFileShare 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="443e4-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="443e4-144">이 cmdlet은 이 매개 변수가 지정하는 개체를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="443e4-144">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="443e4-145">**CloudFileShare** 개체를 얻습니다. Get-AzStorageShare cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="443e4-145">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="443e4-146">이 개체에는 저장소 컨텍스트가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="443e4-146">This object contains the storage context.</span></span>
<span data-ttu-id="443e4-147">이 매개 변수를 지정하는 경우 Context 매개 변수를 *지정하지* 않습니다.</span><span class="sxs-lookup"><span data-stu-id="443e4-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="443e4-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="443e4-148">-Confirm</span></span>
<span data-ttu-id="443e4-149">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="443e4-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="443e4-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="443e4-150">-WhatIf</span></span>
<span data-ttu-id="443e4-151">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="443e4-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="443e4-152">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="443e4-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="443e4-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="443e4-153">CommonParameters</span></span>
<span data-ttu-id="443e4-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="443e4-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="443e4-155">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="443e4-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="443e4-156">입력</span><span class="sxs-lookup"><span data-stu-id="443e4-156">INPUTS</span></span>

### <span data-ttu-id="443e4-157">System.String</span><span class="sxs-lookup"><span data-stu-id="443e4-157">System.String</span></span>

### <span data-ttu-id="443e4-158">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="443e4-158">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="443e4-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="443e4-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="443e4-160">출력</span><span class="sxs-lookup"><span data-stu-id="443e4-160">OUTPUTS</span></span>

### <span data-ttu-id="443e4-161">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="443e4-161">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="443e4-162">참고 사항</span><span class="sxs-lookup"><span data-stu-id="443e4-162">NOTES</span></span>

## <span data-ttu-id="443e4-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="443e4-163">RELATED LINKS</span></span>

[<span data-ttu-id="443e4-164">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="443e4-164">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="443e4-165">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="443e4-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="443e4-166">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="443e4-166">New-AzStorageShare</span></span>](./New-AzStorageShare.md)
