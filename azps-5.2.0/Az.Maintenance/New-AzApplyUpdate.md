---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzApplyUpdate.md
ms.openlocfilehash: 05403ce85b80238aeee8749322bdd94d28be68da
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340821"
---
# <span data-ttu-id="7a842-101">New-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="7a842-101">New-AzApplyUpdate</span></span>

## <span data-ttu-id="7a842-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a842-102">SYNOPSIS</span></span>
<span data-ttu-id="7a842-103">리소스에 유지 관리 업데이트 적용</span><span class="sxs-lookup"><span data-stu-id="7a842-103">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="7a842-104">구문</span><span class="sxs-lookup"><span data-stu-id="7a842-104">SYNTAX</span></span>

```
New-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a842-105">설명</span><span class="sxs-lookup"><span data-stu-id="7a842-105">DESCRIPTION</span></span>
<span data-ttu-id="7a842-106">리소스에 유지 관리 업데이트 적용</span><span class="sxs-lookup"><span data-stu-id="7a842-106">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="7a842-107">예제</span><span class="sxs-lookup"><span data-stu-id="7a842-107">EXAMPLES</span></span>

### <span data-ttu-id="7a842-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7a842-108">Example 1</span></span>
```powershell
PS C:\> New-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/cbd4c97d-2011-4fa3-9df1-525f97e74eac
Name           : cbd4c97d-2011-4fa3-9df1-525f97e74eac
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="7a842-109">리소스에 유지 관리 업데이트 적용</span><span class="sxs-lookup"><span data-stu-id="7a842-109">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="7a842-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a842-110">PARAMETERS</span></span>

### <span data-ttu-id="7a842-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a842-111">-AsJob</span></span>
<span data-ttu-id="7a842-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7a842-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a842-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a842-113">-DefaultProfile</span></span>
<span data-ttu-id="7a842-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a842-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a842-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="7a842-115">-ProviderName</span></span>
<span data-ttu-id="7a842-116">리소스 공급자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a842-116">The resource provider Name.</span></span>

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

### <span data-ttu-id="7a842-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a842-117">-ResourceGroupName</span></span>
<span data-ttu-id="7a842-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a842-118">The resource Group Name.</span></span>

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

### <span data-ttu-id="7a842-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7a842-119">-ResourceName</span></span>
<span data-ttu-id="7a842-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a842-120">The resource name.</span></span>

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

### <span data-ttu-id="7a842-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="7a842-121">-ResourceParentName</span></span>
<span data-ttu-id="7a842-122">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a842-122">The parent resource name.</span></span>

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

### <span data-ttu-id="7a842-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="7a842-123">-ResourceParentType</span></span>
<span data-ttu-id="7a842-124">부모 리소스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="7a842-124">The parent resource type.</span></span>

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

### <span data-ttu-id="7a842-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="7a842-125">-ResourceType</span></span>
<span data-ttu-id="7a842-126">리소스 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="7a842-126">The resource type.</span></span>

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

### <span data-ttu-id="7a842-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a842-127">-Confirm</span></span>
<span data-ttu-id="7a842-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a842-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a842-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a842-129">-WhatIf</span></span>
<span data-ttu-id="7a842-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7a842-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a842-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a842-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a842-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a842-132">CommonParameters</span></span>
<span data-ttu-id="7a842-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7a842-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a842-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7a842-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a842-135">입력</span><span class="sxs-lookup"><span data-stu-id="7a842-135">INPUTS</span></span>

### <span data-ttu-id="7a842-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7a842-136">System.String</span></span>

## <span data-ttu-id="7a842-137">출력</span><span class="sxs-lookup"><span data-stu-id="7a842-137">OUTPUTS</span></span>

### <span data-ttu-id="7a842-138">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="7a842-138">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="7a842-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7a842-139">NOTES</span></span>

## <span data-ttu-id="7a842-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a842-140">RELATED LINKS</span></span>
