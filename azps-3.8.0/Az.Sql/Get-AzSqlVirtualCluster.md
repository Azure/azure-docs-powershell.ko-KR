---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
ms.openlocfilehash: bd12fd2067c931f05266ed1ed24fb5666ead59a9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034218"
---
# <span data-ttu-id="377e0-101">Get-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="377e0-101">Get-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="377e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="377e0-102">SYNOPSIS</span></span>
<span data-ttu-id="377e0-103">Azure SQL 가상 클러스터에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="377e0-103">Returns information about Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="377e0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="377e0-104">SYNTAX</span></span>

### <span data-ttu-id="377e0-105">GetVirtualClusterByResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="377e0-105">GetVirtualClusterByResourceGroup (Default)</span></span>
```
Get-AzSqlVirtualCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="377e0-106">GetVirtualClusterByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="377e0-106">GetVirtualClusterByNameAndResourceGroup</span></span>
```
Get-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="377e0-107">GetVirtualClusterByResourceId</span><span class="sxs-lookup"><span data-stu-id="377e0-107">GetVirtualClusterByResourceId</span></span>
```
Get-AzSqlVirtualCluster [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="377e0-108">설명은</span><span class="sxs-lookup"><span data-stu-id="377e0-108">DESCRIPTION</span></span>
<span data-ttu-id="377e0-109">**AzSqlVirtualCluster** cmdlet은 하나 이상의 Azure SQL 가상 클러스터에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="377e0-109">The **Get-AzSqlVirtualCluster** cmdlet returns information about one or more Azure SQL Virtual Clusters.</span></span>
<span data-ttu-id="377e0-110">해당 클러스터에 대 한 정보만 보려면 가상 클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="377e0-110">Specify the name of a virtual cluster to see information for only that cluster.</span></span>

## <span data-ttu-id="377e0-111">예제의</span><span class="sxs-lookup"><span data-stu-id="377e0-111">EXAMPLES</span></span>

### <span data-ttu-id="377e0-112">예제 1: 리소스 그룹에 할당 된 모든 가상 클러스터 가져오기</span><span class="sxs-lookup"><span data-stu-id="377e0-112">Example 1: Get all virtual clusters assigned to a resource group</span></span>
```powershell
PS C:> Get-AzSqlVirtualCluster -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1

Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster2
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster2
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name2

Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster3
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster3
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name3
```

<span data-ttu-id="377e0-113">이 명령은 리소스 그룹 ResourceGroup01에 할당 된 모든 가상 클러스터에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="377e0-113">This command gets information about all Virtual Clusters assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="377e0-114">예제 2: 특정 가상 클러스터에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="377e0-114">Example 2: Get information about specific virtual cluster</span></span>
```
PS C:\>  Get-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1
```

<span data-ttu-id="377e0-115">이 명령은 리소스 그룹 ResourceGroup01의 가상 클러스터 VirtualCluster1에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="377e0-115">This command gets information about the virtual cluster VirtualCluster1 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="377e0-116">변수</span><span class="sxs-lookup"><span data-stu-id="377e0-116">PARAMETERS</span></span>

### <span data-ttu-id="377e0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="377e0-117">-DefaultProfile</span></span>
<span data-ttu-id="377e0-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="377e0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="377e0-119">-이름</span><span class="sxs-lookup"><span data-stu-id="377e0-119">-Name</span></span>
<span data-ttu-id="377e0-120">가상 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="377e0-120">The name of the virtual cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByNameAndResourceGroup
Aliases: VirtualClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="377e0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="377e0-121">-ResourceGroupName</span></span>
<span data-ttu-id="377e0-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="377e0-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="377e0-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="377e0-123">-ResourceId</span></span>
<span data-ttu-id="377e0-124">가져올 인스턴스 개체의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="377e0-124">The resource id of instance object to get</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="377e0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="377e0-125">CommonParameters</span></span>
<span data-ttu-id="377e0-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="377e0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="377e0-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="377e0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="377e0-128">입력</span><span class="sxs-lookup"><span data-stu-id="377e0-128">INPUTS</span></span>

### <span data-ttu-id="377e0-129">않아야</span><span class="sxs-lookup"><span data-stu-id="377e0-129">None</span></span>

## <span data-ttu-id="377e0-130">출력</span><span class="sxs-lookup"><span data-stu-id="377e0-130">OUTPUTS</span></span>

### <span data-ttu-id="377e0-131">AzureSqlVirtualClusterModel/. m a m.</span><span class="sxs-lookup"><span data-stu-id="377e0-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="377e0-132">상속자</span><span class="sxs-lookup"><span data-stu-id="377e0-132">NOTES</span></span>

## <span data-ttu-id="377e0-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="377e0-133">RELATED LINKS</span></span>