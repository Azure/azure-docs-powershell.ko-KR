---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 64eb11604d1b75682b95851f87ff8aa9d2b26466
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531545"
---
# <span data-ttu-id="eeb52-101">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eeb52-101">Remove-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="eeb52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eeb52-102">SYNOPSIS</span></span>
<span data-ttu-id="eeb52-103">저장소 공유에서 저장 된 액세스 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="eeb52-103">Removes a stored access policy from a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eeb52-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eeb52-104">SYNTAX</span></span>

```
Remove-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eeb52-105">설명은</span><span class="sxs-lookup"><span data-stu-id="eeb52-105">DESCRIPTION</span></span>
<span data-ttu-id="eeb52-106">**AzureStorageShareStoredAccessPolicy** Cmdlet은 Azure 저장소 공유에서 저장 된 액세스 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="eeb52-106">The **Remove-AzureStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="eeb52-107">예제의</span><span class="sxs-lookup"><span data-stu-id="eeb52-107">EXAMPLES</span></span>

### <span data-ttu-id="eeb52-108">예제 1: Azure 저장소 공유에서 저장 된 액세스 정책 제거</span><span class="sxs-lookup"><span data-stu-id="eeb52-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="eeb52-109">이 명령은 ContosoShare에서 일반 정책 이라는 저장 된 액세스 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="eeb52-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="eeb52-110">변수</span><span class="sxs-lookup"><span data-stu-id="eeb52-110">PARAMETERS</span></span>

### <span data-ttu-id="eeb52-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="eeb52-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="eeb52-112">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eeb52-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="eeb52-113">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="eeb52-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="eeb52-114">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="eeb52-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="eeb52-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="eeb52-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="eeb52-116">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eeb52-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="eeb52-117">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eeb52-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="eeb52-118">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="eeb52-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="eeb52-119">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eeb52-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="eeb52-120">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="eeb52-120">The default value is 10.</span></span>

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

### <span data-ttu-id="eeb52-121">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="eeb52-121">-Context</span></span>
<span data-ttu-id="eeb52-122">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eeb52-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="eeb52-123">저장소 컨텍스트를 얻으려면 [새로운-AzureStorageContext](./New-AzureStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eeb52-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb52-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeb52-124">-DefaultProfile</span></span>
<span data-ttu-id="eeb52-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eeb52-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eeb52-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eeb52-126">-PassThru</span></span>
<span data-ttu-id="eeb52-127">이 cmdlet이 작업의 성공 여부를 반영 하는 **Boolean** 을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="eeb52-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="eeb52-128">기본적으로이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eeb52-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="eeb52-129">-정책</span><span class="sxs-lookup"><span data-stu-id="eeb52-129">-Policy</span></span>
<span data-ttu-id="eeb52-130">이 cmdlet이 제거 하는 저장 된 액세스 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eeb52-130">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb52-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="eeb52-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="eeb52-132">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eeb52-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="eeb52-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="eeb52-133">-ShareName</span></span>
<span data-ttu-id="eeb52-134">이 cmdlet이 정책을 제거할 저장소 공유 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eeb52-134">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb52-135">-확인</span><span class="sxs-lookup"><span data-stu-id="eeb52-135">-Confirm</span></span>
<span data-ttu-id="eeb52-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eeb52-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eeb52-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeb52-137">-WhatIf</span></span>
<span data-ttu-id="eeb52-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="eeb52-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eeb52-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eeb52-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eeb52-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeb52-140">CommonParameters</span></span>
<span data-ttu-id="eeb52-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eeb52-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeb52-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeb52-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeb52-143">입력</span><span class="sxs-lookup"><span data-stu-id="eeb52-143">INPUTS</span></span>

### <span data-ttu-id="eeb52-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="eeb52-144">System.String</span></span>

### <span data-ttu-id="eeb52-145">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="eeb52-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="eeb52-146">출력</span><span class="sxs-lookup"><span data-stu-id="eeb52-146">OUTPUTS</span></span>

### <span data-ttu-id="eeb52-147">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="eeb52-147">System.Boolean</span></span>

## <span data-ttu-id="eeb52-148">상속자</span><span class="sxs-lookup"><span data-stu-id="eeb52-148">NOTES</span></span>

## <span data-ttu-id="eeb52-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eeb52-149">RELATED LINKS</span></span>

[<span data-ttu-id="eeb52-150">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eeb52-150">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="eeb52-151">새로운 AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eeb52-151">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="eeb52-152">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="eeb52-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="eeb52-153">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="eeb52-153">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
