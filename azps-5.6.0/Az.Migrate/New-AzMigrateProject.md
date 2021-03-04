---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
ms.openlocfilehash: 8b3a14c9e8416c1ffc9809d09d664b7809f53a1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982688"
---
# <span data-ttu-id="998e8-101">New-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="998e8-101">New-AzMigrateProject</span></span>

## <span data-ttu-id="998e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="998e8-102">SYNOPSIS</span></span>
<span data-ttu-id="998e8-103">새 마이그레이션 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="998e8-103">Creates a new Migrate project.</span></span>

## <span data-ttu-id="998e8-104">구문</span><span class="sxs-lookup"><span data-stu-id="998e8-104">SYNTAX</span></span>

```
New-AzMigrateProject -Location <String> -Name <String> -ResourceGroupName <String> [-ETag <String>]
 [-Property <IMigrateProjectProperties>] [-SubscriptionId <String>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="998e8-105">설명</span><span class="sxs-lookup"><span data-stu-id="998e8-105">DESCRIPTION</span></span>
<span data-ttu-id="998e8-106">새 마이그레이션 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="998e8-106">Creates a new Migrate project.</span></span>

## <span data-ttu-id="998e8-107">예제</span><span class="sxs-lookup"><span data-stu-id="998e8-107">EXAMPLES</span></span>

### <span data-ttu-id="998e8-108">예제 1: 만들기(기본값)</span><span class="sxs-lookup"><span data-stu-id="998e8-108">Example 1: Create (Default)</span></span>
```powershell
PS C:\> New-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName kuchaturimpkocrg1 -Name kuchaturimpkocrg1pwshp14 -Location "centralus"

ETag Location  Name                     Type
---- --------  ----                     ----
     centralus kuchaturimpkocrg1pwshp14 Microsoft.Migrate/MigrateProjects

```

<span data-ttu-id="998e8-109">새 마이그레이션 프로젝트를 만드는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="998e8-109">Method to create a new migrate project.</span></span>

## <span data-ttu-id="998e8-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="998e8-110">PARAMETERS</span></span>

### <span data-ttu-id="998e8-111">-ETag</span><span class="sxs-lookup"><span data-stu-id="998e8-111">-ETag</span></span>
<span data-ttu-id="998e8-112">VMware 컴퓨터 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="998e8-112">Specifies the VMware machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="998e8-113">-Location</span><span class="sxs-lookup"><span data-stu-id="998e8-113">-Location</span></span>
<span data-ttu-id="998e8-114">VMware 컴퓨터 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="998e8-114">Specifies the VMware machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="998e8-115">-Name</span><span class="sxs-lookup"><span data-stu-id="998e8-115">-Name</span></span>
<span data-ttu-id="998e8-116">마이그레이션 프로젝트 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="998e8-116">Specifies the migrate project name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="998e8-117">-속성</span><span class="sxs-lookup"><span data-stu-id="998e8-117">-Property</span></span>
<span data-ttu-id="998e8-118">프로젝트 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="998e8-118">Specifies the project properties.</span></span>
<span data-ttu-id="998e8-119">생성을 위해 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="998e8-119">To construct, see NOTES section for PROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProjectProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="998e8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="998e8-120">-ResourceGroupName</span></span>
<span data-ttu-id="998e8-121">리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="998e8-121">Specifies the resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="998e8-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="998e8-122">-SubscriptionId</span></span>
<span data-ttu-id="998e8-123">구독 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="998e8-123">Specifies the subscription id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="998e8-124">-확인</span><span class="sxs-lookup"><span data-stu-id="998e8-124">-Confirm</span></span>
<span data-ttu-id="998e8-125">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="998e8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="998e8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="998e8-126">-WhatIf</span></span>
<span data-ttu-id="998e8-127">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="998e8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="998e8-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="998e8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="998e8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="998e8-129">CommonParameters</span></span>
<span data-ttu-id="998e8-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="998e8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="998e8-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="998e8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="998e8-132">입력</span><span class="sxs-lookup"><span data-stu-id="998e8-132">INPUTS</span></span>

## <span data-ttu-id="998e8-133">출력</span><span class="sxs-lookup"><span data-stu-id="998e8-133">OUTPUTS</span></span>

## <span data-ttu-id="998e8-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="998e8-134">NOTES</span></span>

<span data-ttu-id="998e8-135">별칭</span><span class="sxs-lookup"><span data-stu-id="998e8-135">ALIASES</span></span>

<span data-ttu-id="998e8-136">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="998e8-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="998e8-137">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="998e8-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="998e8-138">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="998e8-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="998e8-139">속성 <IMigrateProjectProperties> : 프로젝트 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="998e8-139">PROPERTY <IMigrateProjectProperties>: Specifies the project properties.</span></span>
  - <span data-ttu-id="998e8-140">`[ProvisioningState <ProvisioningState?>]`: 마이그레이션 프로젝트의 프로비전 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="998e8-140">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of the migrate project.</span></span>
  - <span data-ttu-id="998e8-141">`[RegisteredTool <String[]>]`: 마이그레이션 프로젝트에 등록된 도구 목록을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="998e8-141">`[RegisteredTool <String[]>]`: Gets or sets the list of tools registered with the migrate project.</span></span>

## <span data-ttu-id="998e8-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="998e8-142">RELATED LINKS</span></span>

