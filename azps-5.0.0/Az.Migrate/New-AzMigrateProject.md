---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
ms.openlocfilehash: 32c4799f574e94eecee1f7ebf810c2f27bc5eccf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218864"
---
# <span data-ttu-id="01ffd-101">New-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="01ffd-101">New-AzMigrateProject</span></span>

## <span data-ttu-id="01ffd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01ffd-102">SYNOPSIS</span></span>
<span data-ttu-id="01ffd-103">새 마이그레이션 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01ffd-103">Creates a new Migrate project.</span></span>

## <span data-ttu-id="01ffd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="01ffd-104">SYNTAX</span></span>

```
New-AzMigrateProject -Location <String> -Name <String> -ResourceGroupName <String> [-ETag <String>]
 [-Property <IMigrateProjectProperties>] [-SubscriptionId <String>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="01ffd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="01ffd-105">DESCRIPTION</span></span>
<span data-ttu-id="01ffd-106">새 마이그레이션 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01ffd-106">Creates a new Migrate project.</span></span>

## <span data-ttu-id="01ffd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="01ffd-107">EXAMPLES</span></span>

### <span data-ttu-id="01ffd-108">예제 1: 만들기 (기본값)</span><span class="sxs-lookup"><span data-stu-id="01ffd-108">Example 1: Create (Default)</span></span>
```powershell
PS C:\> New-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName kuchaturimpkocrg1 -Name kuchaturimpkocrg1pwshp14 -Location "centralus"

ETag Location  Name                     Type
---- --------  ----                     ----
     centralus kuchaturimpkocrg1pwshp14 Microsoft.Migrate/MigrateProjects

```

<span data-ttu-id="01ffd-109">새 마이그레이션 프로젝트를 만드는 메서드입니다.</span><span class="sxs-lookup"><span data-stu-id="01ffd-109">Method to create a new migrate project.</span></span>

## <span data-ttu-id="01ffd-110">변수</span><span class="sxs-lookup"><span data-stu-id="01ffd-110">PARAMETERS</span></span>

### <span data-ttu-id="01ffd-111">-ETag</span><span class="sxs-lookup"><span data-stu-id="01ffd-111">-ETag</span></span>
<span data-ttu-id="01ffd-112">VMware 컴퓨터 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ffd-112">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="01ffd-113">-위치</span><span class="sxs-lookup"><span data-stu-id="01ffd-113">-Location</span></span>
<span data-ttu-id="01ffd-114">VMware 컴퓨터 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ffd-114">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="01ffd-115">-이름</span><span class="sxs-lookup"><span data-stu-id="01ffd-115">-Name</span></span>
<span data-ttu-id="01ffd-116">마이그레이션 프로젝트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ffd-116">Specifies the migrate project name.</span></span>

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

### <span data-ttu-id="01ffd-117">-속성</span><span class="sxs-lookup"><span data-stu-id="01ffd-117">-Property</span></span>
<span data-ttu-id="01ffd-118">프로젝트 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ffd-118">Specifies the project properties.</span></span>
<span data-ttu-id="01ffd-119">생성 하려면 속성 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01ffd-119">To construct, see NOTES section for PROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="01ffd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01ffd-120">-ResourceGroupName</span></span>
<span data-ttu-id="01ffd-121">리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ffd-121">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="01ffd-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="01ffd-122">-SubscriptionId</span></span>
<span data-ttu-id="01ffd-123">구독 id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ffd-123">Specifies the subscription id.</span></span>

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

### <span data-ttu-id="01ffd-124">-확인</span><span class="sxs-lookup"><span data-stu-id="01ffd-124">-Confirm</span></span>
<span data-ttu-id="01ffd-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ffd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01ffd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01ffd-126">-WhatIf</span></span>
<span data-ttu-id="01ffd-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="01ffd-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01ffd-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01ffd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01ffd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01ffd-129">CommonParameters</span></span>
<span data-ttu-id="01ffd-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ffd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01ffd-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="01ffd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01ffd-132">입력</span><span class="sxs-lookup"><span data-stu-id="01ffd-132">INPUTS</span></span>

## <span data-ttu-id="01ffd-133">출력</span><span class="sxs-lookup"><span data-stu-id="01ffd-133">OUTPUTS</span></span>

## <span data-ttu-id="01ffd-134">상속자</span><span class="sxs-lookup"><span data-stu-id="01ffd-134">NOTES</span></span>

<span data-ttu-id="01ffd-135">별칭과</span><span class="sxs-lookup"><span data-stu-id="01ffd-135">ALIASES</span></span>

<span data-ttu-id="01ffd-136">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="01ffd-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="01ffd-137">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ffd-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="01ffd-138">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="01ffd-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="01ffd-139">속성 <IMigrateProjectProperties> : 프로젝트 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ffd-139">PROPERTY <IMigrateProjectProperties>: Specifies the project properties.</span></span>
  - <span data-ttu-id="01ffd-140">`[ProvisioningState <ProvisioningState?>]`: 마이그레이션 프로젝트의 상태를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ffd-140">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of the migrate project.</span></span>
  - <span data-ttu-id="01ffd-141">`[RegisteredTool <String[]>]`: 마이그레이션 프로젝트에 등록 된 도구 목록을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01ffd-141">`[RegisteredTool <String[]>]`: Gets or sets the list of tools registered with the migrate project.</span></span>

## <span data-ttu-id="01ffd-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01ffd-142">RELATED LINKS</span></span>

