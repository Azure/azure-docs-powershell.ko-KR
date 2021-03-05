---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
ms.openlocfilehash: e27d956f8530fb45f5927ece22302d21acafc503
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960379"
---
# <span data-ttu-id="32548-101">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="32548-101">New-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="32548-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32548-102">SYNOPSIS</span></span>
<span data-ttu-id="32548-103">네트워크 가상 어플라이언스에 연결된 사이트를 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="32548-103">Create a site connected to a Network Virtual Appliance.</span></span>

## <span data-ttu-id="32548-104">구문</span><span class="sxs-lookup"><span data-stu-id="32548-104">SYNTAX</span></span>

### <span data-ttu-id="32548-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="32548-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32548-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="32548-106">ResourceIdParameterSet</span></span>
```
New-AzVirtualApplianceSite -ResourceId <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32548-107">설명</span><span class="sxs-lookup"><span data-stu-id="32548-107">DESCRIPTION</span></span>
<span data-ttu-id="32548-108">New-AzVirtualApplianceSite 가상 어플라이언스 리소스에 연결된 Virtual Appliance 사이트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="32548-108">The New-AzVirtualApplianceSite command creates a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="32548-109">예제</span><span class="sxs-lookup"><span data-stu-id="32548-109">EXAMPLES</span></span>

### <span data-ttu-id="32548-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="32548-110">Example 1</span></span>
```powershell
PS C:\> $nva = Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva 
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize
PS C:\> $site = New-AzVirtualApplianceSite -ResourceGroupName testrg -Name testsite -NetworkVirtualApplianceId $nva.Id -AddressPrefix 10.0.1.0/24 -O365Policy $o365Policy
```

<span data-ttu-id="32548-111">리소스 그룹( testrg)에서 새 Virtual Appliance 사이트를 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="32548-111">Create a new Virtual Appliance site in the resource group: testrg.</span></span>

## <span data-ttu-id="32548-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="32548-112">PARAMETERS</span></span>

### <span data-ttu-id="32548-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="32548-113">-AddressPrefix</span></span>
<span data-ttu-id="32548-114">사이트의 주소 연결선입니다.</span><span class="sxs-lookup"><span data-stu-id="32548-114">The address prefix for the site.</span></span>

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

### <span data-ttu-id="32548-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32548-115">-AsJob</span></span>
<span data-ttu-id="32548-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="32548-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32548-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32548-117">-DefaultProfile</span></span>
<span data-ttu-id="32548-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="32548-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32548-119">-Force</span><span class="sxs-lookup"><span data-stu-id="32548-119">-Force</span></span>
<span data-ttu-id="32548-120">리소스를 덮어 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="32548-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="32548-121">-Name</span><span class="sxs-lookup"><span data-stu-id="32548-121">-Name</span></span>
<span data-ttu-id="32548-122">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32548-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32548-123">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="32548-123">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="32548-124">이 사이트에 연결된 네트워크 가상 어플라이언스입니다.</span><span class="sxs-lookup"><span data-stu-id="32548-124">The Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="32548-125">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="32548-125">-O365Policy</span></span>
<span data-ttu-id="32548-126">Office 365 브레이크아웃 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="32548-126">The Office 365 breakout policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32548-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32548-127">-ResourceGroupName</span></span>
<span data-ttu-id="32548-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32548-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32548-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32548-129">-ResourceId</span></span>
<span data-ttu-id="32548-130">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="32548-130">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32548-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="32548-131">-Tag</span></span>
<span data-ttu-id="32548-132">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="32548-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="32548-133">-확인</span><span class="sxs-lookup"><span data-stu-id="32548-133">-Confirm</span></span>
<span data-ttu-id="32548-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="32548-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32548-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32548-135">-WhatIf</span></span>
<span data-ttu-id="32548-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="32548-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32548-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="32548-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32548-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32548-138">CommonParameters</span></span>
<span data-ttu-id="32548-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="32548-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32548-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32548-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32548-141">입력</span><span class="sxs-lookup"><span data-stu-id="32548-141">INPUTS</span></span>

### <span data-ttu-id="32548-142">System.String</span><span class="sxs-lookup"><span data-stu-id="32548-142">System.String</span></span>

### <span data-ttu-id="32548-143">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="32548-143">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="32548-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="32548-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="32548-145">출력</span><span class="sxs-lookup"><span data-stu-id="32548-145">OUTPUTS</span></span>

### <span data-ttu-id="32548-146">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="32548-146">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="32548-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="32548-147">NOTES</span></span>

## <span data-ttu-id="32548-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32548-148">RELATED LINKS</span></span>
