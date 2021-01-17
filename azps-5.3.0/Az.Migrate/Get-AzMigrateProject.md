---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
ms.openlocfilehash: 1e3fdb2eabd986907a4b702a62caa3a0d9c34e85
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490147"
---
# <span data-ttu-id="7069a-101">Get-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="7069a-101">Get-AzMigrateProject</span></span>

## <span data-ttu-id="7069a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7069a-102">SYNOPSIS</span></span>
<span data-ttu-id="7069a-103">마이그레이션 프로젝트를 얻을 수 있는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="7069a-103">Method to get a migrate project.</span></span>

## <span data-ttu-id="7069a-104">구문</span><span class="sxs-lookup"><span data-stu-id="7069a-104">SYNTAX</span></span>

```
Get-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7069a-105">설명</span><span class="sxs-lookup"><span data-stu-id="7069a-105">DESCRIPTION</span></span>
<span data-ttu-id="7069a-106">마이그레이션 프로젝트를 얻을 수 있는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="7069a-106">Method to get a migrate project.</span></span>

## <span data-ttu-id="7069a-107">예제</span><span class="sxs-lookup"><span data-stu-id="7069a-107">EXAMPLES</span></span>

### <span data-ttu-id="7069a-108">예제 1: Get</span><span class="sxs-lookup"><span data-stu-id="7069a-108">Example 1: Get</span></span>
```powershell
PS C:\> Get-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

ETag Location      Name             Type
---- --------      ----             ----
     southeastasia BugBashAVSVMware Microsoft.Migrate/MigrateProjects
```

<span data-ttu-id="7069a-109">마이그레이션 프로젝트를 얻을 수 있는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="7069a-109">Method to get a migrate project.</span></span>

## <span data-ttu-id="7069a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7069a-110">PARAMETERS</span></span>

### <span data-ttu-id="7069a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7069a-111">-DefaultProfile</span></span>
<span data-ttu-id="7069a-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7069a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7069a-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7069a-113">-Name</span></span>
<span data-ttu-id="7069a-114">Azure Migrate 프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7069a-114">Name of the Azure Migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrateProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7069a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7069a-115">-ResourceGroupName</span></span>
<span data-ttu-id="7069a-116">프로젝트를 마이그레이션하는 Azure 리소스 그룹의 이름은 일부입니다.</span><span class="sxs-lookup"><span data-stu-id="7069a-116">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="7069a-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7069a-117">-SubscriptionId</span></span>
<span data-ttu-id="7069a-118">마이그레이션 프로젝트를 만든 Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7069a-118">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="7069a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7069a-119">CommonParameters</span></span>
<span data-ttu-id="7069a-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7069a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7069a-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7069a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7069a-122">입력</span><span class="sxs-lookup"><span data-stu-id="7069a-122">INPUTS</span></span>

## <span data-ttu-id="7069a-123">출력</span><span class="sxs-lookup"><span data-stu-id="7069a-123">OUTPUTS</span></span>

### <span data-ttu-id="7069a-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span><span class="sxs-lookup"><span data-stu-id="7069a-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span></span>

## <span data-ttu-id="7069a-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7069a-125">NOTES</span></span>

<span data-ttu-id="7069a-126">별칭</span><span class="sxs-lookup"><span data-stu-id="7069a-126">ALIASES</span></span>

## <span data-ttu-id="7069a-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7069a-127">RELATED LINKS</span></span>

