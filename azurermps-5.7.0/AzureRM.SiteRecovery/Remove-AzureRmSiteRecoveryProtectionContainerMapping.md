---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B1D914F8-4181-4BF1-B1D3-A5857DA8254C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 27c90687b212c0ed41dcb080df1be5686a876725
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703962"
---
# <span data-ttu-id="5ad30-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5ad30-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="5ad30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ad30-102">SYNOPSIS</span></span>
<span data-ttu-id="5ad30-103">Azure Site Recovery 보호 컨테이너 매핑을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ad30-103">Removes an Azure Site Recovery Protection Container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ad30-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5ad30-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryProtectionContainerMapping
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ad30-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5ad30-105">DESCRIPTION</span></span>
<span data-ttu-id="5ad30-106">**AzureRmSiteRecoveryProtectionContainerMapping** Cmdlet은 Azure Site Recovery 보호 컨테이너 매핑을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ad30-106">The **Remove-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet removes an Azure Site Recovery Protection Container mapping.</span></span>

## <span data-ttu-id="5ad30-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5ad30-107">EXAMPLES</span></span>

## <span data-ttu-id="5ad30-108">변수</span><span class="sxs-lookup"><span data-stu-id="5ad30-108">PARAMETERS</span></span>

### <span data-ttu-id="5ad30-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ad30-109">-DefaultProfile</span></span>
<span data-ttu-id="5ad30-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5ad30-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ad30-111">-Force</span><span class="sxs-lookup"><span data-stu-id="5ad30-111">-Force</span></span>
<span data-ttu-id="5ad30-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ad30-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5ad30-113">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5ad30-113">-ProtectionContainerMapping</span></span>
<span data-ttu-id="5ad30-114">Azure Site Recovery 보호 컨테이너 매핑 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ad30-114">Specifies the Azure Site Recovery Protection Container mapping object.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ad30-115">-확인</span><span class="sxs-lookup"><span data-stu-id="5ad30-115">-Confirm</span></span>
<span data-ttu-id="5ad30-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ad30-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ad30-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ad30-117">-WhatIf</span></span>
<span data-ttu-id="5ad30-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5ad30-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="5ad30-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5ad30-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ad30-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ad30-120">CommonParameters</span></span>
<span data-ttu-id="5ad30-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ad30-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ad30-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ad30-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ad30-123">입력</span><span class="sxs-lookup"><span data-stu-id="5ad30-123">INPUTS</span></span>

### <span data-ttu-id="5ad30-124">ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5ad30-124">ASRProtectionContainerMapping</span></span>
<span data-ttu-id="5ad30-125">' ProtectionContainerMapping ' 매개 변수는 파이프라인에서 ' ASRProtectionContainerMapping ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ad30-125">Parameter 'ProtectionContainerMapping' accepts value of type 'ASRProtectionContainerMapping' from the pipeline</span></span>

## <span data-ttu-id="5ad30-126">출력</span><span class="sxs-lookup"><span data-stu-id="5ad30-126">OUTPUTS</span></span>

### <span data-ttu-id="5ad30-127">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="5ad30-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5ad30-128">상속자</span><span class="sxs-lookup"><span data-stu-id="5ad30-128">NOTES</span></span>

## <span data-ttu-id="5ad30-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5ad30-129">RELATED LINKS</span></span>

[<span data-ttu-id="5ad30-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5ad30-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="5ad30-131">새로운 AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="5ad30-131">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./New-AzureRmSiteRecoveryProtectionContainerMapping.md)
