---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
ms.openlocfilehash: 9a6c84c0ff5d22a4f6c6038266598c6adfe19b29
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379107"
---
# <span data-ttu-id="47713-101">New-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="47713-101">New-AzIpAllocation</span></span>

## <span data-ttu-id="47713-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47713-102">SYNOPSIS</span></span>
<span data-ttu-id="47713-103">Azure IpAllocation을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="47713-103">Creates an Azure IpAllocation.</span></span>

## <span data-ttu-id="47713-104">구문</span><span class="sxs-lookup"><span data-stu-id="47713-104">SYNTAX</span></span>

```
New-AzIpAllocation -Name <String> -ResourceGroupName <String> -Location <String>
 -IpAllocationType <String> [-Prefix <String>] [-PrefixLength <Int32>] [-PrefixType <String>]
 [-IpamAllocationId <String>] [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47713-105">설명</span><span class="sxs-lookup"><span data-stu-id="47713-105">DESCRIPTION</span></span>
<span data-ttu-id="47713-106">**New-AzIpAllocation** cmdlet은 Azure IpAllocation을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="47713-106">The **New-AzIpAllocation** cmdlet creates an Azure IpAllocation</span></span>

## <span data-ttu-id="47713-107">예제</span><span class="sxs-lookup"><span data-stu-id="47713-107">EXAMPLES</span></span>

### <span data-ttu-id="47713-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="47713-108">Example 1</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -Prefix '1.2.3.4/32' -IpAllocationTag @{"VnetId"="vnet1"}
```

### <span data-ttu-id="47713-109">예제 2</span><span class="sxs-lookup"><span data-stu-id="47713-109">Example 2</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -PrefixLength 32 -PrefixType 'ipv4' -IpAllocationTag @{"VnetId"="vnet1"}
```

## <span data-ttu-id="47713-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47713-110">PARAMETERS</span></span>

### <span data-ttu-id="47713-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47713-111">-AsJob</span></span>
<span data-ttu-id="47713-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="47713-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47713-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47713-113">-DefaultProfile</span></span>
<span data-ttu-id="47713-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="47713-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47713-115">-Force</span><span class="sxs-lookup"><span data-stu-id="47713-115">-Force</span></span>
<span data-ttu-id="47713-116">리소스를 다시 하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47713-116">Do not ask for confirmation if you want to override a resource</span></span>

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

### <span data-ttu-id="47713-117">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="47713-117">-IpAllocationTag</span></span>
<span data-ttu-id="47713-118">IP 할당의 할당 태그</span><span class="sxs-lookup"><span data-stu-id="47713-118">The allocation tags of the IP allocation</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47713-119">-IpAllocationType</span><span class="sxs-lookup"><span data-stu-id="47713-119">-IpAllocationType</span></span>
<span data-ttu-id="47713-120">IP 할당의 유형</span><span class="sxs-lookup"><span data-stu-id="47713-120">The type of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hypernet, Undefined

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47713-121">-IpamAllocationId</span><span class="sxs-lookup"><span data-stu-id="47713-121">-IpamAllocationId</span></span>
<span data-ttu-id="47713-122">IP 할당의 ipam 할당 ID</span><span class="sxs-lookup"><span data-stu-id="47713-122">The ipam allocation ID of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47713-123">-Location</span><span class="sxs-lookup"><span data-stu-id="47713-123">-Location</span></span>
<span data-ttu-id="47713-124">위치.</span><span class="sxs-lookup"><span data-stu-id="47713-124">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47713-125">-Name</span><span class="sxs-lookup"><span data-stu-id="47713-125">-Name</span></span>
<span data-ttu-id="47713-126">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47713-126">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47713-127">-Prefix</span><span class="sxs-lookup"><span data-stu-id="47713-127">-Prefix</span></span>
<span data-ttu-id="47713-128">IP 할당의 prefix</span><span class="sxs-lookup"><span data-stu-id="47713-128">The prefix of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47713-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="47713-129">-PrefixLength</span></span>
<span data-ttu-id="47713-130">IP 할당의 연결선 길이입니다.</span><span class="sxs-lookup"><span data-stu-id="47713-130">The prefix length of the IP allocation</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47713-131">-PrefixType</span><span class="sxs-lookup"><span data-stu-id="47713-131">-PrefixType</span></span>
<span data-ttu-id="47713-132">IP 할당의 prefix 형식</span><span class="sxs-lookup"><span data-stu-id="47713-132">The prefix type of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPV4, IPV6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47713-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47713-133">-ResourceGroupName</span></span>
<span data-ttu-id="47713-134">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47713-134">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47713-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="47713-135">-Tag</span></span>
<span data-ttu-id="47713-136">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="47713-136">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47713-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47713-137">-Confirm</span></span>
<span data-ttu-id="47713-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="47713-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47713-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47713-139">-WhatIf</span></span>
<span data-ttu-id="47713-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="47713-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47713-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47713-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47713-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47713-142">CommonParameters</span></span>
<span data-ttu-id="47713-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="47713-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47713-144">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="47713-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47713-145">입력</span><span class="sxs-lookup"><span data-stu-id="47713-145">INPUTS</span></span>

### <span data-ttu-id="47713-146">System.String</span><span class="sxs-lookup"><span data-stu-id="47713-146">System.String</span></span>

### <span data-ttu-id="47713-147">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="47713-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="47713-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="47713-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="47713-149">출력</span><span class="sxs-lookup"><span data-stu-id="47713-149">OUTPUTS</span></span>

### <span data-ttu-id="47713-150">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="47713-150">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="47713-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="47713-151">NOTES</span></span>

## <span data-ttu-id="47713-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="47713-152">RELATED LINKS</span></span>
