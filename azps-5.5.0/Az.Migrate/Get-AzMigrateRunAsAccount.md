---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigraterunasaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
ms.openlocfilehash: 6f78a326efc29e3ba89f774575df1c4b7472e70c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185100"
---
# <span data-ttu-id="b9e94-101">Get-AzMigrateRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="b9e94-101">Get-AzMigrateRunAsAccount</span></span>

## <span data-ttu-id="b9e94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9e94-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e94-103">계정으로 실행하는 메서드입니다.</span><span class="sxs-lookup"><span data-stu-id="b9e94-103">Method to get run as account.</span></span>

## <span data-ttu-id="b9e94-104">구문</span><span class="sxs-lookup"><span data-stu-id="b9e94-104">SYNTAX</span></span>

### <span data-ttu-id="b9e94-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="b9e94-105">List (Default)</span></span>
```
Get-AzMigrateRunAsAccount -ResourceGroupName <String> -SiteName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b9e94-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="b9e94-106">Get</span></span>
```
Get-AzMigrateRunAsAccount -AccountName <String> -ResourceGroupName <String> -SiteName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b9e94-107">설명</span><span class="sxs-lookup"><span data-stu-id="b9e94-107">DESCRIPTION</span></span>
<span data-ttu-id="b9e94-108">계정으로 실행하는 메서드입니다.</span><span class="sxs-lookup"><span data-stu-id="b9e94-108">Method to get run as account.</span></span>

## <span data-ttu-id="b9e94-109">예제</span><span class="sxs-lookup"><span data-stu-id="b9e94-109">EXAMPLES</span></span>

### <span data-ttu-id="b9e94-110">예제 1: 목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="b9e94-110">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="b9e94-111">사이트의 모든 실행을 계정으로 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e94-111">List all run as accounts in a site.</span></span>

### <span data-ttu-id="b9e94-112">예제 2: Get</span><span class="sxs-lookup"><span data-stu-id="b9e94-112">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite -AccountName b090bef3-b733-5e34-bc8f-eb6f2701432a

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="b9e94-113">이름으로 실행 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b9e94-113">Get Run as account by name.</span></span>

## <span data-ttu-id="b9e94-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9e94-114">PARAMETERS</span></span>

### <span data-ttu-id="b9e94-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b9e94-115">-AccountName</span></span>
<span data-ttu-id="b9e94-116">계정 이름으로 실행 ARM 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9e94-116">Run as account ARM name.</span></span>

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

### <span data-ttu-id="b9e94-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e94-117">-DefaultProfile</span></span>
<span data-ttu-id="b9e94-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b9e94-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9e94-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9e94-119">-ResourceGroupName</span></span>
<span data-ttu-id="b9e94-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9e94-120">The name of the resource group.</span></span>
<span data-ttu-id="b9e94-121">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e94-121">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b9e94-122">-SiteName</span><span class="sxs-lookup"><span data-stu-id="b9e94-122">-SiteName</span></span>
<span data-ttu-id="b9e94-123">사이트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9e94-123">Site name.</span></span>

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

### <span data-ttu-id="b9e94-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b9e94-124">-SubscriptionId</span></span>
<span data-ttu-id="b9e94-125">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b9e94-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b9e94-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e94-126">CommonParameters</span></span>
<span data-ttu-id="b9e94-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b9e94-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e94-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b9e94-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e94-129">입력</span><span class="sxs-lookup"><span data-stu-id="b9e94-129">INPUTS</span></span>

## <span data-ttu-id="b9e94-130">출력</span><span class="sxs-lookup"><span data-stu-id="b9e94-130">OUTPUTS</span></span>

### <span data-ttu-id="b9e94-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="b9e94-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span></span>

## <span data-ttu-id="b9e94-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b9e94-132">NOTES</span></span>

<span data-ttu-id="b9e94-133">별칭</span><span class="sxs-lookup"><span data-stu-id="b9e94-133">ALIASES</span></span>

## <span data-ttu-id="b9e94-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b9e94-134">RELATED LINKS</span></span>

