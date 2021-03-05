---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
ms.openlocfilehash: 52b6a4b7c5f78359ffc046953101aaa01bb7a435
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993925"
---
# <span data-ttu-id="7f62b-101">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7f62b-101">Get-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="7f62b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f62b-102">SYNOPSIS</span></span>
<span data-ttu-id="7f62b-103">애플리케이션 보안 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7f62b-103">Gets an application security group.</span></span>

## <span data-ttu-id="7f62b-104">구문</span><span class="sxs-lookup"><span data-stu-id="7f62b-104">SYNTAX</span></span>

```
Get-AzApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f62b-105">설명</span><span class="sxs-lookup"><span data-stu-id="7f62b-105">DESCRIPTION</span></span>
<span data-ttu-id="7f62b-106">**Get-AzApplicationSecurityGroup** cmdlet은 애플리케이션 보안 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7f62b-106">The **Get-AzApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="7f62b-107">예제</span><span class="sxs-lookup"><span data-stu-id="7f62b-107">EXAMPLES</span></span>

### <span data-ttu-id="7f62b-108">예제 1: 모든 애플리케이션 보안 그룹을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="7f62b-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="7f62b-109">위의 명령은 구독의 모든 애플리케이션 보안 그룹을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7f62b-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="7f62b-110">예제 2: 리소스 그룹에서 애플리케이션 보안 그룹을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="7f62b-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="7f62b-111">위의 명령은 리소스 그룹에 속하는 모든 애플리케이션 보안 그룹을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7f62b-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="7f62b-112">예제 3: 특정 애플리케이션 보안 그룹을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="7f62b-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1
```

<span data-ttu-id="7f62b-113">위의 명령은 리소스 그룹 MyResourceGroup의 애플리케이션 보안 그룹 MyApplicationSecurityGroup을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7f62b-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="7f62b-114">예제 4: 필터링을 사용하여 애플리케이션 보안 그룹을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="7f62b-114">Example 4: Retrieve application security groups using filtering.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -Name MyApplicationSecurityGroup*

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="7f62b-115">위의 명령은 "MyApplicationSecurityGroup"으로 시작하는 모든 애플리케이션 보안 그룹을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7f62b-115">The command above returns all application security groups that start with "MyApplicationSecurityGroup".</span></span>

## <span data-ttu-id="7f62b-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7f62b-116">PARAMETERS</span></span>

### <span data-ttu-id="7f62b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f62b-117">-DefaultProfile</span></span>
<span data-ttu-id="7f62b-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7f62b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f62b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7f62b-119">-Name</span></span>
<span data-ttu-id="7f62b-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f62b-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="7f62b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f62b-121">-ResourceGroupName</span></span>
<span data-ttu-id="7f62b-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f62b-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="7f62b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f62b-123">CommonParameters</span></span>
<span data-ttu-id="7f62b-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7f62b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f62b-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7f62b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f62b-126">입력</span><span class="sxs-lookup"><span data-stu-id="7f62b-126">INPUTS</span></span>

### <span data-ttu-id="7f62b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="7f62b-127">System.String</span></span>

## <span data-ttu-id="7f62b-128">출력</span><span class="sxs-lookup"><span data-stu-id="7f62b-128">OUTPUTS</span></span>

### <span data-ttu-id="7f62b-129">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7f62b-129">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="7f62b-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7f62b-130">NOTES</span></span>

## <span data-ttu-id="7f62b-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f62b-131">RELATED LINKS</span></span>

[<span data-ttu-id="7f62b-132">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7f62b-132">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="7f62b-133">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7f62b-133">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="7f62b-134">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7f62b-134">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7f62b-135">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7f62b-135">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)
