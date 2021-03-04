---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualApplianceSite.md
ms.openlocfilehash: 7d0d292cb7eba6b776371493e9ceb7e19ef17115
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951600"
---
# <span data-ttu-id="807c7-101">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="807c7-101">Update-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="807c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="807c7-102">SYNOPSIS</span></span>
<span data-ttu-id="807c7-103">네트워크 가상 어플라이언스 리소스에 연결된 가상 어플라이언스 사이트를 변경하거나 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="807c7-103">Change or Modify a Virtual Appliance site connected to a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="807c7-104">구문</span><span class="sxs-lookup"><span data-stu-id="807c7-104">SYNTAX</span></span>

```
Update-AzVirtualApplianceSite -Name <String> -ResourceGroupName <String> -NetworkVirtualApplianceId <String>
 [-AddresssPrefix <String>] [-O365Policy <PSOffice365PolicyProperties>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="807c7-105">설명</span><span class="sxs-lookup"><span data-stu-id="807c7-105">DESCRIPTION</span></span>
<span data-ttu-id="807c7-106">Update-AzVirtualApplianceSite 명령은 Virtual Appliance 사이트 리소스를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="807c7-106">The Update-AzVirtualApplianceSite command modifies a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="807c7-107">예제</span><span class="sxs-lookup"><span data-stu-id="807c7-107">EXAMPLES</span></span>

### <span data-ttu-id="807c7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="807c7-108">Example 1</span></span>
```powershell
PS C:\> $nva=Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
PS C:\> Update-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -AddresssPrefix 10.0.4.0/24 -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="807c7-109">Virtual Appliance 사이트 리소스에 대한 주소 연결부를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="807c7-109">Modify the address prefix for a Virtual Appliance site resource.</span></span>

## <span data-ttu-id="807c7-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="807c7-110">PARAMETERS</span></span>

### <span data-ttu-id="807c7-111">-AddresssPrefix</span><span class="sxs-lookup"><span data-stu-id="807c7-111">-AddresssPrefix</span></span>
<span data-ttu-id="807c7-112">사이트의 주소 연결선입니다.</span><span class="sxs-lookup"><span data-stu-id="807c7-112">The address prefix for the site.</span></span>

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

### <span data-ttu-id="807c7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="807c7-113">-AsJob</span></span>
<span data-ttu-id="807c7-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="807c7-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="807c7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="807c7-115">-DefaultProfile</span></span>
<span data-ttu-id="807c7-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="807c7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="807c7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="807c7-117">-Force</span></span>
<span data-ttu-id="807c7-118">리소스를 덮어 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="807c7-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="807c7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="807c7-119">-Name</span></span>
<span data-ttu-id="807c7-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="807c7-120">The resource name.</span></span>

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

### <span data-ttu-id="807c7-121">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="807c7-121">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="807c7-122">이 사이트가 연결된 네트워크 가상 어플라이언스입니다.</span><span class="sxs-lookup"><span data-stu-id="807c7-122">Network virtual appliance that this site is attached to.</span></span>

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

### <span data-ttu-id="807c7-123">-O365Policy</span><span class="sxs-lookup"><span data-stu-id="807c7-123">-O365Policy</span></span>
<span data-ttu-id="807c7-124">Office 365 브레이크아웃 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="807c7-124">Office 365 breakout policy.</span></span>

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

### <span data-ttu-id="807c7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="807c7-125">-ResourceGroupName</span></span>
<span data-ttu-id="807c7-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="807c7-126">The resource group name.</span></span>

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

### <span data-ttu-id="807c7-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="807c7-127">-Tag</span></span>
<span data-ttu-id="807c7-128">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="807c7-128">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="807c7-129">-확인</span><span class="sxs-lookup"><span data-stu-id="807c7-129">-Confirm</span></span>
<span data-ttu-id="807c7-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="807c7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="807c7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="807c7-131">-WhatIf</span></span>
<span data-ttu-id="807c7-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="807c7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="807c7-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="807c7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="807c7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="807c7-134">CommonParameters</span></span>
<span data-ttu-id="807c7-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="807c7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="807c7-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="807c7-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="807c7-137">입력</span><span class="sxs-lookup"><span data-stu-id="807c7-137">INPUTS</span></span>

### <span data-ttu-id="807c7-138">System.String</span><span class="sxs-lookup"><span data-stu-id="807c7-138">System.String</span></span>

### <span data-ttu-id="807c7-139">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="807c7-139">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

### <span data-ttu-id="807c7-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="807c7-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="807c7-141">출력</span><span class="sxs-lookup"><span data-stu-id="807c7-141">OUTPUTS</span></span>

### <span data-ttu-id="807c7-142">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="807c7-142">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="807c7-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="807c7-143">NOTES</span></span>

## <span data-ttu-id="807c7-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="807c7-144">RELATED LINKS</span></span>
