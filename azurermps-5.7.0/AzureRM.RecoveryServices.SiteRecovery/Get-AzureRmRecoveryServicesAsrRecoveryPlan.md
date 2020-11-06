---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: b95c3ab14d50558ef184beabcd461a59bb1a05ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528871"
---
# <span data-ttu-id="00928-101">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="00928-101">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="00928-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00928-102">SYNOPSIS</span></span>
<span data-ttu-id="00928-103">복구 계획 또는 복구 서비스 자격 증명 모음의 모든 복구 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="00928-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00928-104">구문과</span><span class="sxs-lookup"><span data-stu-id="00928-104">SYNTAX</span></span>

### <span data-ttu-id="00928-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="00928-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00928-106">ByName</span><span class="sxs-lookup"><span data-stu-id="00928-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00928-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="00928-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00928-108">설명은</span><span class="sxs-lookup"><span data-stu-id="00928-108">DESCRIPTION</span></span>
<span data-ttu-id="00928-109">**AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet은 지정 된 복구 계획 또는 복구 서비스 자격 증명 모음의 모든 복구 계획에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="00928-109">The **Get-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="00928-110">예제의</span><span class="sxs-lookup"><span data-stu-id="00928-110">EXAMPLES</span></span>

### <span data-ttu-id="00928-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="00928-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="00928-112">지정 된 이름의 복구 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="00928-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="00928-113">변수</span><span class="sxs-lookup"><span data-stu-id="00928-113">PARAMETERS</span></span>

### <span data-ttu-id="00928-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00928-114">-DefaultProfile</span></span>
<span data-ttu-id="00928-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="00928-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00928-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="00928-116">-FriendlyName</span></span>
<span data-ttu-id="00928-117">가져올 복구 계획의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00928-117">Specifies the friendly name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="00928-118">-이름</span><span class="sxs-lookup"><span data-stu-id="00928-118">-Name</span></span>
<span data-ttu-id="00928-119">가져올 복구 계획의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00928-119">Specifies the name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="00928-120">-Path</span><span class="sxs-lookup"><span data-stu-id="00928-120">-Path</span></span>
<span data-ttu-id="00928-121">이 cmdlet이 복구 계획 json 정의를 저장할 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00928-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="00928-122">복구 계획을 수정 하 고 Update-AzureRmRecoveryServicesASRRecoveryPlan cmdlet을 통해 복구 계획을 업데이트 하는 데 사용 되는 json 정의를 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00928-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzureRmRecoveryServicesASRRecoveryPlan cmdlet</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByFriendlyName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00928-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00928-123">CommonParameters</span></span>
<span data-ttu-id="00928-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="00928-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00928-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00928-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00928-126">입력</span><span class="sxs-lookup"><span data-stu-id="00928-126">INPUTS</span></span>

### <span data-ttu-id="00928-127">않아야</span><span class="sxs-lookup"><span data-stu-id="00928-127">None</span></span>

## <span data-ttu-id="00928-128">출력</span><span class="sxs-lookup"><span data-stu-id="00928-128">OUTPUTS</span></span>

### <span data-ttu-id="00928-129">System.webserver. t e r ' 1 [[SiteRecovery] Recoveryrrecoveryplan, Microsoft Azure. SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="00928-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="00928-130">상속자</span><span class="sxs-lookup"><span data-stu-id="00928-130">NOTES</span></span>

## <span data-ttu-id="00928-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00928-131">RELATED LINKS</span></span>

[<span data-ttu-id="00928-132">새로운 AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="00928-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="00928-133">제거-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="00928-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="00928-134">업데이트-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="00928-134">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)
