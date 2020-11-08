---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancepoolusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePoolUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePoolUsage.md
ms.openlocfilehash: c2acc357e53a57060f7ba1ff3e19a5344ceee412
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034050"
---
# <span data-ttu-id="965d7-101">Get-AzSqlInstancePoolUsage</span><span class="sxs-lookup"><span data-stu-id="965d7-101">Get-AzSqlInstancePoolUsage</span></span>

## <span data-ttu-id="965d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="965d7-102">SYNOPSIS</span></span>
<span data-ttu-id="965d7-103">Azure SQL 인스턴스 풀의 사용에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-103">Returns information about an Azure SQL Instance pool's usage.</span></span>

## <span data-ttu-id="965d7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="965d7-104">SYNTAX</span></span>

### <span data-ttu-id="965d7-105">InstancePoolUsageDefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="965d7-105">InstancePoolUsageDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstancePoolUsage [-ResourceGroupName] <String> [-Name] <String> [-ExpandChildren]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="965d7-106">InstancePoolUsageParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="965d7-106">InstancePoolUsageParentObjectParameterSet</span></span>
```
Get-AzSqlInstancePoolUsage [-InstancePool] <AzureSqlInstancePoolModel> [-ExpandChildren]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="965d7-107">InstancePoolUsageResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="965d7-107">InstancePoolUsageResourceIdParameterSet</span></span>
```
Get-AzSqlInstancePoolUsage [-ResourceId] <String> [-ExpandChildren] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="965d7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="965d7-108">DESCRIPTION</span></span>
<span data-ttu-id="965d7-109">**AzSqlInstancePoolUsage** Cmdlet은 Azure SQL 인스턴스 풀의 사용에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-109">The **Get-AzSqlInstancePoolUsage** cmdlet returns information an Azure SQL Instance pool's usage.</span></span>

## <span data-ttu-id="965d7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="965d7-110">EXAMPLES</span></span>

### <span data-ttu-id="965d7-111">예제 1: Azure SQL 인스턴스 풀의 사용 현황을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-111">Example 1 : Gets the usage of an Azure SQL Instance pool</span></span>
```powershell
PS C:\> Get-AzSqlInstancePoolUsage -ResourceGroupName resourcegroup01 -Name instancepool0

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages
```

<span data-ttu-id="965d7-112">Azure SQL 인스턴스 풀 instancepool0에 대 한 사용을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-112">Gets the usage for the Azure SQL Instance pool instancepool0.</span></span>

### <span data-ttu-id="965d7-113">예제 2: 인스턴스 풀 개체를 사용 하 여 Azure SQL 인스턴스 풀의 사용을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-113">Example 2: Gets the usage of an Azure SQL Instance pool using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0
PS C:\> Get-AzSqlInstancePoolUsage -InstancePool $instancePool

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages
```

<span data-ttu-id="965d7-114">인스턴스 풀 개체를 사용 하 여 Azure SQL 인스턴스 풀 instancepool0에 대 한 사용을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-114">Gets the usage for the Azure SQL Instance pool instancepool0 using an instance pool object.</span></span>

### <span data-ttu-id="965d7-115">예제 3: 인스턴스 풀 리소스 id를 사용 하 여 Azure SQL 인스턴스 풀의 사용을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-115">Example 3: Gets the usage of an Azure SQL Instance pool using an instance pool resource id</span></span>
```powershell
PS C:\> Get-AzSqlInstancePoolUsage -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages
```

<span data-ttu-id="965d7-116">인스턴스 풀 리소스 식별자를 사용 하 여 Azure SQL 인스턴스 풀 instancepool0에 대 한 사용을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-116">Gets the usage for the Azure SQL Instance pool instancepool0 using an instance pool resource identifier.</span></span>

### <span data-ttu-id="965d7-117">예제 3: 풀 내의 관리 되는 인스턴스 사용에 대 한 분석 결과를 포함 하는 Azure SQL 인스턴스 풀의 사용량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-117">Example 3: Gets the usage of an Azure SQL Instance pool with a breakdown of the managed instance usages within the pool.</span></span>
```powershell
PS C:\> Get-AzSqlInstancePoolUsage -ResourceGroupName resourcegroup01 -Name instancepool0 -ExpandChildren

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/2e7fe4bd-90c7-454e-8bb6-dc44649f27b2/resourceGroups/poolsPS/providers/Microsoft.Sql/instancePools/instancepool0/managedInstances/managedinstance0/usages/vcore_utilization
CurrentValue   :
Limit          : 2
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/managedInstances/usages

