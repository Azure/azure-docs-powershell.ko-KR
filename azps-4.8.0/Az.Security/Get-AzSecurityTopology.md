---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityTopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
ms.openlocfilehash: ef984a1cbb1cf922ddc931a7924a5d39ba6c6a0b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047637"
---
# <span data-ttu-id="c02f9-101">Get-AzSecurityTopology</span><span class="sxs-lookup"><span data-stu-id="c02f9-101">Get-AzSecurityTopology</span></span>

## <span data-ttu-id="c02f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c02f9-102">SYNOPSIS</span></span>
<span data-ttu-id="c02f9-103">구독에 대 한 보안 토폴로지 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c02f9-103">Gets a list of Security Topologies on a subscription</span></span>

## <span data-ttu-id="c02f9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c02f9-104">SYNTAX</span></span>

### <span data-ttu-id="c02f9-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="c02f9-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityTopology [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c02f9-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="c02f9-106">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c02f9-107">리소스</span><span class="sxs-lookup"><span data-stu-id="c02f9-107">ResourceId</span></span>
```
Get-AzSecurityTopology -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c02f9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c02f9-108">DESCRIPTION</span></span>
<span data-ttu-id="c02f9-109">보안 토폴로지가 Azure 보안 센터에서 자동으로 검색 되는 경우이 cmdlet을 사용 하 여 보안 토폴로지를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="c02f9-109">Security Topologies are automatically discovered by Azure Security Center, use this cmdlet to view security topologies.</span></span>

## <span data-ttu-id="c02f9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c02f9-110">EXAMPLES</span></span>

### <span data-ttu-id="c02f9-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c02f9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityTopology
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="c02f9-112">구독에서 모든 보안 토폴로지 보기</span><span class="sxs-lookup"><span data-stu-id="c02f9-112">View all security topologies in a subscription</span></span>

### <span data-ttu-id="c02f9-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="c02f9-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityTopology -ResourceGroupName "myService1" -Location "centralus" -Name "virtualMachines"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="c02f9-114">특정 보안 토폴로지 가져오기</span><span class="sxs-lookup"><span data-stu-id="c02f9-114">Get a specific security topologies</span></span>

## <span data-ttu-id="c02f9-115">변수</span><span class="sxs-lookup"><span data-stu-id="c02f9-115">PARAMETERS</span></span>

### <span data-ttu-id="c02f9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c02f9-116">-DefaultProfile</span></span>
<span data-ttu-id="c02f9-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c02f9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c02f9-118">-위치</span><span class="sxs-lookup"><span data-stu-id="c02f9-118">-Location</span></span>
<span data-ttu-id="c02f9-119">Location.</span><span class="sxs-lookup"><span data-stu-id="c02f9-119">Location.</span></span>

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

### <span data-ttu-id="c02f9-120">-이름</span><span class="sxs-lookup"><span data-stu-id="c02f9-120">-Name</span></span>
<span data-ttu-id="c02f9-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c02f9-121">Resource name.</span></span>

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

### <span data-ttu-id="c02f9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c02f9-122">-ResourceGroupName</span></span>
<span data-ttu-id="c02f9-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c02f9-123">Resource group name.</span></span>

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

### <span data-ttu-id="c02f9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c02f9-124">-ResourceId</span></span>
<span data-ttu-id="c02f9-125">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c02f9-125">Resource ID.</span></span>

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

### <span data-ttu-id="c02f9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c02f9-126">CommonParameters</span></span>
<span data-ttu-id="c02f9-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c02f9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c02f9-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c02f9-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c02f9-129">입력</span><span class="sxs-lookup"><span data-stu-id="c02f9-129">INPUTS</span></span>

### <span data-ttu-id="c02f9-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c02f9-130">System.String</span></span>

## <span data-ttu-id="c02f9-131">출력</span><span class="sxs-lookup"><span data-stu-id="c02f9-131">OUTPUTS</span></span>

### <span data-ttu-id="c02f9-132">Microsoft. Azure. PSSecurityTopologies.</span><span class="sxs-lookup"><span data-stu-id="c02f9-132">Microsoft.Azure.Commands.Security.Models.Topology.PSSecurityTopologies</span></span>

## <span data-ttu-id="c02f9-133">상속자</span><span class="sxs-lookup"><span data-stu-id="c02f9-133">NOTES</span></span>

## <span data-ttu-id="c02f9-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c02f9-134">RELATED LINKS</span></span>
