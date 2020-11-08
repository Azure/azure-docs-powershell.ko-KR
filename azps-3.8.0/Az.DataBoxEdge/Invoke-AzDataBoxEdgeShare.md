---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/invoke-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Invoke-AzDataBoxEdgeShare.md
ms.openlocfilehash: c3fa71b6fb54f359f035f4f6c2f18789ff24b3ac
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043404"
---
# <span data-ttu-id="11c36-101">Invoke-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="11c36-101">Invoke-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="11c36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11c36-102">SYNOPSIS</span></span>
<span data-ttu-id="11c36-103">공유에 대 한 특정 작업을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c36-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="11c36-104">구문과</span><span class="sxs-lookup"><span data-stu-id="11c36-104">SYNTAX</span></span>

### <span data-ttu-id="11c36-105">InvokeByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="11c36-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11c36-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11c36-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzDataBoxEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11c36-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11c36-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzDataBoxEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11c36-108">설명은</span><span class="sxs-lookup"><span data-stu-id="11c36-108">DESCRIPTION</span></span>
<span data-ttu-id="11c36-109">**AzDataBoxEdgeShare** Cmdlet은 데이터 상자 가장자리 장치에서 공유에 있는 데이터를 새로 고치는 동작을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c36-109">The **Invoke-AzDataBoxEdgeShare** cmdlet invokes action to refresh data on a share on a Data Box Edge device.</span></span>

## <span data-ttu-id="11c36-110">예제의</span><span class="sxs-lookup"><span data-stu-id="11c36-110">EXAMPLES</span></span>

### <span data-ttu-id="11c36-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="11c36-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="11c36-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="11c36-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzDataBoxEdgeShare
```

## <span data-ttu-id="11c36-113">변수</span><span class="sxs-lookup"><span data-stu-id="11c36-113">PARAMETERS</span></span>

### <span data-ttu-id="11c36-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11c36-114">-AsJob</span></span>
<span data-ttu-id="11c36-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="11c36-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11c36-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11c36-116">-DefaultProfile</span></span>
<span data-ttu-id="11c36-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11c36-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11c36-118">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="11c36-118">-DeviceName</span></span>
<span data-ttu-id="11c36-119">장치 이름</span><span class="sxs-lookup"><span data-stu-id="11c36-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11c36-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11c36-120">-InputObject</span></span>
<span data-ttu-id="11c36-121">입력 개체</span><span class="sxs-lookup"><span data-stu-id="11c36-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11c36-122">-이름</span><span class="sxs-lookup"><span data-stu-id="11c36-122">-Name</span></span>
<span data-ttu-id="11c36-123">자원 이름</span><span class="sxs-lookup"><span data-stu-id="11c36-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11c36-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11c36-124">-PassThru</span></span>
<span data-ttu-id="11c36-125">성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c36-125">returns true if successful</span></span>

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

### <span data-ttu-id="11c36-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="11c36-126">-RefreshData</span></span>
<span data-ttu-id="11c36-127">클라우드의 데이터와 공유 메타 데이터를 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="11c36-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="11c36-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11c36-128">-ResourceGroupName</span></span>
<span data-ttu-id="11c36-129">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="11c36-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11c36-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11c36-130">-ResourceId</span></span>
<span data-ttu-id="11c36-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="11c36-131">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11c36-132">-확인</span><span class="sxs-lookup"><span data-stu-id="11c36-132">-Confirm</span></span>
<span data-ttu-id="11c36-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c36-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11c36-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11c36-134">-WhatIf</span></span>
<span data-ttu-id="11c36-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="11c36-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11c36-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11c36-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11c36-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11c36-137">CommonParameters</span></span>
<span data-ttu-id="11c36-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c36-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11c36-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="11c36-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11c36-140">입력</span><span class="sxs-lookup"><span data-stu-id="11c36-140">INPUTS</span></span>

### <span data-ttu-id="11c36-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="11c36-141">System.String</span></span>

### <span data-ttu-id="11c36-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="11c36-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="11c36-143">출력</span><span class="sxs-lookup"><span data-stu-id="11c36-143">OUTPUTS</span></span>

### <span data-ttu-id="11c36-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="11c36-144">System.Boolean</span></span>

## <span data-ttu-id="11c36-145">상속자</span><span class="sxs-lookup"><span data-stu-id="11c36-145">NOTES</span></span>

## <span data-ttu-id="11c36-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11c36-146">RELATED LINKS</span></span>
