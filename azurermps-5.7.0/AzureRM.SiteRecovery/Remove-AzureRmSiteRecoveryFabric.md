---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 612D343A-89BA-491C-B20B-147715A2EF4F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 43d9603a5938ecef084191ebe77888a5f1769673
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534596"
---
# <span data-ttu-id="2e53b-101">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="2e53b-101">Remove-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="2e53b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e53b-102">SYNOPSIS</span></span>
<span data-ttu-id="2e53b-103">Azure Site Recovery 패브릭을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e53b-103">Removes an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e53b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2e53b-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryFabric -Fabric <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e53b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2e53b-105">DESCRIPTION</span></span>
<span data-ttu-id="2e53b-106">**AzureRmSiteRecoveryFabric** Cmdlet은 Azure Site Recovery 패브릭을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e53b-106">The **Remove-AzureRmSiteRecoveryFabric** cmdlet removes an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="2e53b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2e53b-107">EXAMPLES</span></span>

## <span data-ttu-id="2e53b-108">변수</span><span class="sxs-lookup"><span data-stu-id="2e53b-108">PARAMETERS</span></span>

### <span data-ttu-id="2e53b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e53b-109">-DefaultProfile</span></span>
<span data-ttu-id="2e53b-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2e53b-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e53b-111">-패브릭</span><span class="sxs-lookup"><span data-stu-id="2e53b-111">-Fabric</span></span>
<span data-ttu-id="2e53b-112">Azure Site Recovery Fabric 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e53b-112">Specifies the Azure Site Recovery Fabric object.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e53b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2e53b-113">-Force</span></span>
<span data-ttu-id="2e53b-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e53b-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e53b-115">-확인</span><span class="sxs-lookup"><span data-stu-id="2e53b-115">-Confirm</span></span>
<span data-ttu-id="2e53b-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e53b-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e53b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e53b-117">-WhatIf</span></span>
<span data-ttu-id="2e53b-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2e53b-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="2e53b-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2e53b-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e53b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e53b-120">CommonParameters</span></span>
<span data-ttu-id="2e53b-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e53b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e53b-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e53b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e53b-123">입력</span><span class="sxs-lookup"><span data-stu-id="2e53b-123">INPUTS</span></span>

### <span data-ttu-id="2e53b-124">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="2e53b-124">ASRFabric</span></span>
<span data-ttu-id="2e53b-125">' Fabric ' 매개 변수는 파이프라인에서 ' ASRFabric ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e53b-125">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="2e53b-126">출력</span><span class="sxs-lookup"><span data-stu-id="2e53b-126">OUTPUTS</span></span>

### <span data-ttu-id="2e53b-127">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="2e53b-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2e53b-128">상속자</span><span class="sxs-lookup"><span data-stu-id="2e53b-128">NOTES</span></span>

## <span data-ttu-id="2e53b-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2e53b-129">RELATED LINKS</span></span>

[<span data-ttu-id="2e53b-130">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="2e53b-130">Get-AzureRmSiteRecoveryFabric</span></span>](./Get-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="2e53b-131">새로운 AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="2e53b-131">New-AzureRmSiteRecoveryFabric</span></span>](./New-AzureRmSiteRecoveryFabric.md)
