---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/initialize-azmigratereplicationinfrastructure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Initialize-AzMigrateReplicationInfrastructure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Initialize-AzMigrateReplicationInfrastructure.md
ms.openlocfilehash: 27206ac1c4e256efcd4093c8cdc9647b6059b3ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982784"
---
# <span data-ttu-id="5abd3-101">Initialize-AzMigrateReplicationInfrastructure</span><span class="sxs-lookup"><span data-stu-id="5abd3-101">Initialize-AzMigrateReplicationInfrastructure</span></span>

## <span data-ttu-id="5abd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5abd3-102">SYNOPSIS</span></span>
<span data-ttu-id="5abd3-103">마이그레이션 프로젝트에 대한 인프라를 초기화합니다.</span><span class="sxs-lookup"><span data-stu-id="5abd3-103">Initialises the infrastructure for the migrate project.</span></span>

## <span data-ttu-id="5abd3-104">구문</span><span class="sxs-lookup"><span data-stu-id="5abd3-104">SYNTAX</span></span>

```
Initialize-AzMigrateReplicationInfrastructure -ProjectName <String> -ResourceGroupName <String>
 -Scenario <String> -TargetRegion <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5abd3-105">설명</span><span class="sxs-lookup"><span data-stu-id="5abd3-105">DESCRIPTION</span></span>
<span data-ttu-id="5abd3-106">Initialize-AzMigrateReplicationInfrastructure cmdlet은 마이그레이션 프로젝트에 대한 인프라를 초기화합니다.</span><span class="sxs-lookup"><span data-stu-id="5abd3-106">The Initialize-AzMigrateReplicationInfrastructure cmdlet initialises the infrastructure for the migrate project.</span></span>

## <span data-ttu-id="5abd3-107">예제</span><span class="sxs-lookup"><span data-stu-id="5abd3-107">EXAMPLES</span></span>

### <span data-ttu-id="5abd3-108">예제 1: 마이그레이션 프로젝트에 대한 인프라를 초기화합니다.</span><span class="sxs-lookup"><span data-stu-id="5abd3-108">Example 1: Initialises the infrastructure for the migrate project.</span></span>
```powershell
PS C:\> Initialize-AzMigrateReplicationInfrastructure.ps1 -ResourceGroupName TestRG  -ProjectName TestProject -Vmwareagentless -TargetRegion centralus

True
```

<span data-ttu-id="5abd3-109">마이그레이션 프로젝트에 대한 인프라를 초기화합니다.</span><span class="sxs-lookup"><span data-stu-id="5abd3-109">Initialises the infrastructure for the migrate project.</span></span>

## <span data-ttu-id="5abd3-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5abd3-110">PARAMETERS</span></span>

### <span data-ttu-id="5abd3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5abd3-111">-DefaultProfile</span></span>
<span data-ttu-id="5abd3-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5abd3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5abd3-113">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="5abd3-113">-ProjectName</span></span>
<span data-ttu-id="5abd3-114">서버 마이그레이션에 사용할 Azure Migrate 프로젝트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5abd3-114">Specifies the name of the Azure Migrate project to be used for server migration.</span></span>

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

### <span data-ttu-id="5abd3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5abd3-115">-ResourceGroupName</span></span>
<span data-ttu-id="5abd3-116">현재 구독에서 Azure Migrate 프로젝트의 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5abd3-116">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

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

### <span data-ttu-id="5abd3-117">-시나리오</span><span class="sxs-lookup"><span data-stu-id="5abd3-117">-Scenario</span></span>
<span data-ttu-id="5abd3-118">복제 인프라를 초기화해야 하는 서버 마이그레이션 시나리오를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5abd3-118">Specifies the server migration scenario for which the replication infrastructure needs to be initialized.</span></span>

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

### <span data-ttu-id="5abd3-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5abd3-119">-SubscriptionId</span></span>
<span data-ttu-id="5abd3-120">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5abd3-120">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="5abd3-121">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="5abd3-121">-TargetRegion</span></span>
<span data-ttu-id="5abd3-122">서버 마이그레이션에 대한 대상 Azure 지역을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5abd3-122">Specifies the target Azure region for server migrations.</span></span>

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

### <span data-ttu-id="5abd3-123">-확인</span><span class="sxs-lookup"><span data-stu-id="5abd3-123">-Confirm</span></span>
<span data-ttu-id="5abd3-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5abd3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5abd3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5abd3-125">-WhatIf</span></span>
<span data-ttu-id="5abd3-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5abd3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5abd3-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5abd3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5abd3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5abd3-128">CommonParameters</span></span>
<span data-ttu-id="5abd3-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5abd3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5abd3-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5abd3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5abd3-131">입력</span><span class="sxs-lookup"><span data-stu-id="5abd3-131">INPUTS</span></span>

## <span data-ttu-id="5abd3-132">출력</span><span class="sxs-lookup"><span data-stu-id="5abd3-132">OUTPUTS</span></span>

### <span data-ttu-id="5abd3-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5abd3-133">System.Boolean</span></span>

## <span data-ttu-id="5abd3-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5abd3-134">NOTES</span></span>

<span data-ttu-id="5abd3-135">별칭</span><span class="sxs-lookup"><span data-stu-id="5abd3-135">ALIASES</span></span>

## <span data-ttu-id="5abd3-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5abd3-136">RELATED LINKS</span></span>

