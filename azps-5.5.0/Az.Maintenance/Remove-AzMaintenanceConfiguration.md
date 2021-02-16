---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzMaintenanceConfiguration.md
ms.openlocfilehash: 5f212240eaee9ebc46fd7d5cde2ee2e2ec311ac2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185137"
---
# <span data-ttu-id="9a77a-101">Remove-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a77a-101">Remove-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="9a77a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a77a-102">SYNOPSIS</span></span>
<span data-ttu-id="9a77a-103">구성 레코드 삭제</span><span class="sxs-lookup"><span data-stu-id="9a77a-103">Delete Configuration record</span></span>

## <span data-ttu-id="9a77a-104">구문</span><span class="sxs-lookup"><span data-stu-id="9a77a-104">SYNTAX</span></span>

```
Remove-AzMaintenanceConfiguration [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a77a-105">설명</span><span class="sxs-lookup"><span data-stu-id="9a77a-105">DESCRIPTION</span></span>
<span data-ttu-id="9a77a-106">유지 관리 구성 레코드 삭제</span><span class="sxs-lookup"><span data-stu-id="9a77a-106">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="9a77a-107">예제</span><span class="sxs-lookup"><span data-stu-id="9a77a-107">EXAMPLES</span></span>

### <span data-ttu-id="9a77a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9a77a-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus

Remove-AzMaintenanceConfiguration operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="9a77a-109">유지 관리 구성 레코드 삭제</span><span class="sxs-lookup"><span data-stu-id="9a77a-109">Delete Maintenance Configuration record</span></span>

## <span data-ttu-id="9a77a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a77a-110">PARAMETERS</span></span>

### <span data-ttu-id="9a77a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a77a-111">-AsJob</span></span>
<span data-ttu-id="9a77a-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9a77a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a77a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a77a-113">-DefaultProfile</span></span>
<span data-ttu-id="9a77a-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a77a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a77a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9a77a-115">-Force</span></span>
<span data-ttu-id="9a77a-116">확인 없이 강제로 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9a77a-116">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="9a77a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9a77a-117">-Name</span></span>
<span data-ttu-id="9a77a-118">유지 관리 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a77a-118">The maintenance configuration Name.</span></span>

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

### <span data-ttu-id="9a77a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a77a-119">-PassThru</span></span>
<span data-ttu-id="9a77a-120">제거 작업의 상태를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9a77a-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="9a77a-121">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a77a-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9a77a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a77a-122">-ResourceGroupName</span></span>
<span data-ttu-id="9a77a-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a77a-123">The resource Group Name.</span></span>

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

### <span data-ttu-id="9a77a-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a77a-124">-Confirm</span></span>
<span data-ttu-id="9a77a-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a77a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a77a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a77a-126">-WhatIf</span></span>
<span data-ttu-id="9a77a-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9a77a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a77a-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a77a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a77a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a77a-129">CommonParameters</span></span>
<span data-ttu-id="9a77a-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9a77a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a77a-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9a77a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a77a-132">입력</span><span class="sxs-lookup"><span data-stu-id="9a77a-132">INPUTS</span></span>

### <span data-ttu-id="9a77a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="9a77a-133">System.String</span></span>

## <span data-ttu-id="9a77a-134">출력</span><span class="sxs-lookup"><span data-stu-id="9a77a-134">OUTPUTS</span></span>

### <span data-ttu-id="9a77a-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9a77a-135">System.Boolean</span></span>

## <span data-ttu-id="9a77a-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9a77a-136">NOTES</span></span>

## <span data-ttu-id="9a77a-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a77a-137">RELATED LINKS</span></span>
