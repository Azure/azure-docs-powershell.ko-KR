---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
ms.openlocfilehash: cecfa3e009f6d6fbc7167c4b8f1ca110d547b5b7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493580"
---
# <span data-ttu-id="4cbe6-101">Remove-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="4cbe6-101">Remove-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="4cbe6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cbe6-102">SYNOPSIS</span></span>
<span data-ttu-id="4cbe6-103">디바이스에서 사용자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbe6-103">Removes a user on a device.</span></span>

## <span data-ttu-id="4cbe6-104">구문</span><span class="sxs-lookup"><span data-stu-id="4cbe6-104">SYNTAX</span></span>

### <span data-ttu-id="4cbe6-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4cbe6-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cbe6-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cbe6-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cbe6-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cbe6-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-InputObject] <PSDataBoxEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cbe6-108">설명</span><span class="sxs-lookup"><span data-stu-id="4cbe6-108">DESCRIPTION</span></span>
<span data-ttu-id="4cbe6-109">**Remove-AzDataBoxEdgeUser** cmdlet은 Data Box Edge 디바이스에서 사용자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbe6-109">The **Remove-AzDataBoxEdgeUser** cmdlet removes a user on the Data Box Edge device.</span></span> <span data-ttu-id="4cbe6-110">형식의 사용자만 만들 `Share` 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4cbe6-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="4cbe6-111">예제</span><span class="sxs-lookup"><span data-stu-id="4cbe6-111">EXAMPLES</span></span>

### <span data-ttu-id="4cbe6-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="4cbe6-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="4cbe6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cbe6-113">PARAMETERS</span></span>

### <span data-ttu-id="4cbe6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4cbe6-114">-AsJob</span></span>
<span data-ttu-id="4cbe6-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="4cbe6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4cbe6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cbe6-116">-DefaultProfile</span></span>
<span data-ttu-id="4cbe6-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4cbe6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cbe6-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="4cbe6-118">-DeviceName</span></span>
<span data-ttu-id="4cbe6-119">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="4cbe6-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cbe6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4cbe6-120">-InputObject</span></span>
<span data-ttu-id="4cbe6-121">입력 개체</span><span class="sxs-lookup"><span data-stu-id="4cbe6-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4cbe6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4cbe6-122">-Name</span></span>
<span data-ttu-id="4cbe6-123">사용자 이름</span><span class="sxs-lookup"><span data-stu-id="4cbe6-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cbe6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4cbe6-124">-PassThru</span></span>
<span data-ttu-id="4cbe6-125">성공한 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbe6-125">returns true if successful</span></span>

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

### <span data-ttu-id="4cbe6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cbe6-126">-ResourceGroupName</span></span>
<span data-ttu-id="4cbe6-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="4cbe6-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cbe6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4cbe6-128">-ResourceId</span></span>
<span data-ttu-id="4cbe6-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="4cbe6-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="4cbe6-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4cbe6-130">-Confirm</span></span>
<span data-ttu-id="4cbe6-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cbe6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cbe6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cbe6-132">-WhatIf</span></span>
<span data-ttu-id="4cbe6-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4cbe6-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4cbe6-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4cbe6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cbe6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cbe6-135">CommonParameters</span></span>
<span data-ttu-id="4cbe6-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4cbe6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cbe6-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4cbe6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cbe6-138">입력</span><span class="sxs-lookup"><span data-stu-id="4cbe6-138">INPUTS</span></span>

### <span data-ttu-id="4cbe6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4cbe6-139">System.String</span></span>

### <span data-ttu-id="4cbe6-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="4cbe6-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="4cbe6-141">출력</span><span class="sxs-lookup"><span data-stu-id="4cbe6-141">OUTPUTS</span></span>

### <span data-ttu-id="4cbe6-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="4cbe6-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="4cbe6-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4cbe6-143">NOTES</span></span>

## <span data-ttu-id="4cbe6-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4cbe6-144">RELATED LINKS</span></span>
