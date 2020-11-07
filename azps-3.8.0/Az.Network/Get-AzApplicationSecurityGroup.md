---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
ms.openlocfilehash: aa03f7d410d704e8e5b9ea4b974e3050a3304342
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877678"
---
# <span data-ttu-id="a442d-101">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a442d-101">Get-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="a442d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a442d-102">SYNOPSIS</span></span>
<span data-ttu-id="a442d-103">응용 프로그램 보안 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a442d-103">Gets an application security group.</span></span>

## <span data-ttu-id="a442d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a442d-104">SYNTAX</span></span>

```
Get-AzApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a442d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a442d-105">DESCRIPTION</span></span>
<span data-ttu-id="a442d-106">**Get-AzApplicationSecurityGroup** cmdlet은 응용 프로그램 보안 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a442d-106">The **Get-AzApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="a442d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a442d-107">EXAMPLES</span></span>

### <span data-ttu-id="a442d-108">예제 1: 모든 응용 프로그램 보안 그룹을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="a442d-108">Example 1: Retrieve all application security groups.</span></span>
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

<span data-ttu-id="a442d-109">위의 명령은 구독에 있는 모든 응용 프로그램 보안 그룹을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a442d-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="a442d-110">예제 2: 리소스 그룹의 응용 프로그램 보안 그룹을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="a442d-110">Example 2: Retrieve application security groups in a resource group.</span></span>
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

<span data-ttu-id="a442d-111">위의 명령은 리소스 그룹 MyResourceGroup에 속하는 모든 응용 프로그램 보안 그룹을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a442d-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="a442d-112">예제 3: 특정 응용 프로그램 보안 그룹 검색</span><span class="sxs-lookup"><span data-stu-id="a442d-112">Example 3: Retrieve a specific application security group.</span></span>
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

<span data-ttu-id="a442d-113">위의 명령은 리소스 그룹 MyApplicationSecurityGroup 아래에 있는 응용 프로그램 보안 그룹</span><span class="sxs-lookup"><span data-stu-id="a442d-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="a442d-114">예제 4: 필터링을 사용 하 여 응용 프로그램 보안 그룹 검색</span><span class="sxs-lookup"><span data-stu-id="a442d-114">Example 4: Retrieve application security groups using filtering.</span></span>
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

<span data-ttu-id="a442d-115">위의 명령은 "MyApplicationSecurityGroup"으로 시작 하는 모든 응용 프로그램 보안 그룹을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a442d-115">The command above returns all application security groups that start with "MyApplicationSecurityGroup".</span></span>

## <span data-ttu-id="a442d-116">변수</span><span class="sxs-lookup"><span data-stu-id="a442d-116">PARAMETERS</span></span>

### <span data-ttu-id="a442d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a442d-117">-DefaultProfile</span></span>
<span data-ttu-id="a442d-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a442d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a442d-119">-이름</span><span class="sxs-lookup"><span data-stu-id="a442d-119">-Name</span></span>
<span data-ttu-id="a442d-120">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a442d-120">The resource name.</span></span>

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

### <span data-ttu-id="a442d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a442d-121">-ResourceGroupName</span></span>
<span data-ttu-id="a442d-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a442d-122">The resource group name.</span></span>

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

### <span data-ttu-id="a442d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a442d-123">CommonParameters</span></span>
<span data-ttu-id="a442d-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a442d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a442d-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a442d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a442d-126">입력</span><span class="sxs-lookup"><span data-stu-id="a442d-126">INPUTS</span></span>

### <span data-ttu-id="a442d-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a442d-127">System.String</span></span>

## <span data-ttu-id="a442d-128">출력</span><span class="sxs-lookup"><span data-stu-id="a442d-128">OUTPUTS</span></span>

### <span data-ttu-id="a442d-129">Microsoft. \* PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a442d-129">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="a442d-130">상속자</span><span class="sxs-lookup"><span data-stu-id="a442d-130">NOTES</span></span>

## <span data-ttu-id="a442d-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a442d-131">RELATED LINKS</span></span>

[<span data-ttu-id="a442d-132">새로운 AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a442d-132">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="a442d-133">제거-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a442d-133">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="a442d-134">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a442d-134">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="a442d-135">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a442d-135">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)
