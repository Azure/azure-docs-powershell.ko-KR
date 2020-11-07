---
external help file: ''
Module Name: Azs.KeyVault.Admin
online version: https://docs.microsoft.com/powershell/module/azs.keyvault.admin/get-azskeyvaultquota
schema: 2.0.0
ms.openlocfilehash: 813e0e7dc2535b3c7cd424e55ff924c380d84e2f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876041"
---
# <span data-ttu-id="209b6-101">Get-AzsKeyvaultQuota</span><span class="sxs-lookup"><span data-stu-id="209b6-101">Get-AzsKeyvaultQuota</span></span>

## <span data-ttu-id="209b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="209b6-102">SYNOPSIS</span></span>
<span data-ttu-id="209b6-103">위치에 있는 KeyVault에 대 한 모든 할당량 개체의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="209b6-103">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="209b6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="209b6-104">SYNTAX</span></span>

```
Get-AzsKeyvaultQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="209b6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="209b6-105">DESCRIPTION</span></span>
<span data-ttu-id="209b6-106">위치에 있는 KeyVault에 대 한 모든 할당량 개체의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="209b6-106">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="209b6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="209b6-107">EXAMPLES</span></span>

### <span data-ttu-id="209b6-108">예제 1:</span><span class="sxs-lookup"><span data-stu-id="209b6-108">Example 1:</span></span>
```powershell
PS C:\> Get-AzsKeyVaultQuota

Location  Name                Type
--------  ----                ----
northwest northwest/Unlimited Microsoft.KeyVault.Admin/locations/quotas

```

<span data-ttu-id="209b6-109">위치에 있는 KeyVault에 대 한 모든 할당량 개체의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="209b6-109">Get a list of all quota objects for KeyVault at a location.</span></span>

## <span data-ttu-id="209b6-110">변수</span><span class="sxs-lookup"><span data-stu-id="209b6-110">PARAMETERS</span></span>

### <span data-ttu-id="209b6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="209b6-111">-DefaultProfile</span></span>
<span data-ttu-id="209b6-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="209b6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="209b6-113">-위치</span><span class="sxs-lookup"><span data-stu-id="209b6-113">-Location</span></span>
<span data-ttu-id="209b6-114">할당량의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="209b6-114">The location of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="209b6-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="209b6-115">-SubscriptionId</span></span>
<span data-ttu-id="209b6-116">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="209b6-116">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="209b6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="209b6-117">CommonParameters</span></span>
<span data-ttu-id="209b6-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="209b6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="209b6-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="209b6-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="209b6-120">입력</span><span class="sxs-lookup"><span data-stu-id="209b6-120">INPUTS</span></span>

## <span data-ttu-id="209b6-121">출력</span><span class="sxs-lookup"><span data-stu-id="209b6-121">OUTPUTS</span></span>

### <span data-ttu-id="209b6-122">KeyVaultAdmin (Api20170201Preview)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="209b6-122">Microsoft.Azure.PowerShell.Cmdlets.KeyVaultAdmin.Models.Api20170201Preview.IQuota</span></span>



## <span data-ttu-id="209b6-123">상속자</span><span class="sxs-lookup"><span data-stu-id="209b6-123">NOTES</span></span>

## <span data-ttu-id="209b6-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="209b6-124">RELATED LINKS</span></span>

