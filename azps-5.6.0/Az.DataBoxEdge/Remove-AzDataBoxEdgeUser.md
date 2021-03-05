---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
ms.openlocfilehash: 8c977c61f332ccdc927dd3f0e070d635e6095acf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983243"
---
# <span data-ttu-id="a3c03-101">Remove-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="a3c03-101">Remove-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="a3c03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3c03-102">SYNOPSIS</span></span>
<span data-ttu-id="a3c03-103">디바이스에서 사용자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c03-103">Removes a user on a device.</span></span>

## <span data-ttu-id="a3c03-104">구문</span><span class="sxs-lookup"><span data-stu-id="a3c03-104">SYNTAX</span></span>

### <span data-ttu-id="a3c03-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a3c03-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3c03-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3c03-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3c03-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3c03-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-InputObject] <PSDataBoxEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3c03-108">설명</span><span class="sxs-lookup"><span data-stu-id="a3c03-108">DESCRIPTION</span></span>
<span data-ttu-id="a3c03-109">**Remove-AzDataBoxEdgeUser** cmdlet은 Data Box Edge 디바이스에서 사용자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c03-109">The **Remove-AzDataBoxEdgeUser** cmdlet removes a user on the Data Box Edge device.</span></span> <span data-ttu-id="a3c03-110">형식의 사용자만 만들 `Share` 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c03-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="a3c03-111">예제</span><span class="sxs-lookup"><span data-stu-id="a3c03-111">EXAMPLES</span></span>

### <span data-ttu-id="a3c03-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="a3c03-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="a3c03-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a3c03-113">PARAMETERS</span></span>

### <span data-ttu-id="a3c03-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3c03-114">-AsJob</span></span>
<span data-ttu-id="a3c03-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a3c03-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3c03-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3c03-116">-DefaultProfile</span></span>
<span data-ttu-id="a3c03-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a3c03-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3c03-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a3c03-118">-DeviceName</span></span>
<span data-ttu-id="a3c03-119">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="a3c03-119">Device Name</span></span>

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

### <span data-ttu-id="a3c03-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3c03-120">-InputObject</span></span>
<span data-ttu-id="a3c03-121">입력 개체</span><span class="sxs-lookup"><span data-stu-id="a3c03-121">Input Object</span></span>

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

### <span data-ttu-id="a3c03-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a3c03-122">-Name</span></span>
<span data-ttu-id="a3c03-123">사용자 이름</span><span class="sxs-lookup"><span data-stu-id="a3c03-123">Username</span></span>

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

### <span data-ttu-id="a3c03-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3c03-124">-PassThru</span></span>
<span data-ttu-id="a3c03-125">성공한 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c03-125">returns true if successful</span></span>

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

### <span data-ttu-id="a3c03-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3c03-126">-ResourceGroupName</span></span>
<span data-ttu-id="a3c03-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="a3c03-127">Resource Group Name</span></span>

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

### <span data-ttu-id="a3c03-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3c03-128">-ResourceId</span></span>
<span data-ttu-id="a3c03-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3c03-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="a3c03-130">-확인</span><span class="sxs-lookup"><span data-stu-id="a3c03-130">-Confirm</span></span>
<span data-ttu-id="a3c03-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3c03-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3c03-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3c03-132">-WhatIf</span></span>
<span data-ttu-id="a3c03-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a3c03-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3c03-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a3c03-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3c03-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3c03-135">CommonParameters</span></span>
<span data-ttu-id="a3c03-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a3c03-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3c03-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3c03-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3c03-138">입력</span><span class="sxs-lookup"><span data-stu-id="a3c03-138">INPUTS</span></span>

### <span data-ttu-id="a3c03-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a3c03-139">System.String</span></span>

### <span data-ttu-id="a3c03-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="a3c03-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="a3c03-141">출력</span><span class="sxs-lookup"><span data-stu-id="a3c03-141">OUTPUTS</span></span>

### <span data-ttu-id="a3c03-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="a3c03-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="a3c03-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a3c03-143">NOTES</span></span>

## <span data-ttu-id="a3c03-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3c03-144">RELATED LINKS</span></span>
