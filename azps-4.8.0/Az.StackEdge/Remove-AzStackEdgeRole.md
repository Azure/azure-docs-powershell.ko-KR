---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
ms.openlocfilehash: 7e462c7f6d22a071217a7279a44114c3a95504bd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213818"
---
# <span data-ttu-id="7749f-101">Remove-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="7749f-101">Remove-AzStackEdgeRole</span></span>

## <span data-ttu-id="7749f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7749f-102">SYNOPSIS</span></span>
<span data-ttu-id="7749f-103">장치에 연결 된 IoT 역할을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7749f-103">Removes the associated IoT role for a device.</span></span>

## <span data-ttu-id="7749f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7749f-104">SYNTAX</span></span>

### <span data-ttu-id="7749f-105">DeleteByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7749f-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7749f-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7749f-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeRole -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7749f-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7749f-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeRole -InputObject <PSStackEdgeRole> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7749f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7749f-108">DESCRIPTION</span></span>
<span data-ttu-id="7749f-109">**AzStackEdgeRole** Cmdlet은 스택 경계 장치에 대 한 연결 된 IoT 역할을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7749f-109">The **Remove-AzStackEdgeRole** cmdlet removes the associated IoT role for a Stack Edge device.</span></span>

## <span data-ttu-id="7749f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7749f-110">EXAMPLES</span></span>

### <span data-ttu-id="7749f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7749f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleName
```

## <span data-ttu-id="7749f-112">변수</span><span class="sxs-lookup"><span data-stu-id="7749f-112">PARAMETERS</span></span>

### <span data-ttu-id="7749f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7749f-113">-AsJob</span></span>
<span data-ttu-id="7749f-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7749f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7749f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7749f-115">-DefaultProfile</span></span>
<span data-ttu-id="7749f-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7749f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7749f-117">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="7749f-117">-DeviceName</span></span>
<span data-ttu-id="7749f-118">장치 이름</span><span class="sxs-lookup"><span data-stu-id="7749f-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7749f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7749f-119">-InputObject</span></span>
<span data-ttu-id="7749f-120">입력 개체</span><span class="sxs-lookup"><span data-stu-id="7749f-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7749f-121">-이름</span><span class="sxs-lookup"><span data-stu-id="7749f-121">-Name</span></span>
<span data-ttu-id="7749f-122">자원 이름</span><span class="sxs-lookup"><span data-stu-id="7749f-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7749f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7749f-123">-PassThru</span></span>
<span data-ttu-id="7749f-124">성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7749f-124">returns true if successful</span></span>

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

### <span data-ttu-id="7749f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7749f-125">-ResourceGroupName</span></span>
<span data-ttu-id="7749f-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="7749f-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7749f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7749f-127">-ResourceId</span></span>
<span data-ttu-id="7749f-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7749f-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7749f-129">-확인</span><span class="sxs-lookup"><span data-stu-id="7749f-129">-Confirm</span></span>
<span data-ttu-id="7749f-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7749f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7749f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7749f-131">-WhatIf</span></span>
<span data-ttu-id="7749f-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7749f-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7749f-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7749f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7749f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7749f-134">CommonParameters</span></span>
<span data-ttu-id="7749f-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7749f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7749f-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7749f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7749f-137">입력</span><span class="sxs-lookup"><span data-stu-id="7749f-137">INPUTS</span></span>

### <span data-ttu-id="7749f-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7749f-138">System.String</span></span>

### <span data-ttu-id="7749f-139">StackEdge. PSStackEdgeRole에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="7749f-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="7749f-140">출력</span><span class="sxs-lookup"><span data-stu-id="7749f-140">OUTPUTS</span></span>

### <span data-ttu-id="7749f-141">StackEdge. PSStackEdgeRole에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="7749f-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="7749f-142">상속자</span><span class="sxs-lookup"><span data-stu-id="7749f-142">NOTES</span></span>

## <span data-ttu-id="7749f-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7749f-143">RELATED LINKS</span></span>
