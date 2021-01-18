---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskAccess.md
ms.openlocfilehash: 69f83b7c98850ba74476e6d81803e748f48bea6a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496100"
---
# <span data-ttu-id="99cff-101">Get-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="99cff-101">Get-AzDiskAccess</span></span>

## <span data-ttu-id="99cff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99cff-102">SYNOPSIS</span></span>
<span data-ttu-id="99cff-103">디스크 액세스의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="99cff-103">Gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="99cff-104">구문</span><span class="sxs-lookup"><span data-stu-id="99cff-104">SYNTAX</span></span>

### <span data-ttu-id="99cff-105">DefaultParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="99cff-105">DefaultParameterSet (Default)</span></span>
```
Get-AzDiskAccess [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="99cff-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="99cff-106">ResourceIDParameterSet</span></span>
```
Get-AzDiskAccess [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99cff-107">설명</span><span class="sxs-lookup"><span data-stu-id="99cff-107">DESCRIPTION</span></span>
<span data-ttu-id="99cff-108">**Get-AzDiskAccess** cmdlet은 디스크 액세스의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="99cff-108">The **Get-AzDiskAccess** cmdlet gets the properties of Disk Accesses</span></span>

## <span data-ttu-id="99cff-109">예제</span><span class="sxs-lookup"><span data-stu-id="99cff-109">EXAMPLES</span></span>

### <span data-ttu-id="99cff-110">예제 1: 기본 매개 변수 집합 사용</span><span class="sxs-lookup"><span data-stu-id="99cff-110">Example 1: Using Default Parameter Set</span></span> 
```
PS C:\> Get-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -Name 'DiskAccess01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="99cff-111">이 명령은 리소스 그룹 'ResourceGroup01'에서 'DiskAccess01'이라는 디스크 액세스 리소스의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="99cff-111">This command gets the properties of a Disk Access resource named 'DiskAccess01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="99cff-112">예제 2: Get-AzDiskAccess 그룹으로 관리</span><span class="sxs-lookup"><span data-stu-id="99cff-112">Example 2: Get-AzDiskAccess by Resource Group</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceGroupName 'ResourceGroup01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess02
Name                       : DiskAccess02
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="99cff-113">이 명령은 리소스 그룹 'ResourceGroup01'에서 모든 디스크 액세스의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="99cff-113">This command gets the properties of all disk accesses in the resource group 'ResourceGroup01'.</span></span>


### <span data-ttu-id="99cff-114">예제 3: 모든 디스크 액세스하기</span><span class="sxs-lookup"><span data-stu-id="99cff-114">Example 3: Getting all Disk Access</span></span>
```
PS C:\> Get-AzDiskAccess

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup21/providers/Microsoft.Compute/diskAccesses/DiskAccess02
Name                       : DiskAccess02
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup08/providers/Microsoft.Compute/diskAccesses/DiskAccess03
Name                       : DiskAccess03
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="99cff-115">이 명령은 구독에 속한 모든 디스크 액세스의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="99cff-115">This command gets the properties of all disk accesses under the subscription.</span></span>

### <span data-ttu-id="99cff-116">예제 4: 와일드카드 문자를 사용하여 모든 디스크 액세스 액세스</span><span class="sxs-lookup"><span data-stu-id="99cff-116">Example 4: Get all Disk Access using Wildcard Character</span></span>
```
PS C:\> Get-AzDiskAccess -Name DiskAccessMicrosoft*

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccessMicrosoftAzure
Name                       : DiskAccessMicrosoftAzure
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:05:19 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccessMicrosoftTeams
Name                       : DiskAccessMicrosoftTeams
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="99cff-117">이 명령은 'DiskAccessMicrosoft'로 시작하는 구독 이름 아래에 있는 모든 디스크 액세스의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="99cff-117">This command gets the properties of all disk accesses under the subscription name starting with 'DiskAccessMicrosoft'.</span></span>

### <span data-ttu-id="99cff-118">예제 5: ResourceId를 사용하여 디스크 액세스 권한을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="99cff-118">Example 5: Get Disk Access using ResourceId.</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceId '/subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01'

PrivateEndpointConnections : {}
ProvisioningState          : Succeeded
TimeCreated                : 8/13/2020 7:02:50 PM
Location                   : northcentralus
Id                         : /subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/diskAccesses/DiskAccess01
Name                       : DiskAccess01
Type                       : Microsoft.Compute/diskAccesses
Tags                       : {}
```

<span data-ttu-id="99cff-119">이 명령은 주어진 ResourceId를 사용하여 디스크 액세스의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="99cff-119">This command gets the properties of a Disk Access with the given ResourceId.</span></span>


## <span data-ttu-id="99cff-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99cff-120">PARAMETERS</span></span>

### <span data-ttu-id="99cff-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99cff-121">-DefaultProfile</span></span>
<span data-ttu-id="99cff-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="99cff-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99cff-123">-Name</span><span class="sxs-lookup"><span data-stu-id="99cff-123">-Name</span></span>
<span data-ttu-id="99cff-124">디스크 액세스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99cff-124">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: diskAccessName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="99cff-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99cff-125">-ResourceGroupName</span></span>
<span data-ttu-id="99cff-126">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99cff-126">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="99cff-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99cff-127">-ResourceId</span></span>
<span data-ttu-id="99cff-128">디스크 액세스에 대한 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="99cff-128">Resource ID for your disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99cff-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99cff-129">CommonParameters</span></span>
<span data-ttu-id="99cff-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="99cff-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99cff-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="99cff-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99cff-132">입력</span><span class="sxs-lookup"><span data-stu-id="99cff-132">INPUTS</span></span>

### <span data-ttu-id="99cff-133">System.String</span><span class="sxs-lookup"><span data-stu-id="99cff-133">System.String</span></span>

## <span data-ttu-id="99cff-134">출력</span><span class="sxs-lookup"><span data-stu-id="99cff-134">OUTPUTS</span></span>

### <span data-ttu-id="99cff-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="99cff-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="99cff-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="99cff-136">NOTES</span></span>

## <span data-ttu-id="99cff-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99cff-137">RELATED LINKS</span></span>
