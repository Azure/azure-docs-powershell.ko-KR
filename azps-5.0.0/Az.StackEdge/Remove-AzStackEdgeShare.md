---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeShare.md
ms.openlocfilehash: 3f5855d329daba44b26e2c79cbc07608222db5f9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216176"
---
# <span data-ttu-id="072bb-101">Remove-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="072bb-101">Remove-AzStackEdgeShare</span></span>

## <span data-ttu-id="072bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="072bb-102">SYNOPSIS</span></span>
<span data-ttu-id="072bb-103">장치에서 공유를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="072bb-103">Removes a share from the device.</span></span>

## <span data-ttu-id="072bb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="072bb-104">SYNTAX</span></span>

### <span data-ttu-id="072bb-105">DeleteByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="072bb-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="072bb-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="072bb-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeShare [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="072bb-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="072bb-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeShare [-InputObject] <PSStackEdgeShare> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="072bb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="072bb-108">DESCRIPTION</span></span>
<span data-ttu-id="072bb-109">**AzStackEdgeEdgeShare** Cmdlet은 스택 경계 장치에 대 한 연결 된 edge 공유를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="072bb-109">The **Remove-AzStackEdgeEdgeShare** cmdlet removes the associated edge shares for a Stack Edge device.</span></span>

## <span data-ttu-id="072bb-110">예제의</span><span class="sxs-lookup"><span data-stu-id="072bb-110">EXAMPLES</span></span>

### <span data-ttu-id="072bb-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="072bb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name shareName
```

## <span data-ttu-id="072bb-112">변수</span><span class="sxs-lookup"><span data-stu-id="072bb-112">PARAMETERS</span></span>

### <span data-ttu-id="072bb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="072bb-113">-AsJob</span></span>
<span data-ttu-id="072bb-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="072bb-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="072bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="072bb-115">-DefaultProfile</span></span>
<span data-ttu-id="072bb-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="072bb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="072bb-117">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="072bb-117">-DeviceName</span></span>
<span data-ttu-id="072bb-118">장치 이름</span><span class="sxs-lookup"><span data-stu-id="072bb-118">Device Name</span></span>

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

### <span data-ttu-id="072bb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="072bb-119">-InputObject</span></span>
<span data-ttu-id="072bb-120">입력 개체</span><span class="sxs-lookup"><span data-stu-id="072bb-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="072bb-121">-이름</span><span class="sxs-lookup"><span data-stu-id="072bb-121">-Name</span></span>
<span data-ttu-id="072bb-122">자원 이름</span><span class="sxs-lookup"><span data-stu-id="072bb-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="072bb-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="072bb-123">-PassThru</span></span>
<span data-ttu-id="072bb-124">성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="072bb-124">returns true if successful</span></span>

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

### <span data-ttu-id="072bb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="072bb-125">-ResourceGroupName</span></span>
<span data-ttu-id="072bb-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="072bb-126">Resource Group Name</span></span>

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

### <span data-ttu-id="072bb-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="072bb-127">-ResourceId</span></span>
<span data-ttu-id="072bb-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="072bb-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="072bb-129">-확인</span><span class="sxs-lookup"><span data-stu-id="072bb-129">-Confirm</span></span>
<span data-ttu-id="072bb-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="072bb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="072bb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="072bb-131">-WhatIf</span></span>
<span data-ttu-id="072bb-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="072bb-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="072bb-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="072bb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="072bb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="072bb-134">CommonParameters</span></span>
<span data-ttu-id="072bb-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="072bb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="072bb-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="072bb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="072bb-137">입력</span><span class="sxs-lookup"><span data-stu-id="072bb-137">INPUTS</span></span>

### <span data-ttu-id="072bb-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="072bb-138">System.String</span></span>

### <span data-ttu-id="072bb-139">StackEdge. PSStackEdgeShare에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="072bb-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="072bb-140">출력</span><span class="sxs-lookup"><span data-stu-id="072bb-140">OUTPUTS</span></span>

### <span data-ttu-id="072bb-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="072bb-141">System.Boolean</span></span>

## <span data-ttu-id="072bb-142">상속자</span><span class="sxs-lookup"><span data-stu-id="072bb-142">NOTES</span></span>

## <span data-ttu-id="072bb-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="072bb-143">RELATED LINKS</span></span>
