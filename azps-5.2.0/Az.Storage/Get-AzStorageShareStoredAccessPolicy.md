---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 2e444fba12f0ffebfd3d6679293cac31fc574e93
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324925"
---
# <span data-ttu-id="4cbea-101">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4cbea-101">Get-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="4cbea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cbea-102">SYNOPSIS</span></span>
<span data-ttu-id="4cbea-103">저장소 공유에 대한 저장된 액세스 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4cbea-103">Gets stored access policies for a Storage share.</span></span>

## <span data-ttu-id="4cbea-104">구문</span><span class="sxs-lookup"><span data-stu-id="4cbea-104">SYNTAX</span></span>

```
Get-AzStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="4cbea-105">설명</span><span class="sxs-lookup"><span data-stu-id="4cbea-105">DESCRIPTION</span></span>
<span data-ttu-id="4cbea-106">**Get-AzStorageShareStoredAccessPolicy** cmdlet은 Azure Storage 공유에 대한 저장된 액세스 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4cbea-106">The **Get-AzStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="4cbea-107">특정 정책을 얻습니다. 이름을 사용하여 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbea-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="4cbea-108">예제</span><span class="sxs-lookup"><span data-stu-id="4cbea-108">EXAMPLES</span></span>

### <span data-ttu-id="4cbea-109">예제 1: 공유에 저장된 액세스 정책 얻기</span><span class="sxs-lookup"><span data-stu-id="4cbea-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="4cbea-110">이 명령은 ContosoShare에서 GeneralPolicy라는 저장된 액세스 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4cbea-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="4cbea-111">예제 2: 공유에 저장된 모든 액세스 정책 얻기</span><span class="sxs-lookup"><span data-stu-id="4cbea-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="4cbea-112">이 명령은 ContosoShare에 저장된 모든 액세스 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4cbea-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="4cbea-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cbea-113">PARAMETERS</span></span>

### <span data-ttu-id="4cbea-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4cbea-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4cbea-115">하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbea-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4cbea-116">이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbea-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4cbea-117">이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbea-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4cbea-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4cbea-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4cbea-119">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbea-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4cbea-120">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4cbea-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4cbea-121">지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4cbea-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4cbea-122">이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4cbea-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4cbea-123">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="4cbea-123">The default value is 10.</span></span>

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

### <span data-ttu-id="4cbea-124">-Context</span><span class="sxs-lookup"><span data-stu-id="4cbea-124">-Context</span></span>
<span data-ttu-id="4cbea-125">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbea-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="4cbea-126">컨텍스트를 얻습니다. [New-AzStorageContext](./New-AzStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbea-126">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="4cbea-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cbea-127">-DefaultProfile</span></span>
<span data-ttu-id="4cbea-128">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4cbea-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cbea-129">-Policy</span><span class="sxs-lookup"><span data-stu-id="4cbea-129">-Policy</span></span>
<span data-ttu-id="4cbea-130">이 cmdlet에서 얻을 저장된 액세스 정책의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbea-130">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cbea-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4cbea-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4cbea-132">요청의 서버 부분에 대한 시간 제한 기간의 길이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbea-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4cbea-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="4cbea-133">-ShareName</span></span>
<span data-ttu-id="4cbea-134">이 cmdlet에서 정책을 받을 저장소 공유 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbea-134">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4cbea-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cbea-135">CommonParameters</span></span>
<span data-ttu-id="4cbea-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbea-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cbea-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4cbea-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cbea-138">입력</span><span class="sxs-lookup"><span data-stu-id="4cbea-138">INPUTS</span></span>

### <span data-ttu-id="4cbea-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4cbea-139">System.String</span></span>

### <span data-ttu-id="4cbea-140">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4cbea-140">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4cbea-141">출력</span><span class="sxs-lookup"><span data-stu-id="4cbea-141">OUTPUTS</span></span>

### <span data-ttu-id="4cbea-142">Microsoft.Azure.Storage.File.SharedAccessFilePolicy</span><span class="sxs-lookup"><span data-stu-id="4cbea-142">Microsoft.Azure.Storage.File.SharedAccessFilePolicy</span></span>

## <span data-ttu-id="4cbea-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4cbea-143">NOTES</span></span>

## <span data-ttu-id="4cbea-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4cbea-144">RELATED LINKS</span></span>

[<span data-ttu-id="4cbea-145">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4cbea-145">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="4cbea-146">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4cbea-146">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="4cbea-147">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4cbea-147">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="4cbea-148">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4cbea-148">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)