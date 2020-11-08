---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
ms.openlocfilehash: 0b29719dee8a1e69d27dd36cee2888df4575eefc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048877"
---
# <span data-ttu-id="71101-101">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="71101-101">Remove-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="71101-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71101-102">SYNOPSIS</span></span>
<span data-ttu-id="71101-103">네트워크 가상 기기 리소스에서 가상 기기 사이트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="71101-103">Remove a virtual appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="71101-104">구문과</span><span class="sxs-lookup"><span data-stu-id="71101-104">SYNTAX</span></span>

### <span data-ttu-id="71101-105">ResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="71101-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzVirtualApplianceSite -Name <String> -NetworkVirtualApplianceId <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71101-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="71101-106">ResourceIdParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71101-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="71101-107">ResourceObjectParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -VirtualApplianceSite <PSVirtualApplianceSite> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71101-108">설명은</span><span class="sxs-lookup"><span data-stu-id="71101-108">DESCRIPTION</span></span>
<span data-ttu-id="71101-109">Remove-AzVirtualApplianceSite 명령은 네트워크 가상 기기 리소스에서 가상 기기 사이트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="71101-109">The Remove-AzVirtualApplianceSite command removes a Virtual Appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="71101-110">예제의</span><span class="sxs-lookup"><span data-stu-id="71101-110">EXAMPLES</span></span>

### <span data-ttu-id="71101-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="71101-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="71101-112">가상 기기 사이트 리소스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="71101-112">Delete a Virtual Appliance site resource.</span></span> 

## <span data-ttu-id="71101-113">변수</span><span class="sxs-lookup"><span data-stu-id="71101-113">PARAMETERS</span></span>

### <span data-ttu-id="71101-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71101-114">-AsJob</span></span>
<span data-ttu-id="71101-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="71101-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71101-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71101-116">-DefaultProfile</span></span>
<span data-ttu-id="71101-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="71101-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71101-118">-Force</span><span class="sxs-lookup"><span data-stu-id="71101-118">-Force</span></span>
<span data-ttu-id="71101-119">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71101-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="71101-120">-이름</span><span class="sxs-lookup"><span data-stu-id="71101-120">-Name</span></span>
<span data-ttu-id="71101-121">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="71101-121">The resource name.</span></span>

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

### <span data-ttu-id="71101-122">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="71101-122">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="71101-123">이 사이트와 연결 된 네트워크 가상 기기의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="71101-123">The resource ID of the Network Virtual Appliance associated with this site.</span></span>

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

### <span data-ttu-id="71101-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71101-124">-PassThru</span></span>
<span data-ttu-id="71101-125">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="71101-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="71101-126">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71101-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="71101-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71101-127">-ResourceGroupName</span></span>
<span data-ttu-id="71101-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="71101-128">The resource group name.</span></span>

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

### <span data-ttu-id="71101-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71101-129">-ResourceId</span></span>
<span data-ttu-id="71101-130">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="71101-130">The resource id.</span></span>

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

### <span data-ttu-id="71101-131">-VirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="71101-131">-VirtualApplianceSite</span></span>
<span data-ttu-id="71101-132">가상 기기 사이트 개체</span><span class="sxs-lookup"><span data-stu-id="71101-132">The virtual appliance site object.</span></span>

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

### <span data-ttu-id="71101-133">-확인</span><span class="sxs-lookup"><span data-stu-id="71101-133">-Confirm</span></span>
<span data-ttu-id="71101-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="71101-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71101-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71101-135">-WhatIf</span></span>
<span data-ttu-id="71101-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="71101-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71101-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71101-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71101-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71101-138">CommonParameters</span></span>
<span data-ttu-id="71101-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="71101-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71101-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="71101-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71101-141">입력</span><span class="sxs-lookup"><span data-stu-id="71101-141">INPUTS</span></span>

### <span data-ttu-id="71101-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="71101-142">System.String</span></span>

### <span data-ttu-id="71101-143">PSVirtualApplianceSite에 대 한.</span><span class="sxs-lookup"><span data-stu-id="71101-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="71101-144">출력</span><span class="sxs-lookup"><span data-stu-id="71101-144">OUTPUTS</span></span>

### <span data-ttu-id="71101-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="71101-145">System.Boolean</span></span>

## <span data-ttu-id="71101-146">상속자</span><span class="sxs-lookup"><span data-stu-id="71101-146">NOTES</span></span>

## <span data-ttu-id="71101-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71101-147">RELATED LINKS</span></span>
