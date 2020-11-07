---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3B879056-5BF3-4262-8BAA-E79589149370
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: ae5a1d5a70064b3849bc8f38cab46ecfabaf4968
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703981"
---
# <span data-ttu-id="caa13-101">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="caa13-101">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="caa13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="caa13-102">SYNOPSIS</span></span>
<span data-ttu-id="caa13-103">사이트 복구의 복구 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="caa13-103">Gets a recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="caa13-104">구문과</span><span class="sxs-lookup"><span data-stu-id="caa13-104">SYNTAX</span></span>

### <span data-ttu-id="caa13-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="caa13-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="caa13-106">ByName</span><span class="sxs-lookup"><span data-stu-id="caa13-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="caa13-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="caa13-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="caa13-108">설명은</span><span class="sxs-lookup"><span data-stu-id="caa13-108">DESCRIPTION</span></span>
<span data-ttu-id="caa13-109">**AzureRmSiteRecoveryRecoveryPlan** Cmdlet은 Azure Site recovery의 복구 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="caa13-109">The **Get-AzureRmSiteRecoveryRecoveryPlan** cmdlet gets a recovery plan in Azure Site Recovery.</span></span>

## <span data-ttu-id="caa13-110">예제의</span><span class="sxs-lookup"><span data-stu-id="caa13-110">EXAMPLES</span></span>

## <span data-ttu-id="caa13-111">변수</span><span class="sxs-lookup"><span data-stu-id="caa13-111">PARAMETERS</span></span>

### <span data-ttu-id="caa13-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caa13-112">-DefaultProfile</span></span>
<span data-ttu-id="caa13-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="caa13-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="caa13-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="caa13-114">-FriendlyName</span></span>
<span data-ttu-id="caa13-115">이 cmdlet이 가져오는 복구 계획의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="caa13-115">Specifies the friendly name of the recovery plan that this cmdlet gets.</span></span>

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

### <span data-ttu-id="caa13-116">-이름</span><span class="sxs-lookup"><span data-stu-id="caa13-116">-Name</span></span>
<span data-ttu-id="caa13-117">이 cmdlet이 가져오는 복구 계획의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="caa13-117">Specifies the name of the recovery plan that this cmdlet gets.</span></span>

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

### <span data-ttu-id="caa13-118">-Path</span><span class="sxs-lookup"><span data-stu-id="caa13-118">-Path</span></span>
<span data-ttu-id="caa13-119">이 cmdlet이 복구 계획을 저장할 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="caa13-119">Specifies the file path to which this cmdlet saves the recovery plan.</span></span>

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

### <span data-ttu-id="caa13-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caa13-120">CommonParameters</span></span>
<span data-ttu-id="caa13-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="caa13-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caa13-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caa13-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caa13-123">입력</span><span class="sxs-lookup"><span data-stu-id="caa13-123">INPUTS</span></span>

### <span data-ttu-id="caa13-124">않아야</span><span class="sxs-lookup"><span data-stu-id="caa13-124">None</span></span>
<span data-ttu-id="caa13-125">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="caa13-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="caa13-126">출력</span><span class="sxs-lookup"><span data-stu-id="caa13-126">OUTPUTS</span></span>

### <span data-ttu-id="caa13-127">System.webserver. t e r ' 1 [SiteRecovery Rrecoveryplan]</span><span class="sxs-lookup"><span data-stu-id="caa13-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan]</span></span>

## <span data-ttu-id="caa13-128">상속자</span><span class="sxs-lookup"><span data-stu-id="caa13-128">NOTES</span></span>

## <span data-ttu-id="caa13-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="caa13-129">RELATED LINKS</span></span>

[<span data-ttu-id="caa13-130">새로운 AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="caa13-130">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="caa13-131">제거-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="caa13-131">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="caa13-132">업데이트-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="caa13-132">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)
