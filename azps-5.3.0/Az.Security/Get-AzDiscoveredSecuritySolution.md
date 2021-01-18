---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDiscoveredSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
ms.openlocfilehash: 1fbe9e790966a92c38ba79b56221e5e6083b649c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495042"
---
# <span data-ttu-id="34a21-101">Get-AzDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="34a21-101">Get-AzDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="34a21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34a21-102">SYNOPSIS</span></span>
<span data-ttu-id="34a21-103">Azure Security Center에서 검색한 보안 솔루션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="34a21-103">Gets security solutions that were discovered by Azure Security Center</span></span>

## <span data-ttu-id="34a21-104">구문</span><span class="sxs-lookup"><span data-stu-id="34a21-104">SYNTAX</span></span>

### <span data-ttu-id="34a21-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="34a21-105">SubscriptionScope (Default)</span></span>
```
Get-AzDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34a21-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="34a21-106">ResourceGroupLevelResource</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34a21-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="34a21-107">ResourceId</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34a21-108">설명</span><span class="sxs-lookup"><span data-stu-id="34a21-108">DESCRIPTION</span></span>
<span data-ttu-id="34a21-109">보안 솔루션은 Azure Security Center에서 자동으로 검색됩니다. 검색된 보안 솔루션을 보기 위해 이 cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="34a21-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="34a21-110">예제</span><span class="sxs-lookup"><span data-stu-id="34a21-110">EXAMPLES</span></span>

### <span data-ttu-id="34a21-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="34a21-111">Example 1</span></span>
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

<span data-ttu-id="34a21-112">구독에서 검색된 보안 솔루션 모두를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="34a21-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="34a21-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="34a21-113">Example 2</span></span>
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

<span data-ttu-id="34a21-114">검색된 특정 보안 솔루션 얻기</span><span class="sxs-lookup"><span data-stu-id="34a21-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="34a21-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34a21-115">PARAMETERS</span></span>

### <span data-ttu-id="34a21-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34a21-116">-DefaultProfile</span></span>
<span data-ttu-id="34a21-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="34a21-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34a21-118">-Location</span><span class="sxs-lookup"><span data-stu-id="34a21-118">-Location</span></span>
<span data-ttu-id="34a21-119">위치.</span><span class="sxs-lookup"><span data-stu-id="34a21-119">Location.</span></span>

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

### <span data-ttu-id="34a21-120">-Name</span><span class="sxs-lookup"><span data-stu-id="34a21-120">-Name</span></span>
<span data-ttu-id="34a21-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="34a21-121">Resource name.</span></span>

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

### <span data-ttu-id="34a21-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34a21-122">-ResourceGroupName</span></span>
<span data-ttu-id="34a21-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="34a21-123">Resource group name.</span></span>

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

### <span data-ttu-id="34a21-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34a21-124">-ResourceId</span></span>
<span data-ttu-id="34a21-125">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="34a21-125">Resource ID.</span></span>

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

### <span data-ttu-id="34a21-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34a21-126">CommonParameters</span></span>
<span data-ttu-id="34a21-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="34a21-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34a21-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="34a21-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34a21-129">입력</span><span class="sxs-lookup"><span data-stu-id="34a21-129">INPUTS</span></span>

### <span data-ttu-id="34a21-130">System.String</span><span class="sxs-lookup"><span data-stu-id="34a21-130">System.String</span></span>

## <span data-ttu-id="34a21-131">출력</span><span class="sxs-lookup"><span data-stu-id="34a21-131">OUTPUTS</span></span>

### <span data-ttu-id="34a21-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="34a21-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="34a21-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="34a21-133">NOTES</span></span>

## <span data-ttu-id="34a21-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34a21-134">RELATED LINKS</span></span>
