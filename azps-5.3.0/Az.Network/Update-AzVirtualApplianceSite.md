---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
ms.openlocfilehash: 4d63726f67cb43f34e58c8e560a08adefce5fcbd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490916"
---
# <span data-ttu-id="2ed5a-101">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="2ed5a-101">Update-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="2ed5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ed5a-102">SYNOPSIS</span></span>
<span data-ttu-id="2ed5a-103">네트워크 가상 어플라이언스 리소스에 연결된 가상 어플라이언스 사이트를 변경하거나 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed5a-103">Change or Modify a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="2ed5a-104">구문</span><span class="sxs-lookup"><span data-stu-id="2ed5a-104">SYNTAX</span></span>

```
Update-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -NetworkVirtualApplianceId <String>
 [-AddresssPrefix <String>] [-O365Policy <PSOffice365PolicyProperties>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ed5a-105">설명</span><span class="sxs-lookup"><span data-stu-id="2ed5a-105">DESCRIPTION</span></span>
<span data-ttu-id="2ed5a-106">이 Update-AzVirtualApplianceSite 가상 어플라이언스 사이트 리소스를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed5a-106">The Update-AzVirtualApplianceSite command modifies a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="2ed5a-107">예제</span><span class="sxs-lookup"><span data-stu-id="2ed5a-107">EXAMPLES</span></span>

### <span data-ttu-id="2ed5a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2ed5a-108">Example 1</span></span>
```powershell
PS C:\> $nva=Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
PS C:\> Update-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -AddresssPrefix 10.0.4.0/24 -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="2ed5a-109">가상 어플라이언스 사이트 리소스에 대한 주소 연결 주소를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed5a-109">Modify the address prefix for a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="2ed5a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ed5a-110">PARAMETERS</span></span>

### <span data-ttu-id="2ed5a-111">-AddresssPrefix</span><span class="sxs-lookup"><span data-stu-id="2ed5a-111">-AddresssPrefix</span></span>
<span data-ttu-id="2ed5a-112">사이트의 주소 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="2ed5a-112">The address prefix for the site.</span></span>

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

### <span data-ttu-id="2ed5a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ed5a-113">-AsJob</span></span>
<span data-ttu-id="2ed5a-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2ed5a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2ed5a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ed5a-115">-DefaultProfile</span></span>
<span data-ttu-id="2ed5a-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2ed5a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ed5a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2ed5a-117">-Force</span></span>
<span data-ttu-id="2ed5a-118">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2ed5a-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="2ed5a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2ed5a-119">-Name</span></span>
<span data-ttu-id="2ed5a-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2ed5a-120">The resource name.</span></span>

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

### <span data-ttu-id="2ed5a-121">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="2ed5a-121">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="2ed5a-122">이 사이트가 연결된 네트워크 가상 어플라이언스입니다.</span><span class="sxs-lookup"><span data-stu-id="2ed5a-122">Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="2ed5a-123">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="2ed5a-123">-O365Policy</span></span>
<span data-ttu-id="2ed5a-124">Office 365 중단 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="2ed5a-124">Office 365 breakout policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ed5a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ed5a-125">-ResourceGroupName</span></span>
<span data-ttu-id="2ed5a-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2ed5a-126">The resource group name.</span></span>

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

### <span data-ttu-id="2ed5a-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="2ed5a-127">-Tag</span></span>
<span data-ttu-id="2ed5a-128">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="2ed5a-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="2ed5a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ed5a-129">-Confirm</span></span>
<span data-ttu-id="2ed5a-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ed5a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ed5a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ed5a-131">-WhatIf</span></span>
<span data-ttu-id="2ed5a-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2ed5a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ed5a-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2ed5a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ed5a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ed5a-134">CommonParameters</span></span>
<span data-ttu-id="2ed5a-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed5a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ed5a-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2ed5a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ed5a-137">입력</span><span class="sxs-lookup"><span data-stu-id="2ed5a-137">INPUTS</span></span>

### <span data-ttu-id="2ed5a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2ed5a-138">System.String</span></span>

### <span data-ttu-id="2ed5a-139">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="2ed5a-139">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="2ed5a-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2ed5a-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2ed5a-141">출력</span><span class="sxs-lookup"><span data-stu-id="2ed5a-141">OUTPUTS</span></span>

### <span data-ttu-id="2ed5a-142">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="2ed5a-142">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="2ed5a-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2ed5a-143">NOTES</span></span>

## <span data-ttu-id="2ed5a-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2ed5a-144">RELATED LINKS</span></span>
