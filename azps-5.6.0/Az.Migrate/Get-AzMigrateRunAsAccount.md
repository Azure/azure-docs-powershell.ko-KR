---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigraterunasaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
ms.openlocfilehash: d028e66fc5f1f4b2c3ab520bd76615e8e9e79099
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982816"
---
# <span data-ttu-id="798b0-101">Get-AzMigrateRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="798b0-101">Get-AzMigrateRunAsAccount</span></span>

## <span data-ttu-id="798b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="798b0-102">SYNOPSIS</span></span>
<span data-ttu-id="798b0-103">계정으로 실행하는 메서드입니다.</span><span class="sxs-lookup"><span data-stu-id="798b0-103">Method to get run as account.</span></span>

## <span data-ttu-id="798b0-104">구문</span><span class="sxs-lookup"><span data-stu-id="798b0-104">SYNTAX</span></span>

### <span data-ttu-id="798b0-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="798b0-105">List (Default)</span></span>
```
Get-AzMigrateRunAsAccount -ResourceGroupName <String> -SiteName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="798b0-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="798b0-106">Get</span></span>
```
Get-AzMigrateRunAsAccount -AccountName <String> -ResourceGroupName <String> -SiteName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="798b0-107">설명</span><span class="sxs-lookup"><span data-stu-id="798b0-107">DESCRIPTION</span></span>
<span data-ttu-id="798b0-108">계정으로 실행하는 메서드입니다.</span><span class="sxs-lookup"><span data-stu-id="798b0-108">Method to get run as account.</span></span>

## <span data-ttu-id="798b0-109">예제</span><span class="sxs-lookup"><span data-stu-id="798b0-109">EXAMPLES</span></span>

### <span data-ttu-id="798b0-110">예제 1: 목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="798b0-110">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="798b0-111">모든 실행을 사이트의 계정으로 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="798b0-111">List all run as accounts in a site.</span></span>

### <span data-ttu-id="798b0-112">예제 2: Get</span><span class="sxs-lookup"><span data-stu-id="798b0-112">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite -AccountName b090bef3-b733-5e34-bc8f-eb6f2701432a

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="798b0-113">이름으로 실행을 계정으로 하세요.</span><span class="sxs-lookup"><span data-stu-id="798b0-113">Get Run as account by name.</span></span>

## <span data-ttu-id="798b0-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="798b0-114">PARAMETERS</span></span>

### <span data-ttu-id="798b0-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="798b0-115">-AccountName</span></span>
<span data-ttu-id="798b0-116">계정 이름으로 ARM 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="798b0-116">Run as account ARM name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="798b0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="798b0-117">-DefaultProfile</span></span>
<span data-ttu-id="798b0-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="798b0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="798b0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="798b0-119">-ResourceGroupName</span></span>
<span data-ttu-id="798b0-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="798b0-120">The name of the resource group.</span></span>
<span data-ttu-id="798b0-121">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="798b0-121">The name is case insensitive.</span></span>

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

### <span data-ttu-id="798b0-122">-SiteName</span><span class="sxs-lookup"><span data-stu-id="798b0-122">-SiteName</span></span>
<span data-ttu-id="798b0-123">사이트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="798b0-123">Site name.</span></span>

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

### <span data-ttu-id="798b0-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="798b0-124">-SubscriptionId</span></span>
<span data-ttu-id="798b0-125">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="798b0-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="798b0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="798b0-126">CommonParameters</span></span>
<span data-ttu-id="798b0-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="798b0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="798b0-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="798b0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="798b0-129">입력</span><span class="sxs-lookup"><span data-stu-id="798b0-129">INPUTS</span></span>

## <span data-ttu-id="798b0-130">출력</span><span class="sxs-lookup"><span data-stu-id="798b0-130">OUTPUTS</span></span>

### <span data-ttu-id="798b0-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="798b0-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span></span>

## <span data-ttu-id="798b0-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="798b0-132">NOTES</span></span>

<span data-ttu-id="798b0-133">별칭</span><span class="sxs-lookup"><span data-stu-id="798b0-133">ALIASES</span></span>

## <span data-ttu-id="798b0-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="798b0-134">RELATED LINKS</span></span>

