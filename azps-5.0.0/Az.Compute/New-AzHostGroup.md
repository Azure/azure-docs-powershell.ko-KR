---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
ms.openlocfilehash: 2fdb5317504bb1bc08ed45e8224a30a61cca8e8c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217067"
---
# <span data-ttu-id="8cdbf-101">New-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="8cdbf-101">New-AzHostGroup</span></span>

## <span data-ttu-id="8cdbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cdbf-102">SYNOPSIS</span></span>
<span data-ttu-id="8cdbf-103">호스트 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8cdbf-103">Creates a host group.</span></span>

## <span data-ttu-id="8cdbf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8cdbf-104">SYNTAX</span></span>

```
New-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 -PlatformFaultDomain <Int32> [-Zone <String[]>] [-SupportAutomaticPlacement <bool>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cdbf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8cdbf-105">DESCRIPTION</span></span>
<span data-ttu-id="8cdbf-106">이 cmdlet은 호스트 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8cdbf-106">This cmdlet will create a Host group.</span></span>

## <span data-ttu-id="8cdbf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8cdbf-107">EXAMPLES</span></span>

### <span data-ttu-id="8cdbf-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8cdbf-108">Example 1</span></span>
```
PS C:\> New-AzHostGroup -ResourceGroupName $resourceGroupName -Name $hostGroupName -Location $location -Zone $zone

ResourceGroupName        : myrg01
PlatformFaultDomainCount : 2
Hosts                    : {/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01}
Zones                    : {1}
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01
Name                     : myhostgroup01
Location                 : eastus
Tags                     : {[key1, val1]}
```

<span data-ttu-id="8cdbf-109">이 명령은 지정 된 위치와 영역에 호스트 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8cdbf-109">This command creates a host group in the given location and zone.</span></span>

## <span data-ttu-id="8cdbf-110">변수</span><span class="sxs-lookup"><span data-stu-id="8cdbf-110">PARAMETERS</span></span>

### <span data-ttu-id="8cdbf-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8cdbf-111">-AsJob</span></span>
<span data-ttu-id="8cdbf-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8cdbf-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8cdbf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cdbf-113">-DefaultProfile</span></span>
<span data-ttu-id="8cdbf-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8cdbf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cdbf-115">-위치</span><span class="sxs-lookup"><span data-stu-id="8cdbf-115">-Location</span></span>
<span data-ttu-id="8cdbf-116">위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdbf-116">Specifies location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cdbf-117">-이름</span><span class="sxs-lookup"><span data-stu-id="8cdbf-117">-Name</span></span>
<span data-ttu-id="8cdbf-118">호스트 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdbf-118">Specifies the name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cdbf-119">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="8cdbf-119">-PlatformFaultDomain</span></span>
<span data-ttu-id="8cdbf-120">호스트 그룹이 확장할 수 있는 장애 도메인의 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdbf-120">Specifies the number of fault domains that the host group can span.</span></span>  <span data-ttu-id="8cdbf-121">Minimum 값은 1이 고 최대값은 3입니다.</span><span class="sxs-lookup"><span data-stu-id="8cdbf-121">The minimum value is 1 and the maximum value is 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cdbf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cdbf-122">-ResourceGroupName</span></span>
<span data-ttu-id="8cdbf-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8cdbf-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cdbf-124">태그</span><span class="sxs-lookup"><span data-stu-id="8cdbf-124">-Tag</span></span>
<span data-ttu-id="8cdbf-125">태그를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdbf-125">Specifies Tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cdbf-126">-Zone</span><span class="sxs-lookup"><span data-stu-id="8cdbf-126">-Zone</span></span>
<span data-ttu-id="8cdbf-127">호스트 그룹의 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdbf-127">Specifies Zones of the host group.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cdbf-128">-Support자동 배치</span><span class="sxs-lookup"><span data-stu-id="8cdbf-128">-SupportAutomaticPlacement</span></span>
<span data-ttu-id="8cdbf-129">HostGroup에서 vm의 자동 배치를 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdbf-129">Specifies if HostGroup will enable automatic placement of vm's.</span></span>
<span data-ttu-id="8cdbf-130">자동 배치는 이러한 Vm이 Azure에 의해 선택 된 전용 호스트 그룹의 전용 호스트에 배치 됨을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdbf-130">Automatic placement means these VMs are placed on dedicated hosts, chosen by Azure, under the dedicated host group.</span></span>
<span data-ttu-id="8cdbf-131">지정 되지 않은 경우 기본값은 true입니다.</span><span class="sxs-lookup"><span data-stu-id="8cdbf-131">If not specified, default value will be true.</span></span>

```yaml
Type: bool
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: True
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="8cdbf-132">-확인</span><span class="sxs-lookup"><span data-stu-id="8cdbf-132">-Confirm</span></span>
<span data-ttu-id="8cdbf-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdbf-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cdbf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cdbf-134">-WhatIf</span></span>
<span data-ttu-id="8cdbf-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8cdbf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cdbf-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8cdbf-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cdbf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cdbf-137">CommonParameters</span></span>
<span data-ttu-id="8cdbf-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cdbf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cdbf-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8cdbf-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cdbf-140">입력</span><span class="sxs-lookup"><span data-stu-id="8cdbf-140">INPUTS</span></span>

### <span data-ttu-id="8cdbf-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8cdbf-141">System.String</span></span>

## <span data-ttu-id="8cdbf-142">출력</span><span class="sxs-lookup"><span data-stu-id="8cdbf-142">OUTPUTS</span></span>

### <span data-ttu-id="8cdbf-143">PSHostGroup의. m a.</span><span class="sxs-lookup"><span data-stu-id="8cdbf-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="8cdbf-144">상속자</span><span class="sxs-lookup"><span data-stu-id="8cdbf-144">NOTES</span></span>

## <span data-ttu-id="8cdbf-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8cdbf-145">RELATED LINKS</span></span>
