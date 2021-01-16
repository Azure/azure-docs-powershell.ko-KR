---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
ms.openlocfilehash: ec8703b5b107758a331407d431f871acf249885d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350001"
---
# <span data-ttu-id="9eaf2-101">Remove-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="9eaf2-101">Remove-AzStackEdgeUser</span></span>

## <span data-ttu-id="9eaf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9eaf2-102">SYNOPSIS</span></span>
<span data-ttu-id="9eaf2-103">디바이스에서 사용자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9eaf2-103">Removes a user on a device.</span></span>

## <span data-ttu-id="9eaf2-104">구문</span><span class="sxs-lookup"><span data-stu-id="9eaf2-104">SYNTAX</span></span>

### <span data-ttu-id="9eaf2-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9eaf2-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9eaf2-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9eaf2-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9eaf2-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9eaf2-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeUser [-InputObject] <PSStackEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9eaf2-108">설명</span><span class="sxs-lookup"><span data-stu-id="9eaf2-108">DESCRIPTION</span></span>
<span data-ttu-id="9eaf2-109">**Remove-AzStackEdgeUser** cmdlet은 Stack Edge 디바이스에서 사용자를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9eaf2-109">The **Remove-AzStackEdgeUser** cmdlet removes a user on the Stack Edge device.</span></span> <span data-ttu-id="9eaf2-110">형식의 사용자만 만들 `Share` 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9eaf2-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="9eaf2-111">예제</span><span class="sxs-lookup"><span data-stu-id="9eaf2-111">EXAMPLES</span></span>

### <span data-ttu-id="9eaf2-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="9eaf2-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="9eaf2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9eaf2-113">PARAMETERS</span></span>

### <span data-ttu-id="9eaf2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9eaf2-114">-AsJob</span></span>
<span data-ttu-id="9eaf2-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9eaf2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9eaf2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eaf2-116">-DefaultProfile</span></span>
<span data-ttu-id="9eaf2-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9eaf2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9eaf2-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9eaf2-118">-DeviceName</span></span>
<span data-ttu-id="9eaf2-119">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="9eaf2-119">Device Name</span></span>

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

### <span data-ttu-id="9eaf2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9eaf2-120">-InputObject</span></span>
<span data-ttu-id="9eaf2-121">입력 개체</span><span class="sxs-lookup"><span data-stu-id="9eaf2-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: User

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9eaf2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9eaf2-122">-Name</span></span>
<span data-ttu-id="9eaf2-123">사용자 이름</span><span class="sxs-lookup"><span data-stu-id="9eaf2-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9eaf2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9eaf2-124">-PassThru</span></span>
<span data-ttu-id="9eaf2-125">성공한 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9eaf2-125">returns true if successful</span></span>

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

### <span data-ttu-id="9eaf2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eaf2-126">-ResourceGroupName</span></span>
<span data-ttu-id="9eaf2-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9eaf2-127">Resource Group Name</span></span>

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

### <span data-ttu-id="9eaf2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9eaf2-128">-ResourceId</span></span>
<span data-ttu-id="9eaf2-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="9eaf2-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="9eaf2-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9eaf2-130">-Confirm</span></span>
<span data-ttu-id="9eaf2-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9eaf2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9eaf2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9eaf2-132">-WhatIf</span></span>
<span data-ttu-id="9eaf2-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9eaf2-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9eaf2-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9eaf2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9eaf2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eaf2-135">CommonParameters</span></span>
<span data-ttu-id="9eaf2-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9eaf2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eaf2-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9eaf2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eaf2-138">입력</span><span class="sxs-lookup"><span data-stu-id="9eaf2-138">INPUTS</span></span>

### <span data-ttu-id="9eaf2-139">System.String</span><span class="sxs-lookup"><span data-stu-id="9eaf2-139">System.String</span></span>

### <span data-ttu-id="9eaf2-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="9eaf2-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="9eaf2-141">출력</span><span class="sxs-lookup"><span data-stu-id="9eaf2-141">OUTPUTS</span></span>

### <span data-ttu-id="9eaf2-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="9eaf2-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="9eaf2-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9eaf2-143">NOTES</span></span>

## <span data-ttu-id="9eaf2-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9eaf2-144">RELATED LINKS</span></span>