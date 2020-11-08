---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 2e444fba12f0ffebfd3d6679293cac31fc574e93
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042281"
---
# <span data-ttu-id="f2024-101">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f2024-101">Get-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="f2024-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2024-102">SYNOPSIS</span></span>
<span data-ttu-id="f2024-103">저장소 공유에 대 한 저장 된 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f2024-103">Gets stored access policies for a Storage share.</span></span>

## <span data-ttu-id="f2024-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f2024-104">SYNTAX</span></span>

```
Get-AzStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="f2024-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f2024-105">DESCRIPTION</span></span>
<span data-ttu-id="f2024-106">**AzStorageShareStoredAccessPolicy** Cmdlet은 Azure 저장소 공유에 대 한 저장 된 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f2024-106">The **Get-AzStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="f2024-107">특정 정책을 가져오려면 name을 기준으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2024-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="f2024-108">예제의</span><span class="sxs-lookup"><span data-stu-id="f2024-108">EXAMPLES</span></span>

### <span data-ttu-id="f2024-109">예제 1: 공유에 저장 된 액세스 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="f2024-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="f2024-110">이 명령은 ContosoShare의 일반 Policy (저장 된 액세스 정책)를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f2024-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="f2024-111">예제 2: 공유에 저장 된 모든 액세스 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="f2024-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="f2024-112">이 명령은 ContosoShare에 저장 된 모든 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f2024-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="f2024-113">변수</span><span class="sxs-lookup"><span data-stu-id="f2024-113">PARAMETERS</span></span>

### <span data-ttu-id="f2024-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f2024-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f2024-115">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2024-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f2024-116">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2024-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f2024-117">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2024-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f2024-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f2024-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f2024-119">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2024-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f2024-120">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2024-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f2024-121">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="f2024-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f2024-122">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f2024-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f2024-123">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="f2024-123">The default value is 10.</span></span>

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

### <span data-ttu-id="f2024-124">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="f2024-124">-Context</span></span>
<span data-ttu-id="f2024-125">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2024-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="f2024-126">컨텍스트를 얻으려면 [New AzStorageContext](./New-AzStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2024-126">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="f2024-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2024-127">-DefaultProfile</span></span>
<span data-ttu-id="f2024-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f2024-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2024-129">-정책</span><span class="sxs-lookup"><span data-stu-id="f2024-129">-Policy</span></span>
<span data-ttu-id="f2024-130">이 cmdlet이 가져오는 저장 된 액세스 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2024-130">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f2024-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f2024-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f2024-132">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2024-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="f2024-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="f2024-133">-ShareName</span></span>
<span data-ttu-id="f2024-134">이 cmdlet에서 정책을 가져오는 저장소 공유 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2024-134">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

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

### <span data-ttu-id="f2024-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2024-135">CommonParameters</span></span>
<span data-ttu-id="f2024-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f2024-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2024-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2024-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2024-138">입력</span><span class="sxs-lookup"><span data-stu-id="f2024-138">INPUTS</span></span>

### <span data-ttu-id="f2024-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f2024-139">System.String</span></span>

### <span data-ttu-id="f2024-140">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f2024-140">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f2024-141">출력</span><span class="sxs-lookup"><span data-stu-id="f2024-141">OUTPUTS</span></span>

### <span data-ttu-id="f2024-142">SharedAccessFilePolicy를 통해 파일 저장</span><span class="sxs-lookup"><span data-stu-id="f2024-142">Microsoft.Azure.Storage.File.SharedAccessFilePolicy</span></span>

## <span data-ttu-id="f2024-143">상속자</span><span class="sxs-lookup"><span data-stu-id="f2024-143">NOTES</span></span>

## <span data-ttu-id="f2024-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2024-144">RELATED LINKS</span></span>

[<span data-ttu-id="f2024-145">새로운 AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f2024-145">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="f2024-146">새로운 AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f2024-146">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="f2024-147">제거-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f2024-147">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="f2024-148">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f2024-148">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
