---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
ms.openlocfilehash: 5588a3abecdec741aa6630083c38c01178669bae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178972"
---
# <span data-ttu-id="1330c-101">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="1330c-101">Get-AzRedisCacheKey</span></span>

## <span data-ttu-id="1330c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1330c-102">SYNOPSIS</span></span>
<span data-ttu-id="1330c-103">Redis Cache에 대한 액세스 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1330c-103">Gets the access keys for a Redis Cache.</span></span>

## <span data-ttu-id="1330c-104">구문</span><span class="sxs-lookup"><span data-stu-id="1330c-104">SYNTAX</span></span>

```
Get-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1330c-105">설명</span><span class="sxs-lookup"><span data-stu-id="1330c-105">DESCRIPTION</span></span>
<span data-ttu-id="1330c-106">**Get-AzRedisCacheKey** cmdlet은 Azure Redis Cache에 대한 액세스 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1330c-106">The **Get-AzRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="1330c-107">예제</span><span class="sxs-lookup"><span data-stu-id="1330c-107">EXAMPLES</span></span>

### <span data-ttu-id="1330c-108">예제 1: Redis Cache에 대한 선택키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1330c-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="1330c-109">이 명령은 MyCacheKey라는 액세스 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1330c-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="1330c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1330c-110">PARAMETERS</span></span>

### <span data-ttu-id="1330c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1330c-111">-DefaultProfile</span></span>
<span data-ttu-id="1330c-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1330c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1330c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="1330c-113">-Name</span></span>
<span data-ttu-id="1330c-114">Redis Cache의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1330c-114">Specifies the name of a Redis Cache.</span></span>

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

### <span data-ttu-id="1330c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1330c-115">-ResourceGroupName</span></span>
<span data-ttu-id="1330c-116">Redis Cache를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1330c-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="1330c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1330c-117">CommonParameters</span></span>
<span data-ttu-id="1330c-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1330c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1330c-119">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1330c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1330c-120">입력</span><span class="sxs-lookup"><span data-stu-id="1330c-120">INPUTS</span></span>

### <span data-ttu-id="1330c-121">System.String</span><span class="sxs-lookup"><span data-stu-id="1330c-121">System.String</span></span>

## <span data-ttu-id="1330c-122">출력</span><span class="sxs-lookup"><span data-stu-id="1330c-122">OUTPUTS</span></span>

### <span data-ttu-id="1330c-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="1330c-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="1330c-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1330c-124">NOTES</span></span>

## <span data-ttu-id="1330c-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1330c-125">RELATED LINKS</span></span>

[<span data-ttu-id="1330c-126">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="1330c-126">New-AzRedisCacheKey</span></span>](./New-AzRedisCacheKey.md)


