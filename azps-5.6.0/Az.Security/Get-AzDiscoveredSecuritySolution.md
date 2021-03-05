---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzDiscoveredSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
ms.openlocfilehash: d351ab76941d16e3d3e091e223524863d4256d75
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986589"
---
# <span data-ttu-id="639c8-101">Get-AzDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="639c8-101">Get-AzDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="639c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="639c8-102">SYNOPSIS</span></span>
<span data-ttu-id="639c8-103">Azure Security Center에서 검색된 보안 솔루션을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="639c8-103">Gets security solutions that were discovered by Azure Security Center</span></span>

## <span data-ttu-id="639c8-104">구문</span><span class="sxs-lookup"><span data-stu-id="639c8-104">SYNTAX</span></span>

### <span data-ttu-id="639c8-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="639c8-105">SubscriptionScope (Default)</span></span>
```
Get-AzDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="639c8-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="639c8-106">ResourceGroupLevelResource</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="639c8-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="639c8-107">ResourceId</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="639c8-108">설명</span><span class="sxs-lookup"><span data-stu-id="639c8-108">DESCRIPTION</span></span>
<span data-ttu-id="639c8-109">보안 솔루션은 Azure Security Center에서 자동으로 검색되며, 이 cmdlet을 사용하여 검색된 보안 솔루션을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="639c8-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="639c8-110">예제</span><span class="sxs-lookup"><span data-stu-id="639c8-110">EXAMPLES</span></span>

### <span data-ttu-id="639c8-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="639c8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDiscoveredSecuritySolution
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="639c8-112">구독에서 검색된 모든 보안 솔루션 사용</span><span class="sxs-lookup"><span data-stu-id="639c8-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="639c8-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="639c8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDiscoveredSecuritySolution -ResourceGroupName "myService1" -Location "centralus" -Name "ContosoWAF2"
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="639c8-114">특정 검색된 보안 솔루션 사용</span><span class="sxs-lookup"><span data-stu-id="639c8-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="639c8-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="639c8-115">PARAMETERS</span></span>

### <span data-ttu-id="639c8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="639c8-116">-DefaultProfile</span></span>
<span data-ttu-id="639c8-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="639c8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="639c8-118">-Location</span><span class="sxs-lookup"><span data-stu-id="639c8-118">-Location</span></span>
<span data-ttu-id="639c8-119">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="639c8-119">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="639c8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="639c8-120">-Name</span></span>
<span data-ttu-id="639c8-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="639c8-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="639c8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="639c8-122">-ResourceGroupName</span></span>
<span data-ttu-id="639c8-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="639c8-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="639c8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="639c8-124">-ResourceId</span></span>
<span data-ttu-id="639c8-125">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="639c8-125">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="639c8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="639c8-126">CommonParameters</span></span>
<span data-ttu-id="639c8-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="639c8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="639c8-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="639c8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="639c8-129">입력</span><span class="sxs-lookup"><span data-stu-id="639c8-129">INPUTS</span></span>

### <span data-ttu-id="639c8-130">System.String</span><span class="sxs-lookup"><span data-stu-id="639c8-130">System.String</span></span>

## <span data-ttu-id="639c8-131">출력</span><span class="sxs-lookup"><span data-stu-id="639c8-131">OUTPUTS</span></span>

### <span data-ttu-id="639c8-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="639c8-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="639c8-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="639c8-133">NOTES</span></span>

## <span data-ttu-id="639c8-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="639c8-134">RELATED LINKS</span></span>
