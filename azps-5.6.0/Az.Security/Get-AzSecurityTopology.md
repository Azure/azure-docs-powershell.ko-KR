---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityTopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
ms.openlocfilehash: 0f6cbe88eaabb49a07bb0704f0d6ea547449a229
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990752"
---
# <span data-ttu-id="1c3a0-101">Get-AzSecurityTopology</span><span class="sxs-lookup"><span data-stu-id="1c3a0-101">Get-AzSecurityTopology</span></span>

## <span data-ttu-id="1c3a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c3a0-102">SYNOPSIS</span></span>
<span data-ttu-id="1c3a0-103">구독에서 보안 토폴로지 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1c3a0-103">Gets a list of Security Topologies on a subscription</span></span>

## <span data-ttu-id="1c3a0-104">구문</span><span class="sxs-lookup"><span data-stu-id="1c3a0-104">SYNTAX</span></span>

### <span data-ttu-id="1c3a0-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="1c3a0-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityTopology [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c3a0-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="1c3a0-106">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c3a0-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c3a0-107">ResourceId</span></span>
```
Get-AzSecurityTopology -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1c3a0-108">설명</span><span class="sxs-lookup"><span data-stu-id="1c3a0-108">DESCRIPTION</span></span>
<span data-ttu-id="1c3a0-109">보안 토폴로지는 Azure Security Center에서 자동으로 검색되며 이 cmdlet을 사용하여 보안 토폴로지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c3a0-109">Security Topologies are automatically discovered by Azure Security Center, use this cmdlet to view security topologies.</span></span>

## <span data-ttu-id="1c3a0-110">예제</span><span class="sxs-lookup"><span data-stu-id="1c3a0-110">EXAMPLES</span></span>

### <span data-ttu-id="1c3a0-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="1c3a0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityTopology
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="1c3a0-112">구독의 모든 보안 토폴로지 보기</span><span class="sxs-lookup"><span data-stu-id="1c3a0-112">View all security topologies in a subscription</span></span>

### <span data-ttu-id="1c3a0-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="1c3a0-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityTopology -ResourceGroupName "myService1" -Location "centralus" -Name "virtualMachines"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="1c3a0-114">특정 보안 토폴로지 사용</span><span class="sxs-lookup"><span data-stu-id="1c3a0-114">Get a specific security topologies</span></span>

## <span data-ttu-id="1c3a0-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1c3a0-115">PARAMETERS</span></span>

### <span data-ttu-id="1c3a0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c3a0-116">-DefaultProfile</span></span>
<span data-ttu-id="1c3a0-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3a0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c3a0-118">-Location</span><span class="sxs-lookup"><span data-stu-id="1c3a0-118">-Location</span></span>
<span data-ttu-id="1c3a0-119">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3a0-119">Location.</span></span>

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

### <span data-ttu-id="1c3a0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1c3a0-120">-Name</span></span>
<span data-ttu-id="1c3a0-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3a0-121">Resource name.</span></span>

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

### <span data-ttu-id="1c3a0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c3a0-122">-ResourceGroupName</span></span>
<span data-ttu-id="1c3a0-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3a0-123">Resource group name.</span></span>

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

### <span data-ttu-id="1c3a0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c3a0-124">-ResourceId</span></span>
<span data-ttu-id="1c3a0-125">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1c3a0-125">Resource ID.</span></span>

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

### <span data-ttu-id="1c3a0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c3a0-126">CommonParameters</span></span>
<span data-ttu-id="1c3a0-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1c3a0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c3a0-128">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1c3a0-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c3a0-129">입력</span><span class="sxs-lookup"><span data-stu-id="1c3a0-129">INPUTS</span></span>

### <span data-ttu-id="1c3a0-130">System.String</span><span class="sxs-lookup"><span data-stu-id="1c3a0-130">System.String</span></span>

## <span data-ttu-id="1c3a0-131">출력</span><span class="sxs-lookup"><span data-stu-id="1c3a0-131">OUTPUTS</span></span>

### <span data-ttu-id="1c3a0-132">Microsoft.Azure.Commands.Security.Models.Topology.PSSecurityTopologies</span><span class="sxs-lookup"><span data-stu-id="1c3a0-132">Microsoft.Azure.Commands.Security.Models.Topology.PSSecurityTopologies</span></span>

## <span data-ttu-id="1c3a0-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1c3a0-133">NOTES</span></span>

## <span data-ttu-id="1c3a0-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c3a0-134">RELATED LINKS</span></span>
