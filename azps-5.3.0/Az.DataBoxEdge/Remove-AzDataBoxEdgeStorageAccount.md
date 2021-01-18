---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 1f8e20b826a477778de5325ff147cbd7ad28a9fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493583"
---
# <span data-ttu-id="035ff-101">Remove-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="035ff-101">Remove-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="035ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="035ff-102">SYNOPSIS</span></span>
<span data-ttu-id="035ff-103">디바이스에 대한 Edge Storage 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="035ff-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="035ff-104">구문</span><span class="sxs-lookup"><span data-stu-id="035ff-104">SYNTAX</span></span>

### <span data-ttu-id="035ff-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="035ff-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="035ff-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="035ff-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="035ff-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="035ff-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccount [-InputObject] <PSDataBoxEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="035ff-108">설명</span><span class="sxs-lookup"><span data-stu-id="035ff-108">DESCRIPTION</span></span>
<span data-ttu-id="035ff-109">**Remove-AzDataBoxEdgeStorageAccount** cmdlet은 Data Box Edge 디바이스에 대한 연결된 Edge Storage 계정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="035ff-109">The **Remove-AzDataBoxEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Data Box Edge device.</span></span> <span data-ttu-id="035ff-110">cmdlet에서 매개 변수로 제거할 Edge Storage 계정의 이름을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="035ff-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="035ff-111">예제</span><span class="sxs-lookup"><span data-stu-id="035ff-111">EXAMPLES</span></span>

### <span data-ttu-id="035ff-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="035ff-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="035ff-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="035ff-113">PARAMETERS</span></span>

### <span data-ttu-id="035ff-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="035ff-114">-AsJob</span></span>
<span data-ttu-id="035ff-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="035ff-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="035ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="035ff-116">-DefaultProfile</span></span>
<span data-ttu-id="035ff-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="035ff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="035ff-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="035ff-118">-DeviceName</span></span>
<span data-ttu-id="035ff-119">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="035ff-119">Device Name</span></span>

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

### <span data-ttu-id="035ff-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="035ff-120">-InputObject</span></span>
<span data-ttu-id="035ff-121">입력 개체</span><span class="sxs-lookup"><span data-stu-id="035ff-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="035ff-122">-Name</span><span class="sxs-lookup"><span data-stu-id="035ff-122">-Name</span></span>
<span data-ttu-id="035ff-123">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="035ff-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="035ff-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="035ff-124">-PassThru</span></span>
<span data-ttu-id="035ff-125">성공한 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="035ff-125">returns true if successful</span></span>

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

### <span data-ttu-id="035ff-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="035ff-126">-ResourceGroupName</span></span>
<span data-ttu-id="035ff-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="035ff-127">Resource Group Name</span></span>

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

### <span data-ttu-id="035ff-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="035ff-128">-ResourceId</span></span>
<span data-ttu-id="035ff-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="035ff-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="035ff-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="035ff-130">-Confirm</span></span>
<span data-ttu-id="035ff-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="035ff-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="035ff-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="035ff-132">-WhatIf</span></span>
<span data-ttu-id="035ff-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="035ff-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="035ff-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="035ff-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="035ff-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="035ff-135">CommonParameters</span></span>
<span data-ttu-id="035ff-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="035ff-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="035ff-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="035ff-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="035ff-138">입력</span><span class="sxs-lookup"><span data-stu-id="035ff-138">INPUTS</span></span>

### <span data-ttu-id="035ff-139">System.String</span><span class="sxs-lookup"><span data-stu-id="035ff-139">System.String</span></span>

### <span data-ttu-id="035ff-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="035ff-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="035ff-141">출력</span><span class="sxs-lookup"><span data-stu-id="035ff-141">OUTPUTS</span></span>

### <span data-ttu-id="035ff-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="035ff-142">System.Boolean</span></span>

## <span data-ttu-id="035ff-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="035ff-143">NOTES</span></span>

## <span data-ttu-id="035ff-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="035ff-144">RELATED LINKS</span></span>
