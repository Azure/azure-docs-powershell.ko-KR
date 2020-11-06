---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 7ac4db45f9eb0332217c5097802904cd2146aca5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537027"
---
# <span data-ttu-id="06f20-101">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="06f20-101">Get-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="06f20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06f20-102">SYNOPSIS</span></span>
<span data-ttu-id="06f20-103">ASR 복제 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06f20-103">Gets ASR replication policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06f20-104">구문과</span><span class="sxs-lookup"><span data-stu-id="06f20-104">SYNTAX</span></span>

### <span data-ttu-id="06f20-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="06f20-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy [<CommonParameters>]
```

### <span data-ttu-id="06f20-106">ByName</span><span class="sxs-lookup"><span data-stu-id="06f20-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="06f20-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="06f20-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrPolicy -FriendlyName <String> [<CommonParameters>]
```

## <span data-ttu-id="06f20-108">설명은</span><span class="sxs-lookup"><span data-stu-id="06f20-108">DESCRIPTION</span></span>
<span data-ttu-id="06f20-109">**AzureRmRecoveryServicesAsrPolicy** cmdlet은 구성 된 Azure Site Recovery 복제 정책 또는 이름에 따른 특정 복제 정책의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="06f20-109">The **Get-AzureRmRecoveryServicesAsrPolicy** cmdlet gets the list of configured Azure Site Recovery replication policies or a specific replication policy by name.</span></span>

## <span data-ttu-id="06f20-110">예제의</span><span class="sxs-lookup"><span data-stu-id="06f20-110">EXAMPLES</span></span>

### <span data-ttu-id="06f20-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="06f20-111">Example 1</span></span>
```
PS C:\> $Policy = Get-AzureRmRecoveryServicesAsrPolicy -Name $PolicyName
```

<span data-ttu-id="06f20-112">지정 된 이름을 사용 하 여 복제 정책을 Retruns.</span><span class="sxs-lookup"><span data-stu-id="06f20-112">Retruns the replication policy with the specified name.</span></span>

## <span data-ttu-id="06f20-113">변수</span><span class="sxs-lookup"><span data-stu-id="06f20-113">PARAMETERS</span></span>

### <span data-ttu-id="06f20-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="06f20-114">-FriendlyName</span></span>
<span data-ttu-id="06f20-115">ASR 복제 정책의 대화명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06f20-115">Specifies the friendly name of the ASR replication policy.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06f20-116">-이름</span><span class="sxs-lookup"><span data-stu-id="06f20-116">-Name</span></span>
<span data-ttu-id="06f20-117">ASR 복제 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06f20-117">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="06f20-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06f20-118">CommonParameters</span></span>
<span data-ttu-id="06f20-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="06f20-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06f20-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06f20-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06f20-121">입력</span><span class="sxs-lookup"><span data-stu-id="06f20-121">INPUTS</span></span>

### <span data-ttu-id="06f20-122">않아야</span><span class="sxs-lookup"><span data-stu-id="06f20-122">None</span></span>

## <span data-ttu-id="06f20-123">출력</span><span class="sxs-lookup"><span data-stu-id="06f20-123">OUTPUTS</span></span>

### <span data-ttu-id="06f20-124">System.webserver. t e r ' 1 [[SiteRecovery], [[Microsoft Azure. SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null]],,.</span><span class="sxs-lookup"><span data-stu-id="06f20-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="06f20-125">상속자</span><span class="sxs-lookup"><span data-stu-id="06f20-125">NOTES</span></span>

## <span data-ttu-id="06f20-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06f20-126">RELATED LINKS</span></span>

[<span data-ttu-id="06f20-127">새로운 AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="06f20-127">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="06f20-128">제거-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="06f20-128">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
