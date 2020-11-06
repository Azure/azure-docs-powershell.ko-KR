---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 7C695E83-78AA-4008-91D6-D6B23BC96B92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 5657701475e81b302d761193cd542ee38ea9c16e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530656"
---
# <span data-ttu-id="39150-101">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="39150-101">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="39150-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39150-102">SYNOPSIS</span></span>
<span data-ttu-id="39150-103">사이트 복구에서 사이트 복구 계획을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="39150-103">Removes a site recovery plan from Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39150-104">구문과</span><span class="sxs-lookup"><span data-stu-id="39150-104">SYNTAX</span></span>

### <span data-ttu-id="39150-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="39150-105">ByObject (Default)</span></span>
```
Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39150-106">ByName</span><span class="sxs-lookup"><span data-stu-id="39150-106">ByName</span></span>
```
Remove-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39150-107">설명은</span><span class="sxs-lookup"><span data-stu-id="39150-107">DESCRIPTION</span></span>
<span data-ttu-id="39150-108">**AzureRmSiteRecoveryRecoveryPlan** cmdlet은 현재 Azure site recovery에서 사이트 복구 계획을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="39150-108">The **Remove-AzureRmSiteRecoveryRecoveryPlan** cmdlet removes a site recovery plan from the current Azure Site Recovery.</span></span>

## <span data-ttu-id="39150-109">예제의</span><span class="sxs-lookup"><span data-stu-id="39150-109">EXAMPLES</span></span>

### <span data-ttu-id="39150-110">예제 1: 복구 계획 제거</span><span class="sxs-lookup"><span data-stu-id="39150-110">Example 1: Remove a recovery plan</span></span>
```
PS C:\>$RecoveryPlan = Get-AzureRmSiteRecoveryRecoveryPlan 
PS C:\> Remove-AzureRmSiteRecoveryRecoveryPlan -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="39150-111">첫 번째 명령은 Get-AzureRmSiteRecoveryRecoveryPlan cmdlet을 사용 하 여 사이트 복구 계획을 얻은 다음 $RecoveryPlan 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="39150-111">The first command uses the Get-AzureRmSiteRecoveryRecoveryPlan cmdlet to get the Site Recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="39150-112">두 번째 명령은 $RecoveryPlan 복구 계획을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="39150-112">The second command removes the recovery plan in $RecoveryPlan.</span></span>

## <span data-ttu-id="39150-113">변수</span><span class="sxs-lookup"><span data-stu-id="39150-113">PARAMETERS</span></span>

### <span data-ttu-id="39150-114">-이름</span><span class="sxs-lookup"><span data-stu-id="39150-114">-Name</span></span>
<span data-ttu-id="39150-115">이 cmdlet이 제거 하는 복구 계획의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39150-115">Specifies the name of the recovery plan that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39150-116">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="39150-116">-RecoveryPlan</span></span>
<span data-ttu-id="39150-117">이 cmdlet이 제거 하는 복구 계획을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39150-117">Specifies the recovery plan that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39150-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39150-118">-DefaultProfile</span></span>
<span data-ttu-id="39150-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="39150-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39150-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39150-120">CommonParameters</span></span>
<span data-ttu-id="39150-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="39150-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39150-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39150-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39150-123">입력</span><span class="sxs-lookup"><span data-stu-id="39150-123">INPUTS</span></span>

### <span data-ttu-id="39150-124">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="39150-124">ASRRecoveryPlan</span></span>
<span data-ttu-id="39150-125">' RecoveryPlan ' 매개 변수는 파이프라인에서 ' ASRRecoveryPlan ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="39150-125">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

## <span data-ttu-id="39150-126">출력</span><span class="sxs-lookup"><span data-stu-id="39150-126">OUTPUTS</span></span>

## <span data-ttu-id="39150-127">상속자</span><span class="sxs-lookup"><span data-stu-id="39150-127">NOTES</span></span>

## <span data-ttu-id="39150-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39150-128">RELATED LINKS</span></span>

[<span data-ttu-id="39150-129">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="39150-129">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="39150-130">새로운 AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="39150-130">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="39150-131">업데이트-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="39150-131">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)


