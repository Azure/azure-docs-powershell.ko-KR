---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmDiscoveredSecuritySolution.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmDiscoveredSecuritySolution.md
ms.openlocfilehash: ecea7ba6aa34df73de65a4d03e004531e81ff497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529390"
---
# <span data-ttu-id="b90b1-101">Get-AzureRmDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="b90b1-101">Get-AzureRmDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="b90b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b90b1-102">SYNOPSIS</span></span>
<span data-ttu-id="b90b1-103">Azure 보안 센터에서 검색 된 보안 솔루션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b90b1-103">Gets security solutions that were discovered by Azure Security Center</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b90b1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b90b1-104">SYNTAX</span></span>

### <span data-ttu-id="b90b1-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b90b1-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b90b1-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="b90b1-106">ResourceGroupLevelResource</span></span>
```
Get-AzureRmDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b90b1-107">리소스</span><span class="sxs-lookup"><span data-stu-id="b90b1-107">ResourceId</span></span>
```
Get-AzureRmDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b90b1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b90b1-108">DESCRIPTION</span></span>
<span data-ttu-id="b90b1-109">보안 솔루션은 Azure 보안 센터에서 자동으로 검색 되며,이 cmdlet을 사용 하 여 검색 된 보안 솔루션을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="b90b1-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="b90b1-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b90b1-110">EXAMPLES</span></span>

### <span data-ttu-id="b90b1-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b90b1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDiscoveredSecuritySolution
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="b90b1-112">구독에서 검색 된 모든 보안 솔루션 가져오기</span><span class="sxs-lookup"><span data-stu-id="b90b1-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="b90b1-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="b90b1-113">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmDiscoveredSecuritySolution -ResourceGroupName "myService1" -Location "centralus" -Name "ContosoWAF2"
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="b90b1-114">특정 검색 된 보안 솔루션 가져오기</span><span class="sxs-lookup"><span data-stu-id="b90b1-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="b90b1-115">변수</span><span class="sxs-lookup"><span data-stu-id="b90b1-115">PARAMETERS</span></span>

### <span data-ttu-id="b90b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b90b1-116">-DefaultProfile</span></span>
<span data-ttu-id="b90b1-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b90b1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b90b1-118">-위치</span><span class="sxs-lookup"><span data-stu-id="b90b1-118">-Location</span></span>
<span data-ttu-id="b90b1-119">Location.</span><span class="sxs-lookup"><span data-stu-id="b90b1-119">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b90b1-120">-이름</span><span class="sxs-lookup"><span data-stu-id="b90b1-120">-Name</span></span>
<span data-ttu-id="b90b1-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b90b1-121">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b90b1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b90b1-122">-ResourceGroupName</span></span>
<span data-ttu-id="b90b1-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b90b1-123">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b90b1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b90b1-124">-ResourceId</span></span>
<span data-ttu-id="b90b1-125">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b90b1-125">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b90b1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b90b1-126">CommonParameters</span></span>
<span data-ttu-id="b90b1-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b90b1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b90b1-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b90b1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b90b1-129">입력</span><span class="sxs-lookup"><span data-stu-id="b90b1-129">INPUTS</span></span>

### <span data-ttu-id="b90b1-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b90b1-130">System.String</span></span>

## <span data-ttu-id="b90b1-131">출력</span><span class="sxs-lookup"><span data-stu-id="b90b1-131">OUTPUTS</span></span>

### <span data-ttu-id="b90b1-132">DiscoveredSecuritySolutions. PSSecurityDiscoveredSecuritySolution에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="b90b1-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="b90b1-133">상속자</span><span class="sxs-lookup"><span data-stu-id="b90b1-133">NOTES</span></span>

## <span data-ttu-id="b90b1-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b90b1-134">RELATED LINKS</span></span>
