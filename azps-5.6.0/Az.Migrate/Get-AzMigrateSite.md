---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
ms.openlocfilehash: b00010096b39cd714f01f33012309f8528a5ae3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982800"
---
# <span data-ttu-id="865e3-101">Get-AzMigrateSite</span><span class="sxs-lookup"><span data-stu-id="865e3-101">Get-AzMigrateSite</span></span>

## <span data-ttu-id="865e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="865e3-102">SYNOPSIS</span></span>
<span data-ttu-id="865e3-103">사이트를 얻을 수 있는 메서드입니다.</span><span class="sxs-lookup"><span data-stu-id="865e3-103">Method to get a site.</span></span>

## <span data-ttu-id="865e3-104">구문</span><span class="sxs-lookup"><span data-stu-id="865e3-104">SYNTAX</span></span>

```
Get-AzMigrateSite -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="865e3-105">설명</span><span class="sxs-lookup"><span data-stu-id="865e3-105">DESCRIPTION</span></span>
<span data-ttu-id="865e3-106">사이트를 얻을 수 있는 메서드입니다.</span><span class="sxs-lookup"><span data-stu-id="865e3-106">Method to get a site.</span></span>

## <span data-ttu-id="865e3-107">예제</span><span class="sxs-lookup"><span data-stu-id="865e3-107">EXAMPLES</span></span>

### <span data-ttu-id="865e3-108">예제 1: Get(기본값)</span><span class="sxs-lookup"><span data-stu-id="865e3-108">Example 1: Get (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateSite -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

ETag Location      Name                Type
---- --------      ----                ----
     southeastasia BBVMwareAVScbbcsite Microsoft.OffAzure/VMwareSites

```

<span data-ttu-id="865e3-109">이름에 의해 사이트 를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="865e3-109">Get site by name</span></span>

## <span data-ttu-id="865e3-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="865e3-110">PARAMETERS</span></span>

### <span data-ttu-id="865e3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="865e3-111">-DefaultProfile</span></span>
<span data-ttu-id="865e3-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="865e3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="865e3-113">-Name</span><span class="sxs-lookup"><span data-stu-id="865e3-113">-Name</span></span>
<span data-ttu-id="865e3-114">사이트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="865e3-114">Site name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="865e3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="865e3-115">-ResourceGroupName</span></span>
<span data-ttu-id="865e3-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="865e3-116">The name of the resource group.</span></span>
<span data-ttu-id="865e3-117">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="865e3-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="865e3-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="865e3-118">-SubscriptionId</span></span>
<span data-ttu-id="865e3-119">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="865e3-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="865e3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="865e3-120">CommonParameters</span></span>
<span data-ttu-id="865e3-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="865e3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="865e3-122">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="865e3-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="865e3-123">입력</span><span class="sxs-lookup"><span data-stu-id="865e3-123">INPUTS</span></span>

## <span data-ttu-id="865e3-124">출력</span><span class="sxs-lookup"><span data-stu-id="865e3-124">OUTPUTS</span></span>

### <span data-ttu-id="865e3-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span><span class="sxs-lookup"><span data-stu-id="865e3-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span></span>

## <span data-ttu-id="865e3-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="865e3-126">NOTES</span></span>

<span data-ttu-id="865e3-127">별칭</span><span class="sxs-lookup"><span data-stu-id="865e3-127">ALIASES</span></span>

## <span data-ttu-id="865e3-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="865e3-128">RELATED LINKS</span></span>

