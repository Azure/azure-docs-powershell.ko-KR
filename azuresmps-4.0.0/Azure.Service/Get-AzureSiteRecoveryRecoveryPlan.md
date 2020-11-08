---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 8557B04E-DE35-473E-8F5D-B72B70300AA6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1949d30d6bbea16e1626954bf241df36d81533e1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045585"
---
# <span data-ttu-id="f6e9d-101">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f6e9d-101">Get-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="f6e9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6e9d-102">SYNOPSIS</span></span>
<span data-ttu-id="f6e9d-103">사이트 복구의 복구 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f6e9d-103">Gets a recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="f6e9d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f6e9d-104">SYNTAX</span></span>

### <span data-ttu-id="f6e9d-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="f6e9d-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f6e9d-106">ById</span><span class="sxs-lookup"><span data-stu-id="f6e9d-106">ById</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f6e9d-107">ByName</span><span class="sxs-lookup"><span data-stu-id="f6e9d-107">ByName</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f6e9d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f6e9d-108">DESCRIPTION</span></span>
<span data-ttu-id="f6e9d-109">**AzureSiteRecoveryRecoveryPlan** Cmdlet은 Azure Site recovery의 복구 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f6e9d-109">The **Get-AzureSiteRecoveryRecoveryPlan** cmdlet gets a recovery plan in Azure Site Recovery.</span></span>

## <span data-ttu-id="f6e9d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f6e9d-110">EXAMPLES</span></span>

### <span data-ttu-id="f6e9d-111">예제 1: 복구 계획 가져오기</span><span class="sxs-lookup"><span data-stu-id="f6e9d-111">Example 1: Get a recovery plan</span></span>
```
PS C:\> Get-AzureSiteRecoveryRecoveryPlan
ID                            Name                          ServerId                      TargetServerId
--                            ----                          --------                      --------------
71de8ebc-1e9a-4242-aec3-ee... ContosoPlan                   4a94c4a9-c856-4577-afbd-36... 78facf56-b273-4941-82fd-cc...
```

<span data-ttu-id="f6e9d-112">이 명령은 현재 Azure Site Recovery 자격 증명 모음의 복구 계획에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f6e9d-112">This command gets information about the recovery plan for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="f6e9d-113">변수</span><span class="sxs-lookup"><span data-stu-id="f6e9d-113">PARAMETERS</span></span>

### <span data-ttu-id="f6e9d-114">-Id</span><span class="sxs-lookup"><span data-stu-id="f6e9d-114">-Id</span></span>
<span data-ttu-id="f6e9d-115">가져올 복구 계획의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6e9d-115">Specifies the ID of the recovery plan to get.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6e9d-116">-이름</span><span class="sxs-lookup"><span data-stu-id="f6e9d-116">-Name</span></span>
<span data-ttu-id="f6e9d-117">가져올 복구 계획의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6e9d-117">Specifies the name of the recovery plan to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6e9d-118">-프로필</span><span class="sxs-lookup"><span data-stu-id="f6e9d-118">-Profile</span></span>
<span data-ttu-id="f6e9d-119">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6e9d-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f6e9d-120">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f6e9d-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6e9d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6e9d-121">CommonParameters</span></span>
<span data-ttu-id="f6e9d-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6e9d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6e9d-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6e9d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6e9d-124">입력</span><span class="sxs-lookup"><span data-stu-id="f6e9d-124">INPUTS</span></span>

## <span data-ttu-id="f6e9d-125">출력</span><span class="sxs-lookup"><span data-stu-id="f6e9d-125">OUTPUTS</span></span>

## <span data-ttu-id="f6e9d-126">상속자</span><span class="sxs-lookup"><span data-stu-id="f6e9d-126">NOTES</span></span>

## <span data-ttu-id="f6e9d-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f6e9d-127">RELATED LINKS</span></span>

[<span data-ttu-id="f6e9d-128">새로운 AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f6e9d-128">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="f6e9d-129">제거-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f6e9d-129">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="f6e9d-130">업데이트-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f6e9d-130">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


