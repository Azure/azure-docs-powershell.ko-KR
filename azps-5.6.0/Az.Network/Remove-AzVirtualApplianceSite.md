---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
ms.openlocfilehash: 1456acb101302297e807d6d46bf83183e8a6e523
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006123"
---
# <span data-ttu-id="3c746-101">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="3c746-101">Remove-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="3c746-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c746-102">SYNOPSIS</span></span>
<span data-ttu-id="3c746-103">네트워크 가상 어플라이언스 리소스에서 가상 어플라이언스 사이트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3c746-103">Remove a virtual appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="3c746-104">구문</span><span class="sxs-lookup"><span data-stu-id="3c746-104">SYNTAX</span></span>

### <span data-ttu-id="3c746-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3c746-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzVirtualApplianceSite -Name <String> -NetworkVirtualApplianceId <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c746-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c746-106">ResourceIdParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c746-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c746-107">ResourceObjectParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -VirtualApplianceSite <PSVirtualApplianceSite> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c746-108">설명</span><span class="sxs-lookup"><span data-stu-id="3c746-108">DESCRIPTION</span></span>
<span data-ttu-id="3c746-109">Remove-AzVirtualApplianceSite 명령은 네트워크 가상 어플라이언스 리소스에서 Virtual Appliance 사이트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3c746-109">The Remove-AzVirtualApplianceSite command removes a Virtual Appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="3c746-110">예제</span><span class="sxs-lookup"><span data-stu-id="3c746-110">EXAMPLES</span></span>

### <span data-ttu-id="3c746-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3c746-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="3c746-112">Virtual Appliance 사이트 리소스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="3c746-112">Delete a Virtual Appliance site resource.</span></span> 

## <span data-ttu-id="3c746-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3c746-113">PARAMETERS</span></span>

### <span data-ttu-id="3c746-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c746-114">-AsJob</span></span>
<span data-ttu-id="3c746-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3c746-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c746-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c746-116">-DefaultProfile</span></span>
<span data-ttu-id="3c746-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3c746-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c746-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3c746-118">-Force</span></span>
<span data-ttu-id="3c746-119">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3c746-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3c746-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3c746-120">-Name</span></span>
<span data-ttu-id="3c746-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c746-121">The resource name.</span></span>

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

### <span data-ttu-id="3c746-122">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="3c746-122">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="3c746-123">이 사이트와 연결된 네트워크 가상 어플라이언스의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3c746-123">The resource ID of the Network Virtual Appliance associated with this site.</span></span>

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

### <span data-ttu-id="3c746-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c746-124">-PassThru</span></span>
<span data-ttu-id="3c746-125">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3c746-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="3c746-126">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3c746-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3c746-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c746-127">-ResourceGroupName</span></span>
<span data-ttu-id="3c746-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3c746-128">The resource group name.</span></span>

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

### <span data-ttu-id="3c746-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c746-129">-ResourceId</span></span>
<span data-ttu-id="3c746-130">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3c746-130">The resource id.</span></span>

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

### <span data-ttu-id="3c746-131">-VirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="3c746-131">-VirtualApplianceSite</span></span>
<span data-ttu-id="3c746-132">가상 어플라이언스 사이트 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3c746-132">The virtual appliance site object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c746-133">-확인</span><span class="sxs-lookup"><span data-stu-id="3c746-133">-Confirm</span></span>
<span data-ttu-id="3c746-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3c746-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c746-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c746-135">-WhatIf</span></span>
<span data-ttu-id="3c746-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3c746-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c746-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3c746-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c746-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c746-138">CommonParameters</span></span>
<span data-ttu-id="3c746-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3c746-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c746-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c746-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c746-141">입력</span><span class="sxs-lookup"><span data-stu-id="3c746-141">INPUTS</span></span>

### <span data-ttu-id="3c746-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3c746-142">System.String</span></span>

### <span data-ttu-id="3c746-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="3c746-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="3c746-144">출력</span><span class="sxs-lookup"><span data-stu-id="3c746-144">OUTPUTS</span></span>

### <span data-ttu-id="3c746-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3c746-145">System.Boolean</span></span>

## <span data-ttu-id="3c746-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3c746-146">NOTES</span></span>

## <span data-ttu-id="3c746-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3c746-147">RELATED LINKS</span></span>
