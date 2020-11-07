---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePool.md
ms.openlocfilehash: 8d2d1333a10290c3a321b22cf33b527738d7ecb1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873650"
---
# <span data-ttu-id="070bb-101">Get-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="070bb-101">Get-AzSqlInstancePool</span></span>

## <span data-ttu-id="070bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="070bb-102">SYNOPSIS</span></span>
<span data-ttu-id="070bb-103">Azure SQL 인스턴스 풀에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="070bb-103">Returns information about the Azure SQL Instance pool.</span></span>

## <span data-ttu-id="070bb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="070bb-104">SYNTAX</span></span>

### <span data-ttu-id="070bb-105">ListBySubOrResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="070bb-105">ListBySubOrResourceGroupParameterSet (Default)</span></span>
```
Get-AzSqlInstancePool [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="070bb-106">ListByInstancePoolDefaultsParameterSet</span><span class="sxs-lookup"><span data-stu-id="070bb-106">ListByInstancePoolDefaultsParameterSet</span></span>
```
Get-AzSqlInstancePool -ResourceGroupName <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="070bb-107">GetInstancePoolByInstancePoolResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="070bb-107">GetInstancePoolByInstancePoolResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="070bb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="070bb-108">DESCRIPTION</span></span>
<span data-ttu-id="070bb-109">**AzSqlInstancePool** cmdlet은 하나 이상의 Azure SQL 인스턴스 풀에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="070bb-109">The **Get-AzSqlInstancePool** cmdlet returns information about one or more Azure SQL Instance pool.</span></span>
<span data-ttu-id="070bb-110">해당 인스턴스 풀에 대 한 정보만 표시 하도록 인스턴스 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="070bb-110">Specify the name of an instance pool to see information for only that instance pool.</span></span>

## <span data-ttu-id="070bb-111">예제의</span><span class="sxs-lookup"><span data-stu-id="070bb-111">EXAMPLES</span></span>

### <span data-ttu-id="070bb-112">예제 1: 고객 구독에서 모든 인스턴스 풀 가져오기</span><span class="sxs-lookup"><span data-stu-id="070bb-112">Example 1: Get all instance pools across a customer subscription</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded

ResourceGroupName : resourcegroup02
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup02/providers/Microsoft.Sql/instancePools/ps-instancepool-1
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup02/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="070bb-113">이 명령은 고객 구독 내의 모든 인스턴스 풀에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="070bb-113">This command gets information about all instance pools within the customer subscription.</span></span>

### <span data-ttu-id="070bb-114">예제 2: 리소스 그룹 전체의 모든 인스턴스 풀 가져오기</span><span class="sxs-lookup"><span data-stu-id="070bb-114">Example 2: Get all instance pools across a resource group</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroupName resourcegroup01
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="070bb-115">이 명령은 리소스 그룹 resourcegroup01 내의 모든 인스턴스 풀에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="070bb-115">This command gets information about all instance pools within the resource group resourcegroup01.</span></span>

### <span data-ttu-id="070bb-116">예제 3: 인스턴스 풀에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="070bb-116">Example 3: Get information about an instance pool</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="070bb-117">이 명령은 인스턴스 풀 instancePool0에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="070bb-117">This command gets information about the instance pool instancePool0.</span></span>

### <span data-ttu-id="070bb-118">예제 4: 인스턴스 풀 리소스 id를 사용 하 여 인스턴스 풀에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="070bb-118">Example 4: Get information about an instance pool using instance pool resource id</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="070bb-119">이 명령은 해당 리소스 식별자를 사용 하 여 인스턴스 풀에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="070bb-119">This command gets information about the instance pool with its resource identifier.</span></span>

## <span data-ttu-id="070bb-120">변수</span><span class="sxs-lookup"><span data-stu-id="070bb-120">PARAMETERS</span></span>

### <span data-ttu-id="070bb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="070bb-121">-DefaultProfile</span></span>
<span data-ttu-id="070bb-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="070bb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="070bb-123">-이름</span><span class="sxs-lookup"><span data-stu-id="070bb-123">-Name</span></span>
<span data-ttu-id="070bb-124">인스턴스 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="070bb-124">The instance pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolDefaultsParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070bb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="070bb-125">-ResourceGroupName</span></span>
<span data-ttu-id="070bb-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="070bb-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListBySubOrResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolDefaultsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="070bb-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="070bb-127">-ResourceId</span></span>
<span data-ttu-id="070bb-128">인스턴스 풀 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="070bb-128">The instance pool resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstancePoolByInstancePoolResourceIdentifierParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="070bb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="070bb-129">CommonParameters</span></span>
<span data-ttu-id="070bb-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="070bb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="070bb-131">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="070bb-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="070bb-132">입력</span><span class="sxs-lookup"><span data-stu-id="070bb-132">INPUTS</span></span>

### <span data-ttu-id="070bb-133">않아야</span><span class="sxs-lookup"><span data-stu-id="070bb-133">None</span></span>

## <span data-ttu-id="070bb-134">출력</span><span class="sxs-lookup"><span data-stu-id="070bb-134">OUTPUTS</span></span>

### <span data-ttu-id="070bb-135">Microsoft.Azure.Commands.Sql.Instance_Pools AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="070bb-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

## <span data-ttu-id="070bb-136">상속자</span><span class="sxs-lookup"><span data-stu-id="070bb-136">NOTES</span></span>

## <span data-ttu-id="070bb-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="070bb-137">RELATED LINKS</span></span>
