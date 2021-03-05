---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHost.md
ms.openlocfilehash: d1790f3525e63890d164db1a62903026be4f483a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991531"
---
# <span data-ttu-id="837e9-101">Get-AzHost</span><span class="sxs-lookup"><span data-stu-id="837e9-101">Get-AzHost</span></span>

## <span data-ttu-id="837e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="837e9-102">SYNOPSIS</span></span>
<span data-ttu-id="837e9-103">호스트를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="837e9-103">Get or list hosts.</span></span>

## <span data-ttu-id="837e9-104">구문</span><span class="sxs-lookup"><span data-stu-id="837e9-104">SYNTAX</span></span>

### <span data-ttu-id="837e9-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="837e9-105">DefaultParameter (Default)</span></span>
```
Get-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [[-Name] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="837e9-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="837e9-106">ResourceIdParameter</span></span>
```
Get-AzHost [-ResourceId] <String> [-InstanceView] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="837e9-107">설명</span><span class="sxs-lookup"><span data-stu-id="837e9-107">DESCRIPTION</span></span>
<span data-ttu-id="837e9-108">이 cmdlet은 호스트 그룹에 호스트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="837e9-108">This cmdlet will get a host in a host group.</span></span>
<span data-ttu-id="837e9-109">이 cmdlet에는 호스트 이름이 지정되지 않은 경우 호스트 그룹의 모든 호스트도 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="837e9-109">This cmdlet also lists all hosts in a host group if a host name is not given.</span></span>

## <span data-ttu-id="837e9-110">예제</span><span class="sxs-lookup"><span data-stu-id="837e9-110">EXAMPLES</span></span>

### <span data-ttu-id="837e9-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="837e9-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName

ResourceGroupName    : myrg01
PlatformFaultDomain  : 1
AutoReplaceOnFailure : True
HostId               : 00000000-0000-0000-0000-000000000000
VirtualMachines[0]   : 
  Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/virtualMachines/myvm01
VirtualMachines[1]   : 
  Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/virtualMachines/myvm02
ProvisioningTime     : 7/27/2019 3:22:59 AM
ProvisioningState    : Succeeded
Sku                  : 
  Name               : ESv3-Type1
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                 : myhost01
Location             : eastus
Tags                 : {"key1":"val2"}
```

<span data-ttu-id="837e9-112">이 명령은 호스트를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="837e9-112">This command returns a host.</span></span>

### <span data-ttu-id="837e9-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="837e9-113">Example 2</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName -InstanceView

ResourceGroupName      : myrg01
PlatformFaultDomain    : 0
AutoReplaceOnFailure   : True
HostId                 : 00000000-0000-0000-0000-000000000000
ProvisioningTime       : 8/19/2019 9:13:19 PM
ProvisioningState      : Succeeded
InstanceView           : 
  AssetId              : 00000000-0000-0000-0000-000000000000
  AvailableCapacity    : 
    AllocatableVMs[0]  : 
      VmSize           : Standard_E2s_v3
      Count            : 28
    AllocatableVMs[1]  : 
      VmSize           : Standard_E4-2s_v3
      Count            : 14
    AllocatableVMs[2]  : 
      VmSize           : Standard_E4s_v3
      Count            : 14
  Statuses[0]          : 
    Code               : ProvisioningState/succeeded
    Level              : Info
    DisplayStatus      : Provisioning succeeded
    Time               : 8/19/2019 9:13:19 PM
  Statuses[1]          : 
    Code               : HealthState/available
    Level              : Info
    DisplayStatus      : Host available
Sku                    : 
  Name                 : ESv3-Type1
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                   : crptestps2264host
Location               : eastus
Tags                   : {"key1":"val2"}
```

<span data-ttu-id="837e9-114">이 명령은 호스트의 인스턴스 보기를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="837e9-114">This command returns the instance view of a host.</span></span>

### <span data-ttu-id="837e9-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="837e9-115">Example 3</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName

ResourceGroupName       Name Location           Tags        Sku FD
-----------------       ---- --------           ----        --- --
myrg01              myhost01   eastus {[key1, val2]} ESv3-Type1  0
myrg01              myhost02   eastus {[key1, val2]} ESv3-Type1  1
```

<span data-ttu-id="837e9-116">이 명령은 주어진 호스트 그룹의 모든 호스트를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="837e9-116">This command returns all hosts in the given host group.</span></span>

## <span data-ttu-id="837e9-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="837e9-117">PARAMETERS</span></span>

### <span data-ttu-id="837e9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="837e9-118">-DefaultProfile</span></span>
<span data-ttu-id="837e9-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="837e9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="837e9-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="837e9-120">-HostGroupName</span></span>
<span data-ttu-id="837e9-121">호스트 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="837e9-121">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="837e9-122">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="837e9-122">-InstanceView</span></span>
<span data-ttu-id="837e9-123">이 cmdlet은 호스트의 인스턴스 보기만 을 를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="837e9-123">Indicates that this cmdlet gets only the instance view of the host.</span></span>

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

### <span data-ttu-id="837e9-124">-Name</span><span class="sxs-lookup"><span data-stu-id="837e9-124">-Name</span></span>
<span data-ttu-id="837e9-125">호스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="837e9-125">The name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="837e9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="837e9-126">-ResourceGroupName</span></span>
<span data-ttu-id="837e9-127">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="837e9-127">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="837e9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="837e9-128">-ResourceId</span></span>
<span data-ttu-id="837e9-129">리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="837e9-129">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="837e9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="837e9-130">CommonParameters</span></span>
<span data-ttu-id="837e9-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="837e9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="837e9-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="837e9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="837e9-133">입력</span><span class="sxs-lookup"><span data-stu-id="837e9-133">INPUTS</span></span>

### <span data-ttu-id="837e9-134">System.String</span><span class="sxs-lookup"><span data-stu-id="837e9-134">System.String</span></span>

## <span data-ttu-id="837e9-135">출력</span><span class="sxs-lookup"><span data-stu-id="837e9-135">OUTPUTS</span></span>

### <span data-ttu-id="837e9-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span><span class="sxs-lookup"><span data-stu-id="837e9-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="837e9-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="837e9-137">NOTES</span></span>

## <span data-ttu-id="837e9-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="837e9-138">RELATED LINKS</span></span>
