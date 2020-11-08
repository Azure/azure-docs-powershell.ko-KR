---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
ms.openlocfilehash: ebea7936483a34d2515c69c416146d07651b396b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218874"
---
# <span data-ttu-id="adc17-101">Get-AzMigrateSite</span><span class="sxs-lookup"><span data-stu-id="adc17-101">Get-AzMigrateSite</span></span>

## <span data-ttu-id="adc17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adc17-102">SYNOPSIS</span></span>
<span data-ttu-id="adc17-103">사이트를 가져오는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="adc17-103">Method to get a site.</span></span>

## <span data-ttu-id="adc17-104">구문과</span><span class="sxs-lookup"><span data-stu-id="adc17-104">SYNTAX</span></span>

```
Get-AzMigrateSite -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="adc17-105">설명은</span><span class="sxs-lookup"><span data-stu-id="adc17-105">DESCRIPTION</span></span>
<span data-ttu-id="adc17-106">사이트를 가져오는 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="adc17-106">Method to get a site.</span></span>

## <span data-ttu-id="adc17-107">예제의</span><span class="sxs-lookup"><span data-stu-id="adc17-107">EXAMPLES</span></span>

### <span data-ttu-id="adc17-108">예제 1: Get (기본값)</span><span class="sxs-lookup"><span data-stu-id="adc17-108">Example 1: Get (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateSite -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

ETag Location      Name                Type
---- --------      ----                ----
     southeastasia BBVMwareAVScbbcsite Microsoft.OffAzure/VMwareSites

```

<span data-ttu-id="adc17-109">이름으로 사이트 가져오기</span><span class="sxs-lookup"><span data-stu-id="adc17-109">Get site by name</span></span>

## <span data-ttu-id="adc17-110">변수</span><span class="sxs-lookup"><span data-stu-id="adc17-110">PARAMETERS</span></span>

### <span data-ttu-id="adc17-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adc17-111">-DefaultProfile</span></span>
<span data-ttu-id="adc17-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="adc17-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adc17-113">-이름</span><span class="sxs-lookup"><span data-stu-id="adc17-113">-Name</span></span>
<span data-ttu-id="adc17-114">사이트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="adc17-114">Site name.</span></span>

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

### <span data-ttu-id="adc17-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adc17-115">-ResourceGroupName</span></span>
<span data-ttu-id="adc17-116">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="adc17-116">The name of the resource group.</span></span>
<span data-ttu-id="adc17-117">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc17-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="adc17-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="adc17-118">-SubscriptionId</span></span>
<span data-ttu-id="adc17-119">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="adc17-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="adc17-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adc17-120">CommonParameters</span></span>
<span data-ttu-id="adc17-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="adc17-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adc17-122">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="adc17-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adc17-123">입력</span><span class="sxs-lookup"><span data-stu-id="adc17-123">INPUTS</span></span>

## <span data-ttu-id="adc17-124">출력</span><span class="sxs-lookup"><span data-stu-id="adc17-124">OUTPUTS</span></span>

### <span data-ttu-id="adc17-125">Api202001. a Nivmwaresite.</span><span class="sxs-lookup"><span data-stu-id="adc17-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span></span>

## <span data-ttu-id="adc17-126">상속자</span><span class="sxs-lookup"><span data-stu-id="adc17-126">NOTES</span></span>

<span data-ttu-id="adc17-127">별칭과</span><span class="sxs-lookup"><span data-stu-id="adc17-127">ALIASES</span></span>

## <span data-ttu-id="adc17-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="adc17-128">RELATED LINKS</span></span>

