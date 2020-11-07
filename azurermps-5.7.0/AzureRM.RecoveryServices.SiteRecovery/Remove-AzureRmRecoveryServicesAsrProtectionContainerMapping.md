---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 7a2508669c0beba7fc9edd92ac645ce149633e05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702846"
---
# <span data-ttu-id="17eee-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="17eee-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="17eee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17eee-102">SYNOPSIS</span></span>
<span data-ttu-id="17eee-103">지정 된 Azure Site Recovery 보호 컨테이너 매핑을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="17eee-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17eee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="17eee-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17eee-105">설명은</span><span class="sxs-lookup"><span data-stu-id="17eee-105">DESCRIPTION</span></span>
<span data-ttu-id="17eee-106">**AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet은 지정 된 Azure Site Recovery 보호 컨테이너 매핑을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="17eee-106">The **Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="17eee-107">예제의</span><span class="sxs-lookup"><span data-stu-id="17eee-107">EXAMPLES</span></span>

### <span data-ttu-id="17eee-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="17eee-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="17eee-109">지정 된 보호 컨테이너 매핑의 삭제를 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="17eee-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="17eee-110">변수</span><span class="sxs-lookup"><span data-stu-id="17eee-110">PARAMETERS</span></span>

### <span data-ttu-id="17eee-111">-확인</span><span class="sxs-lookup"><span data-stu-id="17eee-111">-Confirm</span></span>
<span data-ttu-id="17eee-112">확인이 필요한 경우 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17eee-112">Specify if confirmation is required.</span></span> <span data-ttu-id="17eee-113">확인을 건너뛰려면 confirm 매개 변수 값을 $false으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17eee-113">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="17eee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17eee-114">-DefaultProfile</span></span>
<span data-ttu-id="17eee-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="17eee-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="17eee-116">-Force</span><span class="sxs-lookup"><span data-stu-id="17eee-116">-Force</span></span>
<span data-ttu-id="17eee-117">추가 경고를 제공 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="17eee-117">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="17eee-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17eee-118">-InputObject</span></span>
<span data-ttu-id="17eee-119">Cmdlet에 대 한 입력 개체: 삭제할 보호 컨테이너에 해당 하는 ASR protection 컨테이너 매핑 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="17eee-119">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

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

### <span data-ttu-id="17eee-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17eee-120">-WhatIf</span></span>
<span data-ttu-id="17eee-121">Cmdlet을 실제로 실행 하지 않고 cmdlet을 실행 하는 경우 발생 하는 결과를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="17eee-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="17eee-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17eee-122">CommonParameters</span></span>
<span data-ttu-id="17eee-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="17eee-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17eee-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17eee-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17eee-125">입력</span><span class="sxs-lookup"><span data-stu-id="17eee-125">INPUTS</span></span>

### <span data-ttu-id="17eee-126">SiteRecovery. ASRProtectionContainerMapping에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="17eee-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="17eee-127">출력</span><span class="sxs-lookup"><span data-stu-id="17eee-127">OUTPUTS</span></span>

### <span data-ttu-id="17eee-128">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="17eee-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="17eee-129">상속자</span><span class="sxs-lookup"><span data-stu-id="17eee-129">NOTES</span></span>

## <span data-ttu-id="17eee-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17eee-130">RELATED LINKS</span></span>

[<span data-ttu-id="17eee-131">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="17eee-131">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="17eee-132">새로운 AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="17eee-132">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
