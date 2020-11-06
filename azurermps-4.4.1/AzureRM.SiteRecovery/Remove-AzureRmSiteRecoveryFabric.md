---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 612D343A-89BA-491C-B20B-147715A2EF4F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 3d4530090bc1386a34056b315c79a826be5d771f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530659"
---
# <span data-ttu-id="ae3e7-101">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="ae3e7-101">Remove-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="ae3e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae3e7-102">SYNOPSIS</span></span>
<span data-ttu-id="ae3e7-103">Azure Site Recovery 패브릭을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae3e7-103">Removes an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae3e7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ae3e7-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryFabric -Fabric <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae3e7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ae3e7-105">DESCRIPTION</span></span>
<span data-ttu-id="ae3e7-106">**AzureRmSiteRecoveryFabric** Cmdlet은 Azure Site Recovery 패브릭을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae3e7-106">The **Remove-AzureRmSiteRecoveryFabric** cmdlet removes an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="ae3e7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ae3e7-107">EXAMPLES</span></span>

## <span data-ttu-id="ae3e7-108">변수</span><span class="sxs-lookup"><span data-stu-id="ae3e7-108">PARAMETERS</span></span>

### <span data-ttu-id="ae3e7-109">-패브릭</span><span class="sxs-lookup"><span data-stu-id="ae3e7-109">-Fabric</span></span>
<span data-ttu-id="ae3e7-110">Azure Site Recovery Fabric 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae3e7-110">Specifies the Azure Site Recovery Fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae3e7-111">-Force</span><span class="sxs-lookup"><span data-stu-id="ae3e7-111">-Force</span></span>
<span data-ttu-id="ae3e7-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae3e7-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae3e7-113">-확인</span><span class="sxs-lookup"><span data-stu-id="ae3e7-113">-Confirm</span></span>
<span data-ttu-id="ae3e7-114">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae3e7-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae3e7-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae3e7-115">-WhatIf</span></span>
<span data-ttu-id="ae3e7-116">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ae3e7-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="ae3e7-117">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae3e7-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae3e7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae3e7-118">-DefaultProfile</span></span>
<span data-ttu-id="ae3e7-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ae3e7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae3e7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae3e7-120">CommonParameters</span></span>
<span data-ttu-id="ae3e7-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae3e7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae3e7-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae3e7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae3e7-123">입력</span><span class="sxs-lookup"><span data-stu-id="ae3e7-123">INPUTS</span></span>

### <span data-ttu-id="ae3e7-124">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="ae3e7-124">ASRFabric</span></span>
<span data-ttu-id="ae3e7-125">' Fabric ' 매개 변수는 파이프라인에서 ' ASRFabric ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae3e7-125">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="ae3e7-126">출력</span><span class="sxs-lookup"><span data-stu-id="ae3e7-126">OUTPUTS</span></span>

### <span data-ttu-id="ae3e7-127">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="ae3e7-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ae3e7-128">상속자</span><span class="sxs-lookup"><span data-stu-id="ae3e7-128">NOTES</span></span>

## <span data-ttu-id="ae3e7-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae3e7-129">RELATED LINKS</span></span>

[<span data-ttu-id="ae3e7-130">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="ae3e7-130">Get-AzureRmSiteRecoveryFabric</span></span>](./Get-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="ae3e7-131">새로운 AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="ae3e7-131">New-AzureRmSiteRecoveryFabric</span></span>](./New-AzureRmSiteRecoveryFabric.md)
