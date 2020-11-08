---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
ms.openlocfilehash: 62b43668e8d886a11a26204edcd3c8b13635eff4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218871"
---
# <span data-ttu-id="52372-101">Get-AzMigrateSolution</span><span class="sxs-lookup"><span data-stu-id="52372-101">Get-AzMigrateSolution</span></span>

## <span data-ttu-id="52372-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52372-102">SYNOPSIS</span></span>
<span data-ttu-id="52372-103">마이그레이션 프로젝트의 솔루션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="52372-103">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="52372-104">구문과</span><span class="sxs-lookup"><span data-stu-id="52372-104">SYNTAX</span></span>

```
Get-AzMigrateSolution -MigrateProjectName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="52372-105">설명은</span><span class="sxs-lookup"><span data-stu-id="52372-105">DESCRIPTION</span></span>
<span data-ttu-id="52372-106">마이그레이션 프로젝트의 솔루션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="52372-106">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="52372-107">예제의</span><span class="sxs-lookup"><span data-stu-id="52372-107">EXAMPLES</span></span>

### <span data-ttu-id="52372-108">예제 1: Get</span><span class="sxs-lookup"><span data-stu-id="52372-108">Example 1: Get</span></span>
```powershell
PS C:\>Get-AzMigrateSolution -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Name Servers-Migration-ServerMigration

Etag                                   Name                              Type
----                                   ----                              ----
"010097f1-0000-1800-0000-5ee9ae2b0000" Servers-Migration-ServerMigration Microsoft.Migrate/MigrateProjec…
```

<span data-ttu-id="52372-109">이름으로 프로젝트 솔루션 마이그레이션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="52372-109">Get Migrate project solution by name.</span></span>

## <span data-ttu-id="52372-110">변수</span><span class="sxs-lookup"><span data-stu-id="52372-110">PARAMETERS</span></span>

### <span data-ttu-id="52372-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52372-111">-DefaultProfile</span></span>
<span data-ttu-id="52372-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="52372-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52372-113">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="52372-113">-MigrateProjectName</span></span>
<span data-ttu-id="52372-114">Azure 마이그레이션 프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52372-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="52372-115">-이름</span><span class="sxs-lookup"><span data-stu-id="52372-115">-Name</span></span>
<span data-ttu-id="52372-116">마이그레이션 프로젝트 내 마이그레이션 솔루션의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52372-116">Unique name of a migration solution within a migrate project.</span></span>

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

### <span data-ttu-id="52372-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52372-117">-ResourceGroupName</span></span>
<span data-ttu-id="52372-118">프로젝트를 마이그레이션하는 Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52372-118">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="52372-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="52372-119">-SubscriptionId</span></span>
<span data-ttu-id="52372-120">마이그레이션 프로젝트를 만든 Azure 구독 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="52372-120">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="52372-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52372-121">CommonParameters</span></span>
<span data-ttu-id="52372-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="52372-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52372-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="52372-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52372-124">입력</span><span class="sxs-lookup"><span data-stu-id="52372-124">INPUTS</span></span>

## <span data-ttu-id="52372-125">출력</span><span class="sxs-lookup"><span data-stu-id="52372-125">OUTPUTS</span></span>

### <span data-ttu-id="52372-126">Api20180901Preview. ISolution의. PowerShell for.</span><span class="sxs-lookup"><span data-stu-id="52372-126">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.ISolution</span></span>

## <span data-ttu-id="52372-127">상속자</span><span class="sxs-lookup"><span data-stu-id="52372-127">NOTES</span></span>

<span data-ttu-id="52372-128">별칭과</span><span class="sxs-lookup"><span data-stu-id="52372-128">ALIASES</span></span>

## <span data-ttu-id="52372-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="52372-129">RELATED LINKS</span></span>

