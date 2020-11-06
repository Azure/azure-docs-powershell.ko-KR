---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3B879056-5BF3-4262-8BAA-E79589149370
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 2d9f087b87d99003b559fc363265fdb4b996c3f9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529113"
---
# <span data-ttu-id="f1f81-101">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f1f81-101">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="f1f81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1f81-102">SYNOPSIS</span></span>
<span data-ttu-id="f1f81-103">사이트 복구의 복구 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f1f81-103">Gets a recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1f81-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f1f81-104">SYNTAX</span></span>

### <span data-ttu-id="f1f81-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="f1f81-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1f81-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f1f81-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1f81-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="f1f81-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1f81-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f1f81-108">DESCRIPTION</span></span>
<span data-ttu-id="f1f81-109">**AzureRmSiteRecoveryRecoveryPlan** Cmdlet은 Azure Site recovery의 복구 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f1f81-109">The **Get-AzureRmSiteRecoveryRecoveryPlan** cmdlet gets a recovery plan in Azure Site Recovery.</span></span>

## <span data-ttu-id="f1f81-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f1f81-110">EXAMPLES</span></span>

## <span data-ttu-id="f1f81-111">변수</span><span class="sxs-lookup"><span data-stu-id="f1f81-111">PARAMETERS</span></span>

### <span data-ttu-id="f1f81-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f1f81-112">-FriendlyName</span></span>
<span data-ttu-id="f1f81-113">이 cmdlet이 가져오는 복구 계획의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1f81-113">Specifies the friendly name of the recovery plan that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1f81-114">-이름</span><span class="sxs-lookup"><span data-stu-id="f1f81-114">-Name</span></span>
<span data-ttu-id="f1f81-115">이 cmdlet이 가져오는 복구 계획의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1f81-115">Specifies the name of the recovery plan that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f1f81-116">-Path</span><span class="sxs-lookup"><span data-stu-id="f1f81-116">-Path</span></span>
<span data-ttu-id="f1f81-117">이 cmdlet이 복구 계획을 저장할 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1f81-117">Specifies the file path to which this cmdlet saves the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByFriendlyName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1f81-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1f81-118">-DefaultProfile</span></span>
<span data-ttu-id="f1f81-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f1f81-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1f81-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1f81-120">CommonParameters</span></span>
<span data-ttu-id="f1f81-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1f81-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1f81-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1f81-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1f81-123">입력</span><span class="sxs-lookup"><span data-stu-id="f1f81-123">INPUTS</span></span>

## <span data-ttu-id="f1f81-124">출력</span><span class="sxs-lookup"><span data-stu-id="f1f81-124">OUTPUTS</span></span>

### <span data-ttu-id="f1f81-125">System.webserver. t e r ' 1 [SiteRecovery Rrecoveryplan]</span><span class="sxs-lookup"><span data-stu-id="f1f81-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan]</span></span>

## <span data-ttu-id="f1f81-126">상속자</span><span class="sxs-lookup"><span data-stu-id="f1f81-126">NOTES</span></span>

## <span data-ttu-id="f1f81-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1f81-127">RELATED LINKS</span></span>

[<span data-ttu-id="f1f81-128">새로운 AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f1f81-128">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="f1f81-129">제거-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f1f81-129">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="f1f81-130">업데이트-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f1f81-130">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)
