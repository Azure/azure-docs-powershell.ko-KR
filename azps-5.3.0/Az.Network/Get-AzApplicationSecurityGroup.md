---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
ms.openlocfilehash: aa03f7d410d704e8e5b9ea4b974e3050a3304342
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491805"
---
# <span data-ttu-id="ea2fd-101">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ea2fd-101">Get-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="ea2fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea2fd-102">SYNOPSIS</span></span>
<span data-ttu-id="ea2fd-103">애플리케이션 보안 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ea2fd-103">Gets an application security group.</span></span>

## <span data-ttu-id="ea2fd-104">구문</span><span class="sxs-lookup"><span data-stu-id="ea2fd-104">SYNTAX</span></span>

```
Get-AzApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea2fd-105">설명</span><span class="sxs-lookup"><span data-stu-id="ea2fd-105">DESCRIPTION</span></span>
<span data-ttu-id="ea2fd-106">**Get-AzApplicationSecurityGroup** cmdlet은 애플리케이션 보안 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ea2fd-106">The **Get-AzApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="ea2fd-107">예제</span><span class="sxs-lookup"><span data-stu-id="ea2fd-107">EXAMPLES</span></span>

### <span data-ttu-id="ea2fd-108">예제 1: 모든 애플리케이션 보안 그룹을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2fd-108">Example 1: Retrieve all application security groups.</span></span>
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

<span data-ttu-id="ea2fd-109">위의 명령은 구독의 모든 애플리케이션 보안 그룹을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2fd-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="ea2fd-110">예제 2: 리소스 그룹에서 애플리케이션 보안 그룹을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2fd-110">Example 2: Retrieve application security groups in a resource group.</span></span>
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

<span data-ttu-id="ea2fd-111">위의 명령은 리소스 그룹 MyResourceGroup에 속하는 모든 애플리케이션 보안 그룹을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2fd-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="ea2fd-112">예제 3: 특정 애플리케이션 보안 그룹을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2fd-112">Example 3: Retrieve a specific application security group.</span></span>
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

<span data-ttu-id="ea2fd-113">위의 명령은 리소스 그룹 MyResourceGroup 아래에 있는 MyApplicationSecurityGroup 애플리케이션 보안 그룹을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2fd-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="ea2fd-114">예제 4: 필터링을 사용하여 애플리케이션 보안 그룹을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2fd-114">Example 4: Retrieve application security groups using filtering.</span></span>
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

<span data-ttu-id="ea2fd-115">위의 명령은 "MyApplicationSecurityGroup"으로 시작하는 모든 애플리케이션 보안 그룹을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2fd-115">The command above returns all application security groups that start with "MyApplicationSecurityGroup".</span></span>

## <span data-ttu-id="ea2fd-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea2fd-116">PARAMETERS</span></span>

### <span data-ttu-id="ea2fd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea2fd-117">-DefaultProfile</span></span>
<span data-ttu-id="ea2fd-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ea2fd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea2fd-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ea2fd-119">-Name</span></span>
<span data-ttu-id="ea2fd-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea2fd-120">The resource name.</span></span>

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

### <span data-ttu-id="ea2fd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea2fd-121">-ResourceGroupName</span></span>
<span data-ttu-id="ea2fd-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea2fd-122">The resource group name.</span></span>

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

### <span data-ttu-id="ea2fd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea2fd-123">CommonParameters</span></span>
<span data-ttu-id="ea2fd-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2fd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea2fd-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ea2fd-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea2fd-126">입력</span><span class="sxs-lookup"><span data-stu-id="ea2fd-126">INPUTS</span></span>

### <span data-ttu-id="ea2fd-127">System.String</span><span class="sxs-lookup"><span data-stu-id="ea2fd-127">System.String</span></span>

## <span data-ttu-id="ea2fd-128">출력</span><span class="sxs-lookup"><span data-stu-id="ea2fd-128">OUTPUTS</span></span>

### <span data-ttu-id="ea2fd-129">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ea2fd-129">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="ea2fd-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ea2fd-130">NOTES</span></span>

## <span data-ttu-id="ea2fd-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea2fd-131">RELATED LINKS</span></span>

[<span data-ttu-id="ea2fd-132">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ea2fd-132">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="ea2fd-133">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ea2fd-133">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="ea2fd-134">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ea2fd-134">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="ea2fd-135">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ea2fd-135">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)
