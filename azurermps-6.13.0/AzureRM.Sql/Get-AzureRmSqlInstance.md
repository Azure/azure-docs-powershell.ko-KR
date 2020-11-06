---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstance.md
ms.openlocfilehash: 72e3b740a84a46da094208b941e8b68173133e46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531920"
---
# <span data-ttu-id="a01e6-101">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a01e6-101">Get-AzureRmSqlInstance</span></span>

## <span data-ttu-id="a01e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a01e6-102">SYNOPSIS</span></span>
<span data-ttu-id="a01e6-103">Azure SQL 관리 데이터베이스 인스턴스에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a01e6-103">Returns information about Azure SQL Managed Database Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a01e6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a01e6-104">SYNTAX</span></span>

### <span data-ttu-id="a01e6-105">GetInstanceByResourceGroup (기본값)</span><span class="sxs-lookup"><span data-stu-id="a01e6-105">GetInstanceByResourceGroup (Default)</span></span>
```
Get-AzureRmSqlInstance [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a01e6-106">GetInstanceByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a01e6-106">GetInstanceByNameAndResourceGroup</span></span>
```
Get-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a01e6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a01e6-107">DESCRIPTION</span></span>
<span data-ttu-id="a01e6-108">**Get-AzureRmSqlInstance** cmdlet은 하나 이상의 Azure SQL 관리 인스턴스에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a01e6-108">The **Get-AzureRmSqlInstance** cmdlet returns information about one or more Azure SQL Managed Instances.</span></span>
<span data-ttu-id="a01e6-109">해당 인스턴스에 대 한 정보만 보려면 인스턴스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a01e6-109">Specify the name of a instance to see information for only that instance.</span></span>

## <span data-ttu-id="a01e6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a01e6-110">EXAMPLES</span></span>

### <span data-ttu-id="a01e6-111">예제 1: 리소스 그룹에 할당 된 모든 인스턴스 가져오기</span><span class="sxs-lookup"><span data-stu-id="a01e6-111">Example 1: Get all instances assigned to a resource group</span></span>
```
PS C:\>Get-AzureRmSqlInstance -ResourceGroupName "ResourceGroup01"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
```

<span data-ttu-id="a01e6-112">이 명령은 리소스 그룹 ResourceGroup01에 할당 된 모든 인스턴스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a01e6-112">This command gets information about all instances assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="a01e6-113">예제 2: 인스턴스에 대 한 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="a01e6-113">Example 2: Get information about an  instance</span></span>
```
PS C:\>Get-AzureRmSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
```

<span data-ttu-id="a01e6-114">이 명령은 managedInstance1 이라는 인스턴스에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a01e6-114">This command gets information about the instance named managedInstance1.</span></span>

## <span data-ttu-id="a01e6-115">변수</span><span class="sxs-lookup"><span data-stu-id="a01e6-115">PARAMETERS</span></span>

### <span data-ttu-id="a01e6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a01e6-116">-DefaultProfile</span></span>
<span data-ttu-id="a01e6-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a01e6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01e6-118">-이름</span><span class="sxs-lookup"><span data-stu-id="a01e6-118">-Name</span></span>
<span data-ttu-id="a01e6-119">SQL 인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a01e6-119">SQL instance name.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceByNameAndResourceGroup
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01e6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a01e6-120">-ResourceGroupName</span></span>
<span data-ttu-id="a01e6-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a01e6-121">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetInstanceByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a01e6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a01e6-122">CommonParameters</span></span>
<span data-ttu-id="a01e6-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a01e6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a01e6-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a01e6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a01e6-125">입력</span><span class="sxs-lookup"><span data-stu-id="a01e6-125">INPUTS</span></span>

### <span data-ttu-id="a01e6-126">않아야</span><span class="sxs-lookup"><span data-stu-id="a01e6-126">None</span></span>

## <span data-ttu-id="a01e6-127">출력</span><span class="sxs-lookup"><span data-stu-id="a01e6-127">OUTPUTS</span></span>

### <span data-ttu-id="a01e6-128">AzureSqlManagedInstanceModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="a01e6-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="a01e6-129">상속자</span><span class="sxs-lookup"><span data-stu-id="a01e6-129">NOTES</span></span>

## <span data-ttu-id="a01e6-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a01e6-130">RELATED LINKS</span></span>
