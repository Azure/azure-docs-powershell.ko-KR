---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShare.md
ms.openlocfilehash: d51980303d4cb0bcd3ba7ec9e4f976634d37c689
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056886"
---
# <span data-ttu-id="dd066-101">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="dd066-101">Remove-AzStorageShare</span></span>

## <span data-ttu-id="dd066-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd066-102">SYNOPSIS</span></span>
<span data-ttu-id="dd066-103">파일 공유를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-103">Deletes a file share.</span></span>

## <span data-ttu-id="dd066-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dd066-104">SYNTAX</span></span>

### <span data-ttu-id="dd066-105">ShareName (기본값)</span><span class="sxs-lookup"><span data-stu-id="dd066-105">ShareName (Default)</span></span>
```
Remove-AzStorageShare [-Name] <String> [-IncludeAllSnapshot] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd066-106">공유</span><span class="sxs-lookup"><span data-stu-id="dd066-106">Share</span></span>
```
Remove-AzStorageShare [-Share] <CloudFileShare> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd066-107">설명은</span><span class="sxs-lookup"><span data-stu-id="dd066-107">DESCRIPTION</span></span>
<span data-ttu-id="dd066-108">**제거-AzStorageShare** cmdlet은 파일 공유를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-108">The **Remove-AzStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="dd066-109">예제의</span><span class="sxs-lookup"><span data-stu-id="dd066-109">EXAMPLES</span></span>

### <span data-ttu-id="dd066-110">예제 1: 파일 공유 제거</span><span class="sxs-lookup"><span data-stu-id="dd066-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="dd066-111">이 명령은 ContosoShare06 이라는 이름의 파일 공유를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-111">This command removes the file share named ContosoShare06.</span></span>

### <span data-ttu-id="dd066-112">예제 2: 파일 공유 및 모든 스냅숏 제거</span><span class="sxs-lookup"><span data-stu-id="dd066-112">Example 2: Remove a file share and all its snapshots</span></span>
```
PS C:\>Remove-AzStorageShare -Name "ContosoShare06" -IncludeAllSnapshot
```

<span data-ttu-id="dd066-113">이 명령은 ContosoShare06 이라는 파일 공유 및 모든 해당 스냅샷을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-113">This command removes the file share named ContosoShare06 and all its snapshots.</span></span>

## <span data-ttu-id="dd066-114">변수</span><span class="sxs-lookup"><span data-stu-id="dd066-114">PARAMETERS</span></span>

### <span data-ttu-id="dd066-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="dd066-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="dd066-116">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="dd066-117">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="dd066-118">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="dd066-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="dd066-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="dd066-120">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="dd066-121">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="dd066-122">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="dd066-123">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="dd066-124">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-124">The default value is 10.</span></span>

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

### <span data-ttu-id="dd066-125">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="dd066-125">-Context</span></span>
<span data-ttu-id="dd066-126">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-126">Specifies an Azure storage context.</span></span>
<span data-ttu-id="dd066-127">저장소 컨텍스트를 얻으려면 [New AzStorageContext](./New-AzStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-127">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="dd066-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd066-128">-DefaultProfile</span></span>
<span data-ttu-id="dd066-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd066-130">-Force</span><span class="sxs-lookup"><span data-stu-id="dd066-130">-Force</span></span>
<span data-ttu-id="dd066-131">모든 스냅샷과 모든 콘텐츠와 함께 공유를 강제로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-131">Force to remove the share with all of its snapshots, and all content.</span></span>

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

### <span data-ttu-id="dd066-132">-IncludeAllSnapshot</span><span class="sxs-lookup"><span data-stu-id="dd066-132">-IncludeAllSnapshot</span></span>
<span data-ttu-id="dd066-133">모든 스냅숏에서 파일 공유 제거</span><span class="sxs-lookup"><span data-stu-id="dd066-133">Remove File Share with all of its snapshots</span></span>

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

### <span data-ttu-id="dd066-134">-이름</span><span class="sxs-lookup"><span data-stu-id="dd066-134">-Name</span></span>
<span data-ttu-id="dd066-135">파일 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-135">Specifies the name of the file share.</span></span>
<span data-ttu-id="dd066-136">이 cmdlet은이 매개 변수에서 지정 하는 파일 공유를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-136">This cmdlet deletes the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="dd066-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd066-137">-PassThru</span></span>
<span data-ttu-id="dd066-138">이 cmdlet이 작업의 성공 여부를 반영 하는 **Boolean** 을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-138">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="dd066-139">기본적으로이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-139">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="dd066-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="dd066-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="dd066-141">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="dd066-142">-공유</span><span class="sxs-lookup"><span data-stu-id="dd066-142">-Share</span></span>
<span data-ttu-id="dd066-143">**Cloudfileshare** 되지 않는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="dd066-144">이 cmdlet은이 매개 변수에서 지정 하는 개체를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-144">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="dd066-145">**Cloudfileshare** 되지 않는 개체를 가져오려면 Get-AzStorageShare cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-145">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="dd066-146">이 개체는 저장소 컨텍스트를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-146">This object contains the storage context.</span></span>
<span data-ttu-id="dd066-147">이 매개 변수를 지정 하는 경우 *컨텍스트* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="dd066-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="dd066-148">-확인</span><span class="sxs-lookup"><span data-stu-id="dd066-148">-Confirm</span></span>
<span data-ttu-id="dd066-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd066-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd066-150">-WhatIf</span></span>
<span data-ttu-id="dd066-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd066-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd066-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd066-153">CommonParameters</span></span>
<span data-ttu-id="dd066-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd066-155">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd066-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd066-156">입력</span><span class="sxs-lookup"><span data-stu-id="dd066-156">INPUTS</span></span>

### <span data-ttu-id="dd066-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dd066-157">System.String</span></span>

### <span data-ttu-id="dd066-158">Microsoft. c m m. c a c 파일 공유</span><span class="sxs-lookup"><span data-stu-id="dd066-158">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="dd066-159">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="dd066-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="dd066-160">출력</span><span class="sxs-lookup"><span data-stu-id="dd066-160">OUTPUTS</span></span>

### <span data-ttu-id="dd066-161">WindowsAzure. ResourceModel를 AzureStorageFileShare로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="dd066-161">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="dd066-162">상속자</span><span class="sxs-lookup"><span data-stu-id="dd066-162">NOTES</span></span>

## <span data-ttu-id="dd066-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dd066-163">RELATED LINKS</span></span>

[<span data-ttu-id="dd066-164">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="dd066-164">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="dd066-165">새로운 AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="dd066-165">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="dd066-166">새로운 AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="dd066-166">New-AzStorageShare</span></span>](./New-AzStorageShare.md)
