---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontainerstoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 0610e4ca8bf520bc9812599747968a583641dd76
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882062"
---
# <span data-ttu-id="64c02-101">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="64c02-101">New-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="64c02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64c02-102">SYNOPSIS</span></span>
<span data-ttu-id="64c02-103">Azure storage 컨테이너에 대 한 저장 된 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="64c02-103">Creates a stored access policy for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64c02-104">구문과</span><span class="sxs-lookup"><span data-stu-id="64c02-104">SYNTAX</span></span>

```
New-AzureStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="64c02-105">설명은</span><span class="sxs-lookup"><span data-stu-id="64c02-105">DESCRIPTION</span></span>
<span data-ttu-id="64c02-106">**AzureStorageContainerStoredAccessPolicy** Cmdlet은 Azure storage 컨테이너에 대해 저장 된 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="64c02-106">The **New-AzureStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="64c02-107">예제의</span><span class="sxs-lookup"><span data-stu-id="64c02-107">EXAMPLES</span></span>

### <span data-ttu-id="64c02-108">예제 1: 저장소 컨테이너에서 저장 된 액세스 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="64c02-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzureStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="64c02-109">이 명령은 MyContainer 라는 저장소 컨테이너에 Policy01 라는 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="64c02-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="64c02-110">변수</span><span class="sxs-lookup"><span data-stu-id="64c02-110">PARAMETERS</span></span>

### <span data-ttu-id="64c02-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="64c02-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="64c02-112">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c02-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="64c02-113">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c02-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="64c02-114">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c02-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="64c02-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="64c02-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="64c02-116">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c02-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="64c02-117">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64c02-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="64c02-118">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="64c02-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="64c02-119">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64c02-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="64c02-120">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="64c02-120">The default value is 10.</span></span>

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

### <span data-ttu-id="64c02-121">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="64c02-121">-Container</span></span>
<span data-ttu-id="64c02-122">Azure 저장소 컨테이너 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c02-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="64c02-123">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="64c02-123">-Context</span></span>
<span data-ttu-id="64c02-124">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c02-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="64c02-125">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c02-125">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="64c02-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64c02-126">-DefaultProfile</span></span>
<span data-ttu-id="64c02-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="64c02-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64c02-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="64c02-128">-ExpiryTime</span></span>
<span data-ttu-id="64c02-129">저장 된 액세스 정책이 무효화 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c02-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c02-130">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="64c02-130">-Permission</span></span>
<span data-ttu-id="64c02-131">컨테이너에 액세스 하는 저장 된 액세스 정책에서 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c02-131">Specifies permissions in the stored access policy to access the container.</span></span>
<span data-ttu-id="64c02-132">이는 문자열 (예: `rwd` 읽기, 쓰기 및 삭제) 이라고 한다는 점에 유의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c02-132">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c02-133">-정책</span><span class="sxs-lookup"><span data-stu-id="64c02-133">-Policy</span></span>
<span data-ttu-id="64c02-134">이 SAS 토큰에 대 한 사용 권한을 포함 하는 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c02-134">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c02-135">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="64c02-135">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="64c02-136">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c02-136">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="64c02-137">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c02-137">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="64c02-138">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c02-138">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="64c02-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="64c02-139">-StartTime</span></span>
<span data-ttu-id="64c02-140">저장 된 액세스 정책이 유효 하 게 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c02-140">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64c02-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64c02-141">CommonParameters</span></span>
<span data-ttu-id="64c02-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="64c02-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64c02-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64c02-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64c02-144">입력</span><span class="sxs-lookup"><span data-stu-id="64c02-144">INPUTS</span></span>

### <span data-ttu-id="64c02-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="64c02-145">System.String</span></span>

### <span data-ttu-id="64c02-146">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="64c02-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="64c02-147">출력</span><span class="sxs-lookup"><span data-stu-id="64c02-147">OUTPUTS</span></span>

### <span data-ttu-id="64c02-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="64c02-148">System.String</span></span>

## <span data-ttu-id="64c02-149">상속자</span><span class="sxs-lookup"><span data-stu-id="64c02-149">NOTES</span></span>

## <span data-ttu-id="64c02-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="64c02-150">RELATED LINKS</span></span>

[<span data-ttu-id="64c02-151">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="64c02-151">Get-AzureStorageContainerStoredAccessPolicy</span></span>](./Get-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="64c02-152">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="64c02-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="64c02-153">제거-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="64c02-153">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="64c02-154">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="64c02-154">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


