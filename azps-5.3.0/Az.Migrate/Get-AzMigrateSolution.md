---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
ms.openlocfilehash: 62b43668e8d886a11a26204edcd3c8b13635eff4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385778"
---
# <span data-ttu-id="decdf-101">Get-AzMigrateSolution</span><span class="sxs-lookup"><span data-stu-id="decdf-101">Get-AzMigrateSolution</span></span>

## <span data-ttu-id="decdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="decdf-102">SYNOPSIS</span></span>
<span data-ttu-id="decdf-103">마이그레이션 프로젝트에서 솔루션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="decdf-103">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="decdf-104">구문</span><span class="sxs-lookup"><span data-stu-id="decdf-104">SYNTAX</span></span>

```
Get-AzMigrateSolution -MigrateProjectName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="decdf-105">설명</span><span class="sxs-lookup"><span data-stu-id="decdf-105">DESCRIPTION</span></span>
<span data-ttu-id="decdf-106">마이그레이션 프로젝트에서 솔루션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="decdf-106">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="decdf-107">예제</span><span class="sxs-lookup"><span data-stu-id="decdf-107">EXAMPLES</span></span>

### <span data-ttu-id="decdf-108">예제 1: Get</span><span class="sxs-lookup"><span data-stu-id="decdf-108">Example 1: Get</span></span>
```powershell
PS C:\>Get-AzMigrateSolution -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Name Servers-Migration-ServerMigration

Etag                                   Name                              Type
----                                   ----                              ----
"010097f1-0000-1800-0000-5ee9ae2b0000" Servers-Migration-ServerMigration Microsoft.Migrate/MigrateProjec…
```

<span data-ttu-id="decdf-109">이름으로 프로젝트 솔루션 마이그레이션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="decdf-109">Get Migrate project solution by name.</span></span>

## <span data-ttu-id="decdf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="decdf-110">PARAMETERS</span></span>

### <span data-ttu-id="decdf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="decdf-111">-DefaultProfile</span></span>
<span data-ttu-id="decdf-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="decdf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="decdf-113">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="decdf-113">-MigrateProjectName</span></span>
<span data-ttu-id="decdf-114">Azure Migrate 프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="decdf-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="decdf-115">-Name</span><span class="sxs-lookup"><span data-stu-id="decdf-115">-Name</span></span>
<span data-ttu-id="decdf-116">마이그레이션 프로젝트 내의 마이그레이션 솔루션의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="decdf-116">Unique name of a migration solution within a migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="decdf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="decdf-117">-ResourceGroupName</span></span>
<span data-ttu-id="decdf-118">프로젝트를 마이그레이션하는 Azure 리소스 그룹의 이름은 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="decdf-118">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="decdf-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="decdf-119">-SubscriptionId</span></span>
<span data-ttu-id="decdf-120">마이그레이션 프로젝트를 만든 Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="decdf-120">Azure Subscription Id in which migrate project was created.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="decdf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="decdf-121">CommonParameters</span></span>
<span data-ttu-id="decdf-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="decdf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="decdf-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="decdf-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="decdf-124">입력</span><span class="sxs-lookup"><span data-stu-id="decdf-124">INPUTS</span></span>

## <span data-ttu-id="decdf-125">출력</span><span class="sxs-lookup"><span data-stu-id="decdf-125">OUTPUTS</span></span>

### <span data-ttu-id="decdf-126">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="decdf-126">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.ISolution</span></span>

## <span data-ttu-id="decdf-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="decdf-127">NOTES</span></span>

<span data-ttu-id="decdf-128">별칭</span><span class="sxs-lookup"><span data-stu-id="decdf-128">ALIASES</span></span>

## <span data-ttu-id="decdf-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="decdf-129">RELATED LINKS</span></span>

