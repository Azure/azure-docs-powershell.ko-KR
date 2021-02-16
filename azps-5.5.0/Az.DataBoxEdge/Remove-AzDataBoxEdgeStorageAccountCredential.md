---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 00cfc136465cc250d068344158d66f98dc6e0704
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188657"
---
# <span data-ttu-id="2d4a1-101">Remove-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="2d4a1-101">Remove-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="2d4a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d4a1-102">SYNOPSIS</span></span>
<span data-ttu-id="2d4a1-103">디바이스에 대한 저장소 계정 자격 증명을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2d4a1-103">Removes a storage account credential for a device.</span></span>

## <span data-ttu-id="2d4a1-104">구문</span><span class="sxs-lookup"><span data-stu-id="2d4a1-104">SYNTAX</span></span>

### <span data-ttu-id="2d4a1-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="2d4a1-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d4a1-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d4a1-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d4a1-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d4a1-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageAccountCredential [-InputObject] <PSDataBoxEdgeStorageAccountCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d4a1-108">설명</span><span class="sxs-lookup"><span data-stu-id="2d4a1-108">DESCRIPTION</span></span>
<span data-ttu-id="2d4a1-109">**Remove-AzDataBoxEdgeStorageAccountCredential** cmdlet은 Data Box Edge 디바이스에 대한 저장소 계정 자격 증명을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2d4a1-109">The **Remove-AzDataBoxEdgeStorageAccountCredential** cmdlet removes the storage account credential for a Data Box Edge device.</span></span>

## <span data-ttu-id="2d4a1-110">예제</span><span class="sxs-lookup"><span data-stu-id="2d4a1-110">EXAMPLES</span></span>

### <span data-ttu-id="2d4a1-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2d4a1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageAccountCredential ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAccountCredentialName
```

## <span data-ttu-id="2d4a1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d4a1-112">PARAMETERS</span></span>

### <span data-ttu-id="2d4a1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d4a1-113">-AsJob</span></span>
<span data-ttu-id="2d4a1-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2d4a1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d4a1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d4a1-115">-DefaultProfile</span></span>
<span data-ttu-id="2d4a1-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2d4a1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d4a1-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="2d4a1-117">-DeviceName</span></span>
<span data-ttu-id="2d4a1-118">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="2d4a1-118">Device Name</span></span>

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

### <span data-ttu-id="2d4a1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d4a1-119">-InputObject</span></span>
<span data-ttu-id="2d4a1-120">입력 개체</span><span class="sxs-lookup"><span data-stu-id="2d4a1-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d4a1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2d4a1-121">-Name</span></span>
<span data-ttu-id="2d4a1-122">사용할 저장소 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="2d4a1-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="2d4a1-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d4a1-123">-PassThru</span></span>
<span data-ttu-id="2d4a1-124">성공한 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="2d4a1-124">returns true if successful</span></span>

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

### <span data-ttu-id="2d4a1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d4a1-125">-ResourceGroupName</span></span>
<span data-ttu-id="2d4a1-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2d4a1-126">Resource Group Name</span></span>

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

### <span data-ttu-id="2d4a1-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d4a1-127">-ResourceId</span></span>
<span data-ttu-id="2d4a1-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d4a1-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="2d4a1-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d4a1-129">-Confirm</span></span>
<span data-ttu-id="2d4a1-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2d4a1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d4a1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d4a1-131">-WhatIf</span></span>
<span data-ttu-id="2d4a1-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2d4a1-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d4a1-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2d4a1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d4a1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d4a1-134">CommonParameters</span></span>
<span data-ttu-id="2d4a1-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2d4a1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d4a1-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2d4a1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d4a1-137">입력</span><span class="sxs-lookup"><span data-stu-id="2d4a1-137">INPUTS</span></span>

### <span data-ttu-id="2d4a1-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2d4a1-138">System.String</span></span>

### <span data-ttu-id="2d4a1-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="2d4a1-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="2d4a1-140">출력</span><span class="sxs-lookup"><span data-stu-id="2d4a1-140">OUTPUTS</span></span>

### <span data-ttu-id="2d4a1-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2d4a1-141">System.Boolean</span></span>

## <span data-ttu-id="2d4a1-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2d4a1-142">NOTES</span></span>

## <span data-ttu-id="2d4a1-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2d4a1-143">RELATED LINKS</span></span>
