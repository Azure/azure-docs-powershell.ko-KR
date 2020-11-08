---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
ms.openlocfilehash: 1e3fdb2eabd986907a4b702a62caa3a0d9c34e85
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226788"
---
# <span data-ttu-id="d05fd-101">Get-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="d05fd-101">Get-AzMigrateProject</span></span>

## <span data-ttu-id="d05fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d05fd-102">SYNOPSIS</span></span>
<span data-ttu-id="d05fd-103">마이그레이션 프로젝트를 가져오는 메서드입니다.</span><span class="sxs-lookup"><span data-stu-id="d05fd-103">Method to get a migrate project.</span></span>

## <span data-ttu-id="d05fd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d05fd-104">SYNTAX</span></span>

```
Get-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d05fd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d05fd-105">DESCRIPTION</span></span>
<span data-ttu-id="d05fd-106">마이그레이션 프로젝트를 가져오는 메서드입니다.</span><span class="sxs-lookup"><span data-stu-id="d05fd-106">Method to get a migrate project.</span></span>

## <span data-ttu-id="d05fd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d05fd-107">EXAMPLES</span></span>

### <span data-ttu-id="d05fd-108">예제 1: Get</span><span class="sxs-lookup"><span data-stu-id="d05fd-108">Example 1: Get</span></span>
```powershell
PS C:\> Get-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

ETag Location      Name             Type
---- --------      ----             ----
     southeastasia BugBashAVSVMware Microsoft.Migrate/MigrateProjects
```

<span data-ttu-id="d05fd-109">마이그레이션 프로젝트를 가져오는 메서드입니다.</span><span class="sxs-lookup"><span data-stu-id="d05fd-109">Method to get a migrate project.</span></span>

## <span data-ttu-id="d05fd-110">변수</span><span class="sxs-lookup"><span data-stu-id="d05fd-110">PARAMETERS</span></span>

### <span data-ttu-id="d05fd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d05fd-111">-DefaultProfile</span></span>
<span data-ttu-id="d05fd-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d05fd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d05fd-113">-이름</span><span class="sxs-lookup"><span data-stu-id="d05fd-113">-Name</span></span>
<span data-ttu-id="d05fd-114">Azure 마이그레이션 프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d05fd-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="d05fd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d05fd-115">-ResourceGroupName</span></span>
<span data-ttu-id="d05fd-116">프로젝트를 마이그레이션하는 Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d05fd-116">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="d05fd-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d05fd-117">-SubscriptionId</span></span>
<span data-ttu-id="d05fd-118">마이그레이션 프로젝트를 만든 Azure 구독 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="d05fd-118">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="d05fd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d05fd-119">CommonParameters</span></span>
<span data-ttu-id="d05fd-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d05fd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d05fd-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d05fd-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d05fd-122">입력</span><span class="sxs-lookup"><span data-stu-id="d05fd-122">INPUTS</span></span>

## <span data-ttu-id="d05fd-123">출력</span><span class="sxs-lookup"><span data-stu-id="d05fd-123">OUTPUTS</span></span>

### <span data-ttu-id="d05fd-124">Api20180901Preview. IMigrateProject의. PowerShell for.</span><span class="sxs-lookup"><span data-stu-id="d05fd-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span></span>

## <span data-ttu-id="d05fd-125">상속자</span><span class="sxs-lookup"><span data-stu-id="d05fd-125">NOTES</span></span>

<span data-ttu-id="d05fd-126">별칭과</span><span class="sxs-lookup"><span data-stu-id="d05fd-126">ALIASES</span></span>

## <span data-ttu-id="d05fd-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d05fd-127">RELATED LINKS</span></span>

