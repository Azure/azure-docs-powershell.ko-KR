---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/powershell/module/az.rediscache/get-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
ms.openlocfilehash: 1d5f230070f8b8c269137e07b04af970f314d564
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987555"
---
# <span data-ttu-id="67235-101">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="67235-101">Get-AzRedisCacheKey</span></span>

## <span data-ttu-id="67235-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67235-102">SYNOPSIS</span></span>
<span data-ttu-id="67235-103">Redis Cache에 대한 액세스 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67235-103">Gets the access keys for a Redis Cache.</span></span>

## <span data-ttu-id="67235-104">구문</span><span class="sxs-lookup"><span data-stu-id="67235-104">SYNTAX</span></span>

```
Get-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67235-105">설명</span><span class="sxs-lookup"><span data-stu-id="67235-105">DESCRIPTION</span></span>
<span data-ttu-id="67235-106">**Get-AzRedisCacheKey** cmdlet은 Azure Redis Cache에 대한 액세스 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67235-106">The **Get-AzRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="67235-107">예제</span><span class="sxs-lookup"><span data-stu-id="67235-107">EXAMPLES</span></span>

### <span data-ttu-id="67235-108">예제 1: Redis Cache에 대한 액세스 키 사용</span><span class="sxs-lookup"><span data-stu-id="67235-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="67235-109">이 명령은 MyCacheKey라는 액세스 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67235-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="67235-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="67235-110">PARAMETERS</span></span>

### <span data-ttu-id="67235-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67235-111">-DefaultProfile</span></span>
<span data-ttu-id="67235-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="67235-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67235-113">-Name</span><span class="sxs-lookup"><span data-stu-id="67235-113">-Name</span></span>
<span data-ttu-id="67235-114">Redis Cache의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="67235-114">Specifies the name of a Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67235-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67235-115">-ResourceGroupName</span></span>
<span data-ttu-id="67235-116">Redis Cache를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="67235-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67235-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67235-117">CommonParameters</span></span>
<span data-ttu-id="67235-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="67235-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67235-119">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="67235-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67235-120">입력</span><span class="sxs-lookup"><span data-stu-id="67235-120">INPUTS</span></span>

### <span data-ttu-id="67235-121">System.String</span><span class="sxs-lookup"><span data-stu-id="67235-121">System.String</span></span>

## <span data-ttu-id="67235-122">출력</span><span class="sxs-lookup"><span data-stu-id="67235-122">OUTPUTS</span></span>

### <span data-ttu-id="67235-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="67235-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="67235-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="67235-124">NOTES</span></span>

## <span data-ttu-id="67235-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67235-125">RELATED LINKS</span></span>

[<span data-ttu-id="67235-126">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="67235-126">New-AzRedisCacheKey</span></span>](./New-AzRedisCacheKey.md)


