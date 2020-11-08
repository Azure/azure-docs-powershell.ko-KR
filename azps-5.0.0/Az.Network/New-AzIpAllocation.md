---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
ms.openlocfilehash: 9a6c84c0ff5d22a4f6c6038266598c6adfe19b29
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226376"
---
# <span data-ttu-id="27bda-101">New-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="27bda-101">New-AzIpAllocation</span></span>

## <span data-ttu-id="27bda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27bda-102">SYNOPSIS</span></span>
<span data-ttu-id="27bda-103">Azure IpAllocation을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="27bda-103">Creates an Azure IpAllocation.</span></span>

## <span data-ttu-id="27bda-104">구문과</span><span class="sxs-lookup"><span data-stu-id="27bda-104">SYNTAX</span></span>

```
New-AzIpAllocation -Name <String> -ResourceGroupName <String> -Location <String>
 -IpAllocationType <String> [-Prefix <String>] [-PrefixLength <Int32>] [-PrefixType <String>]
 [-IpamAllocationId <String>] [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27bda-105">설명은</span><span class="sxs-lookup"><span data-stu-id="27bda-105">DESCRIPTION</span></span>
<span data-ttu-id="27bda-106">**AzIpAllocation** Cmdlet은 Azure ipallocation 만들기</span><span class="sxs-lookup"><span data-stu-id="27bda-106">The **New-AzIpAllocation** cmdlet creates an Azure IpAllocation</span></span>

## <span data-ttu-id="27bda-107">예제의</span><span class="sxs-lookup"><span data-stu-id="27bda-107">EXAMPLES</span></span>

### <span data-ttu-id="27bda-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="27bda-108">Example 1</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -Prefix '1.2.3.4/32' -IpAllocationTag @{"VnetId"="vnet1"}
```

### <span data-ttu-id="27bda-109">예제 2</span><span class="sxs-lookup"><span data-stu-id="27bda-109">Example 2</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -PrefixLength 32 -PrefixType 'ipv4' -IpAllocationTag @{"VnetId"="vnet1"}
```

## <span data-ttu-id="27bda-110">변수</span><span class="sxs-lookup"><span data-stu-id="27bda-110">PARAMETERS</span></span>

### <span data-ttu-id="27bda-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27bda-111">-AsJob</span></span>
<span data-ttu-id="27bda-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="27bda-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27bda-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27bda-113">-DefaultProfile</span></span>
<span data-ttu-id="27bda-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27bda-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27bda-115">-Force</span><span class="sxs-lookup"><span data-stu-id="27bda-115">-Force</span></span>
<span data-ttu-id="27bda-116">리소스를 재정의 하려는 경우 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="27bda-116">Do not ask for confirmation if you want to override a resource</span></span>

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

### <span data-ttu-id="27bda-117">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="27bda-117">-IpAllocationTag</span></span>
<span data-ttu-id="27bda-118">IP 할당의 할당 태그</span><span class="sxs-lookup"><span data-stu-id="27bda-118">The allocation tags of the IP allocation</span></span>

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

### <span data-ttu-id="27bda-119">-IpAllocationType</span><span class="sxs-lookup"><span data-stu-id="27bda-119">-IpAllocationType</span></span>
<span data-ttu-id="27bda-120">IP 할당의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="27bda-120">The type of the IP allocation</span></span>

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

### <span data-ttu-id="27bda-121">-IpamAllocationId</span><span class="sxs-lookup"><span data-stu-id="27bda-121">-IpamAllocationId</span></span>
<span data-ttu-id="27bda-122">IP 할당의 ipam 할당 ID</span><span class="sxs-lookup"><span data-stu-id="27bda-122">The ipam allocation ID of the IP allocation</span></span>

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

### <span data-ttu-id="27bda-123">-위치</span><span class="sxs-lookup"><span data-stu-id="27bda-123">-Location</span></span>
<span data-ttu-id="27bda-124">location.</span><span class="sxs-lookup"><span data-stu-id="27bda-124">location.</span></span>

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

### <span data-ttu-id="27bda-125">-이름</span><span class="sxs-lookup"><span data-stu-id="27bda-125">-Name</span></span>
<span data-ttu-id="27bda-126">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27bda-126">The resource name.</span></span>

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

### <span data-ttu-id="27bda-127">-접두사</span><span class="sxs-lookup"><span data-stu-id="27bda-127">-Prefix</span></span>
<span data-ttu-id="27bda-128">IP 할당의 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="27bda-128">The prefix of the IP allocation</span></span>

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

### <span data-ttu-id="27bda-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="27bda-129">-PrefixLength</span></span>
<span data-ttu-id="27bda-130">IP 할당의 접두사 길이</span><span class="sxs-lookup"><span data-stu-id="27bda-130">The prefix length of the IP allocation</span></span>

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

### <span data-ttu-id="27bda-131">-PrefixType</span><span class="sxs-lookup"><span data-stu-id="27bda-131">-PrefixType</span></span>
<span data-ttu-id="27bda-132">IP 할당의 접두사 형식</span><span class="sxs-lookup"><span data-stu-id="27bda-132">The prefix type of the IP allocation</span></span>

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

### <span data-ttu-id="27bda-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27bda-133">-ResourceGroupName</span></span>
<span data-ttu-id="27bda-134">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27bda-134">The resource group name.</span></span>

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

### <span data-ttu-id="27bda-135">태그</span><span class="sxs-lookup"><span data-stu-id="27bda-135">-Tag</span></span>
<span data-ttu-id="27bda-136">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="27bda-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="27bda-137">-확인</span><span class="sxs-lookup"><span data-stu-id="27bda-137">-Confirm</span></span>
<span data-ttu-id="27bda-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="27bda-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27bda-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27bda-139">-WhatIf</span></span>
<span data-ttu-id="27bda-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="27bda-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27bda-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="27bda-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27bda-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27bda-142">CommonParameters</span></span>
<span data-ttu-id="27bda-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="27bda-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27bda-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="27bda-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27bda-145">입력</span><span class="sxs-lookup"><span data-stu-id="27bda-145">INPUTS</span></span>

### <span data-ttu-id="27bda-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="27bda-146">System.String</span></span>

### <span data-ttu-id="27bda-147">시스템 Null 허용 ' 1 [[b77a5c561934e089, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="27bda-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="27bda-148">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="27bda-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="27bda-149">출력</span><span class="sxs-lookup"><span data-stu-id="27bda-149">OUTPUTS</span></span>

### <span data-ttu-id="27bda-150">PSIpAllocation에 대 한.</span><span class="sxs-lookup"><span data-stu-id="27bda-150">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="27bda-151">상속자</span><span class="sxs-lookup"><span data-stu-id="27bda-151">NOTES</span></span>

## <span data-ttu-id="27bda-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27bda-152">RELATED LINKS</span></span>
