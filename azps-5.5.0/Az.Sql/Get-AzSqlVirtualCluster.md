---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
ms.openlocfilehash: bd12fd2067c931f05266ed1ed24fb5666ead59a9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178428"
---
# <span data-ttu-id="b7ab5-101">Get-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="b7ab5-101">Get-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="b7ab5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7ab5-102">SYNOPSIS</span></span>
<span data-ttu-id="b7ab5-103">Azure SQL Virtual Cluster에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b7ab5-103">Returns information about Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="b7ab5-104">구문</span><span class="sxs-lookup"><span data-stu-id="b7ab5-104">SYNTAX</span></span>

### <span data-ttu-id="b7ab5-105">GetVirtualClusterByResourceGroup(기본값)</span><span class="sxs-lookup"><span data-stu-id="b7ab5-105">GetVirtualClusterByResourceGroup (Default)</span></span>
```
Get-AzSqlVirtualCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b7ab5-106">GetVirtualClusterByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b7ab5-106">GetVirtualClusterByNameAndResourceGroup</span></span>
```
Get-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7ab5-107">GetVirtualClusterByResourceId</span><span class="sxs-lookup"><span data-stu-id="b7ab5-107">GetVirtualClusterByResourceId</span></span>
```
Get-AzSqlVirtualCluster [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7ab5-108">설명</span><span class="sxs-lookup"><span data-stu-id="b7ab5-108">DESCRIPTION</span></span>
<span data-ttu-id="b7ab5-109">**Get-AzSqlVirtualCluster** cmdlet은 가상 클러스터에서 하나 이상의 Azure SQL 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b7ab5-109">The **Get-AzSqlVirtualCluster** cmdlet returns information about one or more Azure SQL Virtual Clusters.</span></span>
<span data-ttu-id="b7ab5-110">해당 클러스터에 대한 정보만 표시하기 위해 가상 클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b7ab5-110">Specify the name of a virtual cluster to see information for only that cluster.</span></span>

## <span data-ttu-id="b7ab5-111">예제</span><span class="sxs-lookup"><span data-stu-id="b7ab5-111">EXAMPLES</span></span>

### <span data-ttu-id="b7ab5-112">예제 1: 리소스 그룹에 할당된 모든 가상 클러스터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b7ab5-112">Example 1: Get all virtual clusters assigned to a resource group</span></span>
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

<span data-ttu-id="b7ab5-113">이 명령은 리소스 그룹 ResourceGroup01에 할당된 모든 가상 클러스터에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b7ab5-113">This command gets information about all Virtual Clusters assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="b7ab5-114">예제 2: 특정 가상 클러스터에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="b7ab5-114">Example 2: Get information about specific virtual cluster</span></span>
```
PS C:\>  Get-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1
```

<span data-ttu-id="b7ab5-115">이 명령은 리소스 그룹 ResourceGroup01의 가상 클러스터 VirtualCluster1에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b7ab5-115">This command gets information about the virtual cluster VirtualCluster1 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="b7ab5-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7ab5-116">PARAMETERS</span></span>

### <span data-ttu-id="b7ab5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7ab5-117">-DefaultProfile</span></span>
<span data-ttu-id="b7ab5-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b7ab5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7ab5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b7ab5-119">-Name</span></span>
<span data-ttu-id="b7ab5-120">가상 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7ab5-120">The name of the virtual cluster.</span></span>

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

### <span data-ttu-id="b7ab5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7ab5-121">-ResourceGroupName</span></span>
<span data-ttu-id="b7ab5-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7ab5-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="b7ab5-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7ab5-123">-ResourceId</span></span>
<span data-ttu-id="b7ab5-124">얻을 인스턴스 개체의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="b7ab5-124">The resource id of instance object to get</span></span>

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

### <span data-ttu-id="b7ab5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7ab5-125">CommonParameters</span></span>
<span data-ttu-id="b7ab5-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b7ab5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7ab5-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b7ab5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7ab5-128">입력</span><span class="sxs-lookup"><span data-stu-id="b7ab5-128">INPUTS</span></span>

### <span data-ttu-id="b7ab5-129">없음</span><span class="sxs-lookup"><span data-stu-id="b7ab5-129">None</span></span>

## <span data-ttu-id="b7ab5-130">출력</span><span class="sxs-lookup"><span data-stu-id="b7ab5-130">OUTPUTS</span></span>

### <span data-ttu-id="b7ab5-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="b7ab5-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="b7ab5-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b7ab5-132">NOTES</span></span>

## <span data-ttu-id="b7ab5-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7ab5-133">RELATED LINKS</span></span>
