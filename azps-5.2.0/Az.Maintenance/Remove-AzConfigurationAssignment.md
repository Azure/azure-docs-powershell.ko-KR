---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
ms.openlocfilehash: 137540ae71e097e98d390e2ab2efb2f6643928e1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330854"
---
# <span data-ttu-id="849d2-101">Remove-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="849d2-101">Remove-AzConfigurationAssignment</span></span>

## <span data-ttu-id="849d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="849d2-102">SYNOPSIS</span></span>
<span data-ttu-id="849d2-103">리소스에 대한 구성을 등록을 등록하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="849d2-103">Unregister configuration for resource.</span></span>

## <span data-ttu-id="849d2-104">구문</span><span class="sxs-lookup"><span data-stu-id="849d2-104">SYNTAX</span></span>

```
Remove-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="849d2-105">설명</span><span class="sxs-lookup"><span data-stu-id="849d2-105">DESCRIPTION</span></span>
<span data-ttu-id="849d2-106">리소스에 대한 구성을 등록을 등록하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="849d2-106">Unregister configuration for resource.</span></span>

## <span data-ttu-id="849d2-107">예제</span><span class="sxs-lookup"><span data-stu-id="849d2-107">EXAMPLES</span></span>

### <span data-ttu-id="849d2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="849d2-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute -ConfigurationAssignmentName $maintenanceConfigurationName

Remove-AzConfigurationAssignment operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="849d2-109">리소스에 대한 구성을 등록을 등록하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="849d2-109">Unregister configuration for resource.</span></span>

## <span data-ttu-id="849d2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="849d2-110">PARAMETERS</span></span>

### <span data-ttu-id="849d2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="849d2-111">-AsJob</span></span>
<span data-ttu-id="849d2-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="849d2-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="849d2-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="849d2-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="849d2-114">구성 할당 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="849d2-114">The configuration assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="849d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="849d2-115">-DefaultProfile</span></span>
<span data-ttu-id="849d2-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="849d2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="849d2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="849d2-117">-Force</span></span>
<span data-ttu-id="849d2-118">확인 없이 강제로 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="849d2-118">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="849d2-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="849d2-119">-PassThru</span></span>
<span data-ttu-id="849d2-120">제거 작업의 상태를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="849d2-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="849d2-121">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="849d2-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="849d2-122">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="849d2-122">-ProviderName</span></span>
<span data-ttu-id="849d2-123">리소스 공급자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="849d2-123">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="849d2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="849d2-124">-ResourceGroupName</span></span>
<span data-ttu-id="849d2-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="849d2-125">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="849d2-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="849d2-126">-ResourceName</span></span>
<span data-ttu-id="849d2-127">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="849d2-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="849d2-128">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="849d2-128">-ResourceParentName</span></span>
<span data-ttu-id="849d2-129">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="849d2-129">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="849d2-130">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="849d2-130">-ResourceParentType</span></span>
<span data-ttu-id="849d2-131">부모 리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="849d2-131">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="849d2-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="849d2-132">-ResourceType</span></span>
<span data-ttu-id="849d2-133">리소스 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="849d2-133">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="849d2-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="849d2-134">-Confirm</span></span>
<span data-ttu-id="849d2-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="849d2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="849d2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="849d2-136">-WhatIf</span></span>
<span data-ttu-id="849d2-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="849d2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="849d2-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="849d2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="849d2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="849d2-139">CommonParameters</span></span>
<span data-ttu-id="849d2-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="849d2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="849d2-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="849d2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="849d2-142">입력</span><span class="sxs-lookup"><span data-stu-id="849d2-142">INPUTS</span></span>

### <span data-ttu-id="849d2-143">System.String</span><span class="sxs-lookup"><span data-stu-id="849d2-143">System.String</span></span>

## <span data-ttu-id="849d2-144">출력</span><span class="sxs-lookup"><span data-stu-id="849d2-144">OUTPUTS</span></span>

### <span data-ttu-id="849d2-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="849d2-145">System.Boolean</span></span>

## <span data-ttu-id="849d2-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="849d2-146">NOTES</span></span>

## <span data-ttu-id="849d2-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="849d2-147">RELATED LINKS</span></span>
