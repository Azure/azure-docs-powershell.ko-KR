---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 20a57bd70c9cf9b1b533e040001afee0cc5809fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873514"
---
# <span data-ttu-id="660b4-101">Remove-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="660b4-101">Remove-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="660b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="660b4-102">SYNOPSIS</span></span>
<span data-ttu-id="660b4-103">패브릭에서 지정 된 보호 컨테이너를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="660b4-103">Deletes the specified Protection Container from its Fabric.</span></span>

## <span data-ttu-id="660b4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="660b4-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="660b4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="660b4-105">DESCRIPTION</span></span>
<span data-ttu-id="660b4-106">Remove-AzRecoveryServicesAsrProtectionContainer cmdlet은 지정 된 Azure Site Recovery 보호 컨테이너를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="660b4-106">The Remove-AzRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="660b4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="660b4-107">EXAMPLES</span></span>

### <span data-ttu-id="660b4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="660b4-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="660b4-109">지정 된 보호 컨테이너의 삭제를 시작 하 고 제거 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="660b4-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="660b4-110">변수</span><span class="sxs-lookup"><span data-stu-id="660b4-110">PARAMETERS</span></span>

### <span data-ttu-id="660b4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="660b4-111">-DefaultProfile</span></span>
<span data-ttu-id="660b4-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="660b4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="660b4-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="660b4-113">-InputObject</span></span>
<span data-ttu-id="660b4-114">제거할 보호 컨테이너를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="660b4-114">Specifies the protection container to be removed .</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: ProtectionContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="660b4-115">-확인</span><span class="sxs-lookup"><span data-stu-id="660b4-115">-Confirm</span></span>
<span data-ttu-id="660b4-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="660b4-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="660b4-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="660b4-117">-WhatIf</span></span>
<span data-ttu-id="660b4-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="660b4-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="660b4-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="660b4-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="660b4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="660b4-120">CommonParameters</span></span>
<span data-ttu-id="660b4-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="660b4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="660b4-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="660b4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="660b4-123">입력</span><span class="sxs-lookup"><span data-stu-id="660b4-123">INPUTS</span></span>

### <span data-ttu-id="660b4-124">SiteRecovery. ASRProtectionContainer에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="660b4-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="660b4-125">출력</span><span class="sxs-lookup"><span data-stu-id="660b4-125">OUTPUTS</span></span>

### <span data-ttu-id="660b4-126">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="660b4-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="660b4-127">상속자</span><span class="sxs-lookup"><span data-stu-id="660b4-127">NOTES</span></span>

## <span data-ttu-id="660b4-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="660b4-128">RELATED LINKS</span></span>
