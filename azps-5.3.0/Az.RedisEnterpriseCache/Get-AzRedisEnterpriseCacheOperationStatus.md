---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecacheoperationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheOperationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheOperationStatus.md
ms.openlocfilehash: 8416c18ac945eaab5ae9dbd758d2660c4f950417
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378239"
---
# <span data-ttu-id="73992-101">Get-AzRedisEnterpriseCacheOperationStatus</span><span class="sxs-lookup"><span data-stu-id="73992-101">Get-AzRedisEnterpriseCacheOperationStatus</span></span>

## <span data-ttu-id="73992-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73992-102">SYNOPSIS</span></span>
<span data-ttu-id="73992-103">작업의 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="73992-103">Gets the status of operation.</span></span>

## <span data-ttu-id="73992-104">구문</span><span class="sxs-lookup"><span data-stu-id="73992-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheOperationStatus -Location <String> -OperationId <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="73992-105">설명</span><span class="sxs-lookup"><span data-stu-id="73992-105">DESCRIPTION</span></span>
<span data-ttu-id="73992-106">작업의 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="73992-106">Gets the status of operation.</span></span>

## <span data-ttu-id="73992-107">예제</span><span class="sxs-lookup"><span data-stu-id="73992-107">EXAMPLES</span></span>

### <span data-ttu-id="73992-108">예제 1: 작업 상태 확인</span><span class="sxs-lookup"><span data-stu-id="73992-108">Example 1: Get operation status</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheOperationStatus -Location "East US" -OperationId "6432a8f9-0fe6-4339-9303-772c92f35d02"

EndTime                           Name                                 StartTime                         Status
-------                           ----                                 ---------                         ------
2020-12-01T00:12:45.7107366+00:00 6432a8f9-0fe6-4339-9303-772c92f35d02 2020-12-01T00:04:35.7061294+00:00 Succeeded

```

<span data-ttu-id="73992-109">이 명령은 작업의 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="73992-109">This command gets the status of an operation.</span></span>

## <span data-ttu-id="73992-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73992-110">PARAMETERS</span></span>

### <span data-ttu-id="73992-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73992-111">-DefaultProfile</span></span>
<span data-ttu-id="73992-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="73992-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73992-113">-Location</span><span class="sxs-lookup"><span data-stu-id="73992-113">-Location</span></span>
<span data-ttu-id="73992-114">작업이 있는 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="73992-114">The region the operation is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73992-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="73992-115">-OperationId</span></span>
<span data-ttu-id="73992-116">작업의 고유 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="73992-116">The operation's unique identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73992-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="73992-117">-SubscriptionId</span></span>
<span data-ttu-id="73992-118">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="73992-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="73992-119">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="73992-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73992-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73992-120">CommonParameters</span></span>
<span data-ttu-id="73992-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73992-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73992-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="73992-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73992-123">입력</span><span class="sxs-lookup"><span data-stu-id="73992-123">INPUTS</span></span>

## <span data-ttu-id="73992-124">출력</span><span class="sxs-lookup"><span data-stu-id="73992-124">OUTPUTS</span></span>

### <span data-ttu-id="73992-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="73992-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IOperationStatus</span></span>

## <span data-ttu-id="73992-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="73992-126">NOTES</span></span>

<span data-ttu-id="73992-127">별칭</span><span class="sxs-lookup"><span data-stu-id="73992-127">ALIASES</span></span>

## <span data-ttu-id="73992-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="73992-128">RELATED LINKS</span></span>

