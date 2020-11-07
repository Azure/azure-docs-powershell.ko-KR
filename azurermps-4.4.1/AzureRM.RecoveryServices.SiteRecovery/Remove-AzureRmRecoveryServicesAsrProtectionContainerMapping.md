---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 3d26a5285fbe96c0e77c56819567e21820cddf4f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703339"
---
# <span data-ttu-id="f3bbb-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="f3bbb-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="f3bbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3bbb-102">SYNOPSIS</span></span>
<span data-ttu-id="f3bbb-103">지정 된 Azure Site Recovery 보호 컨테이너 매핑을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bbb-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3bbb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f3bbb-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3bbb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f3bbb-105">DESCRIPTION</span></span>
<span data-ttu-id="f3bbb-106">**AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet은 지정 된 Azure Site Recovery 보호 컨테이너 매핑을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bbb-106">The **Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="f3bbb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f3bbb-107">EXAMPLES</span></span>

### <span data-ttu-id="f3bbb-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f3bbb-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="f3bbb-109">지정 된 보호 컨테이너 매핑의 삭제를 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bbb-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f3bbb-110">변수</span><span class="sxs-lookup"><span data-stu-id="f3bbb-110">PARAMETERS</span></span>

### <span data-ttu-id="f3bbb-111">-Force</span><span class="sxs-lookup"><span data-stu-id="f3bbb-111">-Force</span></span>
<span data-ttu-id="f3bbb-112">추가 경고를 제공 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bbb-112">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="f3bbb-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3bbb-113">-InputObject</span></span>
<span data-ttu-id="f3bbb-114">Cmdlet에 대 한 입력 개체: 삭제할 보호 컨테이너에 해당 하는 ASR protection 컨테이너 매핑 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f3bbb-114">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3bbb-115">-확인</span><span class="sxs-lookup"><span data-stu-id="f3bbb-115">-Confirm</span></span>
<span data-ttu-id="f3bbb-116">확인이 필요한 경우 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bbb-116">Specify if confirmation is required.</span></span> <span data-ttu-id="f3bbb-117">확인을 건너뛰려면 confirm 매개 변수 값을 $false으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bbb-117">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3bbb-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3bbb-118">-WhatIf</span></span>
<span data-ttu-id="f3bbb-119">Cmdlet을 실제로 실행 하지 않고 cmdlet을 실행 하는 경우 발생 하는 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f3bbb-119">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3bbb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3bbb-120">CommonParameters</span></span>
<span data-ttu-id="f3bbb-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3bbb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3bbb-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3bbb-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3bbb-123">입력</span><span class="sxs-lookup"><span data-stu-id="f3bbb-123">INPUTS</span></span>

### <span data-ttu-id="f3bbb-124">SiteRecovery. ASRProtectionContainerMapping에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="f3bbb-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="f3bbb-125">출력</span><span class="sxs-lookup"><span data-stu-id="f3bbb-125">OUTPUTS</span></span>

### <span data-ttu-id="f3bbb-126">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="f3bbb-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f3bbb-127">상속자</span><span class="sxs-lookup"><span data-stu-id="f3bbb-127">NOTES</span></span>

## <span data-ttu-id="f3bbb-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3bbb-128">RELATED LINKS</span></span>

[<span data-ttu-id="f3bbb-129">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="f3bbb-129">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="f3bbb-130">새로운 AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="f3bbb-130">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
