---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
ms.openlocfilehash: 624ca943d9adf7df105fae18a0a4a8ccad2b9b9a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984059"
---
# <span data-ttu-id="71567-101">Get-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="71567-101">Get-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="71567-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71567-102">SYNOPSIS</span></span>
<span data-ttu-id="71567-103">Azure 가상 클러스터에 대한 SQL 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="71567-103">Returns information about Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="71567-104">구문</span><span class="sxs-lookup"><span data-stu-id="71567-104">SYNTAX</span></span>

### <span data-ttu-id="71567-105">GetVirtualClusterByResourceGroup(기본값)</span><span class="sxs-lookup"><span data-stu-id="71567-105">GetVirtualClusterByResourceGroup (Default)</span></span>
```
Get-AzSqlVirtualCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="71567-106">GetVirtualClusterByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="71567-106">GetVirtualClusterByNameAndResourceGroup</span></span>
```
Get-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71567-107">GetVirtualClusterByResourceId</span><span class="sxs-lookup"><span data-stu-id="71567-107">GetVirtualClusterByResourceId</span></span>
```
Get-AzSqlVirtualCluster [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71567-108">설명</span><span class="sxs-lookup"><span data-stu-id="71567-108">DESCRIPTION</span></span>
<span data-ttu-id="71567-109">**Get-AzSqlVirtualCluster** cmdlet은 하나 이상의 Azure 클러스터에 대한 정보를 SQL 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="71567-109">The **Get-AzSqlVirtualCluster** cmdlet returns information about one or more Azure SQL Virtual Clusters.</span></span>
<span data-ttu-id="71567-110">해당 클러스터에 대한 정보를 표시하기 위해 가상 클러스터의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71567-110">Specify the name of a virtual cluster to see information for only that cluster.</span></span>

## <span data-ttu-id="71567-111">예제</span><span class="sxs-lookup"><span data-stu-id="71567-111">EXAMPLES</span></span>

### <span data-ttu-id="71567-112">예제 1: 리소스 그룹에 할당된 모든 가상 클러스터를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="71567-112">Example 1: Get all virtual clusters assigned to a resource group</span></span>
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

<span data-ttu-id="71567-113">이 명령은 리소스 그룹 ResourceGroup01에 할당된 모든 가상 클러스터에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="71567-113">This command gets information about all Virtual Clusters assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="71567-114">예제 2: 특정 가상 클러스터에 대한 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="71567-114">Example 2: Get information about specific virtual cluster</span></span>
```
PS C:\>  Get-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1
```

<span data-ttu-id="71567-115">이 명령은 리소스 그룹 ResourceGroup01의 가상 클러스터 VirtualCluster1에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="71567-115">This command gets information about the virtual cluster VirtualCluster1 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="71567-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="71567-116">PARAMETERS</span></span>

### <span data-ttu-id="71567-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71567-117">-DefaultProfile</span></span>
<span data-ttu-id="71567-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="71567-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71567-119">-Name</span><span class="sxs-lookup"><span data-stu-id="71567-119">-Name</span></span>
<span data-ttu-id="71567-120">가상 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="71567-120">The name of the virtual cluster.</span></span>

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

### <span data-ttu-id="71567-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71567-121">-ResourceGroupName</span></span>
<span data-ttu-id="71567-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="71567-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="71567-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71567-123">-ResourceId</span></span>
<span data-ttu-id="71567-124">얻을 인스턴스 개체의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="71567-124">The resource id of instance object to get</span></span>

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

### <span data-ttu-id="71567-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71567-125">CommonParameters</span></span>
<span data-ttu-id="71567-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="71567-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71567-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71567-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71567-128">입력</span><span class="sxs-lookup"><span data-stu-id="71567-128">INPUTS</span></span>

### <span data-ttu-id="71567-129">없음</span><span class="sxs-lookup"><span data-stu-id="71567-129">None</span></span>

## <span data-ttu-id="71567-130">출력</span><span class="sxs-lookup"><span data-stu-id="71567-130">OUTPUTS</span></span>

### <span data-ttu-id="71567-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="71567-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="71567-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="71567-132">NOTES</span></span>

## <span data-ttu-id="71567-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71567-133">RELATED LINKS</span></span>