Id             : /subscriptions/2e7fe4bd-90c7-454e-8bb6-dc44649f27b2/resourceGroups/poolsPS/providers/Microsoft.Sql/instancePools/instancepool0/managedInstances/managedinstance0/usages/storage_utilization
CurrentValue   :
Limit          : 32
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/managedInstances/usages

Id             : /subscriptions/2e7fe4bd-90c7-454e-8bb6-dc44649f27b2/resourceGroups/poolsPS/providers/Microsoft.Sql/instancePools/instancepool0/managedInstances/managedinstance0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/managedInstances/usages
```

<span data-ttu-id="965d7-118">Instancepool0 내에서 관리 되는 인스턴스를 사용 하는 것과 함께 Azure SQL 인스턴스 풀 instancepool0의 사용 현황을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-118">Gets the usage for the Azure SQL Instance pool instancepool0 along with the usages of the managed instances within instancepool0.</span></span>

## <span data-ttu-id="965d7-119">변수</span><span class="sxs-lookup"><span data-stu-id="965d7-119">PARAMETERS</span></span>

### <span data-ttu-id="965d7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="965d7-120">-DefaultProfile</span></span>
<span data-ttu-id="965d7-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="965d7-122">-ExpandChildren</span><span class="sxs-lookup"><span data-stu-id="965d7-122">-ExpandChildren</span></span>
<span data-ttu-id="965d7-123">이 인스턴스 풀의 사용을 자식의 사용으로 확장할지 여부를 나타내는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-123">Flag indicating whether to expand this instance pool's usage with its children's usage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="965d7-124">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="965d7-124">-InstancePool</span></span>
<span data-ttu-id="965d7-125">부모 인스턴스 풀 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-125">The parent instance pool object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: InstancePoolUsageParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="965d7-126">-이름</span><span class="sxs-lookup"><span data-stu-id="965d7-126">-Name</span></span>
<span data-ttu-id="965d7-127">관리 되는 인스턴스 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-127">The managed instance pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: InstancePoolUsageDefaultParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="965d7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="965d7-128">-ResourceGroupName</span></span>
<span data-ttu-id="965d7-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: InstancePoolUsageDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="965d7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="965d7-130">-ResourceId</span></span>
<span data-ttu-id="965d7-131">부모 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-131">The parent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: InstancePoolUsageResourceIdParameterSet
Aliases: InstancePoolResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="965d7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="965d7-132">CommonParameters</span></span>
<span data-ttu-id="965d7-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="965d7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="965d7-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="965d7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="965d7-135">입력</span><span class="sxs-lookup"><span data-stu-id="965d7-135">INPUTS</span></span>

### <span data-ttu-id="965d7-136">Microsoft.Azure.Commands.Sql.Instance_Pools AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="965d7-136">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="965d7-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="965d7-137">System.String</span></span>

## <span data-ttu-id="965d7-138">출력</span><span class="sxs-lookup"><span data-stu-id="965d7-138">OUTPUTS</span></span>

### <span data-ttu-id="965d7-139">AzureSqlUsageModel를 사용 하 여.</span><span class="sxs-lookup"><span data-stu-id="965d7-139">Microsoft.Azure.Commands.Sql.Usages.Models.AzureSqlUsageModel</span></span>

## <span data-ttu-id="965d7-140">상속자</span><span class="sxs-lookup"><span data-stu-id="965d7-140">NOTES</span></span>

## <span data-ttu-id="965d7-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="965d7-141">RELATED LINKS</span></span>
