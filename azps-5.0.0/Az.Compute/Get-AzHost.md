---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzHost.md
ms.openlocfilehash: 692a32372718ee3100bd0ad0038d7ff89d483654
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310370"
---
# <span data-ttu-id="6ce85-101">Get-AzHost</span><span class="sxs-lookup"><span data-stu-id="6ce85-101">Get-AzHost</span></span>

## <span data-ttu-id="6ce85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ce85-102">SYNOPSIS</span></span>
<span data-ttu-id="6ce85-103">호스트를 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ce85-103">Get or list hosts.</span></span>

## <span data-ttu-id="6ce85-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6ce85-104">SYNTAX</span></span>

### <span data-ttu-id="6ce85-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="6ce85-105">DefaultParameter (Default)</span></span>
```
Get-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [[-Name] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ce85-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="6ce85-106">ResourceIdParameter</span></span>
```
Get-AzHost [-ResourceId] <String> [-InstanceView] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ce85-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6ce85-107">DESCRIPTION</span></span>
<span data-ttu-id="6ce85-108">이 cmdlet은 호스트 그룹의 호스트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6ce85-108">This cmdlet will get a host in a host group.</span></span>
<span data-ttu-id="6ce85-109">이 cmdlet은 호스트 이름이 지정 되지 않은 경우 호스트 그룹의 모든 호스트도 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ce85-109">This cmdlet also lists all hosts in a host group if a host name is not given.</span></span>

## <span data-ttu-id="6ce85-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6ce85-110">EXAMPLES</span></span>

### <span data-ttu-id="6ce85-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6ce85-111">Example 1</span></span>
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

<span data-ttu-id="6ce85-112">이 명령은 호스트를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ce85-112">This command returns a host.</span></span>

### <span data-ttu-id="6ce85-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="6ce85-113">Example 2</span></span>
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

<span data-ttu-id="6ce85-114">이 명령은 호스트의 인스턴스 뷰를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ce85-114">This command returns the instance view of a host.</span></span>

### <span data-ttu-id="6ce85-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="6ce85-115">Example 3</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName

ResourceGroupName       Name Location           Tags        Sku FD
-----------------       ---- --------           ----        --- --
myrg01              myhost01   eastus {[key1, val2]} ESv3-Type1  0
myrg01              myhost02   eastus {[key1, val2]} ESv3-Type1  1
```

<span data-ttu-id="6ce85-116">이 명령은 지정 된 호스트 그룹의 모든 호스트를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ce85-116">This command returns all hosts in the given host group.</span></span>

## <span data-ttu-id="6ce85-117">변수</span><span class="sxs-lookup"><span data-stu-id="6ce85-117">PARAMETERS</span></span>

### <span data-ttu-id="6ce85-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ce85-118">-DefaultProfile</span></span>
<span data-ttu-id="6ce85-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6ce85-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ce85-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="6ce85-120">-HostGroupName</span></span>
<span data-ttu-id="6ce85-121">호스트 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ce85-121">The name of the host group.</span></span>

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

### <span data-ttu-id="6ce85-122">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="6ce85-122">-InstanceView</span></span>
<span data-ttu-id="6ce85-123">이 cmdlet이 호스트의 인스턴스 보기만을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6ce85-123">Indicates that this cmdlet gets only the instance view of the host.</span></span>

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

### <span data-ttu-id="6ce85-124">-이름</span><span class="sxs-lookup"><span data-stu-id="6ce85-124">-Name</span></span>
<span data-ttu-id="6ce85-125">호스트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ce85-125">The name of the host.</span></span>

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

### <span data-ttu-id="6ce85-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ce85-126">-ResourceGroupName</span></span>
<span data-ttu-id="6ce85-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ce85-127">The name of the resource group</span></span>

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

### <span data-ttu-id="6ce85-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ce85-128">-ResourceId</span></span>
<span data-ttu-id="6ce85-129">리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6ce85-129">The ID of the resource.</span></span>

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

### <span data-ttu-id="6ce85-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ce85-130">CommonParameters</span></span>
<span data-ttu-id="6ce85-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ce85-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ce85-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6ce85-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ce85-133">입력</span><span class="sxs-lookup"><span data-stu-id="6ce85-133">INPUTS</span></span>

### <span data-ttu-id="6ce85-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6ce85-134">System.String</span></span>

## <span data-ttu-id="6ce85-135">출력</span><span class="sxs-lookup"><span data-stu-id="6ce85-135">OUTPUTS</span></span>

### <span data-ttu-id="6ce85-136">PSHost의. m a.</span><span class="sxs-lookup"><span data-stu-id="6ce85-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="6ce85-137">상속자</span><span class="sxs-lookup"><span data-stu-id="6ce85-137">NOTES</span></span>

## <span data-ttu-id="6ce85-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ce85-138">RELATED LINKS</span></span>
