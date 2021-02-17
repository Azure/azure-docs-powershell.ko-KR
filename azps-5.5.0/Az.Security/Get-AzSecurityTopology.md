---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityTopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityTopology.md
ms.openlocfilehash: ef984a1cbb1cf922ddc931a7924a5d39ba6c6a0b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198732"
---
# <span data-ttu-id="1c947-101">Get-AzSecurityTopology</span><span class="sxs-lookup"><span data-stu-id="1c947-101">Get-AzSecurityTopology</span></span>

## <span data-ttu-id="1c947-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c947-102">SYNOPSIS</span></span>
<span data-ttu-id="1c947-103">구독에 대한 보안 토폴로지 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1c947-103">Gets a list of Security Topologies on a subscription</span></span>

## <span data-ttu-id="1c947-104">구문</span><span class="sxs-lookup"><span data-stu-id="1c947-104">SYNTAX</span></span>

### <span data-ttu-id="1c947-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="1c947-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityTopology [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c947-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="1c947-106">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c947-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c947-107">ResourceId</span></span>
```
Get-AzSecurityTopology -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1c947-108">설명</span><span class="sxs-lookup"><span data-stu-id="1c947-108">DESCRIPTION</span></span>
<span data-ttu-id="1c947-109">Azure Security Center에서 보안 토폴로지가 자동으로 검색됩니다. 이 cmdlet을 사용하여 보안 토폴로지 보기</span><span class="sxs-lookup"><span data-stu-id="1c947-109">Security Topologies are automatically discovered by Azure Security Center, use this cmdlet to view security topologies.</span></span>

## <span data-ttu-id="1c947-110">예제</span><span class="sxs-lookup"><span data-stu-id="1c947-110">EXAMPLES</span></span>

### <span data-ttu-id="1c947-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="1c947-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityTopology
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="1c947-112">구독의 모든 보안 토폴로지 보기</span><span class="sxs-lookup"><span data-stu-id="1c947-112">View all security topologies in a subscription</span></span>

### <span data-ttu-id="1c947-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="1c947-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityTopology -ResourceGroupName "myService1" -Location "centralus" -Name "virtualMachines"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/topologies/virtualMachines
Name:   virtualMachines
Type:   Microsoft.Security/locations/topologies
CalculatedDateTime: 03-Jun-20 3:03:48 PM
TopologyResources:  /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="1c947-114">특정 보안 토폴로지 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1c947-114">Get a specific security topologies</span></span>

## <span data-ttu-id="1c947-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c947-115">PARAMETERS</span></span>

### <span data-ttu-id="1c947-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c947-116">-DefaultProfile</span></span>
<span data-ttu-id="1c947-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1c947-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c947-118">-Location</span><span class="sxs-lookup"><span data-stu-id="1c947-118">-Location</span></span>
<span data-ttu-id="1c947-119">위치.</span><span class="sxs-lookup"><span data-stu-id="1c947-119">Location.</span></span>

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

### <span data-ttu-id="1c947-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1c947-120">-Name</span></span>
<span data-ttu-id="1c947-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c947-121">Resource name.</span></span>

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

### <span data-ttu-id="1c947-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c947-122">-ResourceGroupName</span></span>
<span data-ttu-id="1c947-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1c947-123">Resource group name.</span></span>

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

### <span data-ttu-id="1c947-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c947-124">-ResourceId</span></span>
<span data-ttu-id="1c947-125">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1c947-125">Resource ID.</span></span>

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

### <span data-ttu-id="1c947-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c947-126">CommonParameters</span></span>
<span data-ttu-id="1c947-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1c947-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c947-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1c947-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c947-129">입력</span><span class="sxs-lookup"><span data-stu-id="1c947-129">INPUTS</span></span>

### <span data-ttu-id="1c947-130">System.String</span><span class="sxs-lookup"><span data-stu-id="1c947-130">System.String</span></span>

## <span data-ttu-id="1c947-131">출력</span><span class="sxs-lookup"><span data-stu-id="1c947-131">OUTPUTS</span></span>

### <span data-ttu-id="1c947-132">Microsoft.Azure.Commands.Security.Models.Topology.PSSecurityTopologies</span><span class="sxs-lookup"><span data-stu-id="1c947-132">Microsoft.Azure.Commands.Security.Models.Topology.PSSecurityTopologies</span></span>

## <span data-ttu-id="1c947-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1c947-133">NOTES</span></span>

## <span data-ttu-id="1c947-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c947-134">RELATED LINKS</span></span>
