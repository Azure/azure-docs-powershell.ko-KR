---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
ms.openlocfilehash: f5e52938a6d0f618d53621a895aeb7037dc543ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698911"
---
# <span data-ttu-id="8e851-101">Get-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="8e851-101">Get-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="8e851-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e851-102">SYNOPSIS</span></span>
<span data-ttu-id="8e851-103">Azure SQL 가상 클러스터에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e851-103">Returns information about Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="8e851-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8e851-104">SYNTAX</span></span>

### <span data-ttu-id="8e851-105">GetVirtualClusterByResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="8e851-105">GetVirtualClusterByResourceGroup (Default)</span></span>
```
Get-AzSqlVirtualCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8e851-106">GetVirtualClusterByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8e851-106">GetVirtualClusterByNameAndResourceGroup</span></span>
```
Get-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e851-107">GetVirtualClusterByResourceId</span><span class="sxs-lookup"><span data-stu-id="8e851-107">GetVirtualClusterByResourceId</span></span>
```
Get-AzSqlVirtualCluster [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e851-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8e851-108">DESCRIPTION</span></span>
<span data-ttu-id="8e851-109">**AzSqlVirtualCluster** cmdlet은 하나 이상의 Azure SQL 가상 클러스터에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e851-109">The **Get-AzSqlVirtualCluster** cmdlet returns information about one or more Azure SQL Virtual Clusters.</span></span>
<span data-ttu-id="8e851-110">해당 클러스터에 대 한 정보만 보려면 가상 클러스터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e851-110">Specify the name of a virtual cluster to see information for only that cluster.</span></span>

## <span data-ttu-id="8e851-111">예제의</span><span class="sxs-lookup"><span data-stu-id="8e851-111">EXAMPLES</span></span>

### <span data-ttu-id="8e851-112">예제 1: 리소스 그룹에 할당 된 모든 가상 클러스터 가져오기</span><span class="sxs-lookup"><span data-stu-id="8e851-112">Example 1: Get all virtual clusters assigned to a resource group</span></span>
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

<span data-ttu-id="8e851-113">이 명령은 리소스 그룹 ResourceGroup01에 할당 된 모든 가상 클러스터에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8e851-113">This command gets information about all Virtual Clusters assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="8e851-114">예제 2: 특정 가상 클러스터에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="8e851-114">Example 2: Get information about specific virtual cluster</span></span>
```
PS C:\>  Get-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1
```

<span data-ttu-id="8e851-115">이 명령은 리소스 그룹 ResourceGroup01의 가상 클러스터 VirtualCluster1에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8e851-115">This command gets information about the virtual cluster VirtualCluster1 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="8e851-116">변수</span><span class="sxs-lookup"><span data-stu-id="8e851-116">PARAMETERS</span></span>

### <span data-ttu-id="8e851-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e851-117">-DefaultProfile</span></span>
<span data-ttu-id="8e851-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8e851-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e851-119">-이름</span><span class="sxs-lookup"><span data-stu-id="8e851-119">-Name</span></span>
<span data-ttu-id="8e851-120">가상 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e851-120">The name of the virtual cluster.</span></span>

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

### <span data-ttu-id="8e851-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e851-121">-ResourceGroupName</span></span>
<span data-ttu-id="8e851-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e851-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="8e851-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e851-123">-ResourceId</span></span>
<span data-ttu-id="8e851-124">가져올 인스턴스 개체의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="8e851-124">The resource id of instance object to get</span></span>

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

### <span data-ttu-id="8e851-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e851-125">CommonParameters</span></span>
<span data-ttu-id="8e851-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e851-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e851-127">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8e851-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e851-128">입력</span><span class="sxs-lookup"><span data-stu-id="8e851-128">INPUTS</span></span>

### <span data-ttu-id="8e851-129">않아야</span><span class="sxs-lookup"><span data-stu-id="8e851-129">None</span></span>

## <span data-ttu-id="8e851-130">출력</span><span class="sxs-lookup"><span data-stu-id="8e851-130">OUTPUTS</span></span>

### <span data-ttu-id="8e851-131">AzureSqlVirtualClusterModel/. m a m.</span><span class="sxs-lookup"><span data-stu-id="8e851-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="8e851-132">상속자</span><span class="sxs-lookup"><span data-stu-id="8e851-132">NOTES</span></span>

## <span data-ttu-id="8e851-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e851-133">RELATED LINKS</span></span>
