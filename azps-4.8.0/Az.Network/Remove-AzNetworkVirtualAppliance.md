---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
ms.openlocfilehash: e57b68db7e2ee285ef75e0ada33a6564574bb4ed
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94203919"
---
# <span data-ttu-id="6e345-101">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="6e345-101">Remove-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="6e345-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e345-102">SYNOPSIS</span></span>
<span data-ttu-id="6e345-103">네트워크 가상 기기 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e345-103">Remove a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="6e345-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6e345-104">SYNTAX</span></span>

### <span data-ttu-id="6e345-105">ResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6e345-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e345-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e345-106">ResourceIdParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e345-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e345-107">ResourceObjectParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -NetworkVirtualAppliance <PSNetworkVirtualAppliance> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e345-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6e345-108">DESCRIPTION</span></span>
<span data-ttu-id="6e345-109">Remove-AzNetworkVirtualAppliance 명령은 네트워크 가상 기기 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e345-109">The Remove-AzNetworkVirtualAppliance command removes a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="6e345-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6e345-110">EXAMPLES</span></span>

### <span data-ttu-id="6e345-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6e345-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
```

<span data-ttu-id="6e345-112">네트워크 가상 기기 리소스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e345-112">Delete a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="6e345-113">변수</span><span class="sxs-lookup"><span data-stu-id="6e345-113">PARAMETERS</span></span>

### <span data-ttu-id="6e345-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e345-114">-AsJob</span></span>
<span data-ttu-id="6e345-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6e345-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e345-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e345-116">-DefaultProfile</span></span>
<span data-ttu-id="6e345-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6e345-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e345-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6e345-118">-Force</span></span>
<span data-ttu-id="6e345-119">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e345-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6e345-120">-이름</span><span class="sxs-lookup"><span data-stu-id="6e345-120">-Name</span></span>
<span data-ttu-id="6e345-121">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e345-121">The resource name.</span></span>

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

### <span data-ttu-id="6e345-122">-NetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="6e345-122">-NetworkVirtualAppliance</span></span>
<span data-ttu-id="6e345-123">리소스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6e345-123">The resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e345-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e345-124">-PassThru</span></span>
<span data-ttu-id="6e345-125">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e345-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="6e345-126">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e345-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6e345-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e345-127">-ResourceGroupName</span></span>
<span data-ttu-id="6e345-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e345-128">The resource group name.</span></span>

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

### <span data-ttu-id="6e345-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e345-129">-ResourceId</span></span>
<span data-ttu-id="6e345-130">리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="6e345-130">The Resource Id.</span></span>

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

### <span data-ttu-id="6e345-131">-확인</span><span class="sxs-lookup"><span data-stu-id="6e345-131">-Confirm</span></span>
<span data-ttu-id="6e345-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e345-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e345-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e345-133">-WhatIf</span></span>
<span data-ttu-id="6e345-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6e345-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e345-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e345-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e345-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e345-136">CommonParameters</span></span>
<span data-ttu-id="6e345-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e345-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e345-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e345-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e345-139">입력</span><span class="sxs-lookup"><span data-stu-id="6e345-139">INPUTS</span></span>

### <span data-ttu-id="6e345-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6e345-140">System.String</span></span>

### <span data-ttu-id="6e345-141">Microsoft. 네트워크 모델. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="6e345-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="6e345-142">출력</span><span class="sxs-lookup"><span data-stu-id="6e345-142">OUTPUTS</span></span>

### <span data-ttu-id="6e345-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="6e345-143">System.Boolean</span></span>

## <span data-ttu-id="6e345-144">상속자</span><span class="sxs-lookup"><span data-stu-id="6e345-144">NOTES</span></span>

## <span data-ttu-id="6e345-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e345-145">RELATED LINKS</span></span>
