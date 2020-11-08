---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigraterunasaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
ms.openlocfilehash: 6f78a326efc29e3ba89f774575df1c4b7472e70c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218877"
---
# <span data-ttu-id="7be41-101">Get-AzMigrateRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="7be41-101">Get-AzMigrateRunAsAccount</span></span>

## <span data-ttu-id="7be41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7be41-102">SYNOPSIS</span></span>
<span data-ttu-id="7be41-103">실행 계정을 가져오는 메서드입니다.</span><span class="sxs-lookup"><span data-stu-id="7be41-103">Method to get run as account.</span></span>

## <span data-ttu-id="7be41-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7be41-104">SYNTAX</span></span>

### <span data-ttu-id="7be41-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="7be41-105">List (Default)</span></span>
```
Get-AzMigrateRunAsAccount -ResourceGroupName <String> -SiteName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7be41-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="7be41-106">Get</span></span>
```
Get-AzMigrateRunAsAccount -AccountName <String> -ResourceGroupName <String> -SiteName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7be41-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7be41-107">DESCRIPTION</span></span>
<span data-ttu-id="7be41-108">실행 계정을 가져오는 메서드입니다.</span><span class="sxs-lookup"><span data-stu-id="7be41-108">Method to get run as account.</span></span>

## <span data-ttu-id="7be41-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7be41-109">EXAMPLES</span></span>

### <span data-ttu-id="7be41-110">예제 1: 목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="7be41-110">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="7be41-111">사이트의 모든 실행 계정을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="7be41-111">List all run as accounts in a site.</span></span>

### <span data-ttu-id="7be41-112">예제 2: Get</span><span class="sxs-lookup"><span data-stu-id="7be41-112">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite -AccountName b090bef3-b733-5e34-bc8f-eb6f2701432a

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="7be41-113">이름으로 실행 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="7be41-113">Get Run as account by name.</span></span>

## <span data-ttu-id="7be41-114">변수</span><span class="sxs-lookup"><span data-stu-id="7be41-114">PARAMETERS</span></span>

### <span data-ttu-id="7be41-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7be41-115">-AccountName</span></span>
<span data-ttu-id="7be41-116">계정 팔 이름으로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7be41-116">Run as account ARM name.</span></span>

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

### <span data-ttu-id="7be41-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7be41-117">-DefaultProfile</span></span>
<span data-ttu-id="7be41-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7be41-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7be41-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7be41-119">-ResourceGroupName</span></span>
<span data-ttu-id="7be41-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7be41-120">The name of the resource group.</span></span>
<span data-ttu-id="7be41-121">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="7be41-121">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7be41-122">-SiteName</span><span class="sxs-lookup"><span data-stu-id="7be41-122">-SiteName</span></span>
<span data-ttu-id="7be41-123">사이트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7be41-123">Site name.</span></span>

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

### <span data-ttu-id="7be41-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7be41-124">-SubscriptionId</span></span>
<span data-ttu-id="7be41-125">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7be41-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7be41-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7be41-126">CommonParameters</span></span>
<span data-ttu-id="7be41-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7be41-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7be41-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7be41-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7be41-129">입력</span><span class="sxs-lookup"><span data-stu-id="7be41-129">INPUTS</span></span>

## <span data-ttu-id="7be41-130">출력</span><span class="sxs-lookup"><span data-stu-id="7be41-130">OUTPUTS</span></span>

### <span data-ttu-id="7be41-131">Api202001 Ivm워 Erunasaccount와 같은 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7be41-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span></span>

## <span data-ttu-id="7be41-132">상속자</span><span class="sxs-lookup"><span data-stu-id="7be41-132">NOTES</span></span>

<span data-ttu-id="7be41-133">별칭과</span><span class="sxs-lookup"><span data-stu-id="7be41-133">ALIASES</span></span>

## <span data-ttu-id="7be41-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7be41-134">RELATED LINKS</span></span>

