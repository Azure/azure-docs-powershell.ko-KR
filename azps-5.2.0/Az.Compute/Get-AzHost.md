---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHost.md
ms.openlocfilehash: 692a32372718ee3100bd0ad0038d7ff89d483654
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332714"
---
# <span data-ttu-id="c31b2-101">Get-AzHost</span><span class="sxs-lookup"><span data-stu-id="c31b2-101">Get-AzHost</span></span>

## <span data-ttu-id="c31b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c31b2-102">SYNOPSIS</span></span>
<span data-ttu-id="c31b2-103">호스트를 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c31b2-103">Get or list hosts.</span></span>

## <span data-ttu-id="c31b2-104">구문</span><span class="sxs-lookup"><span data-stu-id="c31b2-104">SYNTAX</span></span>

### <span data-ttu-id="c31b2-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="c31b2-105">DefaultParameter (Default)</span></span>
```
Get-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [[-Name] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c31b2-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="c31b2-106">ResourceIdParameter</span></span>
```
Get-AzHost [-ResourceId] <String> [-InstanceView] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c31b2-107">설명</span><span class="sxs-lookup"><span data-stu-id="c31b2-107">DESCRIPTION</span></span>
<span data-ttu-id="c31b2-108">이 cmdlet은 호스트 그룹에 호스트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c31b2-108">This cmdlet will get a host in a host group.</span></span>
<span data-ttu-id="c31b2-109">또한 이 cmdlet은 호스트 이름이 지정되지 않은 경우 호스트 그룹의 모든 호스트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="c31b2-109">This cmdlet also lists all hosts in a host group if a host name is not given.</span></span>

## <span data-ttu-id="c31b2-110">예제</span><span class="sxs-lookup"><span data-stu-id="c31b2-110">EXAMPLES</span></span>

### <span data-ttu-id="c31b2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c31b2-111">Example 1</span></span>
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

<span data-ttu-id="c31b2-112">이 명령은 호스트를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c31b2-112">This command returns a host.</span></span>

### <span data-ttu-id="c31b2-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="c31b2-113">Example 2</span></span>
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

<span data-ttu-id="c31b2-114">이 명령은 호스트의 인스턴스 보기를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c31b2-114">This command returns the instance view of a host.</span></span>

### <span data-ttu-id="c31b2-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="c31b2-115">Example 3</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName

ResourceGroupName       Name Location           Tags        Sku FD
-----------------       ---- --------           ----        --- --
myrg01              myhost01   eastus {[key1, val2]} ESv3-Type1  0
myrg01              myhost02   eastus {[key1, val2]} ESv3-Type1  1
```

<span data-ttu-id="c31b2-116">이 명령은 주어진 호스트 그룹의 모든 호스트를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c31b2-116">This command returns all hosts in the given host group.</span></span>

## <span data-ttu-id="c31b2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c31b2-117">PARAMETERS</span></span>

### <span data-ttu-id="c31b2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c31b2-118">-DefaultProfile</span></span>
<span data-ttu-id="c31b2-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c31b2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c31b2-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="c31b2-120">-HostGroupName</span></span>
<span data-ttu-id="c31b2-121">호스트 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c31b2-121">The name of the host group.</span></span>

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

### <span data-ttu-id="c31b2-122">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="c31b2-122">-InstanceView</span></span>
<span data-ttu-id="c31b2-123">이 cmdlet이 호스트의 인스턴스 보기만 얻게 된다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c31b2-123">Indicates that this cmdlet gets only the instance view of the host.</span></span>

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

### <span data-ttu-id="c31b2-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c31b2-124">-Name</span></span>
<span data-ttu-id="c31b2-125">호스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c31b2-125">The name of the host.</span></span>

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

### <span data-ttu-id="c31b2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c31b2-126">-ResourceGroupName</span></span>
<span data-ttu-id="c31b2-127">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="c31b2-127">The name of the resource group</span></span>

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

### <span data-ttu-id="c31b2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c31b2-128">-ResourceId</span></span>
<span data-ttu-id="c31b2-129">리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c31b2-129">The ID of the resource.</span></span>

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

### <span data-ttu-id="c31b2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c31b2-130">CommonParameters</span></span>
<span data-ttu-id="c31b2-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c31b2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c31b2-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c31b2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c31b2-133">입력</span><span class="sxs-lookup"><span data-stu-id="c31b2-133">INPUTS</span></span>

### <span data-ttu-id="c31b2-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c31b2-134">System.String</span></span>

## <span data-ttu-id="c31b2-135">출력</span><span class="sxs-lookup"><span data-stu-id="c31b2-135">OUTPUTS</span></span>

### <span data-ttu-id="c31b2-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span><span class="sxs-lookup"><span data-stu-id="c31b2-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="c31b2-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c31b2-137">NOTES</span></span>

## <span data-ttu-id="c31b2-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c31b2-138">RELATED LINKS</span></span>
