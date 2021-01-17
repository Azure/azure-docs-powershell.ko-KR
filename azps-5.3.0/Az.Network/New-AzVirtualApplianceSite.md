---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSite.md
ms.openlocfilehash: 9ac7885cc81744914599308c20bf3350642fc967
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385386"
---
# <span data-ttu-id="1dd2b-101">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="1dd2b-101">New-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="1dd2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dd2b-102">SYNOPSIS</span></span>
<span data-ttu-id="1dd2b-103">네트워크 가상 어플라이언스에 연결된 사이트를 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-103">Create a site connected to a Network Virtual Appliance.</span></span>

## <span data-ttu-id="1dd2b-104">구문</span><span class="sxs-lookup"><span data-stu-id="1dd2b-104">SYNTAX</span></span>

### <span data-ttu-id="1dd2b-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1dd2b-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dd2b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dd2b-106">ResourceIdParameterSet</span></span>
```
New-AzVirtualApplianceSite -ResourceId <String> -AddressPrefix <String>
 -O365Policy <PSOffice365PolicyProperties> -NetworkVirtualApplianceId <String> [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dd2b-107">설명</span><span class="sxs-lookup"><span data-stu-id="1dd2b-107">DESCRIPTION</span></span>
<span data-ttu-id="1dd2b-108">New-AzVirtualApplianceSite 명령은 네트워크 가상 어플라이언스 리소스에 연결된 가상 어플라이언스 사이트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-108">The New-AzVirtualApplianceSite command creates a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="1dd2b-109">예제</span><span class="sxs-lookup"><span data-stu-id="1dd2b-109">EXAMPLES</span></span>

### <span data-ttu-id="1dd2b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="1dd2b-110">Example 1</span></span>
```powershell
PS C:\> $nva = Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva 
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize
PS C:\> $site = New-AzVirtualApplianceSite -ResourceGroupName testrg -Name testsite -NetworkVirtualApplianceId $nva.Id -AddressPrefix 10.0.1.0/24 -O365Policy $o365Policy
```

<span data-ttu-id="1dd2b-111">리소스 그룹: testrg에서 새 가상 어플라이언스 사이트를 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-111">Create a new Virtual Appliance site in the resource group: testrg.</span></span>

## <span data-ttu-id="1dd2b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1dd2b-112">PARAMETERS</span></span>

### <span data-ttu-id="1dd2b-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1dd2b-113">-AddressPrefix</span></span>
<span data-ttu-id="1dd2b-114">사이트의 주소 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-114">The address prefix for the site.</span></span>

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

### <span data-ttu-id="1dd2b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1dd2b-115">-AsJob</span></span>
<span data-ttu-id="1dd2b-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1dd2b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1dd2b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dd2b-117">-DefaultProfile</span></span>
<span data-ttu-id="1dd2b-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dd2b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="1dd2b-119">-Force</span></span>
<span data-ttu-id="1dd2b-120">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1dd2b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1dd2b-121">-Name</span></span>
<span data-ttu-id="1dd2b-122">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-122">The resource name.</span></span>

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

### <span data-ttu-id="1dd2b-123">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="1dd2b-123">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="1dd2b-124">이 사이트가 연결된 네트워크 가상 어플라이언스입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-124">The Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="1dd2b-125">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="1dd2b-125">-O365Policy</span></span>
<span data-ttu-id="1dd2b-126">Office 365 중단 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-126">The Office 365 breakout policy.</span></span>

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

### <span data-ttu-id="1dd2b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dd2b-127">-ResourceGroupName</span></span>
<span data-ttu-id="1dd2b-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-128">The resource group name.</span></span>

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

### <span data-ttu-id="1dd2b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1dd2b-129">-ResourceId</span></span>
<span data-ttu-id="1dd2b-130">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-130">The resource id.</span></span>

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

### <span data-ttu-id="1dd2b-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="1dd2b-131">-Tag</span></span>
<span data-ttu-id="1dd2b-132">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="1dd2b-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1dd2b-133">-Confirm</span></span>
<span data-ttu-id="1dd2b-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dd2b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dd2b-135">-WhatIf</span></span>
<span data-ttu-id="1dd2b-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1dd2b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dd2b-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dd2b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dd2b-138">CommonParameters</span></span>
<span data-ttu-id="1dd2b-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dd2b-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dd2b-141">입력</span><span class="sxs-lookup"><span data-stu-id="1dd2b-141">INPUTS</span></span>

### <span data-ttu-id="1dd2b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="1dd2b-142">System.String</span></span>

### <span data-ttu-id="1dd2b-143">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="1dd2b-143">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="1dd2b-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1dd2b-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1dd2b-145">출력</span><span class="sxs-lookup"><span data-stu-id="1dd2b-145">OUTPUTS</span></span>

### <span data-ttu-id="1dd2b-146">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="1dd2b-146">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="1dd2b-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1dd2b-147">NOTES</span></span>

## <span data-ttu-id="1dd2b-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1dd2b-148">RELATED LINKS</span></span>
