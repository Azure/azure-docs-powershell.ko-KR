---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheKey.md
ms.openlocfilehash: 67ec6bdcce5121c2a80e1f76ea1081f249f15682
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529757"
---
# <span data-ttu-id="3be49-101">Get-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="3be49-101">Get-AzureRmRedisCacheKey</span></span>

## <span data-ttu-id="3be49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3be49-102">SYNOPSIS</span></span>
<span data-ttu-id="3be49-103">Redis 캐시에 대 한 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3be49-103">Gets the access keys for a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3be49-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3be49-104">SYNTAX</span></span>

```
Get-AzureRmRedisCacheKey [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3be49-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3be49-105">DESCRIPTION</span></span>
<span data-ttu-id="3be49-106">**AzureRmRedisCacheKey** Cmdlet은 Azure Redis Cache에 대 한 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3be49-106">The **Get-AzureRmRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="3be49-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3be49-107">EXAMPLES</span></span>

### <span data-ttu-id="3be49-108">예제 1: Redis 캐시에 대 한 선택 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="3be49-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzureRmRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="3be49-109">이 명령은 MyCacheKey 라는 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3be49-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="3be49-110">변수</span><span class="sxs-lookup"><span data-stu-id="3be49-110">PARAMETERS</span></span>

### <span data-ttu-id="3be49-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3be49-111">-DefaultProfile</span></span>
<span data-ttu-id="3be49-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3be49-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3be49-113">-이름</span><span class="sxs-lookup"><span data-stu-id="3be49-113">-Name</span></span>
<span data-ttu-id="3be49-114">Redis 캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3be49-114">Specifies the name of a Redis Cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3be49-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3be49-115">-ResourceGroupName</span></span>
<span data-ttu-id="3be49-116">Redis 캐시를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3be49-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3be49-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3be49-117">CommonParameters</span></span>
<span data-ttu-id="3be49-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3be49-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3be49-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3be49-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3be49-120">입력</span><span class="sxs-lookup"><span data-stu-id="3be49-120">INPUTS</span></span>

### <span data-ttu-id="3be49-121">않아야</span><span class="sxs-lookup"><span data-stu-id="3be49-121">None</span></span>
<span data-ttu-id="3be49-122">속성 이름으로이 cmdlet에 대 한 입력을 파이프로 지정할 수 있지만 값을 기준으로 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3be49-122">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="3be49-123">출력</span><span class="sxs-lookup"><span data-stu-id="3be49-123">OUTPUTS</span></span>

### <span data-ttu-id="3be49-124">Redis. RedisAccessKeys.</span><span class="sxs-lookup"><span data-stu-id="3be49-124">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>
<span data-ttu-id="3be49-125">이 cmdlet은 Redis Cache에 대 한 기본 및 보조 선택 키를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3be49-125">This cmdlet returns primary and secondary access keys for a Redis Cache.</span></span>

## <span data-ttu-id="3be49-126">상속자</span><span class="sxs-lookup"><span data-stu-id="3be49-126">NOTES</span></span>

## <span data-ttu-id="3be49-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3be49-127">RELATED LINKS</span></span>

[<span data-ttu-id="3be49-128">새로운 AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="3be49-128">New-AzureRmRedisCacheKey</span></span>](./New-AzureRmRedisCacheKey.md)


