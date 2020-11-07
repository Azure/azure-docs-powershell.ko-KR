---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDiscoveredSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
ms.openlocfilehash: d5fca22bf289c42681d9af18a9eaff28587f1922
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873214"
---
# <span data-ttu-id="e6216-101">Get-AzDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="e6216-101">Get-AzDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="e6216-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6216-102">SYNOPSIS</span></span>
<span data-ttu-id="e6216-103">Azure 보안 센터에서 검색 된 보안 솔루션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e6216-103">Gets security solutions that were discovered by Azure Security Center</span></span>

## <span data-ttu-id="e6216-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e6216-104">SYNTAX</span></span>

### <span data-ttu-id="e6216-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e6216-105">SubscriptionScope (Default)</span></span>
```
Get-AzDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6216-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="e6216-106">ResourceGroupLevelResource</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6216-107">리소스</span><span class="sxs-lookup"><span data-stu-id="e6216-107">ResourceId</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6216-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e6216-108">DESCRIPTION</span></span>
<span data-ttu-id="e6216-109">보안 솔루션은 Azure 보안 센터에서 자동으로 검색 되며,이 cmdlet을 사용 하 여 검색 된 보안 솔루션을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="e6216-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="e6216-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e6216-110">EXAMPLES</span></span>

### <span data-ttu-id="e6216-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e6216-111">Example 1</span></span>
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

<span data-ttu-id="e6216-112">구독에서 검색 된 모든 보안 솔루션 가져오기</span><span class="sxs-lookup"><span data-stu-id="e6216-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="e6216-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="e6216-113">Example 2</span></span>
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

<span data-ttu-id="e6216-114">특정 검색 된 보안 솔루션 가져오기</span><span class="sxs-lookup"><span data-stu-id="e6216-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="e6216-115">변수</span><span class="sxs-lookup"><span data-stu-id="e6216-115">PARAMETERS</span></span>

### <span data-ttu-id="e6216-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6216-116">-DefaultProfile</span></span>
<span data-ttu-id="e6216-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e6216-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6216-118">-위치</span><span class="sxs-lookup"><span data-stu-id="e6216-118">-Location</span></span>
<span data-ttu-id="e6216-119">Location.</span><span class="sxs-lookup"><span data-stu-id="e6216-119">Location.</span></span>

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

### <span data-ttu-id="e6216-120">-이름</span><span class="sxs-lookup"><span data-stu-id="e6216-120">-Name</span></span>
<span data-ttu-id="e6216-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6216-121">Resource name.</span></span>

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

### <span data-ttu-id="e6216-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6216-122">-ResourceGroupName</span></span>
<span data-ttu-id="e6216-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6216-123">Resource group name.</span></span>

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

### <span data-ttu-id="e6216-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6216-124">-ResourceId</span></span>
<span data-ttu-id="e6216-125">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e6216-125">Resource ID.</span></span>

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

### <span data-ttu-id="e6216-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6216-126">CommonParameters</span></span>
<span data-ttu-id="e6216-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e6216-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6216-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6216-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6216-129">입력</span><span class="sxs-lookup"><span data-stu-id="e6216-129">INPUTS</span></span>

### <span data-ttu-id="e6216-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e6216-130">System.String</span></span>

## <span data-ttu-id="e6216-131">출력</span><span class="sxs-lookup"><span data-stu-id="e6216-131">OUTPUTS</span></span>

### <span data-ttu-id="e6216-132">DiscoveredSecuritySolutions. PSSecurityDiscoveredSecuritySolution에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="e6216-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="e6216-133">상속자</span><span class="sxs-lookup"><span data-stu-id="e6216-133">NOTES</span></span>

## <span data-ttu-id="e6216-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6216-134">RELATED LINKS</span></span>
