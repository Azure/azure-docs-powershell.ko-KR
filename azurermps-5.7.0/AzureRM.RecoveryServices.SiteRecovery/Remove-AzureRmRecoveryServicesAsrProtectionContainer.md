---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 496eeed8b4ed4b41ce2c67d47fc636711cd5cb84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529778"
---
# <span data-ttu-id="cdd0c-101">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="cdd0c-101">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="cdd0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdd0c-102">SYNOPSIS</span></span>
<span data-ttu-id="cdd0c-103">패브릭에서 지정 된 보호 컨테이너를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd0c-103">Deletes the specified Protection Container from its Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdd0c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cdd0c-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdd0c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cdd0c-105">DESCRIPTION</span></span>
<span data-ttu-id="cdd0c-106">Remove-AzureRmRecoveryServicesAsrProtectionContainer cmdlet은 지정 된 Azure Site Recovery 보호 컨테이너를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd0c-106">The Remove-AzureRmRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="cdd0c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cdd0c-107">EXAMPLES</span></span>

### <span data-ttu-id="cdd0c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="cdd0c-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzureRmRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="cdd0c-109">지정 된 보호 컨테이너의 삭제를 시작 하 고 제거 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd0c-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="cdd0c-110">변수</span><span class="sxs-lookup"><span data-stu-id="cdd0c-110">PARAMETERS</span></span>

### <span data-ttu-id="cdd0c-111">-확인</span><span class="sxs-lookup"><span data-stu-id="cdd0c-111">-Confirm</span></span>
<span data-ttu-id="cdd0c-112">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd0c-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdd0c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdd0c-113">-DefaultProfile</span></span>
<span data-ttu-id="cdd0c-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cdd0c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdd0c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cdd0c-115">-InputObject</span></span>
<span data-ttu-id="cdd0c-116">제거할 보호 컨테이너를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd0c-116">Specifies the protection container to be removed .</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: ProtectionContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cdd0c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdd0c-117">-WhatIf</span></span>
<span data-ttu-id="cdd0c-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cdd0c-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdd0c-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cdd0c-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdd0c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdd0c-120">CommonParameters</span></span>
<span data-ttu-id="cdd0c-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cdd0c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdd0c-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdd0c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdd0c-123">입력</span><span class="sxs-lookup"><span data-stu-id="cdd0c-123">INPUTS</span></span>

### <span data-ttu-id="cdd0c-124">SiteRecovery. ASRProtectionContainer에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="cdd0c-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="cdd0c-125">출력</span><span class="sxs-lookup"><span data-stu-id="cdd0c-125">OUTPUTS</span></span>

### <span data-ttu-id="cdd0c-126">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="cdd0c-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="cdd0c-127">상속자</span><span class="sxs-lookup"><span data-stu-id="cdd0c-127">NOTES</span></span>

## <span data-ttu-id="cdd0c-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cdd0c-128">RELATED LINKS</span></span>
