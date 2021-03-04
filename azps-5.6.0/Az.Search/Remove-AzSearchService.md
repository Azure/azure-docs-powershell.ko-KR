---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/remove-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchService.md
ms.openlocfilehash: 0e1011fb8e2aaec7a77f735c961fa6ec2ede9dd7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007659"
---
# <span data-ttu-id="4724d-101">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="4724d-101">Remove-AzSearchService</span></span>

## <span data-ttu-id="4724d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4724d-102">SYNOPSIS</span></span>
<span data-ttu-id="4724d-103">Azure Cognitive Search 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4724d-103">Remove an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="4724d-104">구문</span><span class="sxs-lookup"><span data-stu-id="4724d-104">SYNTAX</span></span>

### <span data-ttu-id="4724d-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4724d-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4724d-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4724d-106">InputObjectParameterSet</span></span>
```
Remove-AzSearchService [-InputObject] <PSSearchService> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4724d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4724d-107">ResourceIdParameterSet</span></span>
```
Remove-AzSearchService [-ResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4724d-108">설명</span><span class="sxs-lookup"><span data-stu-id="4724d-108">DESCRIPTION</span></span>
<span data-ttu-id="4724d-109">**Remove-AzSearchService** cmdlet은 지정된 매개 변수가 있는 Azure Cognitive Search 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4724d-109">The **Remove-AzSearchService** cmdlet removes an Azure Cognitive Search service with specified parameters.</span></span>

## <span data-ttu-id="4724d-110">예제</span><span class="sxs-lookup"><span data-stu-id="4724d-110">EXAMPLES</span></span>

### <span data-ttu-id="4724d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4724d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01"

Confirm
Are you sure you want to remove Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="4724d-112">이 예제에서는 Azure Cognitive Search 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4724d-112">The example removes an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="4724d-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4724d-113">PARAMETERS</span></span>

### <span data-ttu-id="4724d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4724d-114">-DefaultProfile</span></span>
<span data-ttu-id="4724d-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4724d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4724d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4724d-116">-Force</span></span>
<span data-ttu-id="4724d-117">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4724d-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4724d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4724d-118">-InputObject</span></span>
<span data-ttu-id="4724d-119">Azure Cognitive Search Service 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4724d-119">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4724d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4724d-120">-Name</span></span>
<span data-ttu-id="4724d-121">Azure Cognitive Search Service 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4724d-121">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4724d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4724d-122">-PassThru</span></span>
<span data-ttu-id="4724d-123">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4724d-123">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="4724d-124">이 스위치가 지정되어 있는 경우 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4724d-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4724d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4724d-125">-ResourceGroupName</span></span>
<span data-ttu-id="4724d-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4724d-126">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4724d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4724d-127">-ResourceId</span></span>
<span data-ttu-id="4724d-128">Azure Cognitive Search 서비스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4724d-128">Azure Cognitive Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4724d-129">-확인</span><span class="sxs-lookup"><span data-stu-id="4724d-129">-Confirm</span></span>
<span data-ttu-id="4724d-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4724d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4724d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4724d-131">-WhatIf</span></span>
<span data-ttu-id="4724d-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4724d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4724d-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4724d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4724d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4724d-134">CommonParameters</span></span>
<span data-ttu-id="4724d-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4724d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4724d-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4724d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4724d-137">입력</span><span class="sxs-lookup"><span data-stu-id="4724d-137">INPUTS</span></span>

### <span data-ttu-id="4724d-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="4724d-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="4724d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4724d-139">System.String</span></span>

## <span data-ttu-id="4724d-140">출력</span><span class="sxs-lookup"><span data-stu-id="4724d-140">OUTPUTS</span></span>

### <span data-ttu-id="4724d-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4724d-141">System.Boolean</span></span>

## <span data-ttu-id="4724d-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4724d-142">NOTES</span></span>

## <span data-ttu-id="4724d-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4724d-143">RELATED LINKS</span></span>

[<span data-ttu-id="4724d-144">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="4724d-144">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="4724d-145">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="4724d-145">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="4724d-146">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="4724d-146">Set-AzSearchService</span></span>](./Set-AzSearchService.md)
